# 32-bit Binary Formatter

A web-based tool for formatting and visualizing 32-bit binary numbers with customizable highlighting and dynamic contrast adjustment.

## Features

- Convert decimal numbers (0-4,294,967,295) to 32-bit binary representation
- Customize text color and segment highlighting
- Dynamic contrast adjustment for optimal readability (≥ 8:1 ratio)
- Light/dark theme support with persistence
- Responsive design
- Example function call generation
- Modern development setup with Vite and Yarn

## Usage

1. Enter a decimal number between 0 and 4,294,967,295
2. Customize the appearance:
   - Select text color using the color picker
   - Enable/disable segment highlighting
   - Choose highlight colors from preset palettes
3. Toggle between light and dark themes using the theme switch

## Demo

## Technical Details

### Color Contrast

The application automatically adjusts text color in highlighted segments to maintain a high contrast ratio of at least 8:1 for all text. This exceeds WCAG AAA requirements and ensures excellent readability regardless of the chosen highlight colors.

### Preset Color Palettes

Two sets of preset colors are available:

- Light Mode: Optimized for dark text on light backgrounds (contrast ratio ≥ 8:1)
- Dark Mode: Optimized for light text on dark backgrounds (contrast ratio ≥ 8:1)

Each preset color has been carefully selected and tested for contrast compliance.

### Configuration Object

The formatter accepts a configuration object with the following structure:

```javascript
{
  number: number,                    // Required: Decimal number to convert
  segmentColors: [string|null, ...], // Optional: Array of 4 preset IDs or null
  textColor: string                  // Optional: CSS color string for binary digits
}
```

### Local Development

1. Clone the repository
2. Install dependencies:
   ```bash
   yarn install
   ```
3. Start the development server:
   ```bash
   yarn dev
   ```

## Planned Improvements

### Accessibility

- [ ] ARIA labels for color inputs
- [ ] Keyboard navigation for segment controls
- [ ] Screen reader descriptions for binary output
- [ ] Improved focus management

### Performance

- [ ] Input handler debouncing
- [ ] Color contrast calculation memoization
- [ ] Theme preference caching

### Features

- [ ] Copy-to-clipboard functionality
- [ ] Animation transitions for theme changes
- [ ] Color contrast information tooltips
- [ ] TypeScript support
- [ ] Additional number formats (hex, octal)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Repository

View the project on GitHub: [ICJIA/32-bit-binary-formatter](https://github.com/ICJIA/32-bit-binary-formatter)
