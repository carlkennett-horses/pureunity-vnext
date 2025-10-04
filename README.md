# 🏇 PUREUNITY Corrected Filter — vNext (LTO Locked)

Full‑Parse + REL‑Spread + Guardrail Logic. Runs on **Google Colab (mobile or desktop)** and **VS Code/Jupyter**.

## Files
- `PUREUNITY_Corrected_Filter_vNext.ipynb` — main Colab notebook
- `requirements.txt` — libs: `pdfplumber`, `pandas`

## Quick Start (GitHub → Colab, mobile-friendly)

1. **Create a new GitHub repo** (e.g. `pureunity-vnext`).
2. **Upload** both files above to the repo.
3. Open **Google Colab** in your mobile browser → **GitHub** tab → find your repo → open `PUREUNITY_Corrected_Filter_vNext.ipynb`.
4. Run the first cell to install libraries.
5. In the **config cell**, choose input method:
   - `SELECT_INPUT = 'upload'` to pick a PDF from your phone (Files / iCloud / Downloads).
   - or `SELECT_INPUT = 'drive'` to read a PDF from Google Drive (set `DRIVE_PDF_PATH`).
6. Click **Run** on the **input cell** and follow the prompt to upload/pick a file.
7. Run the **core** and **run** cells to produce the table. Copy the Markdown if needed.
8. (Optional) Run the **export** cell to save `pureunity_vnext_selections.csv` (download from left **Files** pane or save to Drive).

## Input Tips (Mobile)
- Best results if your ATR PDF is the **“Form Printouts”** version (not the preview card).
- **Uploads on iOS/Android:** If the picker closes without selection, try again or save the PDF to Google Drive and use `SELECT_INPUT='drive'`.
- Large PDFs parse fine, but give it a few seconds per page.

## Guardrails
- `< 7 runners` → `No Bet (<7)`
- `7–13` → `—`
- `> 13` → `N (default) / Y (expand)`

## Deterministic Rank (per race)
`REL desc → placings desc → LTO asc → alpha`

## Troubleshooting
- **Empty/partial parse**: confirm the PDF contains selectable text (not a scanned image). ATR printouts are usually text-based.
- **Runner count = 0**: the notebook auto-falls back to using the number of parsed horses.
- **Names look truncated**: ensure the PDF is the ATR “Form Printouts” with standard line layout.

---

© 2025 Carl — use, fork, and tweak as you like.
