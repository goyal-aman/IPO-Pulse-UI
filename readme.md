# Setting up a Subdomain with GitHub Pages via Cloudflare

This guide outlines the steps to set up a subdomain for your GitHub Pages site using Cloudflare for DNS management.

## Prerequisites

- A GitHub account
- A Cloudflare account
- A domain name registered and managed through Cloudflare

## Steps

### 1. GitHub Repository Setup

1. Create a new repository or use an existing one for your GitHub Pages site.
2. Add your static site files to the repository.
3. Go to repository Settings > Pages.
4. Under "Build and deployment", select your source branch.

### 2. Cloudflare DNS Configuration

1. Log in to your Cloudflare account.
2. Select your domain.
3. Go to the DNS management page.
4. Add a new DNS record:
   - Type: CNAME
   - Name: Your desired subdomain (e.g., 'blog')
   - Target: Your GitHub Pages URL (e.g., 'username.github.io')
   - Proxy status: Proxied (Orange cloud icon)

### 3. GitHub Custom Domain Configuration

1. In your GitHub repository, go to Settings > Pages.
2. Under "Custom domain", enter your full subdomain (e.g., 'blog.example.com').
3. Click "Save".

### 4. CNAME File

1. Create a file named `CNAME` in the root of your repository.
2. Add a single line with your full subdomain (e.g., 'blog.example.com').
3. Commit and push this file to your repository.

### 5. SSL/TLS Configuration

1. In GitHub Pages settings, enable "Enforce HTTPS" if available.
2. In Cloudflare, go to SSL/TLS settings.
3. Set SSL/TLS encryption mode to "Full" or "Full (strict)".

## Verification

- Wait for DNS propagation (can take up to 24 hours).
- Visit your subdomain (e.g., https://blog.example.com) to verify it's working.

## Troubleshooting

- If your site doesn't load, check GitHub Pages settings for any error messages.
- Ensure your Cloudflare DNS record is correctly set up and proxied.
- Verify that your CNAME file in the GitHub repository contains the correct subdomain.

## Maintenance

- Keep your GitHub repository and Cloudflare settings in sync.
- Regularly check GitHub Pages and Cloudflare dashboards for any issues or updates.

Remember to replace placeholders (e.g., 'username', 'example.com') with your actual information when using this guide.