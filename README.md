# Connectics Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Connectics telecommunication services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Connectics</a>
```
- Replace "Connectics" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```
- Modify text between `<a>` tags
- Maintain the `space-x-8` class for consistent spacing
- Keep the `hover:text-blue-600` for interactive feedback

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Telecommunication Services for Small and Midsize Companies
</h1>
```
- Update heading text while maintaining responsive sizes
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen widths

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg">
    <div class="w-12 h-12 bg-blue-100 rounded-lg">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```
- Maintain padding (`p-8`) and margin (`mb-4`) classes for consistent spacing
- Keep `shadow-lg` for depth effect
- Update text within `<h3>` and `<p>` tags

## Managing Links

### Internal Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match these href values
2. For external pages, replace "#" with full URLs
3. Example: `<a href="https://yoursite.com/features">Features</a>`

### Contact Link
The email link is currently set to:
```html
<a href="mailto:info@connectics.ch">Contact Us</a>
```
To update:
1. Replace "info@connectics.ch" with your email
2. Format: `mailto:your.email@domain.com`

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create privacy.html and terms.html in your root directory
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check for typos in href attributes
- Verify file paths are correct
- Ensure linked files exist in the specified location

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Maintain the existing responsive class structure
- Test on different screen sizes using browser dev tools

3. **Styling Inconsistencies**
- Keep Tailwind color classes consistent (e.g., blue-600, gray-400)
- Maintain spacing classes (mb-4, p-8, etc.)
- Don't remove hover states (hover:text-white, hover:scale-105)

### Need Help?
- Check Tailwind CSS documentation for class references
- Use browser inspector to identify specific elements
- Maintain backup copies before making changes
- Test all changes in a development environment first

Remember to always test your changes across different devices and browsers before deploying to production.