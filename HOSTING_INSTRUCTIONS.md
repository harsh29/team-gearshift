# 🌐 Hosting Instructions for GitHub Pages

## Complete Step-by-Step Guide for Team 60855 Gearshift Website

---

## Part 1: Setting Up GitHub (One Time Only)

### Step 1: Create a GitHub Account
1. Go to https://github.com
2. Click **"Sign up"**
3. Choose a username (e.g., `team-gearshift-60855`)
4. Use your team email address
5. Create a strong password
6. Verify your email

### Step 2: Create a New Repository
1. Click the **"+"** icon in top-right corner
2. Click **"New repository"**
3. Fill in:
   - **Repository name:** `team-gearshift` (or any name you like)
   - **Description:** "Official website for FLL Team 60855 Gearshift"
   - **Visibility:** Select **Public** (required for free GitHub Pages)
   - **DO NOT** check "Add a README file" (we already have one)
4. Click **"Create repository"**

---

## Part 2: Uploading Your Website

### Option A: Using GitHub Web Interface (Recommended for Beginners)

1. **On your new repository page**, you'll see instructions. Look for the link that says **"uploading an existing file"** and click it

2. **Prepare your files:**
   - Open the `team-gearshift-website` folder on your computer
   - Select ALL files and folders inside it

3. **Upload:**
   - Drag and drop all files into the GitHub upload box
   - OR click **"choose your files"** and select everything

4. **Commit:**
   - At the bottom, add commit message: `Initial website setup`
   - Click **"Commit changes"**

5. **Wait** for upload to complete (may take 1-2 minutes for all files)

### Option B: Using Git Command Line (For Advanced Users)

```bash
# Navigate to the website directory
cd /Users/harshtrivedi/team-gearshift-website

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Team Gearshift website"

# Rename branch to main
git branch -M main

# Connect to GitHub (replace YOUR-USERNAME and team-gearshift)
git remote add origin https://github.com/YOUR-USERNAME/team-gearshift.git

# Push to GitHub
git push -u origin main
```

---

## Part 3: Enabling GitHub Pages

1. **Go to repository Settings:**
   - Click **"Settings"** tab (near the top of your repository page)

2. **Navigate to Pages:**
   - In the left sidebar, scroll down and click **"Pages"**

3. **Configure Source:**
   - Under **"Source"**, select **"Deploy from a branch"**
   - Under **"Branch"**, select:
     - Branch: **main**
     - Folder: **/ (root)**
   - Click **"Save"**

4. **Wait for Deployment:**
   - GitHub will start building your site
   - You'll see a message: "Your site is being built"
   - Wait 2-5 minutes

5. **Get Your URL:**
   - Refresh the page
   - You'll see: "Your site is live at https://YOUR-USERNAME.github.io/team-gearshift/"
   - Click the **"Visit site"** button

---

## Part 4: Updating Site Configuration

Now that your site is live, update it with your actual information:

1. **Edit `_config.yml`:**
   - In your GitHub repository, click on `_config.yml`
   - Click the pencil icon (✏️) to edit
   - Update these lines:

```yaml
url: "https://YOUR-USERNAME.github.io"
baseurl: "/team-gearshift"  # Use your actual repository name

team:
  number: "60855"
  name: "Gearshift"
  season: "2025-2026"
  location: "Your School Name, City, State"
  email: "your-team-email@example.com"
```

2. **Save changes:**
   - Scroll to bottom
   - Click **"Commit changes"**
   - Add message: "Update team information"
   - Click **"Commit changes"** again

3. **Wait 2-3 minutes** for GitHub to rebuild your site

4. **Refresh your website** - your changes will appear!

---

## Part 5: Adding Your First Blog Post

### Method 1: Through GitHub Website

1. **Navigate to `_posts` folder:**
   - In your repository, click the `_posts` folder

2. **Create new file:**
   - Click **"Add file" → "Create new file"**

3. **Name your file:**
   - Format MUST be: `YYYY-MM-DD-title-with-hyphens.md`
   - Example: `2025-10-20-our-first-team-meeting.md`
   - ⚠️ Use today's date or earlier (not future dates!)

4. **Add content:**
```markdown
---
layout: post
title: "Our First Team Meeting"
date: 2025-10-20
category: Team
author: "Team Gearshift"
tags: [Team Updates, FLL, Kickoff]
excerpt: "Today was our first official team meeting for the 2025-2026 season!"
---

## What We Did Today

Today was amazing! We had our first team meeting and...

### Highlights

- Met all team members
- Discussed the season challenge
- Assigned initial roles
- Had pizza! 🍕

### Next Steps

Next week, we'll start:
1. Designing the robot
2. Planning our Innovation Project
3. Setting up our workspace

---

**Quote of the Day:** "Coming together is a beginning; keeping together is progress; working together is success." - Henry Ford
```

5. **Commit:**
   - Scroll down
   - Add message: "Add first blog post"
   - Click **"Commit changes"**

6. **Wait 2-3 minutes** and check your website - new post will appear!

---

## 📋 Quick Reference

### Website URLs
- **Repository:** `https://github.com/YOUR-USERNAME/team-gearshift`
- **Live Site:** `https://YOUR-USERNAME.github.io/team-gearshift/`
- **Build Status:** Check in "Actions" tab

### Important Files to Know
- `_config.yml` - Site settings and team info
- `_posts/` - All blog posts go here
- `about.md` - About page content
- `assets/css/styles.css` - Website styling

### Making Changes
1. Edit file on GitHub (pencil icon)
2. Commit changes
3. Wait 2-3 minutes
4. Refresh your site

### Blog Post Naming
- ✅ `2025-10-20-my-post.md` (correct)
- ❌ `my-post.md` (no date)
- ❌ `10-20-2025-my-post.md` (wrong format)
- ❌ `2025-12-01-future-post.md` (future date won't show)

---

## 🆘 Troubleshooting

### Problem: Site shows "404 Page Not Found"
**Solution:**
- Make sure GitHub Pages is enabled (Settings → Pages)
- Check that you selected "main" branch and "/ (root)" folder
- Wait 5 full minutes after enabling
- Try visiting: `https://YOUR-USERNAME.github.io/team-gearshift/index.html`

### Problem: Site looks broken (no styling)
**Solution:**
- Edit `_config.yml`
- Make sure `baseurl: "/team-gearshift"` matches your repository name exactly
- Commit changes and wait 2-3 minutes

### Problem: Blog post doesn't appear
**Solution:**
- Check filename format: `YYYY-MM-DD-title.md`
- Make sure date is today or earlier (not future)
- Check that file is in `_posts/` folder
- Verify the front matter (between `---`) is correct
- Wait 2-3 minutes after committing

### Problem: Build failed (in Actions tab)
**Solution:**
- Click on the failed action to see error details
- Common issues:
  - Missing closing `---` in front matter
  - Incorrect YAML syntax in `_config.yml`
  - Special characters in filenames
- Fix the error and commit again

### Problem: Changes not showing up
**Solution:**
- Wait 2-3 minutes (GitHub needs time to rebuild)
- Hard refresh browser: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
- Clear browser cache
- Check "Actions" tab for build status

---

## 🎓 Learning Resources

### For Students
- **Markdown Guide:** https://www.markdownguide.org/basic-syntax/
- **GitHub Pages Docs:** https://docs.github.com/en/pages
- **Jekyll Tutorial:** https://jekyllrb.com/docs/step-by-step/01-setup/

### For Coaches
- **Jekyll Docs:** https://jekyllrb.com/docs/
- **Liquid Templating:** https://shopify.github.io/liquid/
- **GitHub Actions:** https://docs.github.com/en/actions

---

## 🔒 Security & Privacy

### Important Notes:
- ⚠️ **DO NOT** post personal phone numbers or home addresses
- ⚠️ **DO NOT** share passwords in blog posts or code
- ⚠️ Use school email or team email only
- ⚠️ Get permission before posting photos of team members
- ⚠️ Keep financial information private

### Recommended:
- ✅ Use generic team email (e.g., `team60855@example.com`)
- ✅ Use school/meeting location (not home addresses)
- ✅ Get parental consent for student photos
- ✅ Review posts before publishing

---

## 📞 Getting Help

### If you're stuck:
1. **Check this guide** - read through the troubleshooting section
2. **Check GitHub Actions** - look for build errors
3. **Ask your coaches** - they're there to help!
4. **Google it** - Search "Jekyll GitHub Pages [your issue]"
5. **GitHub Community** - https://github.community/

### Useful Search Terms:
- "Jekyll blog post not showing"
- "GitHub Pages 404 error"
- "Jekyll markdown syntax"
- "GitHub Pages custom domain"

---

## 🎯 Next Steps

Once your site is live:

### Week 1:
- [ ] Customize team information in `_config.yml`
- [ ] Write and publish first blog post
- [ ] Update About page with team photos
- [ ] Share website URL with parents/mentors

### Week 2:
- [ ] Add team logo to site
- [ ] Create custom color scheme
- [ ] Write second blog post about robot design
- [ ] Add social media links (if applicable)

### Ongoing:
- [ ] Post weekly blog updates
- [ ] Share competition experiences
- [ ] Document robot development
- [ ] Showcase Innovation Project progress

---

## 🏆 Success Checklist

- [ ] Website is live and accessible
- [ ] Team information is accurate
- [ ] First blog post is published
- [ ] About page has team info
- [ ] All team members know how to add posts
- [ ] Coaches have repository access
- [ ] Parents have website URL
- [ ] URL shared with FLL community

---

**Congratulations! Your Team Gearshift website is live! 🎉**

*Now go shift into high gear and document your amazing FLL journey!* 🤖⚙️

---

*Last updated: October 2025*
*For Team 60855 Gearshift | FIRST LEGO League 2025-2026*

