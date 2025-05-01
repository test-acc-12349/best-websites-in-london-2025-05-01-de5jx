# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Best Websites London landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**:
```html
<div class="text-2xl font-bold text-gray-800">
    <a href="/" class="hover:text-blue-600 transition duration-300">Best Websites</a>
</div>
```
- Replace "Best Websites" with your company name
- Keep the surrounding classes to maintain styling

2. **Navigation Menu Items**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the `href` attributes to preserve section linking

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Best Websites In London</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```
- Update heading and subheading text
- The `md:` and `lg:` prefixes control responsive text sizes
- Don't remove these classes to maintain mobile responsiveness

### Feature Cards
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless user experience...</p>
</div>
```
To modify:
1. Update the heading text between `<h3>` tags
2. Modify description text between `<p>` tags
3. Keep all classes to maintain card styling and hover effects

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure the referenced section has matching ID
   - Example: `<a href="#features">` links to `<section id="features">`

2. External links:
   - Replace `href="#"` with full URL
   - Example: `<a href="https://your-website.com/page">`

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white...">
```
- Replace `https://sigmaseo.io` with your desired URL
- Maintain all classes to preserve button styling

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder structure:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control mobile responsiveness
- Test all changes on multiple screen sizes

3. **Style Problems**
- Keep all Tailwind classes when updating text
- Classes control spacing, colors, and responsiveness
- If something looks wrong, check for accidentally deleted classes

### Need Help?
- Compare your changes against the original code
- Use browser inspection tools to identify styling issues
- Test all links after making changes
- Verify mobile responsiveness using browser developer tools

Remember to always backup your code before making changes and test thoroughly across different devices and browsers.