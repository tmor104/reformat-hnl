# Stocktake Report Converter

A specialized web tool to convert messy Excel stocktake reports into clean, structured tables with proper formatting. Designed to handle reports with merged cells, blank rows, and grouped data organized by stock groups.

## Features

- **Drag & Drop Upload**: Simply drag your Excel file onto the page or click to browse
- **Stock Group Extraction**: Automatically detects and extracts stock group identifiers from header rows
- **Sparse Column Mapping**: Maps data from non-consecutive columns to a clean, dense table format
- **Smart Data Detection**: Only processes rows with valid inventory codes
- **Live Preview**: See your cleaned data in a formatted table before downloading
- **Formatted Excel Output**: Downloads include proper number formatting, column widths, and styled headers
- **100% Client-Side**: All processing happens in your browser - no data is sent to any server

## How to Use

1. Visit the GitHub Pages site
2. Upload your stocktake Excel file (.xlsx or .xls) by dragging it onto the upload area or clicking to browse
3. Preview the cleaned data in the table
4. Click "Download Clean Excel" to save the converted file

## What It Does

### Input File Processing

The converter handles stocktake reports with:
- **Group Headers**: Rows starting with "Stock Group No: " followed by group identifier
- **Sparse Data**: Data spread across non-consecutive columns (columns 0, 2, 3, 4, 5, 6, 9, 11, 12)
- **Merged Cells**: Multiple merged cells throughout the document
- **Blank Rows**: Extensive blank rows between data sections
- **Inconsistent Structure**: Header rows not at the top, varying row counts per group

### Output Format

Generates a clean Excel file with:
- ✅ **Stock Group Column**: Added as first column for easy filtering
- ✅ **10 Clean Columns**:
  - Stock Group
  - InvCode
  - Stock Description
  - Unit (Inners)
  - Average Unit Cost
  - Quantity Entered
  - Quantity at Stocktake
  - Quantity Difference
  - $ Value of Difference
  - Value on hand at Stocktake
- ✅ **Proper Number Formatting**: Currency and decimal formats applied
- ✅ **Optimized Column Widths**: Set for readability
- ✅ **Styled Headers**: Bold headers with gray background
- ✅ **No Merged Cells or Blank Rows**: Clean tabular format

## Processing Algorithm

1. Reads Excel file and preserves all rows (including blanks)
2. Scans for rows starting with "Stock Group No:" to extract group identifiers
3. Identifies data rows by checking for numeric InvCode in column A
4. Maps sparse input columns to dense output columns:
   - Input columns: 0, 2, 3, 4, 5, 6, 9, 11, 12
   - Output: 10 consecutive columns with Stock Group added
5. Applies formatting and generates downloadable Excel file

## Technologies Used

- Pure HTML, CSS, and JavaScript
- [SheetJS (xlsx)](https://github.com/SheetJS/sheetjs) - For Excel file processing
- GitHub Pages for hosting

## Privacy

All Excel file processing happens entirely in your browser. No data is uploaded to any server or stored anywhere.

## Example Conversion

**Input**: ~1,896 rows with merged cells, blank rows, and grouped data
**Output**: ~815 clean data rows + 1 header row with 10 properly formatted columns

## License

MIT
