# SVG to PNG Converter

This repository contains a simple shell script that converts SVG files to PNG format. The script leverages `rsvg-convert` for the conversion process and optionally uses ImageMagick's `convert` to adjust the DPI setting of the resulting PNG.

## Prerequisites

Before running this script, you must have the following tools installed on your system:

- `rsvg-convert`: This tool is part of the `librsvg` package.
- `convert`: This command is provided by ImageMagick.

These tools are available on macOS and can be installed using [Homebrew](https://brew.sh/):

```sh
brew install librsvg imagemagick
```

## Compatibility

This script has been tested on macOS and is tailored for its default command-line environment. While `rsvg-convert` and ImageMagick are cross-platform, the script has not been tested on other operating systems such as Linux or Windows.

## Installation

Clone this repository or download the `svg-to-png` script directly from it. Make sure the script is executable:

```sh
chmod +x /path/to/svg-to-png
```

Optionally, move the script to a directory in your PATH to run it from anywhere:

```sh
sudo mv /path/to/svg-to-png /usr/local/bin/
```

## Usage

To convert an SVG file to a PNG, navigate to the directory containing your SVG file and execute:

```sh
svg-to-png --file <filename>.svg
```

### Options

- `-h, --help`: Display the help menu and exit.
- `-f, --file FILENAME`: Specify the SVG file to convert.
- `-H, --height HEIGHT`: Optional. Specify the height of the output image in pixels (default is 3200 if no width is specified).
- `-w, --width WIDTH`: Optional. Specify the width of the output image in pixels. If specified, height will adjust automatically to maintain aspect ratio unless also specified.
- `--set-dpi`: Optional. Append this flag to set the DPI to 600 in the PNG file's metadata using ImageMagick.
- `-v, --version`: Display the script version and exit.

### Examples

Convert an SVG file to PNG with default height:

```sh
svg-to-png --file image.svg
```

Convert an SVG file to PNG with a specified height:

```sh
svg-to-png --file image.svg --height 600
```

Convert an SVG file to PNG with a specified width (height will adjust automatically):

```sh
svg-to-png --file image.svg --width 800
```

Convert an SVG file to PNG with specified width and height:

```sh
svg-to-png --file image.svg --width 800 --height 600
```

Convert an SVG file to PNG and set the DPI to 600:

```sh
svg-to-png --file image.svg --set-dpi
```

## Contributing

Contributions to improve the script or extend its compatibility are welcome. Please open an issue to discuss your ideas or submit a pull request.

## License

This project is open source and available under the [MIT License](LICENSE).