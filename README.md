
# XLSX2.jl

[![License][license-img]](LICENSE)
[![CI][ci-img]][ci-url]
[![codecov][codecov-img]][codecov-url]
[![dev][docs-dev-img]][docs-dev-url]
[![stable][docs-stable-img]][docs-stable-url]

[license-img]: http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ci-img]: https://github.com/TimG1964/XLSX2.jl/workflows/CI/badge.svg
[ci-url]: https://github.com/TimG1964/XLSX2.jl/actions?query=workflow%3ACI
[codecov-img]: https://img.shields.io/codecov/c/github/TimG1964/XLSX2.jl/master.svg?label=codecov&style=flat-square
[codecov-url]: http://codecov.io/github/TimG1964/XLSX2.jl?branch=master
[docs-dev-img]: https://img.shields.io/badge/docs-dev-blue.svg?style=flat-square
[docs-dev-url]: https://TimG1964.github.io/XLSX2.jl/dev
[docs-stable-img]: https://img.shields.io/badge/docs-stable-blue.svg?style=flat-square
[docs-stable-url]: https://TimG1964.github.io/XLSX2.jl/stable

Excel file reader/writer for the Julia language.

## Introduction

**XLSX2.jl** is a Julia package to read and write
[Excel](https://products.office.com/excel) spreadsheet files.

Internally, an Excel XLSX file is just a
[Zip](https://en.wikipedia.org/wiki/Zip_(file_format)) file with a set of
[XML](https://en.wikipedia.org/wiki/XML) files inside.
The formats for these XML files are described in
the [Standard ECMA-376](https://ecma-international.org/publications-and-standards/standards/ecma-376/).

This package follows the EMCA-376 to parse and generate XLSX files.

## Requirements

* Julia v1.8

* Linux, macOS or Windows.

## Installation

From a Julia session, run:

```julia
julia> using Pkg

julia> Pkg.add("XLSX2")
```

## Source Code

The source code for this package is hosted at
[https://github.com/TimG1964/XLSX2.jl](https://github.com/TimG1964/XLSX2.jl).

## License

The source code for the package **XLSX2.jl** is licensed under
the [MIT License](https://raw.githubusercontent.com/TimG1964/XLSX2.jl/master/LICENSE).

## Getting Help

If you're having any trouble, have any questions about this package
or want to ask for a new feature,
just open a new [issue](https://github.com/TimG1964/XLSX2.jl/issues).

## Contributing

Contributions are always welcome!

To contribute, fork the project on [GitHub](https://github.com/TimG1964/XLSX2.jl)
and send a Pull Request.

## References

* [ECMA Open XML White Paper](https://www.ecma-international.org/wp-content/uploads/OpenXML-White-Paper.pdf)

* [ECMA-376](https://ecma-international.org/publications-and-standards/standards/ecma-376/)

* [Excel file limits](https://support.microsoft.com/en-us/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3)

## Alternative Packages

* [XLSX.jl](https://github.com/felipenoris/XLSX.jl)

* [LibXLSXWriter.jl](https://github.com/jaakkor2/LibXLSXWriter.jl)

* [ExcelFiles.jl](https://github.com/davidanthoff/ExcelFiles.jl)

* [ExcelReaders.jl](https://github.com/davidanthoff/ExcelReaders.jl)

* [XLSXReader.jl](https://github.com/mpastell/XLSXReader.jl)

* [Taro.jl](https://github.com/aviks/Taro.jl)
