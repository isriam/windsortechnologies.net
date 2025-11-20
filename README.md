# windsortechnologies.llc

A simple landing page for luxury vacation rentals in Destin, Florida.

## Overview

This is a static HTML landing page that redirects visitors to vacation rental listings on the Islander Resort website. The site is designed for deployment on Cloudflare Pages with automatic GitHub integration.

## Features

- Clean, responsive landing page design
- Direct link to vacation rental booking
- SEO-optimized metadata
- Fast loading with no build process required

## Deployment

This site is configured for **Cloudflare Pages** deployment with GitHub integration.

For detailed setup instructions, see [CLOUDFLARE_SETUP.md](./CLOUDFLARE_SETUP.md)

### Quick Deploy

1. Connect this GitHub repository to Cloudflare Pages
2. Set build settings to: No build command, output directory: `/`
3. Deploy automatically on every push to main branch

## Local Development

Simply open `index.html` in a web browser - no build process or local server required.

Alternatively, you can use a simple HTTP server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Project Structure

```
.
├── index.html              # Main landing page
├── README.md               # This file
├── CLOUDFLARE_SETUP.md     # Cloudflare Pages setup guide
└── .gitignore              # Git ignore patterns
```

## License

Private repository - All rights reserved.