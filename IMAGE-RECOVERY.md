# Image Recovery Summary

The original image storage host embedded in the compiled site was no longer serving the referenced files. The site has therefore been rewritten to use local assets wherever the original Pexels/Pixabay source could be recovered.

| Result | Count | Detail |
|---|---:|---|
| Source image records found | 407 | Image metadata recovered from the compiled JavaScript bundle. |
| Images downloaded successfully | 393 | Recovered from the original Pexels CDN URLs. |
| Original source records unavailable | 14 | Two retired Pexels URLs, three Pixabay pages whose image payloads were not exposed, and nine records with no source URL in the bundle. |
| Auxiliary storage references replaced | 76 unique endpoints | Pattern/specimen/sheet assets without recoverable source metadata were mapped to a local fallback. |
| Dead storage URLs remaining in the compiled bundle | 0 | All image requests in the shipped JavaScript now resolve locally. |

The repaired site is a static build consisting of `index.html`, the compiled CSS/JavaScript, and `assets/recovered/`. The uploaded `1021DictionarySourceData.xlsx` supplied **66 embedded pattern visuals covering 52 unique pattern IDs**. Those workbook visuals now replace the pattern placeholders in the site. Where a pattern had duplicate workbook visuals, the largest embedded file was selected as the primary image and the source workbook files were preserved in the working recovery manifest. The file `reference-image-unavailable.svg` remains intentionally labeled and is used only where the original image could not be retrieved; it avoids broken-image requests without presenting a fabricated replacement as the original artwork.

The uploaded `1021DictionarySourceData3.xlsx` supplied **24 embedded product visuals covering 18 unique product-type IDs**. These now replace or fill product-image gaps for IDs including PT-037, PT-051, PT-053, PT-064, PT-069, PT-073, PT-075, PT-078, PT-080, PT-085, PT-127, PT-134, PT-142, PT-179, PT-228, PT-229, PT-233, and PT-289. The selected image for duplicate IDs is the largest embedded workbook file; all 18 selected files are stored under `assets/recovered/workbook-v3-PT-*`. The exact mapping is available in `workbook-v3-product-replacements.json`.

The original photographer and source metadata remains in the compiled bundle for the recovered records. The recovery manifest is available in `recovery-report.json`, and the exact replacement map is available in `recovery-replacements.json`.
