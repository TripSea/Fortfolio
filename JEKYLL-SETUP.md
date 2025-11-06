# Jekyll Blog Setup - Quick Reference

## Installation Steps

1. **Install Ruby+Devkit** (Ruby 3.3.x recommended)
   - Download from: https://rubyinstaller.org/downloads/
   - Run installer with defaults
   - Check "ridk install" at the end

2. **Install Jekyll and Bundler**
   ```powershell
   gem install jekyll bundler
   ```

3. **Install Project Dependencies**
   ```powershell
   cd /path/to/fortfolio
   bundle install
   ```

4. **Test Local Build**
   ```powershell
   bundle exec jekyll serve
   ```
   Then visit: http://localhost:4000

## Project Structure

```
fortfolio/
├── _config.yml              # Jekyll configuration
├── Gemfile                  # Ruby dependencies
├── .gitignore              # Ignore Jekyll build files
├── _layouts/
│   ├── default.html        # Main layout template
│   └── post.html           # Blog post template
├── _market_analysis/       # Market Analysis posts
│   └── 2025-12-15-q4-market-outlook.md
├── _strategies/            # Strategy Guide posts
│   └── 2025-12-10-iron-condor-guide.md
├── _education/             # Educational posts
│   └── 2025-12-05-options-101.md
├── _community/             # Community posts
│   └── 2025-12-12-member-success-story.md
├── _updates/               # Product Update posts
│   └── 2025-12-08-advanced-filtering.md
├── blog/                   # Static HTML category pages (to convert)
│   ├── index.html         # Main blog page
│   ├── market-analysis/
│   ├── strategies/
│   ├── education/
│   ├── community/
│   └── updates/
└── index.html             # Homepage (stays static)
```

## How to Add a New Blog Post

1. **Create markdown file** in appropriate collection folder:
   ```
   _market_analysis/2025-12-20-my-new-post.md
   ```

2. **Add front matter** at the top:
   ```yaml
   ---
   title: "My Post Title"
   subtitle: "Optional subtitle"
   date: 2025-12-20
   read_time: "10 min read"
   author: Fortfolio Team
   tags: [tag1, tag2, tag3]
   ---
   ```

3. **Write content** in Markdown below the front matter

4. **Build and preview**:
   ```powershell
   bundle exec jekyll serve
   ```

## Collections Explained

Each category is a Jekyll "collection" defined in `_config.yml`:

- `_market_analysis` → outputs to `/blog/market-analysis/post-title/`
- `_strategies` → outputs to `/blog/strategies/post-title/`
- `_education` → outputs to `/blog/education/post-title/`
- `_community` → outputs to `/blog/community/post-title/`
- `_updates` → outputs to `/blog/updates/post-title/`

## Next Steps (After Ruby Install)

1. Run `bundle install` to get all gems
2. Run `bundle exec jekyll serve` to test
3. Convert category index pages to use Jekyll (loop through collection posts)
4. Remove "Coming Soon" badges from real posts
5. Set up GitHub Pages deployment

## Current Status

✅ Jekyll config created  
✅ Layouts built with your styling  
✅ Collections configured  
✅ Sample posts created (1 per category)  
✅ Gemfile and .gitignore added  
✅ Blog post content CSS added  
⏳ Waiting for Ruby installation  
⏳ Need to convert category pages to Jekyll  
⏳ Need to configure deployment  

## Useful Commands

```powershell
# Install dependencies
bundle install

# Start local server
bundle exec jekyll serve

# Build site (outputs to _site/)
bundle exec jekyll build

# Build for production
JEKYLL_ENV=production bundle exec jekyll build

# Update gems
bundle update
```

## Deployment Options

**Option 1: GitHub Pages (Recommended)**
- Push to GitHub
- Enable GitHub Pages in repo settings
- Automatic builds on push

**Option 2: Manual Build**
- Run `bundle exec jekyll build`
- Upload `_site/` folder to hosting
- Your main static files stay at root

## Main Site vs Blog

- **Main site** (`index.html`, `about/`, etc.) → Pure HTML, no Jekyll processing
- **Blog** (`/blog/*`) → Jekyll processes markdown posts
- Both use same `styles.css` for consistency

## Sample Post Front Matter Templates

**Market Analysis:**
```yaml
---
title: "Your Title"
subtitle: "Subtitle here"
date: 2025-12-15
read_time: "12 min read"
tags: [technical-analysis, sp500, trading]
---
```

**Strategy Guide:**
```yaml
---
title: "Strategy Name: Full Guide"
subtitle: "Step-by-step walkthrough"
date: 2025-12-10
read_time: "15 min read"
tags: [options, strategy, intermediate]
---
```

**Educational:**
```yaml
---
title: "Topic 101: Basics"
subtitle: "Beginner's guide"
date: 2025-12-05
read_time: "10 min read"
tags: [education, beginner, fundamentals]
---
```

## Questions?

Check Jekyll docs: https://jekyllrb.com/docs/
Or ask in Discord: https://discord.gg/A7pZVkfmaa
