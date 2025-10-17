# 📊 Google Sheets Setup Guide

## Complete Guide: Single HTML File + Google Sheets = Multiple Lessons

---

## 🎯 Overview

**You now have:** `icelandic-verb-game-dynamic.html`

**This single file can load ANY lesson from your Google Sheet using URL parameters!**

---

## 📋 Step 1: Set Up Your Google Sheet

### Your Sheet ID
```
1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes
```

### Create Tabs for Each Lesson

Create separate tabs with these names:
- `Lesson 1`
- `Lesson 2`
- `Lesson 3`
- `Advanced`
- etc.

**Important:** Tab names are case-sensitive and must match URL parameters exactly.

---

## 📝 Step 2: Structure Each Tab

### Format for Each Tab:

| Column A | Column B | Column C | Column D | Column E | Column F | Column G | Column H |
|----------|----------|----------|----------|----------|----------|----------|----------|
| **LESSON_TITLE** | Lesson 1: Basic Verbs - Nútíð | | | | | | |
| **LESSON_SUBTITLE** | Practice present tense conjugations | | | | | | |
| **SHOW_TENSES** | no | | | | | | |
| | | | | | | | |
| **Verb** | **Tense** | **ég** | **þú** | **hann/hún/það** | **við** | **þið** | **þeir/þær/þau** |
| drekka | present | drekk | drekkur | drekkur | drekkum | drekkið | drekka |
| drekka | past | drakk | drakkst | drakk | drukkum | drukkuð | drukku |
| borða | present | borða | borðar | borðar | borðum | borðið | borða |
| borða | past | borðaði | borðaðir | borðaði | borðuðum | borðuðuð | borðuðu |

### Configuration Rules:

**Row 1 (LESSON_TITLE):**
- Column A: `LESSON_TITLE`
- Column B: Your lesson title

**Row 2 (LESSON_SUBTITLE):**
- Column A: `LESSON_SUBTITLE`
- Column B: Your subtitle text

**Row 3 (SHOW_TENSES):**
- Column A: `SHOW_TENSES`
- Column B: `yes` (show both tenses) or `no` (Nútíð only)

**Row 5+ (Verb Data):**
- Column A: Verb infinitive (e.g., `drekka`)
- Column B: Tense (`present` or `past`)
- Columns C-H: Conjugations for each person

---

## 🔗 Step 3: Make Sheet Accessible

### Required Settings:

1. **Click "Share" button** (top right)
2. **Change to:** "Anyone with the link"
3. **Permission:** Viewer
4. **Click "Done"**

### Verify Access:
Open this URL in incognito mode to test:
```
https://docs.google.com/spreadsheets/d/1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes/edit
```

If you can view it without logging in, it's configured correctly!

---

## 🌐 Step 4: Upload to GitHub

### Upload Single File:
1. Create GitHub repository (or use existing)
2. Upload `icelandic-verb-game-dynamic.html`
3. Enable GitHub Pages:
   - Settings → Pages
   - Branch: `main`
   - Folder: `/ (root)`
   - Save

### Your Base URL:
```
https://USERNAME.github.io/REPO-NAME/icelandic-verb-game-dynamic.html
```

---

## 🎓 Step 5: Create Lesson URLs

### URL Format:
```
https://USERNAME.github.io/REPO-NAME/icelandic-verb-game-dynamic.html?lesson=TAB_NAME
```

### Examples:

**Lesson 1:**
```
?lesson=Lesson 1
```

**Lesson 2:**
```
?lesson=Lesson 2
```

**Advanced Lesson:**
```
?lesson=Advanced
```

### Full URL Examples:
```
https://yourusername.github.io/icelandic-verbs/icelandic-verb-game-dynamic.html?lesson=Lesson 1
https://yourusername.github.io/icelandic-verbs/icelandic-verb-game-dynamic.html?lesson=Lesson 2
https://yourusername.github.io/icelandic-verbs/icelandic-verb-game-dynamic.html?lesson=Advanced
```

---

## 🎯 Step 6: Embed in LearnWorlds

### For Each Lesson:

1. Add **HTML block** in LearnWorlds
2. Insert iframe code:

```html
<iframe 
    src="https://USERNAME.github.io/REPO-NAME/icelandic-verb-game-dynamic.html?lesson=Lesson 1"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

### Different Lessons = Different URLs:

**Lesson 1 iframe:**
```html
<iframe src="...?lesson=Lesson 1" ...></iframe>
```

**Lesson 2 iframe:**
```html
<iframe src="...?lesson=Lesson 2" ...></iframe>
```

---

## 📊 Example: Creating 3 Lessons

### In Google Sheets:

**Create 3 tabs:**

#### Tab: "Lesson 1"
```
LESSON_TITLE       | Lesson 1: Basic Verbs - Nútíð
LESSON_SUBTITLE    | Practice present tense
SHOW_TENSES        | no

Verb      | Tense   | ég    | þú      | hann/hún/það | við      | þið     | þeir/þær/þau
drekka    | present | drekk | drekkur | drekkur      | drekkum  | drekkið | drekka
borða     | present | borða | borðar  | borðar       | borðum   | borðið  | borða
```

#### Tab: "Lesson 2"
```
LESSON_TITLE       | Lesson 2: Both Tenses
LESSON_SUBTITLE    | Practice present and past
SHOW_TENSES        | yes

Verb      | Tense   | ég    | þú      | hann/hún/það | við      | þið     | þeir/þær/þau
drekka    | present | drekk | drekkur | drekkur      | drekkum  | drekkið | drekka
drekka    | past    | drakk | drakkst | drakk        | drukkum  | drukkuð | drukku
fara      | present | fer   | ferð    | fer          | förum    | farið   | fara
fara      | past    | fór   | fórst   | fór          | fórum    | fóruð   | fóru
```

#### Tab: "Advanced"
```
LESSON_TITLE       | Advanced: Irregular Verbs
LESSON_SUBTITLE    | Challenge yourself
SHOW_TENSES        | yes

[Add your advanced verbs here]
```

### In LearnWorlds:

**Module 1:**
- Lesson 1.1: Embed with `?lesson=Lesson 1`

**Module 2:**
- Lesson 2.1: Embed with `?lesson=Lesson 2`

**Module 3:**
- Lesson 3.1: Embed with `?lesson=Advanced`

---

## ✅ Benefits of This System

### For You:
- ✅ **No code editing** - Manage everything in Google Sheets
- ✅ **Instant updates** - Changes reflect immediately
- ✅ **Easy collaboration** - Multiple people can edit sheets
- ✅ **Version history** - Google Sheets tracks all changes
- ✅ **Single file** - Only one HTML file to maintain

### For Students:
- ✅ Consistent interface across all lessons
- ✅ Reliable auto-resize in LearnWorlds
- ✅ Same familiar game mechanics
- ✅ Fast loading from GitHub

---

## 🔧 Making Changes

### To Update a Lesson:
1. Open Google Sheet
2. Go to the tab (e.g., "Lesson 1")
3. Edit verbs, conjugations, or settings
4. Save (automatic in Google Sheets)
5. Refresh the lesson page in LearnWorlds
6. Changes appear immediately!

### To Add a New Lesson:
1. Duplicate an existing tab
2. Rename it (e.g., "Lesson 4")
3. Update title, subtitle, and verbs
4. Use `?lesson=Lesson 4` in iframe URL

### To Add a New Verb to Existing Lesson:
1. Go to the lesson tab
2. Add new rows:
   - Row with `present` tense conjugations
   - Row with `past` tense conjugations (if SHOW_TENSES = yes)
3. Fill in all conjugations
4. Done! Verb appears in dropdown automatically

---

## 🆘 Troubleshooting

### Problem: "Failed to load lesson"
**Solutions:**
1. Check Google Sheet sharing is set to "Anyone with link"
2. Verify tab name matches URL parameter exactly (case-sensitive)
3. Ensure sheet structure follows the format above

### Problem: Tense dropdown not hiding
**Solution:** In Google Sheet, set `SHOW_TENSES` to `no` (lowercase)

### Problem: Verb not appearing
**Solution:** 
1. Check verb name is in Column A
2. Verify tense is `present` or `past` (lowercase)
3. Ensure all conjugation columns (C-H) are filled

### Problem: Wrong conjugations showing
**Solution:** Double-check column order matches:
- C = ég
- D = þú  
- E = hann/hún/það
- F = við
- G = þið
- H = þeir/þær/þau

---

## 📋 Quick Reference

### Sheet Structure:
```
Row 1: LESSON_TITLE | Your Title
Row 2: LESSON_SUBTITLE | Your Subtitle  
Row 3: SHOW_TENSES | yes or no
Row 4: [Empty]
Row 5: Headers | Verb | Tense | ég | þú | hann/hún/það | við | þið | þeir/þær/þau
Row 6+: Verb data
```

### URL Format:
```
base-url.html?lesson=TAB_NAME
```

### Embed Code:
```html
<iframe src="YOUR_URL?lesson=TAB_NAME" width="100%" height="900" frameborder="0"></iframe>
```

---

## 🎉 You're Ready!

1. ✅ Structure your Google Sheet with tabs
2. ✅ Make sheet publicly viewable
3. ✅ Upload HTML file to GitHub
4. ✅ Create lesson-specific URLs with `?lesson=` parameter
5. ✅ Embed in LearnWorlds with iframe

**No more managing multiple HTML files!** 🎊

---

## 💡 Pro Tips

### Tip 1: Organize Tabs by Module
```
Module-1-Lesson-1
Module-1-Lesson-2
Module-2-Lesson-1
Module-2-Lesson-2
```

### Tip 2: Use Descriptive Tab Names
```
Beginner-Present
Intermediate-Both-Tenses
Advanced-Irregular
```

### Tip 3: Test in Browser First
Before embedding, test directly:
```
your-github-url.html?lesson=Your Tab Name
```

### Tip 4: Keep a Master Template Tab
Create a template tab with the structure, then duplicate for new lessons.

---

## 📞 Support

**File Location:** `/app/frontend/public/icelandic-verb-game-dynamic.html`

**See Also:**
- `GOOGLE_SHEET_STRUCTURE.md` - Detailed structure guide
- `LEARNWORLDS_SETUP_GUIDE.md` - Original setup documentation

Happy teaching! 🇮🇸
