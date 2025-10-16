# LearnWorlds Setup Guide
## How to Create Multiple Lesson Versions & Embed in LearnWorlds

---

## 📋 Overview

This guide shows you how to:
1. Create different lesson versions with custom verb sets and tense options
2. Host the files on GitHub
3. Embed them in LearnWorlds using iframes

---

## 🎯 Step 1: Create Lesson Versions

### Lesson Structure

Each lesson version is a separate HTML file with:
- **Custom title** (e.g., "Lesson 1: Basic Verbs - Nútíð")
- **Tense configuration** (show both or only present)
- **Custom verb list** (choose which verbs to include)

### Configuration Options

At the top of each HTML file, modify these two sections:

```javascript
// CONFIGURATION
const CONFIG = {
    showTenses: true  // true = show both tenses, false = Nútíð only
};

// VERB_DATA
const VERB_DATA = [
    // Add or remove verbs here
];
```

---

## 📝 Step 2: Example Lesson Configurations

### **Lesson 1: Nútíð Only (Beginner)**

**File:** `lesson-1-nutid-basic.html`

**Changes:**
```javascript
const CONFIG = {
    showTenses: false  // Hide tense selector
};
```

**Title in HTML:**
```html
<h1>Lesson 1: Basic Verbs - Nútíð</h1>
<p class="subtitle">Practice present tense conjugations</p>
```

**Verbs:** Keep only `drekka` and `borða`

---

### **Lesson 2: Both Tenses (Intermediate)**

**File:** `lesson-2-both-tenses.html`

**Changes:**
```javascript
const CONFIG = {
    showTenses: true  // Show tense selector
};
```

**Title in HTML:**
```html
<h1>Lesson 2: Both Tenses</h1>
<p class="subtitle">Practice present and past tense conjugations</p>
```

**Verbs:** Include `drekka`, `borða`, and `fara`

**Add to dropdown:**
```html
<select id="verbSelect">
    <option value="0">að drekka</option>
    <option value="1">að borða</option>
    <option value="2">að fara</option>
</select>
```

---

### **Lesson 3: Advanced Verbs (Nútíð)**

**File:** `lesson-3-advanced-nutid.html`

**Changes:**
```javascript
const CONFIG = {
    showTenses: false
};
```

**Verbs:** Replace with `tala`, `skrifa`, `lesa` (or any verbs you choose)

---

## 🔧 Step 3: How to Add a New Verb

To add a verb to any lesson, insert this template into `VERB_DATA`:

```javascript
,
{
    "verb": "YOUR_VERB",
    "lemmas": ["YOUR_VERB"],
    "tenses": {
        "present": {
            "label": "Nútíð",
            "singular": {
                "1": "",  // ég
                "2": "",  // þú
                "3": ""   // hann/hún/það
            },
            "plural": {
                "1": "",  // við
                "2": "",  // þið
                "3": ""   // þeir/þær/þau
            }
        },
        "past": {
            "label": "Þátíð",
            "singular": {
                "1": "",
                "2": "",
                "3": ""
            },
            "plural": {
                "1": "",
                "2": "",
                "3": ""
            }
        }
    },
    "ui": {
        "pronouns": {
            "singular": { "1": "ég", "2": "þú", "3": "hann / hún / það" },
            "plural":   { "1": "við", "2": "þið", "3": "þeir / þær / þau" }
        }
    }
}
```

**Then add to the dropdown:**
```html
<option value="X">að YOUR_VERB</option>
```
(Replace X with the array position: 0 for first, 1 for second, etc.)

---

## 🌐 Step 4: Host on GitHub

### Option A: GitHub Pages (Recommended)

1. **Create a GitHub repository:**
   - Go to github.com and create a new repository
   - Name it: `icelandic-verb-lessons` (or any name)

2. **Upload your lesson files:**
   ```
   lesson-1-nutid-basic.html
   lesson-2-both-tenses.html
   lesson-3-advanced-nutid.html
   ```

3. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` → `/root` folder
   - Click Save

4. **Your files will be available at:**
   ```
   https://USERNAME.github.io/REPO-NAME/lesson-1-nutid-basic.html
   https://USERNAME.github.io/REPO-NAME/lesson-2-both-tenses.html
   ```

### Option B: GitHub Raw URLs (Alternative)

You can also use raw GitHub URLs:
```
https://raw.githubusercontent.com/USERNAME/REPO-NAME/main/lesson-1-nutid-basic.html
```

---

## 🎓 Step 5: Embed in LearnWorlds

### Method 1: HTML/Embed Block (Recommended)

1. In LearnWorlds lesson editor, add an **HTML block**
2. Insert this iframe code:

```html
<iframe 
    src="https://USERNAME.github.io/REPO-NAME/lesson-1-nutid-basic.html"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none; border-radius: 8px;">
</iframe>
```

3. The game will **auto-resize** based on content

### Method 2: Embed Code Block

If your LearnWorlds plan supports it, use the **Embed Code** block with the same iframe code.

---

## 📊 Lesson Organization Strategy

### Suggested Course Structure:

**Module 1: Present Tense Basics**
- Lesson 1.1: Basic Verbs (drekka, borða) - Nútíð only
- Lesson 1.2: Movement Verbs (fara, koma) - Nútíð only
- Lesson 1.3: Daily Verbs (tala, skrifa, lesa) - Nútíð only

**Module 2: Past Tense Introduction**
- Lesson 2.1: Basic Verbs Review (drekka, borða) - Both tenses
- Lesson 2.2: Mixed Practice - Both tenses

**Module 3: Advanced**
- Lesson 3.1: Irregular Verbs - Both tenses
- Lesson 3.2: Complex Conjugations - Both tenses

---

## 🔄 Quick Reference: File Modifications

### To hide tense selector:
```javascript
const CONFIG = { showTenses: false };
```

### To show tense selector:
```javascript
const CONFIG = { showTenses: true };
```

### To change lesson title:
```html
<h1>Your Lesson Title</h1>
<p class="subtitle">Your subtitle</p>
```

### To add a verb to dropdown:
```html
<option value="2">að YOUR_VERB</option>
```
(Number = position in VERB_DATA array)

---

## ✅ Testing Checklist

Before embedding in LearnWorlds:

1. ✅ Open each lesson file in browser
2. ✅ Verify correct verbs appear in dropdown
3. ✅ Check if tense selector shows/hides as expected
4. ✅ Test both "Fill in the Blank" and "Drag & Drop" modes
5. ✅ Verify conjugations are correct
6. ✅ Test on mobile/tablet view
7. ✅ Confirm auto-resize works when switching modes

---

## 🎨 Customization Options

### Change colors:
Find these in the CSS section:
```css
--primary-green: #21b766;
--error-red: #f15d4e;
--text-color: #121212;
```

### Adjust spacing:
Modify padding/margin values in CSS for:
- `.container` (overall spacing)
- `.game-area` (game box padding)
- `table` (table spacing)

---

## 🆘 Troubleshooting

### Problem: Iframe not showing
**Solution:** Check if GitHub Pages is enabled and URL is correct

### Problem: Tense dropdown still visible when showTenses = false
**Solution:** Clear browser cache and reload

### Problem: New verb not appearing
**Solution:** 
1. Check array position in VERB_DATA
2. Verify dropdown option value matches array position
3. Ensure proper JSON syntax (commas, brackets)

### Problem: Conjugations not checking correctly
**Solution:** Verify exact spelling in VERB_DATA matches expected answers

---

## 📞 Quick Examples

### Example 1: Create a 3-verb Nútíð lesson
1. Copy `icelandic-verb-game.html` → `my-lesson.html`
2. Set `showTenses: false`
3. Keep/modify 3 verbs in VERB_DATA
4. Update dropdown with 3 options (value="0", "1", "2")
5. Upload to GitHub
6. Embed in LearnWorlds

### Example 2: Create both-tenses lesson with 5 verbs
1. Copy `icelandic-verb-game.html` → `advanced-lesson.html`
2. Set `showTenses: true`
3. Add 5 verbs to VERB_DATA
4. Update dropdown with 5 options (value="0" through "4")
5. Upload to GitHub
6. Embed in LearnWorlds

---

## 🎉 You're Ready!

You now have everything needed to:
- ✅ Create custom lesson versions
- ✅ Configure tense visibility
- ✅ Add/remove verbs
- ✅ Host on GitHub
- ✅ Embed in LearnWorlds

**Example files created:**
- `lesson-1-nutid-basic.html` (Nútíð only, 2 verbs)
- `lesson-2-both-tenses.html` (Both tenses, 3 verbs)

Happy teaching! 🇮🇸
