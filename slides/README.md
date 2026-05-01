# slides/

Talk PDFs and matching PPTX originals. Filenames are URL-friendly (lowercase, hyphens) so they look clean in deployed URLs.

| File | Used in section | Notes |
|---|---|---|
| `nanoscale-flow-assurance.pdf` / `.pptx` | Talks · Nanoscale flow assurance | |
| `wo-emulsion-simulations.pdf` / `.pptx` | Talks + Course Projects · W/O emulsions | |
| `bim254-crispr-1.pdf` / `.pptx` | (mid-quarter; not displayed but available) | |
| `bim254-crispr-2.pdf` / `.pptx` | Talks + Course Projects · CRISPR final | |
| `hpc-tutorial.pdf` / `.pptx` | Talks · BIM189C HPC tutorial | |
| `jax-tutorial.pdf` / `.pptx` | Talks · JAX tutorial | |

## Adding a new talk

1. Drop both `your-talk.pdf` and `your-talk.pptx` into this folder (lowercase, hyphens).
2. Generate the thumbnail:
   ```bash
   pdftoppm -f 1 -l 1 -r 80 -png your-talk.pdf ../assets/thumbnails/your-talk
   mv ../assets/thumbnails/your-talk-1.png ../assets/thumbnails/your-talk.png
   ```
3. Add a new `<article class="talk-card">` block in `index.html` (copy an existing one and update title/date/file paths).

## Generating PDF from PPTX

If you only have a PPTX, generate a PDF for in-browser preview:
```bash
soffice --headless --convert-to pdf your-talk.pptx
```
