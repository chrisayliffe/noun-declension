# 🚀 Deployment Guide for Icelandic Noun Declension Game

## 📦 What You Need to Deploy

You need to upload **ONE file** to GitHub (or any web hosting):
- `icelandic-noun-game-dynamic.html`

This file is located at: `/app/frontend/public/icelandic-noun-game-dynamic.html`

---

## 🔧 Step 1: Set Up Your Google Sheet

### A. Sheet Structure

Your sheet ID: `1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8`

**Open your sheet:** https://docs.google.com/spreadsheets/d/1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8/edit

### B. Add Data to "Lesson 1" Tab

Copy and paste this EXACT data into your "Lesson 1" tab:

**ROW 1:**
- Column A: `LESSON_TITLE`
- Column B: `Lesson 1: Basic Nouns - Demo`

**ROW 2:**
- Column A: `LESSON_SUBTITLE`
- Column B: `Practice noun declensions in all cases`

**ROW 3:** Leave completely empty

**ROW 4:** Leave completely empty

**ROW 5 (Headers):**
- Column A: `Noun`
- Column B: `Article`
- Column C: `Number`
- Column D: `Nf.`
- Column E: `Þf.`
- Column F: `Þgf.`
- Column G: `Ef.`

**ROW 6-9 (hestur - horse):**
```
Row 6: hestur    no_article    singular    hestur       hest       hesti      hests
Row 7: hestur    no_article    plural      hestar       hesta      hestum     hesta
Row 8: hestur    with_article  singular    hesturinn    hestinn    hestinum   hestsins
Row 9: hestur    with_article  plural      hestarnir    hestana    hestunum   hestanna
```

**ROW 10-13 (kona - woman):**
```
Row 10: kona    no_article    singular    kona        konu       konu       konu
Row 11: kona    no_article    plural      konur       konur      konum      kvenna
Row 12: kona    with_article  singular    konan       konuna     konunni    konunnar
Row 13: kona    with_article  plural      konurnar    konurnar   konunum    kvennanna
```

### C. Make Sheet Public

1. Click "Share" button (top right of Google Sheets)
2. Click "Change to anyone with the link"
3. Make sure access is set to "Viewer"
4. Click "Done"

---

## 📤 Step 2: Upload to GitHub

### Option A: GitHub Pages (Recommended)

1. **Create a new repository** (or use existing one)
2. **Upload the file:**
   - Go to your repository
   - Click "Add file" → "Upload files"
   - Upload `icelandic-noun-game-dynamic.html`
   - Commit the changes

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Scroll to "Pages"
   - Under "Source", select "main" branch
   - Click "Save"

4. **Your URL will be:**
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/icelandic-noun-game-dynamic.html?lesson=Lesson 1
   ```

### Option B: Other Web Hosting

Upload `icelandic-noun-game-dynamic.html` to any web server. The game will work from any URL.

---

## 🎮 Step 3: Test Your Deployment

### Test URL Format:
```
https://YOUR-DOMAIN/icelandic-noun-game-dynamic.html?lesson=Lesson 1
```

**Important:** The `?lesson=Lesson 1` parameter must match your Google Sheet tab name exactly!

### What You Should See:
- Title: "Lesson 1: Basic Nouns - Demo"
- Subtitle: "Practice noun declensions in all cases"
- Noun dropdown showing: hestur, kona
- Two tables: "Án greinis" and "Með greini"
- Two game modes: "Fill in the Blank" and "Drag & Drop"

---

## 📚 Step 4: Add More Lessons

### A. Create New Tabs

1. In your Google Sheet, create new tabs (e.g., "Lesson 2", "Animals", "Family")
2. Use the same structure as "Lesson 1"
3. Add different nouns

### B. Access Different Lessons

```
Lesson 1: ?lesson=Lesson 1
Lesson 2: ?lesson=Lesson 2
Animals:  ?lesson=Animals
Family:   ?lesson=Family
```

### C. Example: Adding "Animals" Lesson

**Create a new tab named "Animals"**

Then add data:
```
Row 1: LESSON_TITLE      | Lesson 2: Animals
Row 2: LESSON_SUBTITLE   | Learn animal declensions
Row 3: (empty)
Row 4: (empty)
Row 5: Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.
Row 6: hundur | no_article | singular | hundur | hund | hundi | hunds
Row 7: hundur | no_article | plural | hundar | hunda | hundum | hunda
Row 8: hundur | with_article | singular | hundurinn | hundinn | hundinum | hundsins
Row 9: hundur | with_article | plural | hundarnir | hundana | hundunum | hundanna
```

**Access URL:**
```
https://YOUR-DOMAIN/icelandic-noun-game-dynamic.html?lesson=Animals
```

---

## 🔗 Step 5: Embed in LearnWorlds

### A. Get Your Game URL

Example:
```
https://yourusername.github.io/icelandic-games/icelandic-noun-game-dynamic.html?lesson=Lesson 1
```

### B. Add to LearnWorlds

1. Go to your course in LearnWorlds
2. Add a new "Custom Code" section
3. Paste this code:

```html
<iframe 
  src="https://YOUR-GITHUB-URL/icelandic-noun-game-dynamic.html?lesson=Lesson 1"
  style="width: 100%; border: none; overflow: hidden;"
  scrolling="no"
  id="nounGameFrame"
></iframe>

<script>
  window.addEventListener('message', function(e) {
    if (e.data.type === 'IFRAME_HEIGHT') {
      document.getElementById('nounGameFrame').style.height = e.data.height + 'px';
    }
  });
</script>
```

4. **Replace** `YOUR-GITHUB-URL` with your actual URL
5. **Replace** `?lesson=Lesson 1` with the lesson you want

### C. Multiple Lessons in LearnWorlds

Create separate sections for each lesson:

**Section 1: Basic Nouns**
```html
<iframe src="https://YOUR-URL/icelandic-noun-game-dynamic.html?lesson=Lesson 1"...>
```

**Section 2: Animals**
```html
<iframe src="https://YOUR-URL/icelandic-noun-game-dynamic.html?lesson=Animals"...>
```

---

## 🆘 Troubleshooting

### Problem: "Failed to load lesson"

**Solutions:**
1. Check Google Sheet is shared publicly ("Anyone with the link")
2. Verify tab name matches exactly (case-sensitive)
3. Check Sheet ID in the HTML file (line 483)

### Problem: No nouns showing in dropdown

**Solutions:**
1. Verify sheet has data starting at row 6
2. Check column order: Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.
3. Verify article values are exactly: `no_article` or `with_article`
4. Verify number values are exactly: `singular` or `plural`

### Problem: Wrong declensions showing

**Solutions:**
1. Check that each noun has exactly 4 rows
2. Verify case order: Nf., Þf., Þgf., Ef. (columns D, E, F, G)
3. Make sure no empty cells in the declension data

### Problem: Game not resizing in LearnWorlds

**Solutions:**
1. Make sure you included the `<script>` code in the embed
2. Check iframe has `id="nounGameFrame"` attribute
3. Verify `scrolling="no"` is set on iframe

---

## 📝 Quick Reference

### Google Sheet Column Order:
```
A: Noun
B: Article (no_article or with_article)
C: Number (singular or plural)
D: Nf. (Nominative)
E: Þf. (Accusative)
F: Þgf. (Dative)
G: Ef. (Genitive)
```

### Each Noun Needs 4 Rows:
1. no_article + singular
2. no_article + plural
3. with_article + singular
4. with_article + plural

### URL Parameters:
```
?lesson=TAB_NAME
```
(Must match Google Sheet tab name exactly, including spaces and capitalization)

---

## ✅ Checklist Before Going Live

- [ ] Google Sheet has correct structure
- [ ] First tab ("Lesson 1") has sample data
- [ ] Sheet is shared publicly (Anyone with the link)
- [ ] HTML file uploaded to GitHub/web host
- [ ] Tested game URL in browser
- [ ] Noun dropdown shows nouns correctly
- [ ] Both tables display (with/without article)
- [ ] Both game modes work (Fill + Drag)
- [ ] Tested in LearnWorlds iframe (if using)

---

## 🎉 You're Done!

Your game is now live and ready for students to practice Icelandic noun declensions!

**Need help?** Check the detailed structure guide: `NOUN_SHEET_STRUCTURE.md`
