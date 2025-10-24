# 🚀 Complete Setup From Scratch

## Issue: Your URL isn't working

**URL tried:** `https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html`  
**Status:** 404 - File not found

**Likely causes:**
1. Repository doesn't exist yet
2. Repository is private
3. File hasn't been uploaded
4. GitHub Pages not enabled

---

## ✅ START HERE: Complete Setup

### Step 1: Create GitHub Repository

1. **Go to GitHub:** https://github.com
2. **Click:** Green "New" button (or go to https://github.com/new)
3. **Repository name:** `verb-practice-game` (lowercase, no spaces)
4. **Description:** (optional) "Icelandic Verb Practice Game"
5. **Public:** ✅ Must be public for free GitHub Pages
6. **Initialize:** ✅ Check "Add a README file"
7. **Click:** "Create repository"

---

### Step 2: Upload the HTML File

**Option A: Via Web Interface (Easiest)**

1. **In your new repository**, click "Add file" → "Upload files"

2. **Download the file to your computer first:**
   - Location: `/app/frontend/public/icelandic-verb-game-dynamic.html`
   - Save it to your Downloads folder

3. **Drag and drop** the file into GitHub
   - Or click "choose your files" and select it

4. **Scroll down** and click "Commit changes"

**Option B: Via Git (If you're comfortable with Git)**

```bash
git clone https://github.com/chrisayliffe/verb-practice-game.git
cd verb-practice-game
# Copy icelandic-verb-game-dynamic.html into this folder
git add icelandic-verb-game-dynamic.html
git commit -m "Add game file"
git push
```

---

### Step 3: Enable GitHub Pages

1. **In your repository**, click "Settings" (top right)

2. **In left sidebar**, scroll down and click "Pages"

3. **Under "Build and deployment":**
   - Source: **Deploy from a branch**
   - Branch: **main** (select from dropdown)
   - Folder: **/ (root)** (select from dropdown)

4. **Click "Save"**

5. **Wait 2-3 minutes** for GitHub to deploy

6. **Refresh the page** - you should see:
   ```
   ✅ Your site is live at https://chrisayliffe.github.io/verb-practice-game/
   ```

---

### Step 4: Get Your URL

Your base URL will be:
```
https://chrisayliffe.github.io/verb-practice-game/
```

**Full URL for the game:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html
```

**With lesson parameter:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

---

### Step 5: Verify Google Sheet Setup

1. **Open your sheet:**
   ```
   https://docs.google.com/spreadsheets/d/1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes/edit
   ```

2. **Check sharing settings:**
   - Click "Share" button (top right)
   - Under "General access", select: **"Anyone with the link"**
   - Role: **Viewer**
   - Click "Done"

3. **Verify you have a tab called "Lesson 1":**
   - Look at the bottom tabs
   - Must be exactly: "Lesson 1" (with capital L and space)

4. **Check tab structure:**
   ```
   Row 1: LESSON_TITLE | Your Title
   Row 2: LESSON_SUBTITLE | Your Subtitle
   Row 3: SHOW_TENSES | yes or no
   Row 4: [empty]
   Row 5: Verb | Tense | ég | þú | hann/hún/það | við | þið | þeir/þær/þau
   Row 6+: [your verb data]
   ```

---

### Step 6: Test Your Setup

**Test 1: Base URL**
```
https://chrisayliffe.github.io/verb-practice-game/
```
- Should show: File listing or README

**Test 2: HTML File**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html
```
- Should show: "Loading lesson data..." or error message

**Test 3: With Lesson**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```
- Should show: Your game with verbs loaded

---

## 🔍 Verification Checklist

Before proceeding, verify:

**GitHub:**
- [ ] Repository created and is **public**
- [ ] File `icelandic-verb-game-dynamic.html` uploaded to **root**
- [ ] GitHub Pages enabled (Settings → Pages)
- [ ] Status shows "Your site is live at..."
- [ ] Waited 2-3 minutes after enabling Pages

**Google Sheets:**
- [ ] Sheet ID is correct: `1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes`
- [ ] Sharing set to "Anyone with the link"
- [ ] Tab "Lesson 1" exists
- [ ] Tab has correct structure (see template)
- [ ] Verb data filled in rows 6+

**URL:**
- [ ] Using lowercase repository name: `verb-practice-game`
- [ ] File name exact: `icelandic-verb-game-dynamic.html`
- [ ] Lesson parameter matches tab: `?lesson=Lesson 1`

---

## 🎯 Quick Start Alternative

If you want to test without Google Sheets first:

### Use Static Version

Instead of the dynamic version, upload one of these:
- `lesson-1-nutid-basic.html` (Nútíð only, 2 verbs)
- `lesson-2-both-tenses.html` (Both tenses, 3 verbs)

**These work immediately without Google Sheets!**

**URL would be:**
```
https://chrisayliffe.github.io/verb-practice-game/lesson-1-nutid-basic.html
```

---

## 📞 Common Issues & Solutions

### Issue: Repository not found (404)

**Problem:** Repository doesn't exist or is private

**Solution:**
1. Check you're logged into GitHub
2. Verify repository name is correct
3. Make sure it's **public** (not private)

### Issue: File not found (404)

**Problem:** File not uploaded or in wrong location

**Solution:**
1. Go to your repo: https://github.com/chrisayliffe/verb-practice-game
2. Look for `icelandic-verb-game-dynamic.html` in file list
3. If missing, upload it
4. If in subfolder, move to root

### Issue: GitHub Pages not available

**Problem:** Pages not enabled or wrong settings

**Solution:**
1. Settings → Pages
2. Source: Deploy from a branch
3. Branch: main (or master if that's your default)
4. Folder: / (root)
5. Save and wait 2-3 minutes

### Issue: Game loads but shows error

**Problem:** Google Sheet not accessible or wrong structure

**Solution:**
1. Test sheet access in incognito window
2. Verify sharing is "Anyone with link"
3. Check tab name matches exactly
4. Verify row structure matches template

---

## 💻 File Download Instructions

The HTML file you need is located at:
```
/app/frontend/public/icelandic-verb-game-dynamic.html
```

**To download:**
1. Open your workspace file browser
2. Navigate to `/app/frontend/public/`
3. Find `icelandic-verb-game-dynamic.html`
4. Right-click → Download (or use download button)
5. Save to your computer

**Then upload to GitHub as described in Step 2.**

---

## 📋 Your Personal Checklist

Fill this in as you complete each step:

```
[ ] Created GitHub repository: verb-practice-game
[ ] Repository is PUBLIC
[ ] Downloaded icelandic-verb-game-dynamic.html
[ ] Uploaded file to repository root
[ ] Enabled GitHub Pages
[ ] Waited 3 minutes
[ ] Got "Your site is live" message
[ ] Base URL works: https://chrisayliffe.github.io/verb-practice-game/
[ ] HTML file URL works (without lesson)
[ ] Google Sheet is publicly shared
[ ] Google Sheet has "Lesson 1" tab
[ ] Sheet structure matches template
[ ] Full URL works with lesson parameter
```

---

## 🎉 Success Criteria

**You'll know it's working when:**

1. ✅ URL loads without 404 error
2. ✅ Shows "Loading..." message briefly
3. ✅ Loads game with your lesson title
4. ✅ Verb dropdown shows your verbs
5. ✅ Fill in the Blank mode works
6. ✅ Drag & Drop mode works
7. ✅ Tense selector appears/hides based on your settings

---

## 🆘 Need More Help?

**If stuck at any step, note:**
1. Which step you're on
2. What error message you see (if any)
3. Screenshot of your GitHub Pages settings
4. Screenshot of your Google Sheet tab structure

**Common debugging commands:**
```
# Check if file exists
https://github.com/chrisayliffe/verb-practice-game

# Check Pages status
https://github.com/chrisayliffe/verb-practice-game/settings/pages

# Test base URL
https://chrisayliffe.github.io/verb-practice-game/

# Test file directly
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html
```

---

## ✨ Next Steps After Setup

Once working:
1. ✅ Create more tabs in Google Sheet
2. ✅ Test each with: `?lesson=Tab Name`
3. ✅ Embed working URLs in LearnWorlds
4. ✅ Share with students

**Remember:** Same HTML file, different lessons = just change the tab name in URL!
