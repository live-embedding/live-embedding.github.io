# LIVE Project Page

This is the project page for "LIVE: Language-Instructed Vision Embeddings" (ICLR 2026).

## Setup Instructions

### 1. Convert PDF Figures to PNG

The figures are currently in PDF format. You need to convert them to PNG for the web. You can use one of these methods:

**Option A: Using ImageMagick (macOS/Linux)**
```bash
cd assets
for f in *.pdf; do
    convert -density 300 "$f" -quality 95 "${f%.pdf}.png"
done
```

**Option B: Using pdftoppm (Linux)**
```bash
cd assets
for f in *.pdf; do
    pdftoppm -png -r 300 "$f" "${f%.pdf}"
    mv "${f%.pdf}-1.png" "${f%.pdf}.png"
done
```

**Option C: Manual Export**
Open each PDF in Preview (macOS) or any PDF viewer and export as PNG at high resolution (300 DPI recommended).

### 2. Required Image Files

After conversion, ensure you have these PNG files in the `assets/` folder:
- `teaser.png` - Main teaser figure
- `arch.png` - Architecture diagram
- `training_data.png` - Training data generation figure
- `iclip_mmvp.png` - MMVP results visualization
- `retrieval.png` - Retrieval results
- `iclip_att.png` - Attention visualization
- `data.png` - Training data impact analysis
- `comparison.png` - Comparison with baselines

### 3. Update Author Information

Once the paper is de-anonymized, update `index.html`:
1. Replace "Anonymous Authors" with actual author names
2. Replace "Anonymous Institution" with affiliations
3. Update the BibTeX citation at the bottom

### 4. Add Links

Update the link buttons in `index.html` with actual URLs:
- Paper link (arXiv or conference)
- GitHub repository
- Dataset download
- Model weights (HuggingFace, etc.)

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g., `live-project-page`)
2. Push this folder's contents to the repository
3. Go to Settings > Pages
4. Set source to "Deploy from a branch" and select `main` branch
5. Your page will be available at `https://[username].github.io/live-project-page/`

## File Structure

```
project_page/
├── index.html      # Main HTML file
├── style.css       # Stylesheet
├── README.md       # This file
└── assets/         # Images folder
    ├── teaser.png
    ├── arch.png
    ├── training_data.png
    ├── iclip_mmvp.png
    ├── retrieval.png
    ├── iclip_att.png
    ├── data.png
    └── comparison.png
```

## Customization

- **Colors**: Edit CSS variables in `style.css` under `:root`
- **Fonts**: Change Google Fonts import in `index.html`
- **Layout**: Modify sections in `index.html`

## Credits

Website template inspired by [Zero-1-to-3](https://zero123.cs.columbia.edu/).
