# Professional Font Implementation

## Overview
This document outlines the professional font implementation for the Soujanya Ponnapalli academic website.

## Font Stack Implementation

### Primary Fonts

1. **Libre Franklin** - sans-serif used for body text, headings, and navigation
   - Matches [Matei Zaharia's homepage](https://people.eecs.berkeley.edu/~matei/),
     which loads the same face and the same four weights
   - Weights: 400, 500, 600, 700
   - Loaded from Google Fonts with `display=swap`
   - Fallback stack: `-apple-system`, `BlinkMacSystemFont`, `Segoe UI`, Roboto,
     Helvetica, Arial, generic sans-serif

2. **JetBrains Mono** - monospace for code blocks
   - Weights: 400, 500, 600
   - Loaded from Google Fonts

### Font Hierarchy

- **Body text, headings, navigation**: Libre Franklin stack
- **Headings**: weight 600, no negative tracking (matching his `h1`)
- **Code**: JetBrains Mono (400 weight)

### Colour palette

Also taken from that homepage, read off the custom properties in its
`modern-style.css`:

| Role | Value | His variable |
| --- | --- | --- |
| Body text | `#202124` | `--text` |
| Headings | `#151b26` | `--heading` |
| Muted text | `#5f6368` | `--muted` |
| Links | `#1455a3` | `--link` |
| Link hover | `#0b3f7a` | `--link-hover` |
| Rules and borders | `#deded8` | `--rule` |
| Stronger rules | `#c6c6bd` | `--rule-strong` |
| Panels and badges | `#f8f8f6` | `--panel` |
| Accent fill | `#edf3f8` | `--accent-soft` |

This replaced the previous scheme, which took Palatino and `#0000CC` from the
CV. The Palatino stack and the self-hosted TeX Gyre Pagella faces are still in
the repo (commented in `_variables.scss`, declared but unused in `_fonts.scss`)
so that switching back is a one-line change.

## Implementation Details

### Files Modified
1. `_sass/_variables.scss` - Font stacks and the colour palette
2. `_sass/_fonts.scss` - `@font-face` declarations for TeX Gyre Pagella (unused)
3. `assets/fonts/` - Subset WOFF2 files plus licensing and regeneration notes
4. `assets/css/main.scss` - Imports the `fonts` partial
5. `_sass/_base.scss` - Enhanced typography with better spacing and rendering
6. `_sass/_masthead.scss` - Updated navigation font family
7. `_includes/head.html` - Google Fonts import for Libre Franklin and JetBrains Mono
8. `_includes/head/custom.html` - Custom typography styles

### Key Improvements
- **Font Rendering**: Added `-webkit-font-smoothing: antialiased` and `-moz-osx-font-smoothing: grayscale`
- **Text Rendering**: Optimized with `text-rendering: optimizeLegibility`
- **Line Height**: Increased to 1.6 for better readability
- **Font Loading**: Preconnect to Google Fonts for faster loading

### Typography Scale
- Maintained existing type scale but enhanced with better font weights
- Added consistent font weight variables for maintainability
- Improved heading hierarchy with a consistent sans-serif face

## Benefits
1. **Professional Appearance**: Modern, clean typography suitable for academic content
2. **Improved Readability**: Better contrast and spacing for long-form content
3. **Consistency**: Unified font system across all pages
4. **Performance**: Optimized font loading with preconnect and display swap
5. **Accessibility**: High contrast and clear typography for better accessibility

## Browser Support
- Modern browsers with Google Fonts support
- Graceful fallback to system fonts
- Progressive enhancement approach

## Testing
The implementation has been tested with:
- Jekyll build process
- Local development server
- Cross-browser compatibility considerations 