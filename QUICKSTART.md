# Quick Start Guide
## Team 60855 Gearshift Website

### ⚡ Super Fast Setup (5 Minutes)

#### Step 1: Create GitHub Account
Go to [github.com](https://github.com) and sign up (if you don't have an account)

#### Step 2: Create Repository
1. Click **"+" → New repository**
2. Name: `team-gearshift`
3. Make it **Public**
4. Click **"Create repository"**

#### Step 3: Upload Files
1. Click **"uploading an existing file"**
2. Drag ALL files from `team-gearshift-website` folder
3. Click **"Commit changes"**

#### Step 4: Enable GitHub Pages
1. Go to **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main**, Folder: **/ (root)**
4. Click **Save**

#### Step 5: Wait & Visit
- Wait 2-5 minutes
- Visit: `https://YOUR-USERNAME.github.io/team-gearshift/`
- 🎉 Your site is live!

---

### 📝 Add a Blog Post (2 Minutes)

1. Go to your repository on GitHub
2. Click `_posts` folder
3. Click **"Add file" → "Create new file"**
4. Name: `2025-10-20-my-post.md` (use today's date!)
5. Paste this template:

```markdown
---
layout: post
title: "My Awesome Blog Post"
date: 2025-10-20
category: Programming
author: "Your Name"
tags: [FLL, Robotics]
excerpt: "A quick summary of this post."
---

## My First Heading

Write your content here!

- Use bullet points
- Like this

**Bold text** and *italic text*

```python
# Add code
print("Hello FLL!")
```
```

6. Click **"Commit changes"**
7. Wait 2-3 minutes
8. Your post appears on the website!

---

### 🎨 Customize Your Site

#### Change Team Info
Edit `_config.yml`:
```yaml
team:
  number: "60855"
  name: "Gearshift"
  location: "Your School, City, State"
  email: "youremail@example.com"
```

#### Change Colors
Edit `assets/css/styles.css` (lines 11-13):
```css
--primary-color: #FF6B35;    /* Change to your team color */
--secondary-color: #004E89;   /* Change to your second color */
```

---

### 🆘 Common Issues

**Site not showing up?**
- Wait 5 minutes
- Check Settings → Pages is enabled
- Check Actions tab for errors

**Blog post not appearing?**
- File name format: `YYYY-MM-DD-title.md`
- Date must be today or earlier
- Wait 2-3 minutes after committing

**Styling looks wrong?**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Check `baseurl` in `_config.yml`

---

### 📚 Learn More

- Full documentation: See `README.md`
- Markdown guide: [markdownguide.org](https://www.markdownguide.org)
- Jekyll docs: [jekyllrb.com](https://jekyllrb.com)

---

**That's it! You're ready to go! 🚀**

*Questions? Ask your team coaches!*

