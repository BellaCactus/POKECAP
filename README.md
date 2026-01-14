<div align="center">

# POKECAP (google sheets database)

a pokemon database built in **google sheets** with **google apps script** tools.  
designed for fast searching, filtering, and pvp sorting inside the sheet.

static data + simple automation. no backend.

</div>

---

## what is this?

**P.O.K.E.C.A.P.** is a spreadsheet-based pokemon database that helps you:

- browse and organize pokemon data
- quickly filter and search entries
- sort key pvp stats (attack / defense / stamina / overall score)

the goal is simple: make the sheet feel like a usable tool, not just a giant table.

---

## main features

### custom menus (apps script)

when the sheet opens, it adds two custom menus:

#### "Pokedex" menu
- **Hide Everything Except Mega**
- **Hide Everything Except Shadow**
- **Search Pokemon** (exact name match)
- **Search By Type** (partial match in type column)

#### "PVP Menu"
- **Filter by Highest Attack**
- **Filter by Highest Defense**
- **Filter by Highest Stamina**
- **Filter by Highest Overall Score**

---

## how it works (technical)

this project uses **google apps script** to automate actions inside the sheet:

- `onOpen()` injects the menus into the google sheets UI
- search + filter functions hide/show rows based on the query
- pvp functions sort a defined range descending by the chosen stat column

the script uses fixed ranges like:
- pokedex search range: `A4:A14446`
- type range: `B4:B14446`
- pvp sorting range: `A4:R891`

these are editable if your sheet size/layout changes.

---

## how to use (recommended)

### 1) open the sheet
use the template link below, then:
- **File → Make a copy**
so you can run scripts safely in your own version

### 2) enable scripts
the first time you open it:
- allow permissions when google prompts you  
(this is required for custom menus + filtering/sorting to work)

### 3) use the menus
reload the sheet once if needed, then look at the top menu bar for:
- **Pokedex**
- **PVP Menu**

---

## links

```txt
SHEET TEMPLATE:
https://docs.google.com/spreadsheets/d/1ptuq1DLlM3ovBm-CAKQHupEIjNI7pmRUxYxc_wl0BQ4/template/preview?usp=sharing

APPS SCRIPT PROJECT:
https://script.google.com/u/0/home/projects/17_qK2Upog2NM2FDR92Ohs2s_HerP4-L5-3YJbEiQS_SnXdJ7U0-NNYdk/edit
