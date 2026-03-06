# GEMINI.md - Project Context

## Project Overview
This project is the source code for the personal website and blog of **David Edwards** ([davidedwards.io](https://davidedwards.io)). It is a static site built with **Jekyll** and styled using the **Bulma** CSS framework.

The site is hosted on GitHub Pages, which automatically builds the Jekyll site when changes are pushed to the repository.

### Key Technologies
- **Jekyll (v4.4.1)**: Static site generator.
- **Bulma (v1.0.4)**: CSS framework used for styling.
- **SASS/SCSS**: Jekyll natively compiles SCSS using `jekyll-sass-converter`.
- **Ruby**: Required for running Jekyll locally.
- **Node.js/npm**: Used to manage the Bulma dependency.

## Project Structure
- `_config.yml`: Jekyll configuration, including SASS load paths for `node_modules`.
- `_posts/`: Markdown files for blog entries (naming convention: `YYYY-MM-DD-title.md`).
- `_layouts/`: HTML templates (e.g., `default.html`, `post.html`).
- `css/`:
  - `styles.scss`: The main stylesheet (processed by Jekyll).
  - `syntax.css`: Syntax highlighting styles.
- `images/`: Static assets (images, icons).
- `scripts/`: Client-side JavaScript (navbar toggles, analytics).
- `package.json`: Manages frontend dependencies (Bulma).
- `Gemfile`: Manages Ruby dependencies (Jekyll, jekyll-sitemap).

## Building and Running

### Local Development
To preview the site locally, you need Ruby, Bundler, and Node.js installed.

1.  **Install Dependencies**:
    ```shell
    bundle install && npm install
    ```
2.  **Build and Serve**:
    ```shell
    bundle exec jekyll serve --incremental
    ```
    *Note: Jekyll automatically compiles `css/styles.scss` into `_site/css/styles.css`. There is no need for a separate CSS build step.*
3.  **Clean Build**:
    ```shell
    bundle exec jekyll clean
    ```

## Development Conventions
- **Blog Posts**:
  - Add new posts to `_posts/` as `YYYY-MM-DD-filename.md`.
  - Use the `title` field in Front Matter for the actual post title (this is used for SEO and browser tabs).
  - The `section: Blog` metadata in `post.html` layout handles the "BLOG" branding in the navbar.
- **Styling**:
  - Modify `css/styles.scss` for style changes.
  - Do not manually edit or commit a `css/styles.css` file; it is a generated asset in the `_site` directory.
- **SEO/Metadata**:
  - Page titles are automatically generated as `Page Title`.
- **Navigation**:
  - The navigation bar is defined in `_layouts/default.html` and uses the `section` variable for active branding.
