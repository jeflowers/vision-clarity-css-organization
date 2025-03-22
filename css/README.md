# CSS Architecture for Vision Clarity Institute

This directory contains the organized CSS files for the Vision Clarity Institute website. The structure is designed to improve maintainability, collaboration, and performance.

## Directory Structure

- **base/**: Foundational styles and variables
  - `reset.css`: CSS reset/normalize
  - `typography.css`: Font definitions, sizes, weights
  - `colors.css`: Color variables
  - `accessibility.css`: Accessibility utilities
  - `animations.css`: Common animations
  
- **components/**: Reusable UI components
  - `header.css`: Header styles
  - `footer.css`: Footer styles
  - `buttons.css`: Button styles
  - `forms.css`: Form elements
  - `modals.css`: Modal dialogs
  - `cards.css`: Service cards
  - `navigation.css`: Navigation menus
  
- **layout/**: Page structure elements
  - `grid.css`: Grid system
  - `containers.css`: Container elements
  - `section-layouts.css`: Common section layouts
  
- **pages/**: Page-specific styles
  - `home.css`: Home page specific styles
  - `services.css`: Services page styles
  - `technology.css`: Technology page styles
  - `locations.css`: Locations page styles
  - `contact.css`: Contact page styles
  
- **utilities/**: Helper classes and functions
  - `i18n-support.css`: Internationalization support
  - `rtl.css`: Right-to-left language support
  - `theme.css`: Theme variables and customizations

## Usage Guidelines

1. Use BEM naming convention for all CSS classes
2. Keep files focused on a single responsibility
3. Use CSS variables for colors, spacing, and typography
4. Avoid using !important except for utility classes
5. Comment your code for complex selectors and functionality

## Compilation

For production, all CSS files are compiled into a single `main.css` file. This compilation is handled automatically through GitHub Actions when changes are pushed to the repository.