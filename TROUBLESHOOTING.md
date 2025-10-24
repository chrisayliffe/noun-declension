# 🔧 Troubleshooting: Your URL Shows Nothing

## Issue: Getting 404 Error or Blank Page

Your URL: `https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson%201`

**Status:** File not found (404 error)

---

## ✅ Solution Steps

### Step 1: Verify File Upload

1. **Go to your GitHub repository:**
   ```
   https://github.com/chrisayliffe/Verb-practice-game
   ```

2. **Check if the file exists:**
   - Look for: `icelandic-verb-game-dynamic.html`
   - It should be in the **root folder** (not in a subfolder)

3. **If file is missing:**
   - Download it from `/app/frontend/public/icelandic-verb-game-dynamic.html`
   - Upload to your GitHub repo root folder

---

### Step 2: Check File Name Exactly

The file must be named **exactly**:
```
icelandic-verb-game-dynamic.html
```

**Common mistakes:**
- ❌ `icelandic-verb-game.html` (missing "-dynamic")
- ❌ `Icelandic-verb-game-dynamic.html` (capital I)
- ❌ `icelandic-verb-game-dynamic.HTML` (capital HTML)

---

### Step 3: Verify GitHub Pages Settings

1. **Go to repository Settings:**
   ```
   https://github.com/chrisayliffe/Verb-practice-game/settings/pages
   ```

2. **Check these settings:**
   - ✅ Source: Deploy from a branch
   - ✅ Branch: **main** (or master)
   - ✅ Folder: **/ (root)**
   - ✅ Status: Should show green checkmark with "Your site is live"

3. **Wait 2-3 minutes** after any changes for GitHub to deploy

---

### Step 4: Test Without Lesson Parameter First

Try accessing the file without the lesson parameter:

```
https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html
```

**Expected result:**
- Should show "Loading lesson data..." or an error about the lesson
- If you get 404, the file isn't uploaded correctly

---

## 🧪 Quick Test

### Test 1: Check Repository Structure

Your repository should look like this:
```
Verb-practice-game/
├── icelandic-verb-game-dynamic.html   ← File must be here
└── (other files)
```

**NOT like this:**
```
Verb-practice-game/
└── folder/
    └── icelandic-verb-game-dynamic.html   ← Wrong! Not in subfolder
```

### Test 2: Verify File Contents

1. Open the file on GitHub
2. Click on `icelandic-verb-game-dynamic.html`
3. Check first few lines contain:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <title>Icelandic Verb Practice Game</title>
   ```

---

## 🔍 Alternative: Use Simple Static File First

I'll create a simpler test file that you can use while we debug the Google Sheets version.

### Option A: Test File (No Google Sheets)

Create `test.html` with this content:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Test</title>
</head>
<body>
    <h1>It Works!</h1>
    <p>If you see this, your GitHub Pages is working.</p>
</body>
</html>
```

**Upload and test:**
```
https://chrisayliffe.github.io/Verb-practice-game/test.html
```

**If this works:**
- Your GitHub Pages is set up correctly
- Problem is with the dynamic file

**If this doesn't work:**
- GitHub Pages not enabled
- Wrong repository name
- Files in wrong folder

---

## 🎯 Most Common Issues & Fixes

### Issue 1: Wrong Repository Name
**Check:** Is your repo actually called `Verb-practice-game` with capital V?
- GitHub URLs are case-sensitive
- Check actual repo name on GitHub

### Issue 2: File in Subfolder
**Fix:** Move file to root of repository
1. Delete file from subfolder
2. Upload to root (main repository page)

### Issue 3: Branch Name Wrong
**Fix:** 
1. Go to Settings → Pages
2. Make sure branch matches your actual branch
3. Common branches: `main`, `master`, `gh-pages`

### Issue 4: Pages Not Enabled
**Fix:**
1. Settings → Pages
2. Select Source: Deploy from a branch
3. Select Branch: main (or master)
4. Click Save
5. Wait 2-3 minutes

---

## 📞 Step-by-Step Fix

### Do This Now:

**1. Verify file exists:**
```
Go to: https://github.com/chrisayliffe/Verb-practice-game
Look for: icelandic-verb-game-dynamic.html in the file list
```

**2. If file is missing:**
```
Download from: /app/frontend/public/icelandic-verb-game-dynamic.html
Upload to: Root of your GitHub repository
Commit changes
```

**3. Check Pages settings:**
```
Go to: Settings → Pages
Verify: Branch = main, Folder = / (root)
Status: Should say "Your site is live at..."
```

**4. Wait and test:**
```
Wait: 2-3 minutes for deployment
Test: https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html
```

---

## ✅ Verification Checklist

Before trying again:

- [ ] File name is exactly: `icelandic-verb-game-dynamic.html`
- [ ] File is in root folder (not in a subfolder)
- [ ] GitHub Pages is enabled
- [ ] Branch is set correctly (main or master)
- [ ] Waited 2-3 minutes after upload
- [ ] Tested URL without lesson parameter first
- [ ] Repository name is correct (case-sensitive)

---

## 🆘 Still Not Working?

### Share These Details:

1. **Exact file name in your repo:** _____________
2. **File location:** (root or in a folder?)
3. **GitHub Pages status:** (from Settings → Pages)
4. **Branch name:** _____________

### Quick Fixes to Try:

**Option 1: Rename repository**
- Must not have spaces
- Suggest: `verb-practice-game` (all lowercase)

**Option 2: Use different branch**
- Try creating `gh-pages` branch
- Put file in that branch
- Select `gh-pages` in Pages settings

**Option 3: Simple static version**
- Use the non-dynamic HTML files instead
- `lesson-1-nutid-basic.html` (from earlier)
- These work without Google Sheets

---

## 🎯 Expected Working URL

Once fixed, your URL should be:
```
https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html
```

And with lesson:
```
https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

---

## 💡 Pro Tip

**Test this sequence:**

1. First: `https://chrisayliffe.github.io/Verb-practice-game/`
   - Should show: Index or file listing

2. Then: `https://chrisayliffe.github.io/Verb-practice-game/icelandic-verb-game-dynamic.html`
   - Should show: Game or "Loading..." message

3. Finally: Add `?lesson=Lesson 1`
   - Should show: Your actual lesson

If step 1 or 2 fails, GitHub Pages issue.  
If step 3 fails, Google Sheets issue.

---

Let me know which step fails and I can help debug further!
