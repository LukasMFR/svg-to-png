# SVG to PNG Converter

This repository contains a simple shell script that converts SVG files to PNG format using `rsvg-convert`. The script allows for optional specification of the output image's height and whether to set the DPI (Dots Per Inch) for the resulting PNG.

## Prerequisites

Before running this script, ensure you have `rsvg-convert` available on your system. This tool is part of the `librsvg` package.

## Installation

Clone this repository or simply download the `svg-to-png` script directly from it. Make sure the script is executable:

```sh
chmod +x /path/to/svg-to-png
```

Optionally, you can move the script to a directory in your PATH to run it from anywhere:

```sh
sudo mv /path/to/svg-to-png /usr/local/bin/
```

## Usage

To use the script, navigate to the directory containing your SVG files and execute the following command:

```sh
svg-to-png --file <filename>.svg
```

### Options

- `-h, --help`: Display the help menu and exit.
- `-f, --file FILENAME`: Specify the SVG file to convert.
- `-H, --height HEIGHT`: Optional. Specify the height of the output image (default is 3200).
- `--set-dpi`: Optional. Set the DPI to 600 in the PNG file's metadata.

### Examples

Convert an SVG file to PNG with default settings:

```sh
svg-to-png --file image.svg
```

Convert an SVG file to PNG with a specified height:

```sh
svg-to-png --file image.svg --height 600
```

Convert an SVG file to PNG and set the DPI:

```sh
svg-to-png --file image.svg --set-dpi
```

## Contributing

Contributions are welcome. Please open an issue to discuss your ideas or submit a pull request.

## License

This project is open source and available under the [MIT License](LICENSE).