# 📊 Google Sheet Structure for Noun Declension Game

## Your Sheet ID
```
1N3yATmYOAyN1Nfw25IuXl3Dpwx9cxox8G4F-_yyutz8
```

---

## 📋 Sheet Structure for Each Lesson Tab

### Row 1-3: Configuration

| Column A | Column B |
|----------|----------|
| **LESSON_TITLE** | Lesson 1: Basic Nouns |
| **LESSON_SUBTITLE** | Practice noun declensions |
| **(empty)** | |

### Row 4: Empty

### Row 5: Headers

| Noun | Article | Number | Nf. | Þf. | Þgf. | Ef. |
|------|---------|--------|-----|-----|------|-----|

### Row 6+: Noun Data

**For each noun, you need 4 rows:**
1. Singular without article
2. Plural without article
3. Singular with article
4. Plural with article

---

## 📝 Example: hestur (horse)

| Noun | Article | Number | Nf. | Þf. | Þgf. | Ef. |
|------|---------|--------|-----|-----|------|-----|
| hestur | no_article | singular | hestur | hest | hesti | hests |
| hestur | no_article | plural | hestar | hesta | hestum | hesta |
| hestur | with_article | singular | hesturinn | hestinn | hestinum | hestsins |
| hestur | with_article | plural | hestarnir | hestana | hestunum | hestanna |

---

## 📝 Example: kona (woman)

| Noun | Article | Number | Nf. | Þf. | Þgf. | Ef. |
|------|---------|--------|-----|-----|------|-----|
| kona | no_article | singular | kona | konu | konu | konu |
| kona | no_article | plural | konur | konur | konum | kvenna |
| kona | with_article | singular | konan | konuna | konunni | konunnar |
| kona | with_article | plural | konurnar | konurnar | konunum | kvennanna |

---

## 🎯 Complete Template for One Lesson

```
Row 1:  LESSON_TITLE    | Lesson 1: Basic Nouns
Row 2:  LESSON_SUBTITLE | Practice noun declensions
Row 3:  (empty)
Row 4:  (empty)
Row 5:  Noun    | Article      | Number   | Nf.      | Þf.     | Þgf.    | Ef.
Row 6:  hestur  | no_article   | singular | hestur   | hest    | hesti   | hests
Row 7:  hestur  | no_article   | plural   | hestar   | hesta   | hestum  | hesta
Row 8:  hestur  | with_article | singular | hesturinn| hestinn | hestinum| hestsins
Row 9:  hestur  | with_article | plural   | hestarnir| hestana | hestunum| hestanna
Row 10: kona    | no_article   | singular | kona     | konu    | konu    | konu
Row 11: kona    | no_article   | plural   | konur    | konur   | konum   | kvenna
Row 12: kona    | with_article | singular | konan    | konuna  | konunni | konunnar
Row 13: kona    | with_article | plural   | konurnar | konurnar| konunum | kvennanna
```

---

## ⚙️ Column Details

### Column A: Noun
- The base form of the noun
- Example: `hestur`, `kona`, `barn`

### Column B: Article
- Must be exactly: `no_article` or `with_article`
- Case-sensitive!
- `no_article` = án greinis
- `with_article` = með greini

### Column C: Number
- Must be exactly: `singular` or `plural`
- Case-sensitive!

### Columns D-G: Case Forms
- **D = Nf.** (Nefnifall / Nominative)
- **E = Þf.** (Þolfall / Accusative)
- **F = Þgf.** (Þágufall / Dative)
- **G = Ef.** (Eignarfall / Genitive)

---

## 📚 Multiple Tabs = Multiple Lessons

### Example Structure:

**Tab: "Lesson 1"**
- Title: Basic Nouns
- Nouns: hestur, kona

**Tab: "Lesson 2"**
- Title: Animals
- Nouns: hundur, köttur, fugl

**Tab: "Lesson 3"**
- Title: Family Members
- Nouns: móðir, faðir, barn

---

## 🔗 URL Format

```
https://YOUR-GITHUB-URL/icelandic-noun-game-dynamic.html?lesson=LESSON_TAB_NAME
```

**Examples:**
```
?lesson=Lesson 1
?lesson=Lesson 2
?lesson=Animals
```

---

## ✅ Validation Checklist

Before testing:

- [ ] Row 1: LESSON_TITLE with your title
- [ ] Row 2: LESSON_SUBTITLE with your subtitle
- [ ] Row 3: Empty
- [ ] Row 4: Empty
- [ ] Row 5: Headers (Noun | Article | Number | Nf. | Þf. | Þgf. | Ef.)
- [ ] For each noun: 4 rows (2 without article + 2 with article)
- [ ] Article column: Only `no_article` or `with_article`
- [ ] Number column: Only `singular` or `plural`
- [ ] All case forms filled in (no empty cells)
- [ ] Sheet shared as "Anyone with link"

---

## 🎮 Game Display

The game will show **two side-by-side tables:**

### Left Table: Án greinis (Without Article)
```
┌─────────────────────────────────────┐
│   Án greinis (Without Article)     │
├──────────┬────────────┬─────────────┤
│          │  Eintala   │  Fleirtala  │
│          │ (Singular) │  (Plural)   │
├──────────┼────────────┼─────────────┤
│ Nf.      │  hestur    │   hestar    │
│ Nefnifall│            │             │
├──────────┼────────────┼─────────────┤
│ Þf.      │   hest     │   hesta     │
│ Þolfall  │            │             │
├──────────┼────────────┼─────────────┤
│ Þgf.     │   hesti    │   hestum    │
│ Þágufall │            │             │
├──────────┼────────────┼─────────────┤
│ Ef.      │   hests    │   hesta     │
│ Eignarfall│           │             │
└──────────┴────────────┴─────────────┘
```

### Right Table: Með greini (With Article)
```
┌─────────────────────────────────────┐
│    Með greini (With Article)       │
├──────────┬────────────┬─────────────┤
│          │  Eintala   │  Fleirtala  │
│          │ (Singular) │  (Plural)   │
├──────────┼────────────┼─────────────┤
│ Nf.      │ hesturinn  │  hestarnir  │
│ Nefnifall│            │             │
├──────────┼────────────┼─────────────┤
│ Þf.      │  hestinn   │   hestana   │
│ Þolfall  │            │             │
├──────────┼────────────┼─────────────┤
│ Þgf.     │ hestinum   │  hestunum   │
│ Þágufall │            │             │
├──────────┼────────────┼─────────────┤
│ Ef.      │ hestsins   │  hestanna   │
│ Eignarfall│           │             │
└──────────┴────────────┴─────────────┘
```

**Total cells per noun: 16**
- 8 without article (4 cases × 2 numbers)
- 8 with article (4 cases × 2 numbers)

---

## 🆘 Troubleshooting

### Issue: Noun not appearing in dropdown

**Check:**
1. Is noun name in Column A?
2. Do you have all 4 rows for that noun?
3. Are article and number values correct?

### Issue: Wrong forms showing

**Check:**
1. Column order: Noun | Article | Number | Nf | Þf | Þgf | Ef
2. Article values: `no_article` or `with_article` (exact spelling)
3. Number values: `singular` or `plural` (exact spelling)

### Issue: Error loading lesson

**Check:**
1. Tab name matches URL parameter exactly
2. Sheet is shared publicly
3. Rows 1-2 have configuration
4. Row 5 has headers

---

## 💡 Pro Tips

### Tip 1: Copy-Paste from BÍN
Get declensions from: https://bin.arnastofnun.is/

### Tip 2: Use Excel/Sheets Formulas
If you have patterns, use formulas to auto-generate forms.

### Tip 3: Test One Noun First
Start with one complete noun, test it, then add more.

### Tip 4: Keep Consistent Order
Always: no_article singular, no_article plural, with_article singular, with_article plural

---

## 📖 Reference: Case Names

| Abbreviation | Icelandic | English | Question |
|--------------|-----------|---------|----------|
| Nf. | Nefnifall | Nominative | Who/What? |
| Þf. | Þolfall | Accusative | Who/What? (object) |
| Þgf. | Þágufall | Dative | To/For whom? |
| Ef. | Eignarfall | Genitive | Whose? |

---

## ✨ Quick Start Template

Copy this into your sheet:

```
LESSON_TITLE	Lesson 1: Basic Nouns
LESSON_SUBTITLE	Practice noun declensions
		
		
Noun	Article	Number	Nf.	Þf.	Þgf.	Ef.
hestur	no_article	singular	hestur	hest	hesti	hests
hestur	no_article	plural	hestar	hesta	hestum	hesta
hestur	with_article	singular	hesturinn	hestinn	hestinum	hestsins
hestur	with_article	plural	hestarnir	hestana	hestunum	hestanna
```

Then add your own nouns following the same pattern!
