# Calgary HVAC Pros Landing Page - Maintenance Guide

This guide will help you maintain and customize the Calgary HVAC Pros landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Calgary HVAC Pros  <!-- Change this text -->
</div>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Services</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    24/7 HVAC Support  <!-- Change main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Your trusted partner for all HVAC needs in Calgary  <!-- Change subheading -->
</p>
```

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8 transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-blue-500/25">
    <i class="fas fa-bolt text-4xl text-blue-400 mb-6"></i>  <!-- Change icon class -->
    <h3 class="text-xl font-semibold mb-4">Emergency Support</h3>  <!-- Change title -->
    <p class="text-gray-400">Available 24/7 for all your emergency HVAC needs</p>  <!-- Change description -->
</div>
```

### Tailwind CSS Classes Explained
- `bg-gray-900`: Dark background color
- `text-gray-100`: Light text color
- `md:text-2xl`: Larger text on medium screens
- `hover:scale-105`: Slight zoom on hover
- `transition-all`: Smooth transitions
- `duration-300`: Transition timing

## Managing Links

### Internal Navigation Links
Current internal links use section IDs:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Find the section you want to link to
2. Note its `id` attribute
3. Use that id with a `#` prefix in the `href`

### External Links
The emergency support button links to an external website:
```html
<a href="https://calgaryhvavpros.com" class="inline-block bg-gradient-to-r from-blue-500 to-teal-400...">
    Get Emergency Support
</a>
```

To update:
1. Replace the URL in `href`
2. Ensure new URLs include `https://`
3. Test the link after updating

### Email Links
Current email links use mailto:
```html
<a href="mailto:iainhmunro@gmail.com">iainhmunro@gmail.com</a>
```

To update:
1. Replace email address in both the `href` and display text
2. Maintain the `mailto:` prefix

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying the header and footer from index.html to your new pages

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Always test on mobile and desktop views
   - Maintain responsive classes (e.g., `md:`, `lg:` prefixes)
   - Don't remove the viewport meta tag

3. **Icon Problems**
   - Verify Font Awesome is properly loaded
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)
   - Maintain the `fas` prefix for solid icons

4. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent
     ```

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).