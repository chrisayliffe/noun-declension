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
        "translation": "English meaning",
        "present": {
            "singular": {
                "no_article": {
                    "Nf": "nominative_form",
                    "Þf": "accusative_form",
                    "Þgf": "dative_form",
                    "Ef": "genitive_form"
                },
                "with_article": {
                    "Nf": "nominative_with_article",
                    "Þf": "accusative_with_article",
                    "Þgf": "dative_with_article",
                    "Ef": "genitive_with_article"
                }
            },
            "plural": {
                "no_article": {
                    "Nf": "nominative_plural",
                    "Þf": "accusative_plural",
                    "Þgf": "dative_plural",
                    "Ef": "genitive_plural"
                },
                "with_article": {
                    "Nf": "nominative_plural_article",
                    "Þf": "accusative_plural_article",
                    "Þgf": "dative_plural_article",
                    "Ef": "genitive_plural_article"
                }
            }
        },
        "past": {
            // Same structure as present
            "singular": {
                "no_article": {"Nf": "...", "Þf": "...", "Þgf": "...", "Ef": "..."},
                "with_article": {"Nf": "...", "Þf": "...", "Þgf": "...", "Ef": "..."}
            },
            "plural": {
                "no_article": {"Nf": "...", "Þf": "...", "Þgf": "...", "Ef": "..."},
                "with_article": {"Nf": "...", "Þf": "...", "Þgf": "...", "Ef": "..."}
            }
        }
    }
];
```

### 4. Update the dropdown
Find the verb selector (around line 265):
```html
<select id="verbSelect">
    <option value="0">drekka (to drink)</option>
    <option value="1">borða (to eat)</option>
    <!-- Add your new option here -->
    <option value="2">YOUR_VERB (translation)</option>
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
    "translation": "to write",
    "present": {
        "singular": {
            "no_article": {"Nf": "skrifa", "Þf": "skriftu", "Þgf": "skriftu", "Ef": "skriftu"},
            "with_article": {"Nf": "skriftan", "Þf": "skriftuna", "Þgf": "skriftunni", "Ef": "skriftunnar"}
        },
        "plural": {
            "no_article": {"Nf": "skriftur", "Þf": "skriftur", "Þgf": "skriftum", "Ef": "skrifta"},
            "with_article": {"Nf": "skrifturnar", "Þf": "skrifturnar", "Þgf": "skriftunum", "Ef": "skriftanna"}
        }
    },
    "past": {
        "singular": {
            "no_article": {"Nf": "skriftu", "Þf": "skriftu", "Þgf": "skriftu", "Ef": "skriftu"},
            "with_article": {"Nf": "skriftuna", "Þf": "skriftuna", "Þgf": "skriftunni", "Ef": "skriftunnar"}
        },
        "plural": {
            "no_article": {"Nf": "skriftur", "Þf": "skriftur", "Þgf": "skriftum", "Ef": "skrifta"},
            "with_article": {"Nf": "skrifturnar", "Þf": "skrifturnar", "Þgf": "skriftunum", "Ef": "skriftanna"}
        }
    }
}
```

### 3. Add to dropdown:
```html
<option value="2">skrifa (to write)</option>
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

## Understanding the Cases

- **Nf. (Nefnifall)** = Nominative case
- **Þf. (Þolfall)** = Accusative case  
- **Þgf. (Þágufall)** = Dative case
- **Ef. (Eignarfall)** = Genitive case

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
