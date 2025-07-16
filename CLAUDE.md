# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static site for an iOS app landing page, deployed on GitHub Pages. The site is designed to showcase the "Swipe2delete" app - a photo organization tool that allows users to clean up their camera roll by swiping left to delete or right to keep photos.

## Architecture

- **Jekyll Static Site**: Uses Jekyll with GitHub Pages for automatic deployment
- **Configuration-Driven**: Almost all content is managed through `_config.yml` - no HTML/CSS editing required
- **Responsive Design**: Mobile-first design with smart app banner support for iOS devices
- **Modular Structure**: Uses Jekyll includes and layouts for reusable components

### Key Files Structure

- `_config.yml`: Central configuration file containing app info, features, styling, and personal details
- `index.html`: Main landing page template
- `_layouts/`: Page templates (default.html, page.html)
- `_includes/`: Reusable components (header, footer, features, app store images)
- `_pages/`: Markdown pages for changelog, contact, and privacy policy
- `_sass/`: SCSS files for styling
- `assets/`: Images, videos, and other media files

## Development Commands

This is a Jekyll site deployed on GitHub Pages. There are no build scripts or package.json - Jekyll handles compilation automatically.

### Local Development (if Jekyll is installed)
```bash
bundle install
bundle exec jekyll serve
```

### Deployment
- Push to `gh-pages` branch
- GitHub Pages automatically builds and deploys the site

## Configuration

All site customization is done through `_config.yml`:

- **App Details**: iOS app ID (6464102619), name, description, pricing
- **Media**: App icon, screenshots, videos (must be 828x1792, 1125x2436, or 1242x2688 resolution)
- **Features**: List of app features with FontAwesome icons
- **Styling**: Colors, themes, device appearance
- **Social/Contact**: Social media links and contact information

## Content Management

- **Screenshots**: Add to `assets/screenshot/` (delete placeholder file)
- **Videos**: Add to `assets/videos/` (supports .mp4/.mov for Safari, .webm/.ogg for Chrome/Firefox)
- **Pages**: Edit markdown files in `_pages/` directory
- **Features**: Edit the features array in `_config.yml`

## App Store Integration

The site automatically pulls app information from the App Store using the `ios_app_id` in `_config.yml`. This populates:
- App name
- App icon
- App price
- App Store link

## Branch Information

- Main development branch: `master`
- Deployment branch: `gh-pages` (current)
- Site URL: Based on GitHub Pages repository URL format