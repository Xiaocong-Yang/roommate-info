# Local Development Guide

This is a Jekyll-based static website. Here are several options to run it locally:

## Option 1: Manual Setup (Recommended)

Since you don't have Homebrew installed yet, I recommend installing it first:

### Step 1: Install Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After installation, follow the instructions to add Homebrew to your PATH (the installer will tell you exactly what to do).

### Step 2: Install rbenv and Ruby
```bash
brew install rbenv ruby-build
```

### Step 3: Initialize rbenv (add to your ~/.zshrc)
```bash
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
source ~/.zshrc
```

### Step 4: Install a newer Ruby version
```bash
rbenv install 3.1.4
cd /Users/xy51/Desktop/roommate-info-main
rbenv local 3.1.4
```

### Step 5: Install Jekyll and dependencies
```bash
gem install bundler
bundle install
```

### Step 6: Run the development server
```bash
bundle exec jekyll serve
```

Visit: http://localhost:4000/roommate-info

The site will auto-reload when you make changes!

---

## Option 2: Use Docker (If you have Docker installed)

If you have Docker, this is the easiest option:

```bash
cd /Users/xy51/Desktop/roommate-info-main
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll jekyll serve --baseurl ""
```

Visit: http://localhost:4000

---

## Option 3: Quick Preview with Python (No Jekyll features)

If you just want to preview the static HTML without Jekyll processing:

```bash
cd /Users/xy51/Desktop/roommate-info-main
python3 -m http.server 8000
```

Visit: http://localhost:8000

**Note:** This won't process Jekyll templates, SASS, or includes, so styling may be broken.

---

## Making Changes

Once you have the development server running:

1. Edit files in `_includes/`, `_layouts/`, or `index.html`
2. Save your changes
3. The browser will automatically reload (with Jekyll serve)
4. See your changes instantly!

---

## Troubleshooting

- **Port already in use**: Add `--port 4001` to use a different port
- **Changes not showing**: Try refreshing with Cmd+Shift+R (hard refresh)
- **CSS not loading**: Make sure you're using the correct URL with `/roommate-info` baseurl


