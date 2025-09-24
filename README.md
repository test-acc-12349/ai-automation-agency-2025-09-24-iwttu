# Landing Page Maintenance Guide

This guide will help you maintain and customize the AI Automation Agency landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<div class="text-2xl font-bold text-blue-600">AI Automation Agency</div>
```
To change the company name:
1. Locate this div in the header section
2. Replace "AI Automation Agency" with your desired text
3. Maintain the surrounding div tags and classes

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Ultimate n8n Automations
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Transform your business with powerful AI-driven automation solutions
</p>
```
To update the hero content:
1. Replace the h1 text between the tags
2. Modify the paragraph text while keeping the tags intact

### Tailwind CSS Classes Explained

#### Understanding Responsive Classes
- `md:` prefix means the style applies at medium screens (768px+)
- `lg:` prefix applies at large screens (1024px+)
- Example: `text-4xl md:text-5xl lg:text-6xl` means:
  - Mobile: text is 4xl size
  - Tablet: text is 5xl size
  - Desktop: text is 6xl size

#### Common Classes Used
```html
<!-- Component styling -->
bg-white           <!-- White background -->
text-gray-900      <!-- Dark gray text -->
rounded-2xl        <!-- Large rounded corners -->
shadow-lg          <!-- Large shadow effect -->

<!-- Spacing -->
px-6               <!-- Horizontal padding -->
py-4               <!-- Vertical padding -->
mb-6               <!-- Bottom margin -->

<!-- Hover effects -->
hover:bg-blue-700  <!-- Background changes on hover -->
hover:scale-105    <!-- Slight size increase on hover -->
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Internal links (starting with #) connect to section IDs on the same page
2. Replace `href="#sectionname"` with:
   - Internal link: `href="#new-section-id"`
   - External link: `href="https://your-url.com"`

### Call-to-Action Links
Current placeholder:
```html
<a href="https://test.com" class="inline-flex items-center px-6 py-2 bg-blue-600 text-white">
```

To update:
1. Replace `https://test.com` with your actual URL
2. Test the link after updating
3. Maintain the existing classes for consistent styling

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
Current footer structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting Tips

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Test all changes at different screen sizes
   - Maintain responsive classes (md:, lg:)
   - Don't remove container classes that control width

3. **Style Consistency**
   - Copy existing classes when adding new elements
   - Keep color schemes consistent (blue-600, gray-900, etc.)
   - Maintain hover effects on interactive elements

## Need Help?

If you encounter issues:
1. Check for typos in class names
2. Verify all tags are properly closed
3. Test links in multiple browsers
4. Ensure all files are in the correct directory
5. Compare changes against the original code

Remember to backup your files before making significant changes.