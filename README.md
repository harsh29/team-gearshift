# Team 60855 Gearshift Website

A Jekyll-powered website for FIRST LEGO League Team 60855 Gearshift, designed to be hosted on GitHub Pages.

## 🚀 Quick Start

### Hosting on GitHub Pages

1. **Create a GitHub Account** (if you don't have one)
   - Go to [github.com](https://github.com)
   - Sign up for a free account

2. **Create a New Repository**
   - Click the "+" icon in the top right
   - Select "New repository"
   - Name it: `team-gearshift` (or any name you prefer)
   - Make it **Public** (required for free GitHub Pages)
   - Click "Create repository"

3. **Upload Your Website Files**
   
   **Option A: Using GitHub Web Interface (Easiest)**
   - On your repository page, click "uploading an existing file"
   - Drag and drop ALL files from the `team-gearshift-website` folder
   - Click "Commit changes"

   **Option B: Using Git Command Line**
   ```bash
   cd team-gearshift-website
   git init
   git add .
   git commit -m "Initial commit: Team Gearshift website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/team-gearshift.git
   git push -u origin main
   ```

4. **Enable GitHub Pages**
   - Go to repository "Settings"
   - Scroll down to "Pages" section (left sidebar)
   - Under "Source", select "Deploy from a branch"
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click "Save"

5. **Wait for Deployment** (2-5 minutes)
   - GitHub will build your site automatically
   - A green checkmark will appear when ready
   - Your site will be live at: `https://YOUR-USERNAME.github.io/team-gearshift/`

6. **Update Configuration**
   - Edit `_config.yml` file
   - Change `url:` to your GitHub Pages URL
   - Change `baseurl:` to `/team-gearshift` (your repo name)
   - Update team information (email, location, etc.)
   - Commit and push changes

## 📝 How to Add a Blog Post

### Method 1: Using GitHub Web Interface (Easiest for Students)

1. **Go to Your Repository** on GitHub

2. **Navigate to `_posts` Folder**
   - Click on the `_posts` folder

3. **Create New File**
   - Click "Add file" → "Create new file"

4. **Name Your File**
   - Format: `YYYY-MM-DD-title-with-hyphens.md`
   - Example: `2025-10-20-our-first-competition.md`
   - ⚠️ **Important:** Date must be today or earlier (Jekyll won't show future posts)

5. **Add Blog Content**
   ```markdown
   ---
   layout: post
   title: "Your Post Title Here"
   date: 2025-10-20
   category: Programming
   author: "Your Name"
   tags: [tag1, tag2, tag3]
   excerpt: "A short preview of your post that appears on the blog page."
   ---

   Write your blog post content here using Markdown!

   ## Use Headers

   Write paragraphs normally.

   - Make bullet lists
   - Like this

   1. Or numbered lists
   2. Like this

   **Bold text** and *italic text*

   ```python
   # Include code blocks
   def hello():
       print("Hello FLL!")
   ```

   ![Add images](../assets/images/your-image.jpg)
   ```

6. **Commit the File**
   - Scroll down
   - Click "Commit changes"
   - Wait 2-3 minutes for GitHub to rebuild your site
   - Your new post will appear!

### Method 2: Using a Text Editor (For Advanced Users)

1. **Create File Locally**
   - Navigate to `team-gearshift-website/_posts/`
   - Create new file: `2025-10-20-your-title.md`

2. **Write Your Post** (see template above)

3. **Commit and Push**
   ```bash
   cd team-gearshift-website
   git add _posts/2025-10-20-your-title.md
   git commit -m "Add new blog post: Your Title"
   git push origin main
   ```

## 📋 Blog Post Template

Save this as a template for quick blog posts:

```markdown
---
layout: post
title: "Your Amazing Title"
date: 2025-10-20
category: Programming  # Options: Programming, Design, Team, Strategy, Competition
author: "Team Member Name"
tags: [FLL, Robotics, SPIKE Prime]
excerpt: "Write a 1-2 sentence preview of your post here."
---

## Introduction

Start your post here...

## Main Content

Write your content with:
- Headers (##, ###)
- Bullet points
- Numbered lists
- **Bold** and *italic* text

## Code Examples

```python
# Your code here
async def my_function():
    print("Hello!")
```

## Images

![Description](../assets/images/my-image.jpg)

## Conclusion

Wrap up your post here.

---

**Fun Fact:** Add a fun fact or quote at the end!
```

## 🎨 Customizing Your Website

### Update Team Information

Edit `_config.yml`:
```yaml
team:
  number: "60855"
  name: "Gearshift"
  season: "2025-2026"
  location: "Your School Name, City, State"
  email: "your-email@example.com"
```

### Change Colors

Edit `assets/css/styles.css` and modify the CSS variables:
```css
:root {
    --primary-color: #FF6B35;      /* Main orange color */
    --secondary-color: #004E89;    /* Blue color */
    --accent-color: #F7931E;       /* Yellow-orange */
}
```

### Add Team Photos

1. Create folder: `assets/images/`
2. Upload photos there
3. Reference in blog posts: `![Photo](../assets/images/photo.jpg)`

### Add Social Media Links

Edit `_config.yml` and uncomment the social section:
```yaml
social:
  twitter: "https://twitter.com/teamgearshift"
  instagram: "https://instagram.com/teamgearshift"
  youtube: "https://youtube.com/@teamgearshift"
```

Then edit `_layouts/default.html` to add social media icons in the footer.

## 🛠️ Testing Locally (Optional)

If you want to preview your site before publishing:

1. **Install Ruby** (if not already installed)
   - Mac: `brew install ruby`
   - Windows: Download from [rubyinstaller.org](https://rubyinstaller.org)
   - Linux: `sudo apt-get install ruby-full`

2. **Install Jekyll**
   ```bash
   gem install jekyll bundler
   ```

3. **Install Dependencies**
   ```bash
   cd team-gearshift-website
   bundle install
   ```

4. **Run Local Server**
   ```bash
   bundle exec jekyll serve
   ```

5. **View Site**
   - Open browser to `http://localhost:4000`
   - Site auto-updates as you edit files

## 📁 File Structure

```
team-gearshift-website/
├── _config.yml              # Site configuration
├── _layouts/                # Page templates
│   ├── default.html         # Main layout
│   └── post.html           # Blog post layout
├── _posts/                  # Blog posts go here
│   ├── 2025-10-15-post1.md
│   ├── 2025-10-12-post2.md
│   └── ...
├── assets/
│   ├── css/
│   │   └── styles.css      # All styling
│   ├── js/
│   │   └── script.js       # JavaScript
│   └── images/             # Images go here
├── index.md                 # Home page
├── about.md                 # About page
├── blog.md                  # Blog listing page
├── Gemfile                  # Ruby dependencies
└── README.md               # This file
```

## 🆘 Troubleshooting

### Site Not Showing Up
- Wait 5 minutes after pushing changes
- Check "Actions" tab in GitHub for build errors
- Ensure GitHub Pages is enabled in Settings

### Blog Post Not Appearing
- Check date format: `YYYY-MM-DD`
- Date must be today or earlier (not future)
- Check front matter (the --- section) is correct
- Wait 2-3 minutes after committing

### Styling Looks Broken
- Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Check that `styles.css` is in `assets/css/` folder
- Verify `_config.yml` has correct `baseurl`

### Images Not Loading
- Check file path: `../assets/images/filename.jpg`
- Make sure image is committed to repository
- Check image filename matches exactly (case-sensitive)

## 📚 Markdown Guide

Markdown is the formatting language used for blog posts:

```markdown
# Header 1
## Header 2
### Header 3

**Bold text**
*Italic text*

- Bullet point 1
- Bullet point 2

1. Numbered item 1
2. Numbered item 2

[Link text](https://example.com)

![Image](path/to/image.jpg)

> Blockquote

`inline code`

```python
code block
```
```

## 🎓 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Guide](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [FIRST LEGO League](https://www.firstlegoleague.org/)

## 🤝 Contributing

All team members can contribute! To add content:

1. Write your blog post or update
2. Commit to GitHub
3. Team leaders review and approve
4. Changes go live automatically

## 📞 Support

Questions? Ask your team coaches or tech mentors!

## 📄 License

This website is for Team 60855 Gearshift, competing in FIRST LEGO League.

---

**Built with ❤️ by Team Gearshift**

*Let's shift into gear! 🤖⚙️*

