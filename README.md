# Stocktake Report Converter

A simple web tool to convert messy Excel stocktake reports into clean, simple tables without merged cells or formatting issues.

## Features

- **Drag & Drop Upload**: Simply drag your Excel file onto the page or click to browse
- **Automatic Cleaning**: Removes merged cells, empty rows, and empty columns
- **Live Preview**: See your cleaned data in a table format before downloading
- **Download**: Export the cleaned data as a new Excel file
- **100% Client-Side**: All processing happens in your browser - no data is sent to any server

## How to Use

1. Visit the GitHub Pages site
2. Upload your Excel file (.xlsx or .xls) by dragging it onto the upload area or clicking to browse
3. Preview the cleaned data in the table
4. Click "Download Clean Excel" to save the converted file

## What Gets Cleaned

- ✅ Unmerges all merged cells (fills all cells with the merged value)
- ✅ Removes completely empty rows
- ✅ Removes completely empty columns
- ✅ Standardizes data into a simple table format

## Technologies Used

- Pure HTML, CSS, and JavaScript
- [SheetJS (xlsx)](https://github.com/SheetJS/sheetjs) - For Excel file processing
- GitHub Pages for hosting

## Privacy

All Excel file processing happens entirely in your browser. No data is uploaded to any server or stored anywhere.

## License

MIT
