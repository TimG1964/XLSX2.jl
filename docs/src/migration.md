# Migration Guide

Most of the functionality in `XLSX.jl` can be used in exactly the same way in `XLSX2.jl` as it was used before. There are almost no changes in functional APIs. Those changes that have been made are described briefly here to aid users migrating to `XLSX2.jl`. The documentation for this package has been extended substantially to cover the new functionality and all changes are (should be) reflected therein.

## New Functions
A number of new functions have been added compared with `XLSX.jl` v0.10.4 (the most recent release of `XLSX.jl` at the time `XLSX2.jl` was released).

These include 18 new functions to support formatting of cells and cell values together with functions to copy or delete a sheet and to add new defined names for cells or cell ranges. Some additional convenience functions have also been added to streamline functions that were already available (such as `newxlsx`, `savexlsx`).

A wide range of additional indexing options is now widely supported by most functions. Most functions now support indexing rows and columns using vectors, ranges and step ranges and will accept a colon.

## Exported Functions
Most usful functions are now public, and can be used without the `XLSX2.` prefix. The following function names are exported now exported:

- Files and worksheets
    `XLSXFile`, `readxlsx`, `openxlsx`, `opentemplate`, `newxlsx`, `writexlsx`, `savexlsx`,
    `Worksheet`, `sheetnames`, `sheetcount`, `hassheet`, `rename!`, `addsheet!`, `copysheet!`, `deletesheet!` 

- Cells & data
    `CellRef`, `row_number`, `column_number`, `eachrow`, `eachtablerow`,
    `readdata`, `getdata`, `gettable`, `readtable`, `readto`, `writetable`, `writetable!`,
    `addDefinedName`

- Formats
    `setFormat`, `setFont`, `setBorder`, `setFill`, `setAlignment`,
    `setUniformFormat`, `setUniformFont`, `setUniformBorder`, `setUniformFill`, `setUniformAlignment`, `setUniformStyle`,
    `setConditionalFormat`,
    `setColumnWidth`, `setRowHeight`,
    `getMergedCells`, `isMergedCell`, `getMergedBaseCell`, `mergeCells`

## Breaking changes
A small number of breaking chamges have been made. These are mainly in response to issues raised on `XLSX.jl`, or are to package internals which may, nevertheless be in use elsewhere.

- `eachrow` remains functionally the same as before but is now `Base.eachrow` rather than `XLSX.eachrow`.
- `infer_eltypes` now defaults to true (e.g. in `gettable` and `readtable`).
- `enable_cache` now universally defaults to true, including where this was previously not the case (e.g. `readtable`).

In addition, internal changes have been made to the following data `struct`s:
- `SheetRowStreamIteratorState`
- `WorksheetCacheIteratorState`
- `WorksheetCache`
- `Worksheet`
- `SheetRow`

## Changed dependencies
`XLSX2.jl` has fully migrated to `ZipArchives.jl` whereas `XLSX.jl` relied upon both this an `ZipFiles.jl`. In addition, xml support is now from `XML.jl` rather than `EzXML.jl`.
New functionality that has been added has brought the following additional dependencies (compared with `XLSX.jl` v0.10.4)
- `Colors.jl`
- `UUIDs.jl`

## Precompilation
`XLSX2.jl` now makes use of `PrecompileTools.jl` (initially only in a small way).


