# Cloudflare Pages Setup Guide

This repository is configured for deployment to Cloudflare Pages with GitHub integration.

## Quick Setup Steps

### 1. Connect GitHub Repository to Cloudflare Pages

1. **Log in to Cloudflare Dashboard**
   - Go to [dash.cloudflare.com](https://dash.cloudflare.com)
   - Navigate to **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**

2. **Authorize GitHub**
   - Select **GitHub** as your Git provider
   - Authorize Cloudflare to access your GitHub account
   - Select the repository: `isriam/windsortechnologies.llc`

3. **Configure Build Settings**
   - **Project name**: Choose a name (e.g., `windsortechnologies`)
   - **Production branch**: `main` (or your preferred branch)
   - **Build command**: Leave empty (static HTML site)
   - **Build output directory**: `/` (root directory)
   - Click **Save and Deploy**

### 2. Custom Domain Setup (Optional)

After deployment:
1. Go to your Cloudflare Pages project
2. Navigate to **Custom domains**
3. Add your domain (e.g., `windsortechnologies.net`)
4. Follow the DNS configuration instructions

### 3. Automatic Deployments

Once connected:
- **Every push** to the production branch triggers a production deployment
- **Pull requests** automatically create preview deployments
- Preview URLs are available in PR comments

## Project Structure

```
windsortechnologies.llc/
├── index.html              # Main landing page
├── README.md               # Project documentation
├── CLOUDFLARE_SETUP.md     # This file
└── .gitignore              # Git ignore rules
```

## Build Configuration

This is a **static HTML site** with no build process required:
- **Framework**: None (Static HTML/CSS)
- **Build command**: None required
- **Output directory**: `/` (root)
- **Node.js version**: Not required

## Environment Variables

No environment variables are currently required for this static site.

## Deployment Status

After setup, you can view deployment status at:
- Cloudflare Dashboard: `https://dash.cloudflare.com`
- Your live site will be available at: `https://<project-name>.pages.dev`

## Troubleshooting

### Site not updating after push?
- Check the deployments tab in Cloudflare Dashboard
- Verify the correct branch is set as production branch
- Check build logs for any errors

### Custom domain not working?
- Verify DNS records are properly configured
- Allow up to 24-48 hours for DNS propagation
- Check SSL/TLS encryption mode is set to "Full" or "Full (strict)"

## Additional Resources

- [Cloudflare Pages Documentation](https://developers.cloudflare.com/pages/)
- [GitHub Integration Guide](https://developers.cloudflare.com/pages/get-started/git-integration/)
