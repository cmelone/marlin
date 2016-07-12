# marlin
marlin provides an easy way to generate a `Packages.gz` file for your Cydia/APT repository.

marlin runs on Mac, Linux, and Windows.

## Advantages over `dpkg-scanpackages`
- No need to install `dpkg`, `perl`, or other dependancies you don't want.
- Standalone binary, no dependencies
- Cross platform compatibility
- automatically gzips `Packages` file
- very fast

## Installing
- grab a copy of marlin for your correct OS and architecture on the [releases](//github.com/cmelone/marlin/releases) page
- run marlin from the current directory (`./marlin`) because it is most likely not in your `$PATH`

## Compiling
Golang must be installed correctly on your computer in order to compile Marlin correctly.

    go get github.com/blakesmith/ar
    go get github.com/cmelone/marlin
    go install github.com/cmelone/marlin

This will create a binary named marlin in the current folder. Add your deb files to a folder named `debs` (you can configure this in `marlin.go`). Finally, run `marlin` and a `Packages.gz` file will be generated.

## TODO:
- Better error handling
- Ability to create a Release file

Thank you to [OpenRepo](//github.com/eswick/openrepo). Much of this codebase is heavily influenced by it.
