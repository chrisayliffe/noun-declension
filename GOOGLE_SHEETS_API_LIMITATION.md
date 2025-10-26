# ⚠️ IMPORTANT: Google Sheets API Limitation

## The Problem

**Google Sheets visualization API skips the LESSON_TITLE and LESSON_SUBTITLE rows.**

Even though you have these rows in your sheet, Google's API filters them out before sending the data to the game. This is a known limitation of the `gviz` API.

## What This Means

- Your game will always show the default titles:
  - Title: "Icelandic Noun Declension Practice"
  - Subtitle: "Practice noun declensions"
  
- **However**, all other features work perfectly:
  - ✅ SHOW_PLURAL configuration works
  - ✅ VISIBLE_CASES configuration works  
  - ✅ All noun data loads correctly
  - ✅ Multiple lessons work

## Workaround Options

### Option 1: Accept Default Titles (Recommended)
Just use the default titles. They're descriptive enough for most use cases.

### Option 2: Edit the HTML File
If you need custom titles for each lesson, you can:

1. Open the HTML file
2. Find line 530-531:
   ```javascript
   let title = 'Icelandic Noun Declension Practice';
   let subtitle = 'Practice noun declensions';
   ```
3. Change to:
   ```javascript
   const lessonName = getLessonFromURL();
   let title = lessonName; // Uses URL parameter as title
   let subtitle = 'Practice noun declensions';
   ```

This way "Lesson 1" becomes the title, "Lesson 2" becomes the title, etc.

### Option 3: Use Different Google Sheets Method
Switch from `gviz` API to Google Sheets API v4 (requires API key setup - more complex).

## Bottom Line

**Keep the LESSON_TITLE and LESSON_SUBTITLE rows in your sheet** - they document the structure even though the API ignores them. Everything else works perfectly!

Your current structure is correct:
```
Row 1: LESSON_TITLE | Your Title (ignored by API, but good for documentation)
Row 2: LESSON_SUBTITLE | Your Subtitle (ignored by API, but good for documentation)
Row 3: SHOW_PLURAL | true | VISIBLE_CASES | Nf,Þf,Þgf,Ef ← THIS WORKS
Row 4: (empty)
Row 5: Noun | Article | ...
Row 6+: Your data ← THIS WORKS
```
