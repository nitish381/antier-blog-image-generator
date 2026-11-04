# ERC-3643 Explained: blog banner

**Brief** (Google Doc):
- BLOG TITLE: ERC-3643 Explained: The Evolution of Compliance-Enabled Tokenization
- BANNER: Bringing Identity and Compliance On-Chain With ERC-3643

**Figma:** [Antier AI Design → page "Blogs images"](https://www.figma.com/design/7u6NtOAdW99UfZStzIzQdb/Antier-AI-Design?node-id=322-4086)

| Version | Frame | Status |
|---|---|---|
| V1 | `Blog Banner · ERC-3643 Explained` (951×551) | Kept for comparison. Not on-brand: Inter, full-circle logo, vector coin |
| V2 | `Blog Banner · ERC-3643 · V2 (931×551)` | Brand-aligned: glass token cube on a concrete beam, plus a Magnific image slot |
| V3 | `Blog Banner · ERC-3643 · V3 (931×551)` | Brand-aligned: original isometric layers (identity → compliance → token) |
| **V4** | `Blog Banner · ERC-3643 · V4 (931×551)` | **Stock photo ("Neon Ethereum Coin on Circuit Board") re-graded to Antier blues + ERC-3643 board graphic** |

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

## V3 design decisions
- **Concept:** ERC-3643 as a stack of three glass layers. **On-chain identity** at the top (shield), **compliance rules** in the middle (checked document), **token** at the base (coins).
  - Light links between the layers show that transfers pass through identity and compliance checks.
- **Typography and logo:** same as V2 (Almarai Regular 30/130%, official mark at 40 px with a 34 px margin, text centre at y = 268).
- **Style:** dark navy scene, cyan and indigo glow, an isometric floor grid that fades out, and the left ~45% kept dark for the headline.
- **Icons:** upright and glowing, so they stay readable at the ~150 px blog-grid thumbnail size.
- **All original vector artwork.** The third-party image pasted for reference (a Gate Learn illustration with "Gate Learn" watermarks) was **not used**. Removing those watermarks and publishing the art would use another company's copyrighted work without a licence.

## V4 design decisions
- **Image:** the stock render "Neon Ethereum Coin on Circuit Board" (placed in Figma by the team), cover-cropped at 75% so the coin is the hero, right of centre.
- **Neon removed, non-destructively:**
  - The photo fill is fully desaturated (saturation −1, contrast +0.18, shadows −0.15).
  - A **Color** blend layer (navy `#0B3A66` → `#0061BC` → cyan `#0C9EDA`) re-tints it in Antier blues while keeping all the 3D detail and lighting.
  - A Soft-light cyan lift adds brightness, and a Screen-blend cyan rim and bloom bring back the coin's glow in brand colour.
  - All of these are separate layers, so the original image is untouched.
- **ERC-3643 graphic:**
  - Almarai ExtraBold 50 in white with a layered cyan glow and an embossed shadow, so it reads as lit lettering on the board.
  - Underlined by a circuit trace with pads that echoes the PCB.
  - Laid onto the board plane with an affine transform (rotated and foreshortened to match the board's perspective). It stays editable text.
- **Layout:** BRAND.md as before (logo 40 px with a 34 px margin; Almarai Regular 30/130% headline centred at y = 268; dark left side kept by the scrim, plus a top and bottom vignette).

## Diagram: ERC-3643 Architecture (light theme, 931×551)
From the doc's `DIAGRAM HEADING: ERC-3643 Architecture` and the "How ERC-3643 Connects Identity, Ownership and Compliance" section.
- **Top row:** Sender wallet → `transfer()` → **ERC-3643 Permissioned Token** (ERC-20 compatible; admin roles Mint, Burn, Pause, Freeze and Recover) → Receiver wallet ("executes only if every check passes").
- **Layer 1, Identity:** ONCHAINID, Identity Registry, Identity Registry Storage.
- **Layer 2, Verification:** Trusted Issuers Registry and Claim Topics Registry, with example claims (KYC/AML, accreditation, jurisdiction, issuer-defined).
- **Layer 3, Compliance:** Compliance Contract, its configurable modules, and the transfer outcome (executes / reverts).
- **Footnote:** matches the doc's caption ("original high-level diagram, not a deployment-specific contract map").
- **File:** `diagram-erc-3643-architecture.png` (931×551, matching the fixed blog-image size). Figma frame: `Diagram · ERC-3643 Architecture (931×551, light)`. The earlier 1200×956 version is kept in Figma, marked superseded.

## Diagram v2: ERC-3643 Architecture, pipeline layout (light, 931×551)
Same content as the first diagram, redesigned as a **left-to-right transfer pipeline** that's easier to scan in an article.
- **Flow:** Sender wallet → ① **Identity** (ONCHAINID, Identity Registry, Identity Registry Storage) → ② **Verification** (Trusted Issuers Registry, Claim Topics Registry; KYC/AML, Accredited, Jurisdiction) → ③ **Compliance** (Compliance Contract; investor caps, holding limits, jurisdictions, investor class, offering rules) → Receiver wallet (executes / reverts).
- **Each stage opens with the question it answers**, e.g. "Is the receiver a known, registered investor?".
- **Base bar:** the ERC-3643 Permissioned Token runs along the bottom ("calls checks 1–3 on every transfer"), with dashed links up to each stage and its admin roles (Mint, Burn, Pause, Freeze, Recover).
- **Figma:** `Diagram · ERC-3643 Architecture · Pipeline (931×551, light)`. It uses the new `Diagram/Contract row · Mini` and `Diagram/Chip · Mini` components.
- **File:** `diagram-erc-3643-architecture-pipeline.png` (931×551).

## Files
- `banner-v1.png`: V1 render (1×)
- `banner-v2.png`: V2 render (1×, from Figma; export 2× from Figma for production)
- `banner-v3.png`: V3 render (1×, from Figma; export 2× from Figma for production)
- `banner-v4.png`: V4 render (1×, from Figma; export 2× from Figma for production)
