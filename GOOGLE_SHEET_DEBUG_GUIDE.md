# 🔍 Debugging Google Sheet Structure

## Issue: Title/Subtitle Not Showing Correctly

If your game is showing the wrong title/subtitle or no cases are appearing, follow this debug guide.

---

## ✅ EXACT Google Sheet Structure Required

Your sheet must look EXACTLY like this (spaces and empty rows matter!):

```
ROW 1:  | A: LESSON_TITLE      | B: Lesson 1: Basic Nouns - Demo | C: (empty) | D: (empty) |
ROW 2:  | A: LESSON_SUBTITLE   | B: Practice noun declensions    | C: (empty) | D: (empty) |
ROW 3:  | A: SHOW_PLURAL       | B: true                          | C: VISIBLE_CASES | D: Nf,Þf,Þgf,Ef |
ROW 4:  | A: (empty)           | B: (empty)                       | C: (empty) | D: (empty) |
ROW 5:  | A: Noun              | B: Article                       | C: Number  | D: Nf. | E: Þf. | F: Þgf. | G: Ef. |
ROW 6:  | A: hestur            | B: no_article                    | C: singular | D: hestur | E: hest | F: hesti | G: hests |
ROW 7:  | A: hestur            | B: no_article                    | C: plural   | D: hestar | E: hesta | F: hestum | G: hesta |
...
```

---

## 🔧 Step-by-Step Fix

### Step 1: Verify Your Sheet Structure

1. Open your sheet: https://docs.google.com/spreadsheets/d/1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8/edit

2. Check each row carefully:
   - **Row 1, Column A** should contain exactly: `LESSON_TITLE`
   - **Row 1, Column B** should contain your lesson title
   - **Row 2, Column A** should contain exactly: `LESSON_SUBTITLE`  
   - **Row 2, Column B** should contain your subtitle
   - **Row 3, Column A** should contain exactly: `SHOW_PLURAL`
   - **Row 3, Column B** should contain: `true` or `false`
   - **Row 3, Column C** should contain exactly: `VISIBLE_CASES`
   - **Row 3, Column D** should contain: `Nf,Þf,Þgf,Ef` (or subset)
   - **Row 4** should be completely empty
   - **Row 5** should have headers starting with: `Noun`, `Article`, `Number`...

### Step 2: Use Developer Console

1. Open your game URL in browser
2. Press F12 (or right-click → Inspect)
3. Click "Console" tab
4. Refresh the page
5. Look for console log messages showing:
   ```
   Total rows: X
   First 6 rows: [...]
   Parsed data: { title: "...", subtitle: "...", ... }
   ```

6. Check if the data matches your sheet

### Step 3: Common Issues

**Issue:** Title showing as "TRUE" or "Article"
- **Cause:** Rows are misaligned or empty row 4 is missing
- **Fix:** Make sure Row 4 is completely empty

**Issue:** No cases showing in tables
- **Cause:** `VISIBLE_CASES` value is incorrect
- **Fix:** Make sure Row 3, Column D contains: `Nf,Þf,Þgf,Ef`
- **Fix:** Check for extra spaces: should be `Nf,Þf,Þgf,Ef` NOT `Nf, Þf, Þgf, Ef`

**Issue:** Only singular showing (no plural column)
- **Cause:** `SHOW_PLURAL` set to false
- **Fix:** Change Row 3, Column B to: `true`

**Issue:** Drag & Drop mode shows no tiles
- **Cause:** Data not loading correctly or VISIBLE_CASES mismatch
- **Fix:** Check console logs, verify noun data is being parsed

---

## 📋 Copy-Paste Template (Tab-Separated)

Copy this ENTIRE block and paste into cell A1 of your sheet:

```
LESSON_TITLE	Lesson 1: Basic Nouns - Demo			
LESSON_SUBTITLE	Practice noun declensions in all cases			
SHOW_PLURAL	true	VISIBLE_CASES	Nf,Þf,Þgf,Ef
				
Noun	Article	Number	Nf.	Þf.	Þgf.	Ef.
hestur	no_article	singular	hestur	hest	hesti	hests
hestur	no_article	plural	hestar	hesta	hestum	hesta
hestur	with_article	singular	hesturinn	hestinn	hestinum	hestsins
hestur	with_article	plural	hestarnir	hestana	hestunum	hestanna
kona	no_article	singular	kona	konu	konu	konu
kona	no_article	plural	konur	konur	konum	kvenna
kona	with_article	singular	konan	konuna	konunni	konunnar
kona	with_article	plural	konurnar	konurnar	konunum	kvennanna
```

**Important:** The spaces between columns are TAB characters, not regular spaces!

---

## 🧪 Test with Simple Data First

If still having issues, try this minimal test:

1. **Delete everything** in your sheet
2. **Paste this minimal version:**

```
LESSON_TITLE	Test Lesson			
LESSON_SUBTITLE	Testing			
SHOW_PLURAL	true	VISIBLE_CASES	Nf
				
Noun	Article	Number	Nf.	Þf.	Þgf.	Ef.
hestur	no_article	singular	hestur			
hestur	no_article	plural	hestar			
hestur	with_article	singular	hesturinn			
hestur	with_article	plural	hestarnir			
```

3. This should show:
   - Title: "Test Lesson"
   - Subtitle: "Testing"
   - Only 1 case (Nominative)
   - Only 1 noun (hestur)

4. If this works, gradually add more cases and nouns

---

## 📞 Still Not Working?

Share:
1. Screenshot of your Google Sheet (showing rows 1-10)
2. Screenshot of browser Console (F12 → Console tab)
3. The exact URL you're using

This will help identify the exact issue!
