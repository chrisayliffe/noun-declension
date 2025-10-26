# ✅ Fixes Applied to Noun Declension Game

## Issues Fixed:

### 1. ❌ Empty Tiles in Drag & Drop
**Problem:** Empty tiles showing in the drag & drop interface
**Fix:** Updated `createDragTables()` function to filter out empty/null values before creating tiles

```javascript
if (form && form.trim()) { // Only add non-empty forms
    allForms.push(form);
}
```

### 2. ❌ "undefined" Appearing in Cells  
**Problem:** Cells showing "undefined" instead of being empty
**Fix:** 
- Corrected row index from 4 to 5 (data starts at row 6, index 5)
- Added null-safe access operators (`?.`) 
- Added explicit checks before adding data

```javascript
const nf = row.c[3]?.v;
if (nf || þf || þgf || ef) { // Only add if values exist
    nouns[noun][article][number] = { ... };
}
```

### 3. ✅ NEW FEATURE: Hide/Show Plural Columns
**Configuration:** Add to Row 3, Column B of your Google Sheet

```
Row 3: SHOW_PLURAL | true | VISIBLE_CASES | Nf,Þf,Þgf,Ef
```

**Usage:**
- Set to `true` (default) = Show both Singular AND Plural columns
- Set to `false` = Show ONLY Singular column

**Perfect for:**
- Beginners: Start with singular only (`false`)
- Advanced students: Show both (`true`)

### 4. ✅ NEW FEATURE: Hide/Show Specific Cases
**Configuration:** Add to Row 3, Column D of your Google Sheet

```
VISIBLE_CASES | Nf,Þf,Þgf,Ef
```

**Examples:**
- `Nf,Þf` = Show only Nominative and Accusative
- `Nf` = Show only Nominative (great for absolute beginners)
- `Nf,Þgf,Ef` = Hide Accusative case
- `Nf,Þf,Þgf,Ef` = Show all cases (default)

**Perfect for:**
- Progressive learning: Introduce one case at a time
- Focused practice: Practice specific cases
- Lesson customization: Different difficulty levels

### 5. ✅ Reduced Spacing for LearnWorlds
**Changes:**
- Container padding: 16px → 12px
- Heading size: 2rem → 1.75rem  
- Table padding: 10px → 8px
- Tile padding: 8px → 6px
- Margins reduced across all elements
- Drag tiles height: 90-180px → 70-150px

**Result:** More compact layout, less scrolling in iframe

---

## Updated Google Sheet Structure

### Required Format:

```
Row 1: LESSON_TITLE      | Your Title
Row 2: LESSON_SUBTITLE   | Your Subtitle  
Row 3: SHOW_PLURAL       | true/false | VISIBLE_CASES | Nf,Þf,Þgf,Ef
Row 4: (empty)
Row 5: Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.
Row 6+: Your noun data
```

### Example with Configuration:

```
Row 1: LESSON_TITLE      | Lesson 1: Basic Nouns - Demo
Row 2: LESSON_SUBTITLE   | Practice noun declensions
Row 3: SHOW_PLURAL       | true | VISIBLE_CASES | Nf,Þf
Row 4: (empty)
Row 5: Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.
Row 6: hestur | no_article | singular | hestur | hest | hesti | hests
...
```

This will show ONLY Nominative (Nf) and Accusative (Þf) cases, with both singular and plural.

---

## Configuration Examples

### Example 1: Absolute Beginners
**Goal:** Only singular, only nominative case

```
SHOW_PLURAL: false
VISIBLE_CASES: Nf
```

Result: Single column table with only nominative forms

### Example 2: Intermediate
**Goal:** Both singular/plural, but only Nom/Acc cases

```
SHOW_PLURAL: true
VISIBLE_CASES: Nf,Þf
```

Result: 2 columns (Sing/Plural), 2 rows (Nom/Acc)

### Example 3: Advanced (Default)
**Goal:** Full practice

```
SHOW_PLURAL: true
VISIBLE_CASES: Nf,Þf,Þgf,Ef
```

Result: 2 columns (Sing/Plural), 4 rows (all cases)

---

## What Didn't Change

✅ Still works with Google Sheets  
✅ Still supports multiple lessons via URL parameters  
✅ Still has Fill in the Blank + Drag & Drop modes  
✅ Still auto-resizes for LearnWorlds iframes  
✅ Still responsive for mobile/tablet  

---

## Next Steps

1. **Update Your Google Sheet:**
   - Open: https://docs.google.com/spreadsheets/d/1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8/edit
   - Replace Row 3 with: `SHOW_PLURAL | true | VISIBLE_CASES | Nf,Þf,Þgf,Ef`
   - See updated template in `GOOGLE_SHEET_TEMPLATE.txt`

2. **Upload Updated File to GitHub:**
   - Replace `icelandic-noun-game-dynamic.html` in your repository
   - Wait 1-2 minutes for GitHub Pages to update

3. **Test Your URL:**
   ```
   https://chrisayliffe.github.io/noun-declension/frontend/public/icelandic-noun-game-dynamic.html?lesson=Lesson 1
   ```

4. **Try Different Configurations:**
   - Create "Lesson 2" tab with `SHOW_PLURAL: false`
   - Create "Lesson 3" tab with `VISIBLE_CASES: Nf,Þf`
   - Test different URLs: `?lesson=Lesson 2`, `?lesson=Lesson 3`

---

## Files Updated

1. `/app/frontend/public/icelandic-noun-game-dynamic.html` - Main game file
2. `/app/NOUN_SHEET_STRUCTURE.md` - Updated documentation
3. `/app/GOOGLE_SHEET_TEMPLATE.txt` - Updated template with config options

---

## Testing Checklist

- [ ] No empty tiles in Drag & Drop
- [ ] No "undefined" text in cells
- [ ] Setting SHOW_PLURAL to false hides plural column
- [ ] Setting VISIBLE_CASES to "Nf,Þf" shows only 2 cases
- [ ] Layout fits in LearnWorlds without excessive scrolling
- [ ] Both game modes work correctly
- [ ] All buttons function properly

---

**All fixes applied! Ready to upload to GitHub and test!** 🎉
