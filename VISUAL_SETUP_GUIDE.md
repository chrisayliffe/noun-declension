# 📸 Visual Setup Guide - What You Should See

## Following the 6 Steps - Visual Confirmation

---

## STEP 1: Create Repository

### What to Click:
```
https://github.com/new
```

### What to Fill:
```
┌─────────────────────────────────────────┐
│ Repository name *                       │
│ [verb-practice-game              ]      │
│                                         │
│ Description (optional)                  │
│ [Icelandic verb practice         ]      │
│                                         │
│ ○ Public  ● Private                     │
│    ↑                                    │
│    └── SELECT THIS!                     │
│                                         │
│ ☑ Add a README file                     │
│                                         │
│ [Create repository]                     │
└─────────────────────────────────────────┘
```

### What You'll See After:
```
✅ Repository created successfully!
URL: https://github.com/chrisayliffe/verb-practice-game
```

---

## STEP 2: Find the File to Upload

### In Your Workspace:
```
/app
├── frontend
│   └── public
│       ├── icelandic-verb-game-dynamic.html  ← THIS FILE!
│       ├── icelandic-verb-game.html
│       ├── lesson-1-nutid-basic.html
│       └── lesson-2-both-tenses.html
```

### File Details:
- **Name:** `icelandic-verb-game-dynamic.html`
- **Size:** ~35 KB
- **Type:** HTML file

---

## STEP 3: Upload to GitHub

### In Your Repository:
```
┌─────────────────────────────────────────┐
│ chrisayliffe / verb-practice-game       │
│ ─────────────────────────────────────   │
│                                         │
│ [Add file ▼] [<> Code ▼]               │
│     │                                   │
│     └── Click here!                     │
│                                         │
│ Then select: "Upload files"             │
└─────────────────────────────────────────┘
```

### Upload Page:
```
┌─────────────────────────────────────────┐
│ Drag files here to add them to your    │
│ repository                              │
│                                         │
│     📄 Drop your file here!             │
│                                         │
│ or [choose your files]                  │
│                                         │
│ ─────────────────────────────────       │
│ Commit changes                          │
│ [Commit changes]                        │
└─────────────────────────────────────────┘
```

### After Upload - You'll See:
```
┌─────────────────────────────────────────┐
│ chrisayliffe / verb-practice-game       │
│ ─────────────────────────────────────   │
│                                         │
│ 📄 README.md                            │
│ 📄 icelandic-verb-game-dynamic.html ✅  │
│                                         │
└─────────────────────────────────────────┘
```

---

## STEP 4: Enable GitHub Pages

### Navigate to Settings:
```
┌─────────────────────────────────────────────────────────┐
│ [<> Code] [Issues] [Pull requests] [Settings] ← Click!  │
└─────────────────────────────────────────────────────────┘
```

### In Settings Sidebar:
```
┌─────────────────┐
│ General         │
│ Access          │
│ ...             │
│ Pages           │ ← Click!
│ ...             │
└─────────────────┘
```

### Pages Settings:
```
┌──────────────────────────────────────────┐
│ Build and deployment                     │
│                                          │
│ Source                                   │
│ [Deploy from a branch ▼]                 │
│                                          │
│ Branch                                   │
│ [main ▼]  [/ (root) ▼]  [Save]         │
│   ↑         ↑            ↑              │
│   │         │            └── Click!     │
│   │         └── Select this             │
│   └── Select this                       │
└──────────────────────────────────────────┘
```

### Success Message:
```
┌──────────────────────────────────────────┐
│ ✅ Your site is live at                  │
│ https://chrisayliffe.github.io/          │
│        verb-practice-game/               │
└──────────────────────────────────────────┘
```

---

## STEP 5: Wait

### What GitHub is Doing:
```
⏳ Building your site...
⏳ Deploying...
⏳ Publishing...
✅ Done!
```

**Duration:** 2-3 minutes

**While waiting:**
- ☕ Get coffee
- 🚶 Stretch
- 📱 Check email
- ⏰ Set 3-minute timer

---

## STEP 6: Test Your URLs

### Test 1: Base URL
```
Browser Address Bar:
┌────────────────────────────────────────────────┐
│ https://chrisayliffe.github.io/               │
│        verb-practice-game/                     │
└────────────────────────────────────────────────┘

Expected Result:
┌────────────────────────────────────────────────┐
│ verb-practice-game                             │
│                                                │
│ 📄 README.md                                   │
│ 📄 icelandic-verb-game-dynamic.html            │
└────────────────────────────────────────────────┘
```

### Test 2: HTML File
```
Browser Address Bar:
┌────────────────────────────────────────────────┐
│ https://chrisayliffe.github.io/               │
│        verb-practice-game/                     │
│        icelandic-verb-game-dynamic.html        │
└────────────────────────────────────────────────┘

Expected Result:
┌────────────────────────────────────────────────┐
│ Loading lesson data...                         │
└────────────────────────────────────────────────┘

Or:
┌────────────────────────────────────────────────┐
│ Failed to load lesson "Lesson 1"              │
│ (This is OK - means file works!)              │
└────────────────────────────────────────────────┘
```

### Test 3: With Lesson Parameter
```
Browser Address Bar:
┌────────────────────────────────────────────────┐
│ https://chrisayliffe.github.io/               │
│        verb-practice-game/                     │
│        icelandic-verb-game-dynamic.html        │
│        ?lesson=Lesson 1                        │
└────────────────────────────────────────────────┘

Expected Result:
┌────────────────────────────────────────────────┐
│ Lesson 1: Basic Verbs - Nútíð                 │
│ Practice present tense conjugations           │
│                                                │
│ Select Verb: [að drekka ▼]                    │
│                                                │
│ [Fill in the Blank] [Drag & Drop]            │
│                                                │
│ [Table with conjugations]                     │
└────────────────────────────────────────────────┘
```

---

## 🚫 What 404 Looks Like

If you see this, something is wrong:

```
┌────────────────────────────────────────────────┐
│              404                               │
│                                                │
│        File not found                          │
│                                                │
│  The site configured at this address does     │
│  not contain the requested file.               │
└────────────────────────────────────────────────┘
```

**Causes:**
1. ❌ File not uploaded
2. ❌ Wrong file name
3. ❌ Pages not enabled
4. ❌ Didn't wait long enough
5. ❌ Repository is private

---

## ✅ What Success Looks Like

### Success Checklist:

**In GitHub:**
```
✅ Repository exists and is public
✅ File appears in file list
✅ Settings → Pages shows "Your site is live"
✅ Green checkmark visible
```

**In Browser:**
```
✅ Base URL loads (shows files or README)
✅ HTML file URL loads (shows game or error)
✅ With lesson loads (shows actual game)
```

**Game Features Visible:**
```
✅ Title shows your lesson name
✅ Verb dropdown has options
✅ Fill in the Blank mode works
✅ Drag & Drop mode works
✅ Can switch between modes
```

---

## 🎯 Final URL Examples

### Your Working URLs:

**Lesson 1:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson 1
```

**Lesson 2:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html?lesson=Lesson 2
```

**Any Custom Tab:**
```
https://chrisayliffe.github.io/verb-practice-game/icelandic-verb-game-dynamic.html?lesson=YOUR_TAB_NAME
```

---

## 📱 LearnWorlds Embed Preview

### What Students Will See:

```
┌─────────────────────────────────────────────────┐
│ Lesson Title                                    │
│                                                 │
│ ┌─────────────────────────────────────────────┐│
│ │ Lesson 1: Basic Verbs - Nútíð              ││
│ │ Practice present tense conjugations        ││
│ │                                            ││
│ │ Select Verb: [að drekka ▼]                ││
│ │ Tense: [Nútíð (Present) ▼]                ││
│ │                                            ││
│ │ [Fill in the Blank] [Drag & Drop]         ││
│ │                                            ││
│ │ Progress: 0%    Correct: 0/6              ││
│ │                                            ││
│ │ [Game Table Here]                          ││
│ │                                            ││
│ │ [Check Answers] [Reset]                    ││
│ └─────────────────────────────────────────────┘│
│                                                 │
│ [Continue to Next Lesson]                      │
└─────────────────────────────────────────────────┘
```

---

## 🆘 Common Error Messages

### Error 1: "Failed to load lesson"
```
Cause: Google Sheet issue
Fix: Check sheet sharing and tab name
```

### Error 2: "404 - File not found"
```
Cause: File not uploaded or Pages not enabled
Fix: Re-upload file, enable Pages, wait 3 minutes
```

### Error 3: Blank/white page
```
Cause: JavaScript error or loading issue
Fix: Check browser console, verify file uploaded correctly
```

---

## 📞 Need Screenshot Help?

If asking for help, take screenshots of:

1. **Your repository file list:**
   - https://github.com/chrisayliffe/verb-practice-game

2. **Your Pages settings:**
   - https://github.com/chrisayliffe/verb-practice-game/settings/pages

3. **The error you see in browser**

4. **Your Google Sheet tab names**

This helps identify the exact problem!

---

## ✨ You've Got This!

Follow the visual cues above and you'll have it working in 10 minutes! 🚀
