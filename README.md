# Apisearch Website

This is the official website for Apisearch, a static site generator built with PHP, Twig, and YAML.

## Prerequisites

- PHP 8.0 or higher
- Composer (PHP dependency manager)

## Installation

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone <repository-url>
   cd apisearch-io
   ```

2. **Install PHP dependencies**:
   ```bash
   composer install
   ```

   If you encounter version compatibility issues, update the dependencies:
   ```bash
   composer update
   ```

## Running the Project Locally

### 1. Generate the Static Site

The website is generated from Twig templates and YAML configuration files. To build the site:

```bash
php generate.php
```

This command will:
- Read configuration from `config.yml`
- Process Twig templates from the `templates/` directory
- Generate HTML files in the `docs/` directory
- Support multiple languages (Spanish and English)

### 2. Start the Development Server

After generating the site, serve it locally using PHP's built-in web server:

```bash
cd docs
php -S localhost:3000
```

The website will be available at: **http://localhost:3000**

> **Note:** If port 3000 is already in use, you can use a different port (e.g., `php -S localhost:8080`)

## Project Structure

- `templates/` - Twig template files
- `languages/` - YAML translation files (es.yml, en.yml)
- `assets/` - Static assets (CSS, JS, images)
- `docs/` - Generated HTML output (git-ignored)
- `config.yml` - Main configuration file
- `generate.php` - Build script
- `composer.json` - PHP dependencies

## Development Workflow

1. Make changes to templates, translations, or assets
2. Run `php generate.php` to rebuild the site
3. Refresh your browser to see changes (the dev server should still be running)

## Deployment

The generated `docs/` directory contains the complete static website ready for deployment to any web server or hosting platform (GitHub Pages, Netlify, etc.).

