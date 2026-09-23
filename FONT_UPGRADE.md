# Professional Font Implementation

## Overview
This document outlines the professional font implementation for the Soujanya Ponnapalli academic website.

## Font Stack Implementation

### Primary Fonts

1. **Palatino** - serif used for body text, headings, and navigation
   - Matches the CV, whose PDF embeds URW Palladio L (LaTeX `mathpazo`/`palatino`)
   - Resolved from the visitor's own system first: `Palatino Linotype`
     (Windows), `Palatino` (macOS), `Book Antiqua`, `URW Palladio L`
   - Falls back to self-hosted **TeX Gyre Pagella** (GUST Font License), GUST's
     Unicode extension of that same URW Palladio L design
   - Final fallback: Georgia, then generic serif

2. **JetBrains Mono** - monospace for code blocks
   - Weights: 400, 500, 600
   - Loaded from Google Fonts

### Font Hierarchy

- **Body text, headings, navigation**: Palatino stack
- **Code**: JetBrains Mono (400 weight)

### Why the hybrid

Most visitors already have a Palatino, so listing the system faces first means
macOS and Windows render from disk and download nothing. Only visitors without
one fetch the WOFF2 (~33KB per face, loaded lazily per face as needed).

The webfont is deliberately **not** `<link rel="preload">`ed: preload fetches
unconditionally, which would charge every visitor for a font most already have.

macOS ships `/System/Library/Fonts/Palatino.ttc`, but that is Apple's licensed
system font and is only ever used off the visitor's own disk - it is never
converted or self-hosted. See `assets/fonts/README.md`.

## Implementation Details

### Files Modified
1. `_sass/_variables.scss` - Font stacks point at the Palatino stack
2. `_sass/_fonts.scss` - `@font-face` declarations for self-hosted TeX Gyre Pagella
3. `assets/fonts/` - Subset WOFF2 files plus licensing and regeneration notes
4. `assets/css/main.scss` - Imports the `fonts` partial
5. `_sass/_base.scss` - Enhanced typography with better spacing and rendering
6. `_sass/_masthead.scss` - Updated navigation font family
7. `_includes/head.html` - Google Fonts import, now JetBrains Mono only
8. `_includes/head/custom.html` - Custom typography styles

### Key Improvements
- **Font Rendering**: Added `-webkit-font-smoothing: antialiased` and `-moz-osx-font-smoothing: grayscale`
- **Text Rendering**: Optimized with `text-rendering: optimizeLegibility`
- **Letter Spacing**: Improved readability with negative letter spacing for headings
- **Line Height**: Increased to 1.6 for better readability
- **Font Loading**: Preconnect to Google Fonts for faster loading

### Typography Scale
- Maintained existing type scale but enhanced with better font weights
- Added consistent font weight variables for maintainability
- Improved heading hierarchy with serif fonts for academic content

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