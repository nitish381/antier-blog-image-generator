# ERC-3643 Explained: blog banner

**Brief** (Google Doc):
- BLOG TITLE: ERC-3643 Explained: The Evolution of Compliance-Enabled Tokenization
- BANNER: Bringing Identity and Compliance On-Chain With ERC-3643

**Figma:** [Antier AI Design → page "Blogs images"](https://www.figma.com/design/7u6NtOAdW99UfZStzIzQdb/Antier-AI-Design?node-id=322-4086)

| Version | Frame | Status |
|---|---|---|
| V1 | `Blog Banner · ERC-3643 Explained` (951×551) | Kept for comparison. Not on-brand: Inter, full-circle logo, vector coin |
| **V2** | `Blog Banner · ERC-3643 · V2 (931×551)` | **Brand-aligned per `BRAND.md`** |

## V2 design decisions
- **Canvas:** 931×551, the same size as the live antier.com blog banners.
- **Logo:** the official mark (two quarter circles, not a full circle), 40 px, 34 px from the top and left edges.
- **Headline:** the brief's banner line only, in Almarai Regular 30 / 130%, white, 2 lines (`Bringing Identity and Compliance` / `On-Chain With ERC-3643`).
  - It shares the logo's left edge and is optically centred (text centre at y = 268, the same as the live reference).
- **Visual concept:** "identity built into the asset". A glowing glass token cube carries an identity shield, at the end of a rough concrete beam.
  - The scene follows the live "Choosing a Blockchain Partner? Look Deeper." banner: dark cinematic 3D, concrete against glowing glass, diagonal depth.
- **Readability:** the left 45% stays dark, with a gradient scrim inside the image layer. The hero object sits right of centre.
- **No extras:** no highlighted words, no icon rings, no text panels.

## Placing the Magnific stock image
This session couldn't reach Magnific: the network proxy blocks magnific.com, freepik.com and api.freepik.com.
So V2's image slot holds a vector 3D placeholder built in the same style. To finish with stock:

1. Find an image on Magnific stock, e.g. `glowing blue glass cube concrete beams 3d dark`,
   `holographic identity shield cube neon blue 3d`, or `digital identity token glass cube dark background`.
   Subject on the right half, left side dark, at least 1920 px wide.
2. In Figma, select **`Image · Magnific stock slot`**, then add an Image fill set to **Fill** (cover).
3. Hide **`Visual · 3D placeholder`**. Keep **`Scrim · Left readability`** on, and lower its opacity if the image is already dark.
4. Export at **2×** (1862×1102) as PNG.

## Files
- `banner-v1.png`: V1 render (1×)
- `banner-v2.png`: V2 render (1×, from Figma; export 2× from Figma for production)
