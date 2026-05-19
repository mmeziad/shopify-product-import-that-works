# shopify-product-import-that-works

If you've ever tried importing products into Shopify with variants and multiple images, you know how painful it gets. Wrong rows, broken image links, variants merging when they shouldn't, hours of trial and error just to find out one column was named wrong.

This is a Claude skill that fixes that.

You give it two files — your new product spreadsheet and your existing Shopify export — and it figures out the rest. It maps your columns to Shopify's format, handles all the weird multi-row logic for images and variants, catches duplicates before they cause problems, and gives you a test file to check before generating the full import.

---

## What it does

- Maps columns from any source spreadsheet to your store's Shopify format
- Handles multiple images and multiple variants correctly (the multi-row/handle structure that breaks everything)
- Detects duplicates and conflicts before you import
- Generates a small test file first so you can verify it works
- Produces a clean, ready-to-import CSV

---

## What you need

- [Claude Code](https://claude.ai/code) or Claude with skills support
- A spreadsheet of new products (any format — supplier CSV, Excel, whatever)
- An export of your existing Shopify products (from Shopify Admin → Products → Export)

---

## Install

**Via Claude Code plugin system:**
```bash
/plugin marketplace add mmeziad/shopify-product-import-that-works
/plugin install shopify-product-import@mmeziad-skills
```

**Or manually:**
```bash
git clone https://github.com/mmeziad/shopify-product-import-that-works ~/.claude/skills/shopify-product-import
```

---

## How to use it

Once installed, just tell Claude what you're trying to do:

> "I have a supplier CSV and a Shopify export, help me build an import file"

It'll walk you through the rest — column mapping, filters, duplicate handling, test file, full file.

---

## Why this exists

Shopify's CSV import is powerful but unforgiving. The docs don't make it clear which fields do what, image rows have to be in exactly the right order, and one wrong column name silently breaks everything. I built this because I kept running into the same problems and wanted a way to get it right the first time.

---

## License

MIT — use it, fork it, improve it.
