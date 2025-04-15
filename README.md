# Landing Page Maintenance Guide

This guide will help you maintain and customize the ComputerBril landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">ComputerBril</a>
```
- Replace "ComputerBril" with your desired text
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

2. **Navigation Links:**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Keep the `hover:text-blue-600` for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 leading-tight mb-8">
    Wat Is Het Verschil Tussen Een Leesbril En Een Beeldschermbril
</h1>
```
- Replace the Dutch text with your headline
- Don't remove the responsive classes (`text-4xl md:text-5xl lg:text-6xl`)
- `mb-8` adds bottom margin spacing

### Features Section
To add new feature cards:

1. Copy this template:
```html
<div class="p-8 rounded-xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
    </div>
    <h3 class="text-xl font-semibold mb-4">Your Feature Title</h3>
    <p class="text-gray-600">Your feature description here.</p>
</div>
```

2. Paste within the grid container:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Change the `href="#section-name"` to match your section IDs
2. Ensure corresponding sections have matching IDs: `<section id="section-name">`
3. For external links, use full URLs: `href="https://your-url.com"`

### Call-to-Action Buttons
Located in hero and bottom sections:
```html
<a href="https://computerbril.org" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Ontdek Meer
</a>
```
- Replace `https://computerbril.org` with your target URL
- Update button text between `>` and `</a>`

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links:
```html
<li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout:**
- Check that you haven't removed important Tailwind classes
- Verify container divs are properly closed
- Keep the responsive classes (`md:`, `lg:` prefixes)

2. **Links Not Working:**
- Ensure section IDs match navigation href values
- Check for typos in URLs
- Verify file paths for internal pages

3. **Styling Issues:**
- Don't remove `class="font-sans antialiased"` from body
- Maintain the existing color scheme classes
- Keep transition classes for smooth effects

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check that Alpine.js is properly loaded for mobile menu
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different screen sizes using your browser's developer tools.