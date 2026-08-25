# Fabric Reference Manual — Deployment

This folder is a **self-contained static export** of the Fabric Reference Manual. It contains `index.html`, the compiled CSS/JavaScript, and the recovered image archive under `assets/recovered/`. No server, database, package installation, or build command is required.

All image references in the compiled bundle resolve to local files. The original Pexels, Pixabay, and workbook source metadata remains in the page for attribution and credit links. Fourteen source records could not be recovered from the available metadata; those locations use the clearly labeled `assets/recovered/reference-image-unavailable.svg` fallback. See `IMAGE-RECOVERY.md` for the full accounting.

## GitHub Pages

Upload the **contents of this folder** to the repository root, not the enclosing folder. Enable GitHub Pages for the branch and directory containing `index.html`. Because the site uses relative asset paths, it works both at a custom domain and at a repository subpath such as `https://username.github.io/repository-name/`.

No GitHub Actions workflow or build command is required for this prebuilt export. If GitHub Pages asks for a source, select the branch and root directory containing `index.html`.

## Vercel

Import the repository or deploy the folder with the Vercel CLI. For this prebuilt static export, leave the **Build Command** blank and use the folder containing `index.html` as the project root. Leave the **Output Directory** blank or set it to `.`. Vercel will serve `index.html` and the adjacent `assets/` directory directly.

If the repository contains other projects, set the Vercel **Root Directory** to this folder. Do not point Vercel at the enclosing parent directory unless this folder’s contents are at the repository root.

## General checklist

1. Unzip the archive and upload the contents of this folder, including the complete `assets/recovered/` directory.
2. Confirm that the host serves `index.html` at the site root.
3. Open the deployed homepage and check a few Product Types, Attributes, Patterns, and source-credit links.
4. Do not omit or rename files inside `assets/recovered/`; the compiled JavaScript references those exact relative paths.

## Included recovery records

`IMAGE-RECOVERY.md` summarizes the recovery status. `recovery-report.json` records each metadata record and its local path or fallback status. The other inventory JSON/TXT files are diagnostic manifests and are not required for runtime, but may be retained for future maintenance.
