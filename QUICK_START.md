# 🚀 Quick Start Guide - Icelandic Verb Game for LearnWorlds

## ⚡ 3-Step Setup

### 1️⃣ Create Your Lesson Version

Copy `icelandic-verb-game.html` and rename it (e.g., `lesson-1.html`)

### 2️⃣ Configure It

**At the top of the file, modify:**

```javascript
// Hide tense selector? (true = show both, false = Nútíð only)
const CONFIG = { showTenses: false };
```

**Change the title:**
```html
<h1>Your Lesson Title</h1>
```

**Add/Remove verbs in VERB_DATA** (see full guide for template)

**Update dropdown:**
```html
<select id="verbSelect">
    <option value="0">að drekka</option>
    <option value="1">að borða</option>
    <!-- Add more as needed -->
</select>
```

### 3️⃣ Embed in LearnWorlds

**Upload to GitHub Pages**, then in LearnWorlds:

```html
<iframe 
    src="https://YOUR-USERNAME.github.io/YOUR-REPO/lesson-1.html"
    width="100%"
    height="900"
    frameborder="0"
    style="border: none;">
</iframe>
```

---

## 📦 Ready-Made Examples

You have **2 example lessons** ready to use:

### Lesson 1: Nútíð Only
- **File:** `lesson-1-nutid-basic.html`
- **Config:** `showTenses: false`
- **Verbs:** drekka, borða
- **Title:** "Lesson 1: Basic Verbs - Nútíð"

### Lesson 2: Both Tenses  
- **File:** `lesson-2-both-tenses.html`
- **Config:** `showTenses: true`
- **Verbs:** drekka, borða, fara
- **Title:** "Lesson 2: Both Tenses"

---

## 🎯 Common Configurations

### Configuration 1: Beginner (Present Only)
```javascript
const CONFIG = { showTenses: false };
// Shows only Nútíð
```

### Configuration 2: Intermediate (Both Tenses)
```javascript
const CONFIG = { showTenses: true };
// Shows Nútíð and Þátíð dropdown
```

---

## 🔧 Adding a New Verb

### Step 1: Add to VERB_DATA array

```javascript
,
{
    "verb": "tala",
    "lemmas": ["tala"],
    "tenses": {
        "present": {
            "label": "Nútíð",
            "singular": {
                "1": "tala",
                "2": "talar",
                "3": "talar"
            },
            "plural": {
                "1": "tölum",
                "2": "talið",
                "3": "tala"
            }
        },
        "past": {
            "label": "Þátíð",
            "singular": {
                "1": "talaði",
                "2": "talaðir",
                "3": "talaði"
            },
            "plural": {
                "1": "töluðum",
                "2": "töluðuð",
                "3": "töluðu"
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

### Step 2: Add to dropdown

```html
<option value="2">að tala</option>
```

*Note: `value="2"` means it's the 3rd verb (0=first, 1=second, 2=third)*

---

## 🌐 GitHub Hosting

### Quick GitHub Setup:

1. Create new repository on github.com
2. Upload your lesson HTML files
3. Go to **Settings → Pages**
4. Enable Pages: Branch = `main`, Folder = `/ (root)`
5. Your files will be at:
   ```
   https://USERNAME.github.io/REPO-NAME/lesson-1.html
   ```

---

## 📋 Lesson Planning Template

### Module 1: Basics
- ✅ `lesson-1-nutid-drekka-borda.html` (2 verbs, Nútíð only)
- ✅ `lesson-2-nutid-movement.html` (fara, koma, Nútíð only)
- ✅ `lesson-3-nutid-daily.html` (tala, skrifa, lesa, Nútíð only)

### Module 2: Past Tense
- ✅ `lesson-4-both-basic.html` (drekka, borða, both tenses)
- ✅ `lesson-5-both-movement.html` (fara, koma, both tenses)

### Module 3: Mixed
- ✅ `lesson-6-both-all.html` (all verbs, both tenses)

---

## 🎨 Customization Quick Reference

### Hide Tense Dropdown
```javascript
const CONFIG = { showTenses: false };
```

### Show Tense Dropdown
```javascript
const CONFIG = { showTenses: true };
```

### Change Title
```html
<h1>Your Custom Title</h1>
<p class="subtitle">Your subtitle here</p>
```

### Limit to 1 Verb
In `VERB_DATA`, keep only one verb object, and in dropdown:
```html
<select id="verbSelect">
    <option value="0">að drekka</option>
</select>
```

---

## ✅ Testing Checklist

Before going live:

- [ ] Open file in browser - does it load?
- [ ] Are the correct verbs showing in dropdown?
- [ ] Is tense selector hidden/shown as expected?
- [ ] Test Fill in the Blank mode
- [ ] Test Drag & Drop mode
- [ ] Try on mobile/tablet view
- [ ] Verify conjugations are correct

---

## 🆘 Need Help?

**See:** `LEARNWORLDS_SETUP_GUIDE.md` for detailed instructions

**Example Files:**
- `lesson-1-nutid-basic.html` - Working example
- `lesson-2-both-tenses.html` - Working example

---

## 🎉 You're Ready!

1. Pick a lesson example or start fresh
2. Modify CONFIG and verbs
3. Upload to GitHub
4. Embed in LearnWorlds

That's it! 🇮🇸
