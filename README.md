# 32-bit Binary Formatter

A web-based tool for formatting and visualizing 32-bit binary numbers with customizable highlighting and dynamic contrast adjustment.

## Features

- Convert decimal numbers (0-4,294,967,295) to 32-bit binary representation
- Customize text color and segment highlighting
- Dynamic contrast adjustment for optimal readability
- Light/dark theme support with persistence
- Responsive design
- Example function call generation

## Usage

1. Enter a decimal number between 0 and 4,294,967,295
2. Customize the appearance:
   - Select text color using the color picker
   - Enable/disable segment highlighting
   - Choose highlight colors from preset palettes
3. Toggle between light and dark themes using the theme switch

## Technical Details

### Color Contrast

The application automatically adjusts text color in highlighted segments to maintain WCAG AA minimum contrast ratio (4.5:1) for normal text. This ensures readability regardless of the chosen highlight colors.

### Preset Color Palettes

Two sets of preset colors are available:

- Light Mode: Optimized for dark text on light backgrounds
- Dark Mode: Optimized for light text on dark backgrounds

Each preset color has been tested for contrast compliance.

### Configuration Object

The formatter accepts a configuration object with the following structure:

```javascript
{
  number: number,                    // Required: Decimal number to convert
  segmentColors: [string|null, ...], // Optional: Array of 4 preset IDs or null
  textColor: string                  // Optional: CSS color string for binary digits
}
```

## Browser Support

The application is compatible with modern browsers that support:

- CSS Custom Properties (Variables)
- ES6+ JavaScript features
- HTML5 input types (color, number)

## Development

This is a static web application requiring no build step. Simply serve the files through a web server.

### Local Development

1. Clone the repository
2. Serve the files using your preferred method:
   - Python: `python -m http.server`
   - Node.js: `npx serve`
   - VS Code Live Server extension

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
