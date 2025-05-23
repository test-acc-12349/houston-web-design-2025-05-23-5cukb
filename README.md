# Houston Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Houston Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">HWD</a>
```
- Replace "HWD" with your desired logo text
- Adjust size using `text-2xl` (options: `text-xl`, `text-3xl`, `text-4xl`)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Replace text between `>` and `</a>` for each menu item
- Keep the `href` attributes matching your section IDs

### Hero Section
The main banner section at the top:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Houston Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Houston</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Text sizes use responsive classes:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Professional hosting included with every website package.</p>
</div>
```
To modify:
1. Change icon: Update `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading: Replace text between `<h3>` tags
3. Update description: Modify text between `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections: Use `#section-id`
2. For external pages: Use full URL `https://example.com`
3. For local pages: Use relative path `/about.html`

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://hwd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```
Replace `https://hwd.com` with your actual URL or contact form link.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms page (e.g., `terms.html`)
3. Update the links:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
- If elements look wrong on mobile:
  - Check for `md:` prefixed classes
  - Ensure the viewport meta tag is present
  - Test using browser dev tools mobile view

2. **Missing Icons**
- If icons don't appear:
  - Verify Font Awesome CSS is loaded
  - Check icon class names against Font Awesome documentation
  - Ensure internet connection for CDN access

3. **Links Not Working**
- For internal links (#features, etc.):
  - Verify section IDs match exactly
  - Check for typos in href attributes
  - Ensure no spaces in IDs
- For external links:
  - Verify full URL including https://
  - Test links in new tab
  - Check for typos

Remember to:
- Always backup before making changes
- Test on multiple devices and browsers
- Keep the original HTML as reference
- Maintain consistent spacing and indentation
- Test all links after updating

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).