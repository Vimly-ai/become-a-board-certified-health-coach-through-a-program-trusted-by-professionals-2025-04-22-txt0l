# IHI Studies Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the IHI Studies health coach certification landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance below.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">IHI Studies</a>
```
- Replace "IHI Studies" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors">Features</a>
    <!-- Additional navigation items -->
</div>
```
- Modify link text between `>` and `</a>`
- Keep the `hidden md:flex` class to maintain mobile responsiveness

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white leading-tight mb-6">
    Become a board-certified health coach through a program trusted by professionals
</h1>
```
- Update heading text while maintaining the HTML structure
- `text-4xl md:text-6xl` controls text size (smaller on mobile, larger on desktop)
- `mb-6` adds margin bottom (spacing)

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-blue-600`, `text-gray-600`, `text-white`
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom), `mb-4` (margin bottom)
- Background: `bg-white`, `bg-blue-600`, `bg-gray-50`

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Ensure the target section has a matching `id` attribute

### External Links
The main call-to-action button:
```html
<a href="https://www.ihistudies.com/coach/" class="inline-flex items-center px-8 py-4...">
```
To update:
1. Replace the URL in `href` with your desired destination
2. Test the link to ensure it works
3. Consider adding `target="_blank"` for external links

### Link Styling
Maintain consistent styling by copying existing classes:
- Normal links: `text-gray-600 hover:text-blue-600 transition-colors`
- Button links: `inline-flex items-center px-8 py-4 border border-transparent text-lg font-medium rounded-md`

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition">Terms of Service</a></li>
```

### Link Styling Consistency
Copy these classes for new links:
```html
class="hover:text-blue-400 transition"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that the `href` attribute matches the section's `id`
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Keep the `md:` prefix classes for responsive behavior
   - Test on multiple screen sizes using browser dev tools
   - Don't remove `hidden md:flex` from navigation

3. **Styling Inconsistencies**
   - Copy existing Tailwind classes for consistency
   - Use the same color codes (e.g., blue-600) throughout
   - Maintain spacing patterns (px-4, py-4, etc.)

Remember to:
- Always test changes in multiple browsers
- Maintain mobile responsiveness
- Back up files before making changes
- Keep consistent spacing and formatting
- Test all links after updates

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)