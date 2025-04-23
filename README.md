# Ascot Vale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Ascot Vale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To modify:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">
    Ascot Vale  <!-- Replace this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Services</a>  <!-- Modify menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update your main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Ascot Vale accounting services  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accounting excellence with a personal touch  <!-- Subheading -->
</p>
```

### Tailwind CSS Tips for Beginners
- Font sizes use classes like `text-sm`, `text-xl`, `text-2xl`
- Colors use format `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing uses format `m-{number}` for margin or `p-{number}` for padding
- Responsive classes start with `md:` or `lg:` for different screen sizes

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Ensure section IDs match your href values
2. For external pages, use full URLs:
```html
<a href="https://yoursite.com/services">Services</a>
```

### Call-to-Action Buttons
Update the "Get Started" button links:
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-blue-600...">
    Start Your Financial Journey
</a>
```
Replace `https://theaccountants.com` with your actual URL.

### Footer Links
Current placeholder links need updating:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Services</h4>
    <ul class="space-y-2">
        <li><a href="#">Retirement Planning</a></li>  <!-- Add proper URLs -->
        <li><a href="#">Financial Management</a></li>
        <li><a href="#">Expense Tracking</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:
```html
<!-- Before -->
<li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- After -->
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href values exactly
   - IDs are case-sensitive
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Test all changes at different screen sizes
   - Maintain responsive classes (md:, lg:)
   - Don't remove `container` or `mx-auto` classes

3. **Style Inconsistencies**
   - Keep color codes consistent (e.g., `blue-600`)
   - Maintain padding/margin patterns
   - Use existing class combinations for new elements

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test all updates across different browsers and devices.