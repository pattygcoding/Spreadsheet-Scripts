# Google Apps Scripts by Patrick Goodwin
A collection of Scripts I use, especially on Google Sheets to compare SQL outputs when Microsoft SQL server can't do it for me.

To use these on Google Sheets, go to the Extensions -> Apps Script and paste your code.

**Experimental OfficeScript Files:** The TypeScript files are experimental and for OfficeScript. The .gs (Google Sheets) and .vba (Excel) files are the correct files to use

## Table of Contents
- [Compare Columns](#compare-columns)
- [Compare Rows](#compare-rows)
- [Obtain SQL](#obtain-sql)

## Compare Columns
Compares 2 columns and returns the differences.

### Parameters
- `column1`: The number of the first row to compare - must be in string format.
- `column2`: The number of the second row to compare- must be in string format.
- `sheet`: the name of the sheet (defualt: your current sheet)
- `includeTimestamps`: Displays timestamp differences if TRUE

### Examples:
```
=compareColumns("B", "C")
=compareColumns("B", "C", "Sheet2")
=compareColumns("B", "C", , TRUE)
=compareColumns("B", "C", "Sheet2", TRUE)
```

## Compare Rows
Compares 2 rows and returns the differences.

### Parameters
- `row1`: The number of the first row to compare.
- `row2`: The number of the second row to compare.
- `sheet`: the name of the sheet (defualt: your current sheet)
- `includeTimestamps`: Displays timestamp differences if TRUE

### Examples:
```
=compareRows(2, 3)
=compareRows(2, 3, "Sheet2")
=compareRows(2, 3, , TRUE)
=compareRows(2, 3, "Sheet2", TRUE)
```

## Obtain SQL
Obtains the SQL format for a header and value row.

### Parameters
- `headerRow`: The number of the first row to compare.
- `valueRow`: The number of the second row to compare.
- `sheet`: the name of the sheet (defualt: your current sheet)

### Examples:
```
=obtainSQL(2, 3)
=obtainSQL(2, 3, "Sheet2")
```
