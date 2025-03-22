# Vision Clarity Institute - CSS Organization

This repository contains the organized CSS structure for the Vision Clarity Institute website. It follows a modular, component-based approach to improve maintainability, consistency, and performance.

## Directory Structure

The CSS is organized into the following directories:

```
css/
├── main.css              # Compiled CSS for production
├── base/                 # Foundational styles
│   ├── reset.css         # CSS reset/normalize
│   ├── typography.css    # Font definitions
│   ├── colors.css        # Color variables
│   ├── accessibility.css # Accessibility utilities
│   └── animations.css    # Common animations
│
├── components/           # Reusable UI components
│   ├── header.css        # Header styles
│   ├── footer.css        # Footer styles
│   ├── buttons.css       # Button styles
│   ├── forms.css         # Form elements
│   ├── modals.css        # Modal dialogs
│   ├── cards.css         # Service cards
│   └── navigation.css    # Navigation menus
│
├── layout/               # Page structure elements
│   ├── grid.css          # Grid system
│   ├── containers.css    # Container elements
│   └── section-layouts.css # Common section layouts
│
├── pages/                # Page-specific styles
│   ├── home.css          # Home page specific styles
│   ├── services.css      # Services page styles
│   ├── technology.css    # Technology page styles
│   ├── locations.css     # Locations page styles
│   └── contact.css       # Contact page styles
│
└── utilities/            # Helper classes and functions
    ├── i18n-support.css  # Internationalization support
    ├── rtl.css           # Right-to-left language support
    └── theme.css         # Theme variables and customizations
```

## Implementation Guide

### 1. Importing Styles

For development, include the necessary CSS files in your HTML:

```html
<!-- Base styles (always required) -->
<link rel="stylesheet" href="css/base/reset.css">
<link rel="stylesheet" href="css/base/typography.css">
<link rel="stylesheet" href="css/base/colors.css">
<link rel="stylesheet" href="css/base/accessibility.css">
<link rel="stylesheet" href="css/base/animations.css">

<!-- Layout styles (always required) -->
<link rel="stylesheet" href="css/layout/grid.css">
<link rel="stylesheet" href="css/layout/containers.css">
<link rel="stylesheet" href="css/layout/section-layouts.css">

<!-- Component styles (as needed) -->
<link rel="stylesheet" href="css/components/header.css">
<link rel="stylesheet" href="css/components/footer.css">
<link rel="stylesheet" href="css/components/buttons.css">
<link rel="stylesheet" href="css/components/forms.css">
<!-- Add other component styles as needed -->

<!-- Utility styles (always required) -->
<link rel="stylesheet" href="css/utilities/theme.css">
<link rel="stylesheet" href="css/utilities/i18n-support.css">
<link rel="stylesheet" href="css/utilities/rtl.css">

<!-- Page-specific styles (only include what you need) -->
<link rel="stylesheet" href="css/pages/home.css">
<!-- Or other page styles based on the current page -->
```

For production, use the compiled `main.css` file:

```html
<link rel="stylesheet" href="css/main.css">
```

### 2. Compilation for Production

To combine all CSS files into a single `main.css` file for production, you can use a CSS preprocessor or bundler like PostCSS, webpack, or Gulp. Here's a basic PostCSS command:

```bash
npx postcss css/**/*.css --dir dist/css
```

### 3. CSS Variables Usage

This system uses CSS variables for consistent theming. Key variables are defined in `css/base/colors.css` and `css/utilities/theme.css`. Example usage:

```css
.btn-primary {
  background-color: var(--primary-color);
  color: var(--text-light);
}
```

### 4. Responsive Design

The CSS includes breakpoints for responsive design:

- **Mobile**: Up to 576px
- **Tablet**: 577px to 768px
- **Small Desktop**: 769px to 992px
- **Medium Desktop**: 993px to 1200px
- **Large Desktop**: 1201px and above

Example usage:

```css
@media (max-width: 768px) {
  .grid-3 {
    grid-template-columns: 1fr;
  }
}
```

### 5. Internationalization Support

For multilingual support:

1. Set the `lang` attribute on the `<html>` element
2. For RTL languages (Arabic, Hebrew, Persian), add `dir="rtl"` to the `<html>` element
3. Use the appropriate language-specific fonts via `css/utilities/i18n-support.css`

Example:

```html
<html lang="ar" dir="rtl">
```

### 6. Adding New Components

To add a new component:

1. Create a new CSS file in the appropriate directory
2. Use BEM naming convention for classes (Block, Element, Modifier)
3. Use CSS variables for colors, spacing, etc.
4. Import the new file in your HTML or add it to the compilation process

## Coding Standards

1. **BEM Naming Convention**: Use Block, Element, Modifier pattern
   ```css
   .card {} /* Block */
   .card__title {} /* Element */
   .card--featured {} /* Modifier */
   ```

2. **CSS Variables**: Use variables for consistent styling
   ```css
   :root {
     --primary-color: #4CAF50;
   }
   ```

3. **Comments**: Add comments for complex selectors or functionality

4. **File Size**: Keep files focused on a single responsibility

5. **Accessibility**: Ensure styles support accessibility requirements

## Browser Support

This CSS structure supports:

- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- iOS Safari
- Android Chrome

## License

This CSS organization is proprietary to Vision Clarity Institute and is not to be used, reproduced, or distributed without permission.
