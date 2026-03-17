# Avontae — Custom WordPress Theme

A hand-crafted WordPress theme (custom PHP theme) for a minimalist, performance-focused portfolio & editorial website. Clean markup, modular templates, and WordPress components & functions used throughout (`functions.php`, template parts, shortcodes, hooks, and widgets).

---

## 🔖 Overview
This repository contains the theme used for Avontae. It’s built to integrate with WordPress using core theme APIs, custom template parts, and reusable components so it’s easy to extend and maintain.

---

## ⚙️ Requirements
- WordPress 5.8+ (Gutenberg-compatible)  
- PHP 7.4+ (PHP 8.0+ recommended)  
- MySQL 5.7 / MariaDB equivalent  
- Apache or Nginx with rewrite support  
- Recommended: WP-CLI for faster workflow

---

## 📂 Included (example) structure

├─ style.css # Theme meta & main stylesheet (contains theme header)
├─ functions.php # Registers scripts, menus, sidebars, CPTs, hooks
├─ index.php # The main template / fallback loop
├─ header.php # Site header (doctype, head, opening body)
├─ footer.php # Footer markup & wp_footer()
├─ single.php # Single post template
├─ page.php # Static page template
├─ archive.php # Archive / category / author templates
├─ 404.php # 404 template
├─ template-parts/ # Reusable components (see list below)
├─ inc/ # helpers, setup, enqueue, customizer, shortcodes
├─ assets/ # css, js, images
├─ languages/ # .pot translations
└─ readme.md # This file


---

## ✅ Key WordPress integrations & features
- Theme setup via `after_setup_theme()` (supports title-tag, post-thumbnails, menus).  
- Enqueue scripts/styles in `functions.php` using `wp_enqueue_script` / `wp_enqueue_style`.  
- Template parts (`get_template_part()`) for header, footer, post loops, and components.  
- Custom Shortcodes for reusable content blocks.  
- Custom Post Types (if used) registered with `register_post_type()`.  
- Taxonomies and meta boxes via `register_taxonomy()` and `add_meta_box()` (optional).  
- Action & filter hooks to modify or extend behavior without editing core templates.  
- Widget areas / sidebars registered via `register_sidebar()`.  
- Basic REST API support / endpoints (optional) for headless or AJAX features.  
- Accessibility-conscious markup and semantic HTML.  
- Basic SEO-friendly meta structure (title, description, open graph tags via theme functions or plugin compatibility).  
- Image size definitions and responsive `srcset` usage for optimized images.

---

## 🛠 Installation (local / server)
1. Copy the theme folder into your WordPress installation:  
   `wp-content/themes/avontae-theme/`  
2. In WP Admin → Appearance → Themes → Activate **Avontae**.  
3. Import sample content (if included) or recreate menus and widgets:  
   - Appearance → Menus (assign theme locations)  
   - Appearance → Widgets / Block editor widget areas  
4. Configure theme options in Customizer (if the theme exposes any): Appearance → Customize.

---

## 🔧 Setup & Common Tasks
- Update theme settings in `/inc/theme-config.php` or `functions.php` (site name, logo sizes, etc.).  
- Add custom menus: `register_nav_menus()` in `functions.php`.  
- Add image sizes via `add_image_size()` and call them with `the_post_thumbnail()`.  
- Sanitize output with `esc_html()`, `esc_attr()`, and `wp_kses_post()` where needed.  
- Nonce & capability checks for form handlers and AJAX endpoints.  
- Use `wp_localize_script()` to pass PHP values to JavaScript safely.

---

## 💡 Development tips
- Keep template parts small and focused (e.g., `template-parts/card.php`).  
- Use `get_template_part()` instead of copy-pasting markup.  
- Prefer actions & filters to override behavior instead of editing core functions directly.  
- Use child themes for future customizations if this theme is a base.  
- Use `wp_debug` and proper error logging during development; disable debug in production.

---

## 🧪 Testing & Compatibility
- Test on multiple browsers and mobile viewports.  
- Verify theme works with popular plugins (SEO, caching, image optimization).  
- If adding Gutenberg blocks, keep them modular and use server-side rendering for dynamic blocks where appropriate.

---

## 🚀 Deployment checklist
- Set `WP_DEBUG` to `false` on production.  
- Ensure file permissions are correct for uploads and cache directories.  
- Serve assets with gzip/Brotli and set long cache headers for static assets.  
- Configure redirects, HTTPS, and security headers.  
- Verify robots/meta tags for SEO and disable indexing on staging.

---

## 🎯 Troubleshooting
- Blank screen? Check PHP error logs and `WP_DEBUG`.  
- Permalinks 404 — re-save Permalinks in WP Admin.  
- Styles not loading — confirm `wp_enqueue_style()` handles and correct paths.

---

## 📸 Screenshots
Include `screenshots/` in the theme folder (1200x900 recommended) to show preview in WP Admin.

---

## 🤝 Contributing
- Fork, create a branch, and open a PR with a description of your changes.  
- Keep commits small and focused. Add comments for non-obvious template logic.

---

## 📄 License
MIT License — see `LICENSE` file.

---

## ✉️ Author / Contact
Kanishka Verma — open an issue or PR on the repository for bugs, improvements, or deployment help.
