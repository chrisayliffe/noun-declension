# Icelandic Verb Practice Game - Embedding Instructions

## 📋 Overview
This is a standalone HTML game for practicing Icelandic verb conjugations. It's designed to be easily embedded in LearnWorlds LMS or any other platform that supports HTML/iframe embedding.

## 🎮 Features
- **Two Game Modes:**
  - Fill in the Blank: Type the correct conjugations for each person
  - Drag & Drop: Drag verb forms to match pronouns
- **Multiple Verbs:** Dropdown selector to choose different verbs
- **Tense Toggle:** Switch between Nútíð (Present) and Þátíð (Past)
- **Show Answers:** Learning mode to view correct answers
- **Real-time Feedback:** Instant validation with color-coded responses
- **Progress Tracking:** Score display showing percentage and correct count
- **Fully Responsive:** Works on desktop, tablet, and mobile devices

## 🔗 How to Embed in LearnWorlds

### Method 1: HTML Block (Recommended)
1. Go to your LearnWorlds course lesson editor
2. Add an **HTML block** to your page
3. Copy the entire contents of `icelandic-verb-game.html`
4. Paste it into the HTML block
5. Save and publish

### Method 2: iFrame Embedding
1. Host the HTML file on a public server (e.g., GitHub Pages, your own domain)
2. In LearnWorlds, add an **Embed/HTML block**
3. Use this iframe code:
```html
<iframe 
    src="YOUR_HOSTED_URL/icelandic-verb-game.html" 
    width="100%" 
    height="900px" 
    frameborder="0"
    style="border: none; border-radius: 12px; box-shadow: 0 4px 16px rgba(0,0,0,0.1);">
</iframe>
```

### Method 3: Direct Link
Simply provide students with the direct URL to the HTML file:
```
YOUR_HOSTED_URL/icelandic-verb-game.html
```

## ✏️ How to Add New Verbs

### For Non-Technical Users
1. Open the `icelandic-verb-game.html` file in a text editor (Notepad, TextEdit, VS Code, etc.)
2. Find the `VERB_DATA` section (around line 390)
3. Copy an existing verb object and modify it with your new verb data
4. Follow this structure (conjugation by person):

```javascript
{
    "verb": "YOUR_VERB_NAME",
    "lemmas": ["YOUR_VERB_NAME"],
    "tenses": {
        "present": {
            "label": "Nútíð",
            "singular": {
                "1": "1st_person_sing",    // ég
                "2": "2nd_person_sing",    // þú
                "3": "3rd_person_sing"     // hann/hún/það
            },
            "plural": {
                "1": "1st_person_plural",  // við
                "2": "2nd_person_plural",  // þið
                "3": "3rd_person_plural"   // þeir/þær/þau
            }
        },
        "past": {
            "label": "Þátíð",
            "singular": {
                "1": "1st_past_sing",
                "2": "2nd_past_sing",
                "3": "3rd_past_sing"
            },
            "plural": {
                "1": "1st_past_plural",
                "2": "2nd_past_plural",
                "3": "3rd_past_plural"
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

5. Don't forget to add a comma after the previous verb object!
6. Update the dropdown option in the HTML (around line 265):
```html
<option value="0">drekka</option>
<option value="1">borða</option>
<option value="2">YOUR_NEW_VERB</option>
```

### Getting Verb Data from BÍN (bin.arnastofnun.is)
1. Go to https://bin.arnastofnun.is/
2. Search for your verb
3. Look for the verb conjugation table (beygingar)
4. Copy the conjugated forms for:
   - Present tense (Nútíð): 1st, 2nd, 3rd person in both singular and plural
   - Past tense (Þátíð): 1st, 2nd, 3rd person in both singular and plural

## 🎨 Customization

### Change Colors
Find the CSS section (around line 11) and modify these variables:
- Text color: `#121212`
- Background: `#ffffff`
- Success/Correct: `#21b766`
- Error/Incorrect: `#f15d4e`

### Change Font
The game uses **Outfit** from Google Fonts. To change it:
1. Find the Google Fonts link (line 7)
2. Replace with your preferred font
3. Update `font-family: 'Outfit', sans-serif;` throughout the CSS

## 📱 Mobile Optimization
The game is fully responsive and works on:
- Desktop (1920px+)
- Tablet (768px - 1024px)
- Mobile (375px - 767px)

## 🐛 Troubleshooting

### Game not loading in LearnWorlds
- Make sure you're using an HTML block, not a text block
- Check that all HTML code was copied completely
- Try the iframe method instead

### Drag and Drop not working
- Ensure you're using a modern browser (Chrome, Firefox, Safari, Edge)
- On mobile, tap tiles to select and tap drop zones to place

### Incorrect verb forms
- Double-check your verb data against BÍN database
- Make sure case-sensitivity matches (Icelandic is case-sensitive)
- Verify all commas and brackets are in place in the JSON

## 📞 Support
For additional help:
- Check that your verb data follows the exact JSON structure
- Validate your JSON at https://jsonlint.com/
- Test the HTML file locally before embedding

## 📦 File Information
- **File:** `icelandic-verb-game.html`
- **Size:** ~20KB (very lightweight!)
- **Dependencies:** None (all code is self-contained)
- **Browser Support:** All modern browsers (Chrome, Firefox, Safari, Edge)
- **Internet Required:** Only for loading Google Fonts (Outfit)

## 🎯 Usage Tips for Students
1. Start with "Fill in the Blank" mode to test your knowledge
2. Use "Show Answers" to learn correct forms
3. Try "Drag & Drop" mode to practice recognition
4. Switch between verbs and tenses to master different conjugations
5. Aim for 100% correct before moving to the next verb!

## 📊 Tracking Progress
The game shows:
- **Progress:** Percentage of correct answers
- **Correct Count:** Number of correct answers out of total

Progress resets when:
- Switching verbs
- Switching tenses
- Clicking "Reset" button
- Switching game modes
