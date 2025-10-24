# 📍 Step-by-Step: Get Your Exercise URL

## Follow These Steps In Order

---

## ✅ STEP 1: Upload File to GitHub

1. Go to your GitHub repository (or create new one)
2. Click **"Add file"** → **"Upload files"**
3. Upload: `icelandic-verb-game-dynamic.html`
4. Click **"Commit changes"**

---

## ✅ STEP 2: Enable GitHub Pages

1. In your repository, click **"Settings"** (top right)
2. Scroll down left sidebar, click **"Pages"**
3. Under "Branch", select: **main**
4. Under "Folder", select: **/ (root)**
5. Click **"Save"**
6. Wait 1-2 minutes for deployment

---

## ✅ STEP 3: Get Your Base URL

After enabling Pages, you'll see:

```
┌─────────────────────────────────────────────────┐
│ ✅ Your site is live at:                        │
│ https://yourusername.github.io/your-repo-name/  │
└─────────────────────────────────────────────────┘
```

**COPY THIS URL** - This is your Base URL!

---

## ✅ STEP 4: Build Your Complete URL

Take your Base URL and add the file name:

**Your Base URL:**
```
https://yourusername.github.io/your-repo-name/
```

**Add file name:**
```
https://yourusername.github.io/your-repo-name/icelandic-verb-game-dynamic.html
```

---

## ✅ STEP 5: Add Lesson Parameter

Now add `?lesson=` and your Google Sheet tab name:

**If your tab is "Lesson 1":**
```
https://yourusername.github.io/your-repo-name/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

**If your tab is "Beginner":**
```
https://yourusername.github.io/your-repo-name/icelandic-verb-game-dynamic.html?lesson=Beginner
```

---

## ✅ STEP 6: Test Your URL

1. **Copy** your complete URL
2. **Open** a new browser tab
3. **Paste** the URL
4. **Press Enter**

### What You Should See:

**Success ✅**
```
1. Shows "Loading Lesson 1..." (briefly)
2. Loads the game with your title
3. Shows your verbs in dropdown
4. Game is playable
```

**Error ❌**
```
If you see an error message:
- Check Google Sheet is publicly shared
- Check tab name matches exactly
- Check sheet structure follows template
```

---

## ✅ STEP 7: Create URLs for All Lessons

Repeat for each tab in your Google Sheet:

**Tab: "Lesson 1"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

**Tab: "Lesson 2"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Lesson 2
```

**Tab: "Advanced"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Advanced
```

---

## ✅ STEP 8: Embed in LearnWorlds

For each lesson in LearnWorlds:

1. **Add HTML block** to your lesson page
2. **Paste this code:**

```html
<iframe 
    src="YOUR_URL_HERE"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

3. **Replace** `YOUR_URL_HERE` with your URL from Step 7
4. **Save** the lesson

---

## 📝 Real Example Walkthrough

### My Setup:

**GitHub:**
- Username: `john-teacher`
- Repository: `icelandic-lessons`
- GitHub Pages URL: `https://john-teacher.github.io/icelandic-lessons/`

**Google Sheet:**
- Tab 1: "Lesson 1"
- Tab 2: "Lesson 2"
- Tab 3: "Test"

### My URLs:

**Lesson 1:**
```
https://john-teacher.github.io/icelandic-lessons/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

**Lesson 2:**
```
https://john-teacher.github.io/icelandic-lessons/icelandic-verb-game-dynamic.html?lesson=Lesson 2
```

**Test:**
```
https://john-teacher.github.io/icelandic-lessons/icelandic-verb-game-dynamic.html?lesson=Test
```

### My LearnWorlds Embed (for Lesson 1):

```html
<iframe 
    src="https://john-teacher.github.io/icelandic-lessons/icelandic-verb-game-dynamic.html?lesson=Lesson 1"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

---

## 🔍 Verify Your Setup

### Checklist Before Testing:

**GitHub:**
- [ ] File uploaded: `icelandic-verb-game-dynamic.html`
- [ ] Pages enabled in Settings
- [ ] Got Base URL from GitHub Pages

**Google Sheet:**
- [ ] Sheet ID: `1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes`
- [ ] Tabs created with names
- [ ] Shared publicly ("Anyone with link")
- [ ] Structure matches template (rows 1-3 config, row 5+ verbs)

**URL:**
- [ ] Base URL + file name + ?lesson=Tab Name
- [ ] Tab name matches exactly (case-sensitive)
- [ ] Tested in browser directly

---

## 🆘 Still Having Issues?

### Can't find GitHub Pages URL?

**Go to:**
```
https://github.com/YOUR-USERNAME/YOUR-REPO/settings/pages
```

**Look for the green box that says:**
```
✅ Your site is live at: https://...
```

### Sheet loading error?

**Test your sheet access:**
1. Open incognito/private window
2. Go to: `https://docs.google.com/spreadsheets/d/1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes/edit`
3. Can you view without logging in?
   - ✅ Yes → Sheet is public
   - ❌ No → Need to change sharing settings

### URL not working?

**Double check:**
1. Is file name spelled correctly?
   - `icelandic-verb-game-dynamic.html` (not `game.html`)
2. Is tab name spelled exactly as in sheet?
   - Case-sensitive: `Lesson 1` ≠ `lesson 1`
3. Did you include the `?` before lesson?
   - ✅ `?lesson=Lesson 1`
   - ❌ `lesson=Lesson 1`

---

## 💾 Save Your URL Template

Write this down for easy reference:

```
MY BASE URL:
_________________________________________________

MY URL PATTERN:
[Base URL]/icelandic-verb-game-dynamic.html?lesson=[Tab Name]

LESSON 1 URL:
_________________________________________________

LESSON 2 URL:
_________________________________________________

LESSON 3 URL:
_________________________________________________
```

---

## 🎓 Summary

**The URL has 3 parts:**

1. **Base URL** (from GitHub Pages)
2. **File name** (`icelandic-verb-game-dynamic.html`)
3. **Lesson parameter** (`?lesson=Your Tab Name`)

**Put them together:**
```
Base + File + ?lesson=Tab
```

**Example:**
```
https://user.github.io/repo/ + icelandic-verb-game-dynamic.html + ?lesson=Lesson 1
= 
https://user.github.io/repo/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

---

## ✨ You're Done!

Once you have your URL working:
- ✅ You can create unlimited lessons (just add tabs)
- ✅ Updates happen instantly (edit sheet, refresh browser)
- ✅ Same URL format for all lessons (just change tab name)
- ✅ Easy to share with students or embed in LearnWorlds

🇮🇸 **Happy teaching!**
