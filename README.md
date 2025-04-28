# Blueblock Landing Page Maintenance Guide

This guide will help you maintain and customize the Blueblock Computerbril landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-blue-400 bg-clip-text text-transparent">Blueblock</a>
```
- Replace "Blueblock" with your desired text
- Keep the classes to maintain the blue gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <!-- More menu items -->
</div>
```
- Update the text between `>` and `</a>` for each menu item
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-blue-600 to-blue-400 bg-clip-text text-transparent">
    Blueblock Computerbril
</h1>
```
- Update the heading text while maintaining the gradient effect
- The classes ensure responsive text sizing (`text-4xl` for mobile, `lg:text-6xl` for large screens)

### Tailwind CSS Class Guide
Common classes used throughout:
- `container mx-auto`: Centers content with automatic margins
- `px-4 sm:px-6 lg:px-8`: Responsive padding
- `text-gray-600`: Sets text color
- `hover:text-blue-600`: Changes text color on hover
- `transition-colors duration-300`: Smooth color transitions

## Managing Links

### Navigation Links
1. **Internal Section Links:**
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- The `#` symbol links to sections with matching IDs
- Ensure section IDs match these href values

2. **Call-to-Action Button:**
```html
<a href="https://computerbril.org/winkel" class="inline-flex items-center px-6 py-3 rounded-full bg-blue-600">
```
- Replace the URL with your actual shop link
- Keep the classes for consistent button styling

### Updating External Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <!-- Facebook icon -->
    </a>
</div>
```
- Replace `#` with actual social media URLs
- Test all links after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
1. Locate the footer links section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
```

3. Create matching HTML files:
- Create `privacy.html` and `terms.html` in the same directory
- Copy the header and footer from index.html to maintain consistency
- Add your policy content between them

## Troubleshooting

### Common Issues:

1. **Broken Links**
- Check for typos in href attributes
- Verify file names match exactly (case-sensitive)
- Ensure section IDs exist for internal links

2. **Styling Problems**
- Keep all Tailwind classes together without spaces
- Don't remove responsive classes (e.g., `md:` or `lg:` prefixes)
- Maintain the structure of gradient classes for consistent effects

3. **Layout Issues**
- Don't remove container classes
- Keep the responsive padding classes
- Maintain the grid structure in features section

### Need Help?
- Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test on multiple screen sizes using responsive mode

Remember to always backup your files before making changes and test thoroughly across different devices and browsers.