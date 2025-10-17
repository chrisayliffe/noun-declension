# Google Sheet Structure for Icelandic Verb Game

## 📊 Recommended Sheet Structure

### Each Tab = One Lesson

Create tabs like: `Lesson 1`, `Lesson 2`, `Advanced`, etc.

---

## 📋 Column Structure (for each tab)

### **Row 1: Configuration**
| Column A | Column B | Column C | Column D |
|----------|----------|----------|----------|
| `LESSON_TITLE` | Lesson 1: Basic Verbs - Nútíð | | |
| `LESSON_SUBTITLE` | Practice present tense conjugations | | |
| `SHOW_TENSES` | false | | |

### **Row 4 onwards: Verb Data**

| Verb | Person | Number | Tense | Conjugation |
|------|--------|--------|-------|-------------|
| drekka | 1 | singular | present | drekk |
| drekka | 2 | singular | present | drekkur |
| drekka | 3 | singular | present | drekkur |
| drekka | 1 | plural | present | drekkum |
| drekka | 2 | plural | present | drekkið |
| drekka | 3 | plural | present | drekka |
| drekka | 1 | singular | past | drakk |
| drekka | 2 | singular | past | drakkst |
| drekka | 3 | singular | past | drakk |
| drekka | 1 | plural | past | drukkum |
| drekka | 2 | plural | past | drukkuð |
| drekka | 3 | plural | past | drukku |
| borða | 1 | singular | present | borða |
| borða | 2 | singular | present | borðar |
| ... | ... | ... | ... | ... |

---

## 🔧 Alternative: Simplified Structure

### **Configuration Section (Rows 1-3)**

| Setting | Value |
|---------|-------|
| LESSON_TITLE | Lesson 1: Basic Verbs - Nútíð |
| LESSON_SUBTITLE | Practice present tense conjugations |
| SHOW_TENSES | no |

### **Verb Section (Row 5 onwards)**

| Verb | Tense | ég | þú | hann/hún/það | við | þið | þeir/þær/þau |
|------|-------|-----|-----|--------------|-----|-----|--------------|
| drekka | present | drekk | drekkur | drekkur | drekkum | drekkið | drekka |
| drekka | past | drakk | drakkst | drakk | drukkum | drukkuð | drukku |
| borða | present | borða | borðar | borðar | borðum | borðið | borða |
| borða | past | borðaði | borðaðir | borðaði | borðuðum | borðuðuð | borðuðu |

---

## 📝 Example Tabs

### Tab: "Lesson 1"
- LESSON_TITLE: Lesson 1: Basic Verbs - Nútíð
- SHOW_TENSES: no
- Verbs: drekka (present), borða (present)

### Tab: "Lesson 2"
- LESSON_TITLE: Lesson 2: Both Tenses
- SHOW_TENSES: yes
- Verbs: drekka (present + past), borða (present + past), fara (present + past)

### Tab: "Advanced"
- LESSON_TITLE: Advanced Conjugations
- SHOW_TENSES: yes
- Verbs: Complex verbs with both tenses

---

## 🌐 How URLs Will Work

- `game.html?lesson=Lesson 1` → Loads "Lesson 1" tab
- `game.html?lesson=Lesson 2` → Loads "Lesson 2" tab
- `game.html?lesson=Advanced` → Loads "Advanced" tab

**Note:** Tab names must match URL parameter exactly (case-sensitive)

---

## ✅ Benefits

1. **Single HTML file** - No need to create multiple versions
2. **Easy updates** - Edit Google Sheet, changes reflect immediately
3. **Non-technical editing** - Teachers can edit without touching code
4. **Version control** - Google Sheets tracks all changes
5. **Collaboration** - Multiple people can edit lessons

---

## 🔒 Sharing Settings Required

To make this work, your Google Sheet must be:
- **Publicly accessible** (Anyone with the link can view)
- **Published to web** (File → Share → Publish to web)

This allows the HTML file to fetch data without authentication.
