# Lifterbell Landing Page Maintenance Guide

This guide will help you maintain and customize the Lifterbell landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Lifterbell</a>
```
- Replace "Lifterbell" with your desired text
- Keep the classes intact to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="hover:text-purple-400 transition-colors duration-300">FAQ</a>
</div>
```
- Replace text within `<a>` tags
- Don't remove the `hover:text-purple-400` class as it creates the hover effect

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Koop Lifterbell Shirt Met Korting</h1>
```
- Update the heading text while keeping the size classes (`text-4xl`, `md:text-6xl`, `lg:text-7xl`)
- These classes ensure proper sizing across different screen sizes

### Features Section
To modify feature cards:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:bg-gray-700/50 transition-all duration-300 hover:scale-105">
    <div class="text-purple-400 text-4xl mb-4">⚡</div>
    <h3 class="text-xl font-bold mb-4">Hoogwaardig Materiaal</h3>
    <p class="text-gray-400">Premium kwaliteit stof voor optimaal comfort tijdens je workout</p>
</div>
```
- Change emoji icons in the `text-4xl` div
- Update heading and paragraph text
- Maintain the hover classes for animation effects

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```
To update:
1. The `#` symbol indicates section IDs on the same page
2. Ensure section IDs match exactly (case-sensitive)
3. Example: To link to a new section:
   ```html
   <a href="#new-section">New Section</a>
   ```
   Then create the section with matching ID:
   ```html
   <section id="new-section">
   ```

### Call-to-Action Links
Current purchase links:
```html
<a href="https://amzn.to/3EGnZle" class="bg-gradient-to-r from-purple-600 to-pink-600">
```
To update:
1. Replace the Amazon affiliate link with your product URL
2. Keep the gradient classes for consistent styling
3. Test the link thoroughly before deployment

## Adding Privacy and Terms Pages

### Footer Links Setup
Current footer links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms & Conditions</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradient Text**
If gradient text disappears:
```html
<!-- Required classes for gradient text -->
bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
```

2. **Responsive Issues**
Check these class prefixes:
- `md:` (medium screens)
- `lg:` (large screens)
- Example: `text-4xl md:text-6xl lg:text-7xl`

3. **Link Not Working**
- Verify href attributes have correct paths
- Check for typos in section IDs
- Ensure external URLs include `https://`

### Need Help?
For support, contact:
```html
<p class="text-gray-400">support@example.com</p>
```
Update this email address with your actual support contact.

Remember to test all changes in multiple browsers and screen sizes before deploying to production.