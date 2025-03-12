# Landing Page Maintenance Guide

This guide will help you maintain and customize the WillabySolutions landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">WillabySolutions</a>
```
Simply replace "WillabySolutions" with your company name.

### Hero Section
Located at the top of the page, this section contains the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">End Customer Service Nightmares in 60 Seconds</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Human Customer Service is Dead. Welcome to Instant Answers.</p>
```

The classes explain:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `bg-gradient-to-r`: Creates right-flowing gradient
- `text-transparent`: Makes text transparent to show gradient

### Features Section
To modify feature cards:

1. Find the `features` section containing three cards
2. Each card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:shadow-xl hover:shadow-purple-500/10 transition-all duration-300 transform hover:scale-105">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description</p>
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="https://willabysolutions.com" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #) connect to page sections
2. External links (starting with https://) go to other websites
3. Replace `href` values with your desired URLs

### Call-to-Action Buttons
Located in hero and final sections:
```html
<a href="https://willabysolutions.com" class="inline-block px-8 py-4 text-lg font-semibold bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">Transform Your Support Now</a>
```

Update the `href` attribute with your destination URL.

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer's legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add links:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
   - Ensure all gradient classes include both `from-` and `to-` colors
   - Example: `bg-gradient-to-r from-purple-500 to-pink-500`

2. **Responsive Issues**
   - Check mobile-first classes (without prefix)
   - Then add responsive variants (`md:`, `lg:`)
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Link Problems**
   - Internal links (#) must match section IDs exactly
   - External links need complete URLs (https://...)
   - File links need correct paths (./privacy.html)

### Need Help?
For additional support:
- Check Tailwind CSS documentation for class references
- Verify all HTML tags are properly closed
- Test the page on different screen sizes
- Ensure all links are working before deployment

Remember to save your changes and test in a browser after each modification.