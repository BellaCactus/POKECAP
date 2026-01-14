<div align="center">

# <3 POKECAP (google sheets database)

a pokemon database built in **google sheets** with **google apps script** tools.  
fast searching, filtering, and pvp sorting inside a spreadsheet.

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-database-ff78c8?style=for-the-badge)
![Apps Script](https://img.shields.io/badge/Google%20Apps%20Script-automation-ff4db8?style=for-the-badge)
![Static](https://img.shields.io/badge/No%20Backend-static%20tool-0b0b0b?style=for-the-badge)

</div>

---

## what is this?

**P.O.K.E.C.A.P.** is a spreadsheet-based pokemon database that helps you:

- browse and organize pokemon data
- quickly filter and search entries
- sort key pvp stats (attack / defense / stamina / overall score)

the goal is simple: make the sheet feel like an actual tool, not just a giant table.

---

## features

### custom menus (apps script)

when the sheet opens, it adds two custom menus:

**Pokedex menu**
- **Hide Everything Except Mega**
- **Hide Everything Except Shadow**
- **Search Pokemon** (exact name match)
- **Search By Type** (partial match)

**PVP Menu**
- **Filter by Highest Attack**
- **Filter by Highest Defense**
- **Filter by Highest Stamina**
- **Filter by Highest Overall Score**

---

## how it works (technical)

this project uses **google apps script** to automate actions inside the sheet:

- `onOpen()` injects custom menus into google sheets
- search + filter functions hide/show rows based on the query
- pvp functions sort a defined range by chosen stat columns

the script currently uses fixed ranges (edit these if your sheet changes):

- pokedex search range: `A4:A14446`
- type range: `B4:B14446`
- pvp sorting range: `A4:R891`

---

## how to use

### 1) open the sheet
use the template link below, then:
- **File -> Make a copy**
so you can run scripts in your own copy safely

### 2) enable scripts
the first time you open it:
- accept the google permissions prompt  
(this is required for menus + filtering/sorting)

### 3) use the menus
reload the sheet once if needed, then use:
- **Pokedex**
- **PVP Menu**

---

## links

```txt
SHEET TEMPLATE:
https://docs.google.com/spreadsheets/d/1ptuq1DLlM3ovBm-CAKQHupEIjNI7pmRUxYxc_wl0BQ4/template/preview?usp=sharing

APPS SCRIPT PROJECT:
https://script.google.com/u/0/home/projects/17_qK2Upog2NM2FDR92Ohs2s_HerP4-L5-3YJbEiQS_SnXdJ7U0-NNYdk/edit
