# 🔗 URL Guide - How to Identify Your Exercise URLs

## 📍 Understanding the URL Structure

Your exercise URL has **3 parts**:

```
[BASE URL] + [FILE NAME] + [LESSON PARAMETER]
```

### Example:
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Lesson 1
└─────────────────┬──────────────────┘└────────────┬──────────────┘└──────┬─────┘
         BASE URL                      FILE NAME           LESSON PARAMETER
```

---

## 🎯 Step-by-Step: Find Your URL

### **Step 1: Get Your GitHub Pages Base URL**

After uploading to GitHub and enabling Pages:

1. Go to your GitHub repository
2. Click **Settings** → **Pages**
3. You'll see: "Your site is published at:"

**Example URLs:**
```
https://johndoe.github.io/icelandic-verbs/
https://myschool.github.io/language-lessons/
```

This is your **BASE URL**.

---

### **Step 2: Add the File Name**

The file name is: `icelandic-verb-game-dynamic.html`

**Complete URL so far:**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html
```

---

### **Step 3: Add the Lesson Parameter**

The lesson parameter tells the file which Google Sheet tab to load.

**Format:**
```
?lesson=YOUR_TAB_NAME
```

**Important Rules:**
- Must match your Google Sheet tab name **exactly**
- Case-sensitive (Lesson 1 ≠ lesson 1)
- Spaces are OK (they'll be encoded automatically)
- Use %20 for spaces if manually typing: `Lesson%201`

---

## 📝 Examples Based on Tab Names

### If your tab is named: **"Lesson 1"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

### If your tab is named: **"Beginner-Present"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Beginner-Present
```

### If your tab is named: **"Module 1 - Basic Verbs"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Module 1 - Basic Verbs
```

### If your tab is named: **"Advanced"**
```
https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Advanced
```

---

## 🧪 How to Test Your URL

### **Method 1: Direct Browser Test**

1. Copy your complete URL
2. Open a new browser tab
3. Paste the URL
4. Press Enter

**What to look for:**
- ✅ Shows "Loading [Your Lesson Name]..." briefly
- ✅ Then loads the game with your verbs
- ❌ Shows error → Check sheet name or sharing settings

### **Method 2: Test with Different Tabs**

Try each tab:
```
?lesson=Lesson 1     → Should load first tab
?lesson=Lesson 2     → Should load second tab  
?lesson=Advanced     → Should load third tab
```

---

## 📋 Your URL Checklist

Use this checklist to build your URLs:

- [ ] **1. GitHub Pages enabled?**
  - Go to repo Settings → Pages
  - Branch set to `main`
  - Folder set to `/ (root)`

- [ ] **2. HTML file uploaded?**
  - File name: `icelandic-verb-game-dynamic.html`
  - Located in root of repository

- [ ] **3. Google Sheet accessible?**
  - Sheet ID: `1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes`
  - Sharing set to "Anyone with the link"

- [ ] **4. Tab name matches exactly?**
  - Check spelling
  - Check capitalization
  - Check spaces

---

## 🎓 LearnWorlds Embedding

Once you have your URL, embed it like this:

```html
<iframe 
    src="YOUR_COMPLETE_URL_HERE"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

### **Example for "Lesson 1" tab:**

```html
<iframe 
    src="https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html?lesson=Lesson 1"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

---

## 🔍 Real-World Example

### **Your Setup:**

**Google Sheet:**
- Sheet ID: `1TvQ8qTJ2IkaRbyJa3JNbjbLOM0peubS0VDNGupHwZes`
- Tab 1: "Lesson 1"
- Tab 2: "Lesson 2"  
- Tab 3: "Advanced Practice"

**GitHub:**
- Username: `icelandic-teacher`
- Repo: `verb-practice`
- File: `icelandic-verb-game-dynamic.html`

### **Your URLs Would Be:**

**Lesson 1:**
```
https://icelandic-teacher.github.io/verb-practice/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

**Lesson 2:**
```
https://icelandic-teacher.github.io/verb-practice/icelandic-verb-game-dynamic.html?lesson=Lesson 2
```

**Advanced:**
```
https://icelandic-teacher.github.io/verb-practice/icelandic-verb-game-dynamic.html?lesson=Advanced Practice
```

---

## 🆘 Troubleshooting

### ❌ "Failed to load lesson"

**Possible causes:**

1. **Sheet not public**
   - Fix: Share → "Anyone with link" → Viewer

2. **Wrong tab name**
   - Check: Tab name matches URL exactly
   - Fix: Copy tab name directly from Google Sheets

3. **Wrong sheet ID**
   - Check: Sheet ID in HTML file matches your sheet
   - Fix: Update line `const GOOGLE_SHEET_ID = 'YOUR_ID';`

4. **Sheet structure wrong**
   - Check: Rows 1-3 have config, Row 5+ have verbs
   - Fix: Follow SHEET_TEMPLATE.txt format

### ❌ Page shows "Loading..." forever

**Fix:** Make sure your Google Sheet is published/shared publicly

**Test:** Open your sheet in incognito mode - can you view it without logging in?

---

## 📱 URL Encoding Reference

If you need to manually encode spaces and special characters:

| Character | Encoded |
|-----------|---------|
| Space | %20 |
| - | - (no change) |
| _ | _ (no change) |

**Example:**
- Tab name: `Lesson 1`
- Encoded: `?lesson=Lesson%201`

**Note:** Modern browsers handle this automatically, so you can usually just type spaces normally!

---

## ✅ Quick Test Process

1. **Upload** HTML file to GitHub
2. **Enable** GitHub Pages
3. **Get** your base URL from GitHub Pages settings
4. **Build** URL: `base-url/file-name.html?lesson=Tab Name`
5. **Test** in browser directly
6. **Embed** in LearnWorlds if it works

---

## 💡 Pro Tips

### Tip 1: Keep Tab Names Simple
```
✅ Good: "Lesson 1", "Lesson 2", "Advanced"
❌ Avoid: "Lesson #1 (Module 3) - Part A"
```

### Tip 2: Use Consistent Naming
```
Lesson 1
Lesson 2  
Lesson 3
```
or
```
Module-1-Lesson-1
Module-1-Lesson-2
Module-2-Lesson-1
```

### Tip 3: Test Before Embedding
Always test the URL directly in your browser before adding to LearnWorlds.

### Tip 4: Bookmark Base URL
Save your base URL in a note:
```
Base: https://yourusername.github.io/your-repo/icelandic-verb-game-dynamic.html

Lesson 1: ?lesson=Lesson 1
Lesson 2: ?lesson=Lesson 2
Advanced: ?lesson=Advanced
```

---

## 📞 Need Help?

**Can't find your GitHub Pages URL?**
1. Go to your repo on GitHub
2. Click Settings (top right)
3. Scroll down to "Pages" in left sidebar
4. Your URL is displayed at the top

**Still stuck?**
Check these files:
- `GOOGLE_SHEETS_SETUP.md` - Complete setup guide
- `SHEET_TEMPLATE.txt` - Google Sheet format
- `LEARNWORLDS_SETUP_GUIDE.md` - LearnWorlds embedding

---

## 🎉 You're Ready!

Once you have your URL format figured out, you can:
- Create as many lessons as you want (just add tabs)
- Update content without touching code
- Share direct links with students
- Embed seamlessly in LearnWorlds

**Formula:**
```
GitHub Pages URL + /icelandic-verb-game-dynamic.html + ?lesson=Tab Name
```

That's it! 🇮🇸
