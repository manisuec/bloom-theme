# Bloom Theme

A clean, modern landing page theme for Hugo.

## Features

- Responsive design
- Customizable colors and content
- SVG icons included
- Support for social media links
- Navigation menu
- Hero section with CTA buttons
- Features grid section
- Resources section
- Footer with copyright and social links
- Full blog support with posts list and single post templates
- Post categories, tags, author, date, and read time
- Social share buttons
- Previous/Next post navigation
- Comments support (Disqus, Giscus)

## Quick Start

1. Create a new Hugo site:
   ```bash
   hugo new site mysite
   ```

2. Clone this theme into the themes directory:
   ```bash
   cd mysite
   git clone https://github.com/anomalyco/bloom-hugo-theme themes/bloom-hugo-theme
   ```

3. Copy the example config:
   ```bash
   cp themes/bloom-hugo-theme/exampleSite/config.toml config.toml
   ```

4. Start the Hugo server:
   ```bash
   hugo server
   ```

## Configuration

Edit `config.toml` to customize:
- Site title and description
- Hero section content and CTAs
- Features section items
- Resources section
- Navigation menu
- Social media links
- Header CTA button
- Blog comments settings

## Blog Setup

### Create a Blog Post

```markdown
---
title: "Your Post Title"
date: 2025-01-15
description: "A short description for post previews and SEO"
author: "Author Name"
categories: ["Category 1", "Category 2"]
tags: ["tag1", "tag2"]
featuredImage: "/images/your-image.jpg"
readTime: 5
---

Your content here...
```

### Front Matter Parameters

| Parameter | Description |
|-----------|-------------|
| `title` | Post title (required) |
| `date` | Publication date (required) |
| `description` | Short description for SEO and previews |
| `author` | Author name displayed on post |
| `categories` | Array of categories |
| `tags` | Array of tags |
| `featuredImage` | Path to featured image |
| `readTime` | Estimated read time in minutes |

### Comments

Enable comments in `config.toml`:

```toml
[params.blog]
  [params.blog.comments]
    enable = true
    # Disqus
    disqusShortname = "your-shortname"
    # OR Giscus
    [params.blog.comments.giscus]
      repo = "user/repo"
      repoId = "123456"
      categoryId = "789012"
```

## Customization

### Colors

Edit `static/css/styles.css` and modify the CSS variables:

```css
:root {
    --primary: #4A9B7F;
    --secondary: #5B9AA0;
    --accent: #E8916C;
    --dark: #2C3E50;
    --light: #FDF0E6;
    --white: #ffffff;
}
```

### Adding Icons

Add new icon partials in `layouts/partials/icons/` directory.

## License

MIT
