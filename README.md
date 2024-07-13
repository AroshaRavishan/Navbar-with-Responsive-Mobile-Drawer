# Responsive Navbar with Drawer Menu

## Component Structure

This Vue.js component creates a responsive navigation bar with both desktop and mobile layouts. It's structured as follows:

## Component Previews

### Mobile Drawer View
![Responsive Drawer](https://github.com/AroshaRavishan/Navbar-with-Responsive-Mobile-Drawer/raw/main/Responsive%20Drawer.png)
*Mobile Drawer navigation with mega menu dropdown*

### Mobile View
![Mobile Menu](https://github.com/AroshaRavishan/Navbar-with-Responsive-Mobile-Drawer/raw/main/Mobile%20Menu%20View.png)
*Mobile navigation with slide-out drawer*

### Script Section
- Uses Vue 3 Composition API with `<script setup>`
- Imports:
  - `ref` and `onMounted` from Vue
  - `Preline` (likely a UI library)
- State management:
  - `isDrawerOpen`: Reactive reference for mobile drawer state
- Methods:
  - `toggleDrawer()`: Toggles mobile drawer
  - `closeMobileMenu()`: Closes mobile drawer
- Lifecycle hook:
  - `onMounted()`: Initializes Flowbite (another UI library)

### Template Section
The template is divided into two main parts:

1. Main Navigation Bar:
   - Container with flex layout
   - Logo section
   - Mega menu dropdown (desktop only)
   - Navigation links (desktop only)
   - Login and Register buttons (desktop only)
   - Hamburger menu icon (mobile only)

2. Mobile Drawer:
   - Full-screen overlay
   - Side-sliding drawer
   - Close button
   - Mobile navigation links

## Key Features and Implementation Details

### Responsive Design
- Uses Tailwind CSS classes for responsive behavior
- Desktop view: Full menu with dropdowns
- Mobile view: Hamburger icon and slide-out drawer

### Mega Menu (Desktop)
- Implemented as a dropdown
- Uses `hs-dropdown` classes (likely from a UI library)
- Contains multiple columns of links

### Mobile Drawer
- Activated by hamburger icon
- Full-screen overlay with semi-transparent background
- Side-sliding drawer from right
- Contains mobile-optimized navigation links

### Vue Transitions
- Applied to mobile drawer for smooth enter/leave animations
- Uses Vue's `<transition>` component with custom classes

### Dynamic Asset Loading
- Uses ternary operator to handle asset URLs
- Allows for flexible deployment in different environments

### State Management
- `isDrawerOpen` ref controls mobile drawer visibility
- `toggleDrawer` method toggles this state
- `closeMobileMenu` method explicitly sets state to closed

### Event Handling
- Click events on mobile menu items to close drawer
- Click on overlay to close drawer

### Styling
- Extensive use of Tailwind CSS utility classes
- Custom styles for transitions and specific tweaks

### Accessibility Considerations
- Uses semantic HTML elements (nav, button, etc.)
- Aria attributes could be added for improved accessibility

### Performance Optimizations
- Lazy loading of images
- Conditional rendering of mobile drawer

## Component Usage

To use this component:
1. Import it into your Vue application
2. Place it in your app's layout, typically at the top of the page
3. Ensure all required assets (logos, icons) are available
4. Configure router links to match your app's routes
5. Customize the mega menu and mobile drawer contents as needed

## Potential Enhancements

1. Implement active state for current route
2. Add dropdown animations for mega menu
3. Enhance accessibility with ARIA attributes
4. Implement language switching functionality
5. Add search functionality in the navigation

## Dependencies and Requirements

- Vue 3
- Vue Router (for navigation links)
- Tailwind CSS
- Preline and Flowbite UI libraries
- SVG assets for logos and icons

This component provides a robust, feature-rich navigation solution adaptable to various web application needs, with a focus on responsiveness and user experience.
