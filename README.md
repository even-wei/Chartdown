# Chartdown

A markdown to PDF converter with embedded charts, written in Zig.

## Features

- 📈 Convert markdown files containing chart definitions to beautiful PDFs
- 📊 Generate line and bar charts from CSV data
- 🚀 Single binary with no runtime dependencies
- ⚡ Fast and efficient Zig implementation

## Installation

Requires Zig 0.11.0 or later.

```bash
git clone git@github.com:even-wei/Chartdown.git
cd Chartdown
zig build
```

## Usage

```bash
chartdown input.md output.pdf
```

## Syntax

Charts are embedded in markdown using code blocks with the `chart` identifier:

```
# Sales Report

Our quarterly sales:

chart
{
    type: "line",
    data: "sales.csv",
    x: "date",
    y: "revenue",
    title: "Quarterly Revenue"
}
```

### Chart Configuration

Basic options:
- `type`: Chart type ("line", "bar")
- `data`: Path to CSV file (relative to markdown file)
- `x`: Column name for X axis
- `y`: Column name for Y axis
- `title`: Chart title (optional)

Additional options:
- `width`: Chart width in pixels (default: 800)
- `height`: Chart height in pixels (default: 400)
- `color`: Line/bar color (default: "#2E86C1")

## Development

### Project Structure

```
src/
  ├── main.zig       # Entry point
  ├── parser/        # Markdown and chart parsing
  ├── chart/         # Chart generation
  ├── pdf/           # PDF generation
  └── utils/         # Common utilities
```

### Building from source

```bash
# Build the project
zig build

# Run tests
zig build test

# Install locally
zig build install
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see [LICENSE](LICENSE) for details
