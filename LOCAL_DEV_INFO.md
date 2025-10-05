# ✅ Local Development - Ready!

## 🌐 Access Your Website

**Your site is now running at:** http://localhost:4000

(Note: For local development, we use the root URL, not /roommate-info)

---

## 🚀 Quick Start Commands

### Start the server:
```bash
./START_SERVER.sh
```

Or manually:
```bash
cd /Users/xy51/Desktop/roommate-info-main
export PATH="/opt/homebrew/bin:$PATH"
eval "$(rbenv init - zsh)"
bundle exec jekyll serve --livereload --baseurl ""
```

### Stop the server:
```bash
pkill -f "jekyll serve"
```

Or press `Ctrl+C` in the terminal running the server.

---

## 📝 Files You Can Edit

### Content Sections (in `_includes/`):
- `header.html` - Hero section with main image
- `nav.html` - Top navigation
- `call-to-action.html` - CTA section
- `services.html` - Services/features
- `portfolio.html` - Gallery/portfolio
- `aside.html` - Aside content
- `contact.html` - Contact form

### Configuration:
- `_config.yml` - Site title, description, URLs

### Styling:
- `_sass/_base.scss` - Main styles
- `_sass/_mixins.scss` - SASS mixins
- `css/main.scss` - Style imports

---

## ✨ Live Reload

The server has **live reload enabled**! This means:

1. Edit any file and save it
2. The browser automatically refreshes
3. You see your changes instantly!

No need to manually refresh the page! 🎉

---

## 🐛 Troubleshooting

**If changes don't appear:**
- Check the terminal for errors
- Try hard refresh: `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows)
- Restart the server

**If you see a 404:**
- Make sure you're visiting http://localhost:4000 (without /roommate-info)

**Port already in use:**
- Stop existing server: `pkill -f "jekyll serve"`
- Or use different port: `bundle exec jekyll serve --port 4001 --baseurl ""`

---

## 📦 When Deploying to GitHub Pages

The site is configured to deploy to: https://xiaocong-yang.github.io/roommate-info

The `/roommate-info` baseurl is automatically used in production (GitHub Pages).
For local development, we override it to empty string for convenience.
