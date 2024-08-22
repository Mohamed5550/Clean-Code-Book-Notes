# Formatting

## Vertical Formatting

- Vertical Size
  - We can build systems with upper bound of `500` lines per file
  - It is not hard, but it can be considered desirebly

- The Newspaper Metaphor
  - We should start the file the the most abstracted functions, then the details increases as we go down

- Vertical Opennes Between Concepts
  - Different concepts should be separated with a blank line

- Vertical Density
  - Related concepts should appear vertically dense

- Vertical Distance
  - Related concepts should be kept vertically close
  - Variables should be declared close to its usage
  - Instance variables should be declared at the top of the class

- Dependent Functions
  - If one function depends on another function it should be followed by it if possible

- Vertical Ordering
  - The most important function should be written first

## Horizontal Formatting

- Horizontal Size
  - Preferrable size is 120 characters per line

- Horizontal Openness and Density
  - There should be white space between the operators and the variables
  - Function should be close to its arguments
  - When having equations we remove spaces in high precedence operations

- Horizontal Alignment
  - The author was using horizontal alignment in variables declaration, but now he don't like adding them

- Indentation
  - Class declaration should have no indentation
  - When we go in a new scope, we add an indent
  - Try to avoid one line for short statements
  - Avoid dummy scopes

## Team Rules

- Every developer may have his favourite formatting, but when working on a team, he should stick to team rules

## Uncle Bob's Formatting Rules

```Java
public class CodeAnalyzer implements JavaFileAnalysis {
    private int lineCount;
    private int maxLineWidth;
    private int widestLineNumber;
    private LineWidthHistogram lineWidthHistogram;
    private int totalChars;

    public CodeAnalyzer() {
        lineWidthHistogram = new LineWidthHistogram();
    }

    public static List<File> findJavaFiles(File parentDirectory) {
        List<File> files = new ArrayList<File>();
        findJavaFiles(parentDirectory, files);
        return files;
    }

    private static void findJavaFiles(File parentDirectory, List<File> files) {
        for (File file : parentDirectory.listFiles()) {
            if (file.getName().endsWith(".java"))
                files.add(file);
            else if (file.isDirectory())
                findJavaFiles(file, files);
        }
    }

    public void analyzeFile(File javaFile) throws Exception {
        BufferedReader br = new BufferedReader(new FileReader(javaFile));
        String line;
        while ((line = br.readLine()) != null)
            measureLine(line);
    }

    private void measureLine(String line) {
        lineCount++;
        int lineSize = line.length();
        totalChars += lineSize;
        lineWidthHistogram.addLine(lineSize, lineCount);
        recordWidestLine(lineSize);
    }

    private void recordWidestLine(int lineSize) {
        if (lineSize > maxLineWidth) {
            maxLineWidth = lineSize;
            widestLineNumber = lineCount;
        }
    }

    public int getLineCount() {
        return lineCount;
    }

    public int getMaxLineWidth() {
        return maxLineWidth;
    }

    public int getWidestLineNumber() {
        return widestLineNumber;
    }

    public LineWidthHistogram getLineWidthHistogram() {
        return lineWidthHistogram;
    }

    public double getMeanLineWidth() {
        return (double)totalChars/lineCount;
    }

    public int getMedianLineWidth() {
        Integer[] sortedWidths = getSortedWidths();
        int cumulativeLineCount = 0;
        for (int width : sortedWidths) {
            cumulativeLineCount += lineCountForWidth(width);
            if (cumulativeLineCount > lineCount/2)
                return width;
        }
        throw new Error("Cannot get here");
    }

    private int lineCountForWidth(int width) {
        return lineWidthHistogram.getLinesforWidth(width).size();
    }

    private Integer[] getSortedWidths() {
        Set<Integer> widths = lineWidthHistogram.getWidths();
        Integer[] sortedWidths = (widths.toArray(new Integer[0]));
        Arrays.sort(sortedWidths);
        return sortedWidths;
    }
}
```
