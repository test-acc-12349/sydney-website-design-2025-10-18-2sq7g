# Sydney Website Design Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, customize, and update your landing page. Whether you're new to web development or just need a refresher, we've broken everything down into simple, manageable steps.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Section 1: Updating Text and Tailwind CSS Classes](#section-1-updating-text-and-tailwind-css-classes)
3. [Section 2: Fixing Broken Links](#section-2-fixing-broken-links)
4. [Section 3: Linking Privacy and Terms Pages](#section-3-linking-privacy-and-terms-pages)
5. [Troubleshooting Tips](#troubleshooting-tips)
6. [Best Practices](#best-practices)

---

## Quick Start Overview

Your landing page is built with:
- **HTML**: The structure and content of your page
- **Tailwind CSS**: A utility-first CSS framework that handles styling (colors, spacing, responsive design)
- **Custom CSS**: Additional animations and effects
- **JavaScript**: Interactive elements like the FAQ accordion

**Key files you'll be working with:**
- `index.html` - Your main landing page file

**What you'll learn to do:**
- Change text content without breaking the design
- Update navigation links
- Add privacy and terms page links
- Maintain responsive design across devices

---

## Section 1: Updating Text and Tailwind CSS Classes

### Understanding the Page Structure

Your landing page has five main sections:

1. **Navigation Bar** (Top of page - stays visible when scrolling)
2. **Hero Section** (Large welcome section with main headline)
3. **Features Section** (3 feature cards)
4. **Benefits Section** (3 benefit cards)
5. **Call-to-Action Section** (Large promotional area)
6. **FAQ Section** (Questions and answers)

### How to Update Text Content

#### **Navigation Bar Text**

**Location in code:** Lines 44-52

**Current code:**
```html
<a href="#features" class="text-gray-300 hover:text-white smooth-transition font-medium">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white smooth-transition font-medium">Benefits</a>
<a href="#faq" class="text-gray-300 hover:text-white smooth-transition font-medium">FAQ</a>
<a href="#contact" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>
```

**How to change it:**
1. Find the navigation section near the top of your HTML file
2. Look for the text between `<a>` and `</a>` tags
3. Replace the text while keeping the tags intact

**Example - Change "Features" to "Our Services":**
```html
<a href="#features" class="text-gray-300 hover:text-white smooth-transition font-medium">Our Services</a>
```

**Important:** Don't delete or modify the `href="#features"` part - this tells the link where to go!

---

#### **Hero Section - Main Headline**

**Location in code:** Lines 95-99

**Current code:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-black tracking-tight mb-6 leading-tight">
    <span class="block text-white">Sydney Website Design</span>
    <span class="gradient-text block mt-2">Best Websites</span>
</h1>
```

**What you're looking at:**
- `<h1>` = Main headline tag (most important heading)
- `text-5xl sm:text-6xl lg:text-7xl` = Text size (responsive - changes on different devices)
- `gradient-text` = Special class that creates the purple-to-pink color effect
- `<span class="block">` = Creates separate lines

**How to change the headline:**

**Step 1:** Keep the structure exactly as it is
**Step 2:** Replace only the text content

**Example - Change to your own headline:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-black tracking-tight mb-6 leading-tight">
    <span class="block text-white">Your Business Name Here</span>
    <span class="gradient-text block mt-2">Your Main Message</span>
</h1>
```

**Pro tip:** The first line appears in white, the second line has the purple-pink gradient. Use this to highlight your key message!

---

#### **Hero Section - Subtitle**

**Location in code:** Lines 101-104

**Current code:**
```html
<p class="text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto mb-12 leading-relaxed">
    Stunning, fast, and SEO-ready websites designed to convert. Get professional web design with low costs, easy updates, and free hosting included.
</p>
```

**How to change it:**
1. Find this paragraph text
2. Replace it with your own message
3. Keep all the `class="..."` parts the same

**Example:**
```html
<p class="text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto mb-12 leading-relaxed">
    We create beautiful, fast websites that help your business grow. Our designs are optimized for conversions and built to last.
</p>
```

---

#### **Features Section - Card Titles and Descriptions**

**Location in code:** Lines 148-188

**Current code (Feature 1 - Lightning Fast):**
```html
<h3 class="text-2xl font-bold mb-3">Lightning Fast</h3>
<p class="text-gray-400 leading-relaxed">
    Optimized performance that loads in milliseconds. Your website will rank higher and keep visitors engaged with blazing-fast speeds.
</p>
```

**How to update all three feature cards:**

**Step 1:** Find the three feature cards (they're in a grid layout)
**Step 2:** Update the `<h3>` title and the `<p>` description for each

**Example - Customize Feature 1:**
```html
<h3 class="text-2xl font-bold mb-3">Ultra-Fast Loading</h3>
<p class="text-gray-400 leading-relaxed">
    Your website loads instantly, improving user experience and search engine rankings. Speed matters for conversions.
</p>
```

**Do the same for Feature 2 (SEO Ready) and Feature 3 (High Conversion):**

```html
<!-- Feature 2 -->
<h3 class="text-2xl font-bold mb-3">Search Engine Optimized</h3>
<p class="text-gray-400 leading-relaxed">
    Built with SEO best practices to help your business appear on Google. Attract more customers organically.
</p>

<!-- Feature 3 -->
<h3 class="text-2xl font-bold mb-3">Conversion Focused</h3>
<p class="text-gray-400 leading-relaxed">
    Every design element is strategically placed to turn visitors into customers. Psychology-backed design principles.
</p>
```

---

#### **Benefits Section - Card Titles and Descriptions**

**Location in code:** Lines 219-282

**Current code (Benefit 1 - Low Cost):**
```html
<h3 class="text-xl font-bold mb-2">Low Cost</h3>
<p class="text-gray-400 leading-relaxed">
    Premium design at affordable prices. We believe great web design shouldn't break the bank.
</p>
```

**How to update:**
Follow the same pattern as the features section:

```html
<h3 class="text-xl font-bold mb-2">Affordable Pricing</h3>
<p class="text-gray-400 leading-relaxed">
    Professional design without the premium price tag. We make web design accessible to all businesses.
</p>
```

**Do the same for the other two benefits (Easy to Update and Free Hosting).**

---

#### **FAQ Section - Questions and Answers**

**Location in code:** Lines 325-380

**Current code (FAQ Item 1):**
```html
<button class="w-full px-6 py-5 bg-gray-800 border border-gray-700 rounded-lg hover:border-purple-500 smooth-transition text-left flex items-center justify-between" onclick="toggleFAQ(this)">
    <span class="text-lg font-semibold">How long does it take to build a website?</span>
    <svg class="w-6 h-6 transform smooth-transition" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
    </svg>
</button>
<div class="faq-content hidden max-h-0 overflow-hidden bg-gray-800 border border-t-0 border-gray-700 rounded-b-lg smooth-transition">
    <p class="px-6 py-4 text-gray-300 leading-relaxed">
        Most projects are completed within 2-4 weeks depending on complexity and your requirements. We provide a timeline during the initial consultation.
    </p>
</div>
```

**How to update FAQ items:**

**Step 1:** Find the question text (between `<span class="text-lg font-semibold">` and `</span>`)
**Step 2:** Replace with your question
**Step 3:** Find the answer text (between `<p class="px-6 py-4 text-gray-300 leading-relaxed">` and `</p>`)
**Step 4:** Replace with your answer

**Example:**
```html
<button class="w-full px-6 py-5 bg-gray-800 border border-gray-700 rounded-lg hover:border-purple-500 smooth-transition text-left flex items-center justify-between" onclick="toggleFAQ(this)">
    <span class="text-lg font-semibold">What is your design process?</span>
    <svg class="w-6 h-6 transform smooth-transition" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
    </svg>
</button>
<div class="faq-content hidden max-h-0 overflow-hidden bg-gray-800 border border-t-0 border-gray-700 rounded-b-lg smooth-transition">
    <p class="px-6 py-4 text-gray-300 leading-relaxed">
        We follow a collaborative 5-step process: discovery, strategy, design, development, and launch. You're involved at every stage.
    </p>
</div>
```

---

### Understanding Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here are the most common ones in your landing page:

#### **Text Styling Classes**

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | Makes text white | `<p class="text-white">` |
| `text-gray-300` | Makes text light gray | `<p class="text-gray-300">` |
| `text-gray-400` | Makes text medium gray | `<p class="text-gray-400">` |
| `text-2xl` | Makes text large (size 2) | `<h3 class="text-2xl">` |
| `text-5xl` | Makes text extra large (size 5) | `<h1 class="text-5xl">` |
| `font-bold` | Makes text bold | `<p class="font-bold">` |
| `font-black` | Makes text extra bold | `<h1 class="font-black">` |

**How to change text color:**

**Current code:**
```html
<p class="text-gray-300">This text is light gray</p>
```

**To make it white:**
```html
<p class="text-white">This text is now white</p>
```

**Available text colors in this design:**
- `text-white` (brightest)
- `text-gray-300` (light gray)
- `text-gray-400` (medium gray)
- `text-purple-400` (light purple)
- `text-purple-600` (medium purple)

---

#### **Spacing Classes**

Spacing in Tailwind is controlled by padding (`p-`) and margin (`m-`) classes:

| Class | What It Does |
|-------|-------------|
| `mb-6` | Margin (space) below element = 6 units |
| `mt-2` | Margin (space) above element = 2 units |
| `px-4` | Padding (internal space) left and right = 4 units |
| `py-4` | Padding (internal space) top and bottom = 4 units |
| `p-8` | Padding on all sides = 8 units |

**Example - Add more space below a heading:**

**Current:**
```html
<h2 class="text-4xl font-black mb-4">Our Services</h2>
```

**To add more space below:**
```html
<h2 class="text-4xl font-black mb-8">Our Services</h2>
```

(Changed `mb-4` to `mb-8` - doubled the space below)

---

#### **Responsive Design Classes**

Your landing page automatically adjusts for different screen sizes. These prefixes control that:

| Prefix | Screen Size | Example |
|--------|------------|---------|
| None | Mobile (small) | `text-5xl` |
| `sm:` | Small screens | `sm:text-6xl` |
| `md:` | Medium screens (tablets) | `md:grid-cols-3` |
| `lg:` | Large screens (desktops) | `lg:text-7xl` |

**Example - Responsive text sizing:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl">
```

This means:
- On mobile: Use `text-5xl` (size 5)
- On tablets and up: Use `sm:text-6xl` (size 6)
- On desktops: Use `lg:text-7xl` (size 7)

**Don't change these unless you understand responsive design!** They ensure your page looks good on all devices.

---

#### **Background and Border Classes**

| Class | What It Does |
|-------|-------------|
| `bg-gray-900` | Dark gray background |
| `bg-gray-800` | Lighter gray background |
| `border border-gray-700` | Add a gray border |
| `rounded-lg` | Slightly rounded corners |
| `rounded-2xl` | Very rounded corners |
| `shadow-lg` | Add a shadow effect |

**Example - Change card background:**

**Current:**
```html
<div class="bg-gray-800 border border-gray-700 rounded-2xl p-8">
```

**To make it darker:**
```html
<div class="bg-gray-900 border border-gray-700 rounded-2xl p-8">
```

---

### Practical Exercise: Update Your Hero Section

Let's walk through updating the hero section step-by-step:

**Step 1:** Open your `index.html` file in a text editor

**Step 2:** Find the hero section (around line 95)

**Step 3:** Update the main headline:
```html
<!-- BEFORE -->
<span class="block text-white">Sydney Website Design</span>
<span class="gradient-text block mt-2">Best Websites</span>

<!-- AFTER - Your changes -->
<span class="block text-white">Your Company Name</span>
<span class="gradient-text block mt-2">Your Main Value Proposition</span>
```

**Step 4:** Update the subtitle:
```html
<!-- BEFORE -->
<p class="text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto mb-12 leading-relaxed">
    Stunning, fast, and SEO-ready websites designed to convert. Get professional web design with low costs, easy updates, and free hosting included.
</p>

<!-- AFTER -->
<p class="text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto mb-12 leading-relaxed">
    Your custom subtitle here. Explain your unique value and what makes you different.
</p>
```

**Step 5:** Save your file and refresh your browser to see the changes!

---

## Section 2: Fixing Broken Links

### Understanding Links in HTML

Links in HTML use the `<a>` tag. The `href` attribute tells the browser where to go when someone clicks.

**Basic link structure:**
```html
<a href="destination-url">Click here</a>
```

**Example:**
```html
<a href="https://google.com">Go to Google</a>
```

---

### Finding All Links in Your Landing Page

Your landing page has links in three main areas:

#### **1. Navigation Bar Links (Lines 44-52)**

**Current code:**
```html
<a href="#features" class="text-gray-300 hover:text-white smooth-transition font-medium">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white smooth-transition font-medium">Benefits</a>
<a href="#faq" class="text-gray-300 hover:text-white smooth-transition font-medium">FAQ</a>
<a href="#contact" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>
<a href="https://swd.com" class="bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 px-6 py-2 rounded-lg font-semibold smooth-transition transform hover:scale-105">Get Started</a>
```

**What these links do:**
- `href="#features"` - Jump to the features section on this page
- `href="#benefits"` - Jump to the benefits section on this page
- `href="#faq"` - Jump to the FAQ section on this page
- `href="#contact"` - Jump to the contact section (currently doesn't exist on this page)
- `href="https://swd.com"` - Go to external website

---

#### **2. Hero Section CTA Buttons (Lines 108-124)**

**Current code:**
```html
<a href="https://swd.com" class="group relative inline-flex items-center justify-center px-8 py-4 font-bold text-white rounded-lg overflow-hidden smooth-transition transform hover:scale-105">
    Start Your Project
</a>

<a href="#features" class="inline-flex items-center justify-center px-8 py-4 font-bold text-white rounded-lg border-2 border-gray-600 hover:border-purple-500 hover:text-purple-400 smooth-transition">
    Learn More
</a>
```

**What these do:**
- First button goes to `https://swd.com` (external site)
- Second button jumps to `#features` section on this page

---

#### **3. Call-to-Action Section Button (Lines 310-318)**

**Current code:**
```html
<a href="https://swd.com" class="inline-flex items-center justify-center px-10 py-5 font-bold text-white rounded-lg bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 smooth-transition transform hover:scale-105 text-lg shadow-lg hover:shadow-2xl">
    Get Your Free Consultation
</a>
```

**What it does:**
- Goes to `https://swd.com` (external site)

---

### How to Fix Broken Links

#### **Scenario 1: Update External Links (Like "https://swd.com")**

**Problem:** You want to change where the "Get Started" button points

**Solution:**

**Step 1:** Find the link you want to change
```html
<a href="https://swd.com" class="...">Get Started</a>
```

**Step 2:** Replace the URL in the `href` attribute
```html
<a href="https://yourdomain.com" class="...">Get Started</a>
```

**Step 3:** Save and test by clicking the button

**Common URLs to use:**
- Your website: `https://yourdomain.com`
- Contact form: `https://yourdomain.com/contact`
- Booking page: `https://yourdomain.com/book`
- Email link: `mailto:info@yourdomain.com`

**Example - Link to email:**
```html
<a href="mailto:contact@yourcompany.com" class="...">Get Started</a>
```

---

#### **Scenario 2: Fix Internal Links (Sections on This Page)**

**Problem:** The "Contact" navigation link points to `#contact` but there's no contact section

**Solution 1 - Remove the broken link:**
```html
<!-- BEFORE -->
<a href="#contact" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>

<!-- AFTER - Remove it entirely -->
<!-- Link removed -->
```

**Solution 2 - Point it to an existing section:**
```html
<!-- BEFORE -->
<a href="#contact" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>

<!-- AFTER - Point to FAQ instead -->
<a href="#faq" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>
```

**Solution 3 - Create a new section and link to it:**

First, add a new section with an `id`:
```html
<section id="contact" class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-900">
    <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-4xl font-black mb-4">Get in Touch</h2>
        <p class="text-xl text-gray-400">Contact us today for a free consultation</p>
        <a href="mailto:contact@yourcompany.com">Email Us</a>
    </div>
</section>
```

Then the link will work:
```html
<a href="#contact" class="text-gray-300 hover:text-white smooth-transition font-medium">Contact</a>
```

---

#### **Scenario 3: Link to External Websites**

**Problem:** You want to add a link to your social media

**Solution:**

Find where you want to add the link and insert it:

```html
<!-- Example: Add social media link in footer area -->
<a href="https://facebook.com/yourpage" class="text-gray-300 hover:text-white smooth-transition font-medium">Facebook</a>
```

**Common social media URLs:**
- Facebook: `https://facebook.com/yourpage`
- Instagram: `https://instagram.com/yourprofile`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Twitter: `https://twitter.com/yourhandle`
- YouTube: `https://youtube.com/c/yourchannel`

---

### Complete Link Update Checklist

Use this checklist to update all links in your landing page:

**Navigation Links:**
- [ ] `Features` link - Should point to `#features` ✓ (working)
- [ ] `Benefits` link - Should point to `#benefits` ✓ (working)
- [ ] `FAQ` link - Should point to `#faq` ✓ (working)
- [ ] `Contact` link - Update or remove (currently broken)
- [ ] `Get Started` button - Update `https://swd.com` to your URL

**Hero Section:**
- [ ] `Start Your Project` button - Update URL
- [ ] `Learn More` button - Points to `#features` ✓ (working)

**CTA Section:**
- [ ] `Get Your Free Consultation` button - Update URL

**Example of fully updated links:**
```html
<!-- Navigation -->
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#faq" class="...">FAQ</a>
<!-- Contact link removed -->
<a href="https://yourdomain.com/book" class="...">Get Started</a>

<!-- Hero buttons -->
<a href="https://yourdomain.com/book" class="...">Start Your Project</a>
<a href="#features" class="...">Learn More</a>

<!-- CTA button -->
<a href="https://yourdomain.com/book" class="...">Get Your Free Consultation</a>
```

---

## Section 3: Linking Privacy and Terms Pages

### Understanding What You Need

Most professional websites have:
1. **Privacy Policy** - Explains how you handle user data
2. **Terms of Service** - Legal terms for using your website

These are typically in separate HTML files:
- `privacy.html` - Privacy policy page
- `terms.html` - Terms of service page

---

### Step 1: Create the Privacy and Terms Pages

**If you don't have these files yet, create them:**

**File 1: Create `privacy.html`**

Create a new file called `privacy.html` in the same folder as your `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Sydney Website Design">
    <title>Privacy Policy | Sydney Website Design</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Poppins:wght@600;700;800;900&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Navigation -->
    <nav class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold">
                        <span class="gradient-text">SWD</span>
                    </a>
                </div>
                <a href="index.html" class="text-gray-300 hover:text-white font-medium">Back to Home</a>
            </div>
        </div>
    </nav>

    <!-- Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl font-black mb-8">Privacy Policy</h1>
            
            <div class="prose prose-invert max-w-none">
                <h2 class="text-2xl font-bold mt-8 mb-4">Introduction</h2>
                <p class="text-gray-300 mb-6">
                    Your privacy is important to us. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">Information We Collect</h2>
                <p class="text-gray-300 mb-6">
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="text-gray-300 mb-6 list-disc list-inside">
                    <li>Your name and email address when you contact us</li>
                    <li>Information about your browsing activity</li>
                    <li>Device information and IP address</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">How We Use Your Information</h2>
                <p class="text-gray-300 mb-6">
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="text-gray-300 mb-6 list-disc list-inside">
                    <li>Respond to your inquiries and fulfill your requests</li>
                    <li>Send you marketing and promotional communications</li>
                    <li>Monitor and analyze site usage and trends</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">Contact Us</h2>
                <p class="text-gray-300">
                    If you have questions about this Privacy Policy, please contact us at: <a href="mailto:contact@yourdomain.com" class="text-purple-400 hover:text-purple-300">contact@yourdomain.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 border-t border-gray-700 py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto text-center text-gray-400">
            <p>&copy; 2024 Sydney Website Design. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

**File 2: Create `terms.html`**

Create a new file called `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Sydney Website Design">
    <title>Terms of Service | Sydney Website Design</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Poppins:wght@600;700;800;900&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Navigation -->
    <nav class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold">
                        <span class="gradient-text">SWD</span>
                    </a>
                </div>
                <a href="index.html" class="text-gray-300 hover:text-white font-medium">Back to Home</a>
            </div>
        </div>
    </nav>

    <!-- Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-