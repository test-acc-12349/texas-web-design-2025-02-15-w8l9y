# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. **Logo Text (TWD):**
```html
<a href="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition-colors">TWD</a>
```
- Replace "TWD" with your desired text
- The `text-2xl` class controls size
- `text-gray-800` controls color

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>`
- Maintain the `class` attributes to preserve styling
- `space-x-8` controls spacing between items

### Hero Section
The main banner section includes:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6" data-aos="fade-up">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-200 mb-12" data-aos="fade-up" data-aos-delay="100">Best Websites In Texas</p>
```
- Update headline between `<h1>` tags
- Modify subheading in the `<p>` tag
- Keep `data-aos` attributes for animations

### Tailwind CSS Tips
- `text-` classes control font size (xl, 2xl, 4xl, etc.)
- `mb-` classes add bottom margin (mb-6 = 1.5rem)
- `md:` prefix applies styles only on medium screens and larger
- `hover:` prefix adds hover effects

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
   - Ensure section IDs match exactly
   - Example: `<a href="#new-section">New Section</a>`

2. External links:
   - Replace `#` with full URL
   - Example: `<a href="https://your-site.com/page">Page</a>`

### Call-to-Action Buttons
Update the "Get Started" button link:

```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```
- Replace `https://twd.com` with your destination URL
- Maintain the `class` attributes for styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer:

```html
<!-- Add this to the Quick Links section -->
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use consistent styling:
```html
<!-- privacy.html/terms.html template -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Texas Web Design</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Verify section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Check for `md:` prefixed classes
   - Test at different screen sizes
   - Don't remove responsive classes

3. **Animation Problems**
   - Ensure AOS script is loaded
   - Check `data-aos` attributes
   - Verify initialization code is present:
```html
<script>
    AOS.init({
        duration: 800,
        once: true
    });
</script>
```

Need help? Contact support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).