# 🚀 Noun Declension Game - Setup Guide

## What You Have Now

**New File Created:** `icelandic-noun-game-dynamic.html`

**Location:** `/app/frontend/public/icelandic-noun-game-dynamic.html`

**Google Sheet:** `1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8`

---

## 🎯 How It Works

### Game Features:
- ✅ Two side-by-side tables (án greinis & með greini)
- ✅ All 4 cases with Icelandic + English labels
- ✅ Singular & Plural forms
- ✅ Fill in the Blank mode
- ✅ Drag & Drop mode
- ✅ Auto-resize for LearnWorlds
- ✅ Google Sheets powered (easy updates)

### Display Structure:
```
┌─────────────────────────────────────────────────┐
│  Án greinis            │   Með greini          │
│  (Without Article)     │   (With Article)      │
├────────────────────────┼───────────────────────┤
│  4 cases × 2 numbers   │   4 cases × 2 numbers │
│  = 8 forms             │   = 8 forms           │
│                        │                       │
│  Total: 16 forms per noun                      │
└─────────────────────────────────────────────────┘
```

---

## 📝 Setup Steps

### Step 1: Prepare Your Google Sheet

1. **Open your sheet:**
   ```
   https://docs.google.com/spreadsheets/d/1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8/edit
   ```

2. **Create tabs for lessons:**
   - Tab 1: "Lesson 1"
   - Tab 2: "Lesson 2"
   - etc.

3. **Structure each tab:**
   ```
   Row 1: LESSON_TITLE | Your lesson title
   Row 2: LESSON_SUBTITLE | Your subtitle
   Row 3: (empty)
   Row 4: (empty)
   Row 5: Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.
   Row 6+: [Your noun data - 4 rows per noun]
   ```

4. **Share publicly:**
   - Click "Share"
   - "Anyone with the link"
   - Role: Viewer

**See `NOUN_SHEET_STRUCTURE.md` for complete details and examples.**

---

### Step 2: Upload to GitHub

1. **Download the file:**
   - Location: `/app/frontend/public/icelandic-noun-game-dynamic.html`
   - Save to your computer

2. **Upload to GitHub:**
   - Go to your repository: `https://github.com/chrisayliffe/verb-practice-game`
   - Click "Add file" → "Upload files"
   - Drag the noun game file
   - Commit changes

3. **GitHub Pages should already be enabled** (from verb game setup)

---

### Step 3: Create Your URLs

**Pattern:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-noun-game-dynamic.html?lesson=TAB_NAME
```

**Examples:**
```
Lesson 1:
https://chrisayliffe.github.io/verb-practice-game/icelandic-noun-game-dynamic.html?lesson=Lesson 1

Lesson 2:
https://chrisayliffe.github.io/verb-practice-game/icelandic-noun-game-dynamic.html?lesson=Lesson 2
```

---

### Step 4: Test Your Setup

1. **Test URL in browser**
2. **Check:**
   - ✅ Loads lesson title from sheet
   - ✅ Noun dropdown populated
   - ✅ Two tables display side-by-side
   - ✅ Case labels show Icelandic + English
   - ✅ Fill mode works
   - ✅ Drag mode works

---

### Step 5: Embed in LearnWorlds

```html
<iframe 
    src="https://chrisayliffe.github.io/verb-practice-game/icelandic-noun-game-dynamic.html?lesson=Lesson 1"
    width="100%"
    height="950"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

*Note: Height is 950px (slightly taller than verb game) to accommodate two tables.*

---

## 📋 Google Sheet Example

### Complete Example for "hestur":

| Noun | Article | Number | Nf. | Þf. | Þgf. | Ef. |
|------|---------|--------|-----|-----|------|-----|
| hestur | no_article | singular | hestur | hest | hesti | hests |
| hestur | no_article | plural | hestar | hesta | hestum | hesta |
| hestur | with_article | singular | hesturinn | hestinn | hestinum | hestsins |
| hestur | with_article | plural | hestarnir | hestana | hestunum | hestanna |

**Key Points:**
- Each noun needs exactly 4 rows
- Article must be: `no_article` or `with_article`
- Number must be: `singular` or `plural`
- All 4 case forms required

---

## 🎨 Design Matching

The noun game uses the **exact same design** as the verb game:

- ✅ Same font (Outfit)
- ✅ Same colors (#121212, #21b766, #f15d4e)
- ✅ Same layout style
- ✅ Same game mechanics
- ✅ Same responsive behavior
- ✅ Same LearnWorlds integration

**Students will have a consistent experience across both tools!**

---

## 📊 Comparison: Verb vs Noun Games

### Verb Game:
- Practice verb conjugations
- 6 forms per verb (3 persons × 2 numbers)
- One table layout
- Optional tense selector

### Noun Game:
- Practice noun declensions
- 16 forms per noun (4 cases × 2 numbers × 2 articles)
- Two tables side-by-side
- No tense selector (just current forms)

---

## 🔧 Customization

### Change Title/Subtitle:
Edit rows 1-2 in your Google Sheet

### Add More Nouns:
Add 4 rows per noun in your sheet

### Create New Lessons:
Add new tabs to your Google Sheet

### Change Colors:
Edit CSS in HTML file (same process as verb game)

---

## 📁 File Locations

**Noun Game:**
```
/app/frontend/public/icelandic-noun-game-dynamic.html
```

**Verb Game:**
```
/app/frontend/public/icelandic-verb-game-dynamic.html
```

**Both use similar Google Sheets structure - just different data!**

---

## ✅ Quick Checklist

Before going live:

- [ ] Google Sheet structure correct
- [ ] Sheet ID in HTML matches yours
- [ ] Sheet shared publicly
- [ ] Tab names created
- [ ] At least one noun with all 4 rows
- [ ] File uploaded to GitHub
- [ ] Tested URL in browser
- [ ] Two tables display correctly
- [ ] Embedded in LearnWorlds

---

## 🆘 Common Issues

### Issue: Only one table showing

**Cause:** Missing data for with_article or no_article

**Fix:** Ensure each noun has all 4 rows (2 for no_article + 2 for with_article)

### Issue: Wrong case labels

**Cause:** Column order incorrect

**Fix:** Columns must be: Noun | Article | Number | Nf | Þf | Þgf | Ef

### Issue: Forms not matching

**Cause:** Article or Number values incorrect

**Fix:** Must be exactly `no_article`, `with_article`, `singular`, `plural`

---

## 📚 Documentation Files

1. **NOUN_GAME_SETUP.md** (this file) - Overview & setup
2. **NOUN_SHEET_STRUCTURE.md** - Detailed sheet structure with examples
3. **COMPLETE_SETUP_FROM_SCRATCH.md** - GitHub setup (from verb game)
4. **URL_GUIDE.md** - URL creation (same process as verb game)

---

## 🎉 You Now Have Two Tools!

### Verb Conjugation Game
```
https://...../icelandic-verb-game-dynamic.html?lesson=X
```

### Noun Declension Game
```
https://...../icelandic-noun-game-dynamic.html?lesson=X
```

**Same style, same ease of use, powered by Google Sheets!** 🇮🇸

---

## 💡 Pro Tips

### Tip 1: Test with One Noun First
Create one complete noun entry, test it, then add more.

### Tip 2: Copy from BÍN
Get accurate declensions from: https://bin.arnastofnun.is/

### Tip 3: Use Consistent Tab Names
Keep naming consistent: "Lesson 1", "Lesson 2", etc.

### Tip 4: Organize by Difficulty
- Lesson 1: Regular nouns
- Lesson 2: Irregular nouns
- Lesson 3: Mixed practice

---

## 📞 Next Steps

1. ✅ Structure your Google Sheet (see NOUN_SHEET_STRUCTURE.md)
2. ✅ Upload noun game HTML to GitHub
3. ✅ Test your URLs
4. ✅ Embed in LearnWorlds
5. ✅ Start teaching! 🎓
