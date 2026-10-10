# UltraFast Folder Size Analyzer

A fast, privacy-friendly, browser-based folder size analyzer designed for scanning large directories without uploading files or reading their contents.

## Features

- Fast recursive folder scanning
- Folder sizes calculated from file metadata
- Sort folders by size, file count, depth, name, or path
- Search folders by name or path
- Filter results by minimum folder size
- File-type summary based on extensions
- Real-time scan statistics:
  - Files scanned
  - Folders discovered
  - Total size
  - Scan speed
  - Elapsed time
  - Access errors
- Copy folder paths directly from the results table
- Export complete reports as:
  - TXT
  - CSV
  - JSON
- Formula-safe CSV export
- Cancel long-running scans
- Adaptive directory worker count based on available CPU threads
- Fallback support for browsers without the File System Access API
- No installation required
- No server required
- No file uploads

## Privacy

All processing happens locally inside your browser.

The application does not upload your files, folder names, paths, or scan results to any server.

File contents are not read. The analyzer uses file metadata such as filename and file size to calculate directory statistics.

## Usage

1. Download `Folder_Size_Analyzer_UltraFast.html`.
2. Open it in a modern browser.
3. Click **Select Folder**.
4. Choose the directory you want to analyze.
5. Wait for the scan to complete.
6. Search, filter, and sort the results.
7. Export the report if needed.

## Browser Support

For the best performance, use a Chromium-based browser such as:

- Google Chrome
- Microsoft Edge
- Brave
- Chromium

Browsers without `showDirectoryPicker()` can use the fallback directory-selection method when supported.

## Performance

The application is designed to remain lightweight when scanning large folder trees.

It:

- Does not load file contents into memory
- Updates the interface at a controlled rate
- Uses concurrent directory scanning when supported
- Limits the number of displayed table rows while preserving the complete scan result for reports

Actual performance depends on the storage device, filesystem, browser, number of files, directory structure, and operating-system permissions.

## Reports

### TXT

Human-readable report containing scan metadata, file-type statistics, and folders ordered by size.

### CSV

Spreadsheet-friendly folder report with protection against common spreadsheet formula-injection patterns.

### JSON

Machine-readable report containing:

- Scan metadata
- File-type statistics
- Complete folder results

## Security Notes

The application requests read access only to the directory selected by the user.

Some files or directories may be inaccessible because of operating-system permissions. These are skipped and counted as access errors rather than terminating the entire scan.

## Current Version

**v2.0**

## License

A license has not yet been selected for this project.
