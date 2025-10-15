# Quick Guide: Adding New Verbs

## Step-by-Step Instructions

### 1. Open the HTML file
Open `icelandic-verb-game.html` in any text editor.

### 2. Find the VERB_DATA section
Search for `VERB_DATA` (around line 390). You'll see something like:
```javascript
const VERB_DATA = [
    {
        "verb": "drekka",
        "lemmas": ["drekka"],
        "tenses": {...},
        ...
    },
    {
        "verb": "borða",
        "lemmas": ["borða"],
        "tenses": {...},
        ...
    }
];
```

### 3. Add your new verb
At the end of the array (before the `];`), add a comma and your new verb:

```javascript
const VERB_DATA = [
    {
        "verb": "drekka",
        ...
    },
    {
        "verb": "borða",
        ...
    },
    {
        "verb": "YOUR_NEW_VERB",
        "lemmas": ["YOUR_NEW_VERB"],
        "tenses": {
            "present": {
                "label": "Nútíð",
                "singular": {
                    "1": "1st_person_singular",
                    "2": "2nd_person_singular",
                    "3": "3rd_person_singular"
                },
                "plural": {
                    "1": "1st_person_plural",
                    "2": "2nd_person_plural",
                    "3": "3rd_person_plural"
                }
            },
            "past": {
                "label": "Þátíð",
                "singular": {
                    "1": "1st_person_singular_past",
                    "2": "2nd_person_singular_past",
                    "3": "3rd_person_singular_past"
                },
                "plural": {
                    "1": "1st_person_plural_past",
                    "2": "2nd_person_plural_past",
                    "3": "3rd_person_plural_past"
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
];
```

### 4. Update the dropdown
Find the verb selector (around line 265):
```html
<select id="verbSelect">
    <option value="0">drekka</option>
    <option value="1">borða</option>
    <!-- Add your new option here -->
    <option value="2">YOUR_VERB</option>
</select>
```

**Important:** The `value` should match the position in the array (0 for first verb, 1 for second, 2 for third, etc.)

### 5. Save and test
Save the file and open it in your browser to test!

---

## Example: Adding "skrifa" (to write)

### 1. Get data from BÍN
Go to https://bin.arnastofnun.is/ and search for "skrifa"

### 2. Add to VERB_DATA:
```javascript
{
    "verb": "skrifa",
    "lemmas": ["skrifa"],
    "tenses": {
        "present": {
            "label": "Nútíð",
            "singular": {
                "1": "skrifa",
                "2": "skrifar",
                "3": "skrifar"
            },
            "plural": {
                "1": "skrifum",
                "2": "skrifið",
                "3": "skrifa"
            }
        },
        "past": {
            "label": "Þátíð",
            "singular": {
                "1": "skrifaði",
                "2": "skrifaðir",
                "3": "skrifaði"
            },
            "plural": {
                "1": "skrifuðum",
                "2": "skrifuðuð",
                "3": "skrifuðu"
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

### 3. Add to dropdown:
```html
<option value="2">skrifa</option>
```

---

## Common Mistakes to Avoid

❌ **Missing comma** between verb objects
```javascript
{
    "verb": "borða",
    ...
}  // <- Need comma here!
{
    "verb": "skrifa",
    ...
}
```

✅ **Correct:**
```javascript
{
    "verb": "borða",
    ...
},  // <- Comma added
{
    "verb": "skrifa",
    ...
}
```

❌ **Wrong dropdown value**
```html
<option value="1">skrifa</option>  <!-- Should be value="2" if it's the 3rd verb -->
```

❌ **Missing quotes**
```javascript
"Nf": drekka  // Wrong - missing quotes
"Nf": "drekka"  // Correct
```

---

## Understanding the Structure

### Persons
- **1st Person:** ég (singular) / við (plural) - "I" / "we"
- **2nd Person:** þú (singular) / þið (plural) - "you" / "you all"
- **3rd Person:** hann/hún/það (singular) / þeir/þær/þau (plural) - "he/she/it" / "they"

### Tenses
- **Nútíð** = Present tense
- **Þátíð** = Past tense

---

## Quick Copy Template

```javascript
,
{
    "verb": "",
    "translation": "",
    "present": {
        "singular": {
            "no_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""},
            "with_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""}
        },
        "plural": {
            "no_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""},
            "with_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""}
        }
    },
    "past": {
        "singular": {
            "no_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""},
            "with_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""}
        },
        "plural": {
            "no_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""},
            "with_article": {"Nf": "", "Þf": "", "Þgf": "", "Ef": ""}
        }
    }
}
```

Copy this template, fill in the blanks, and add it to your VERB_DATA array!
