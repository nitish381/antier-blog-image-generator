# Antier Blog Image — Brand & Style Guide

The single source of truth for every Antier blog banner made in this repo.
It is based on the live blog images at https://www.antier.com/blogs/ and the official logo file.
Follow it exactly. When it conflicts with any other file (including older Figma banners), **this guide wins**.

> ## 🔒 FIXED SIZE: every blog image is **931 × 551 px**
> This is a locked rule set by the Antier team. **Do not change it.**
> - It applies to **all** blog images: banners, thumbnails and in-article diagrams.
> - Canvas, Figma frame and exported file are all exactly **931 × 551 px** (aspect ~1.69:1).
> - Don't make 1200×630, 1920×1080, square or any other size unless the team explicitly asks for that one image.
> - If content doesn't fit, simplify or tighten the layout inside 931 × 551. Never grow the canvas.

Reference files:
- `references/blog-banner-choosing-a-blockchain-partner.jpg`: the main style reference (931×551)
- `references/blog-listing-page-full.webp`: the full blog listing page (16 cards + spotlight)
- `brand/logo/antier-mark-original.pdf`: the official mark (Adobe Illustrator export)

---

## 1. Logo: the Antier mark

### Construction (from the official PDF)
Two equal squares touching corner to corner on a diagonal, plus two cyan **quarter circles** that sit
*inside* the squares at the corner where they touch.

```
┌───────┐
│   ◜██ │        ◜ = cyan quarter circle in the bottom-right corner of the top-left square
│  ◜███ │
└───────┼───────┐
        │ ██◞   │ ◞ = cyan quarter circle in the top-left corner of the bottom-right square
        │ ██◞   │
        └───────┘
```

On a 100×100 grid:
- Square A: `x 0–50, y 0–50`
- Square B: `x 50–100, y 50–100`
- Quarter circle 1: centre `(50,50)`, radius `25`, top-left quadrant (inside square A)
- Quarter circle 2: centre `(50,50)`, radius `25`, bottom-right quadrant (inside square B)
- Radius = ½ of the square side. The other two quadrants (top-right and bottom-left) stay **empty**.

> ⚠️ It is **not** a full circle over two squares. The first ERC-3643 Figma banner drew a full circle; that is wrong.

### Files
| File | Use |
|---|---|
| `brand/logo/antier-mark-on-dark.svg` | **Blog banners** (white squares, cyan quarters) |
| `brand/logo/antier-mark.svg` | Light backgrounds (navy squares, cyan quarters) |
| `brand/logo/antier-mark-original.pdf` | Master from Illustrator |

### Logo colours
| Part | On dark (banners) | On light |
|---|---|---|
| Squares | `#FFFFFF` | `#002245` (Antier navy) |
| Quarter circles | `#0C9EDA` (Antier cyan) | `#0C9EDA` |

### Placement on a blog banner (measured from the live 931×551 banner)
- **Size:** 40×40 px at 931 px wide, which is **4.3% of the width**
- **Position:** top-left, **34 px** from the top and left edges (3.65% of the width)
- Alone: no wordmark, no tagline, no box or shadow behind it
- The headline's left edge lines up with the logo's left edge (same x)

---

## 2. Colours

### Brand core
| Name | Hex | Role |
|---|---|---|
| Antier Navy | `#002245` | Logo on light, darkest brand blue |
| Antier Cyan | `#0C9EDA` | Logo accent, glow colour, brand highlight |
| White | `#FFFFFF` | Headline text, logo squares on dark |

### Banner palette (sampled from the live blog images)
| Role | Hex range | Notes |
|---|---|---|
| Background shadows | `#000000` – `#001020` | Most of the frame is near-black or very deep navy |
| Background mid-tones | `#102030` – `#203040` | Dark slate and navy surfaces |
| Steel / stone highlights | `#405060` – `#607080` | Textured 3D surfaces catching light |
| Glow, hottest | `#03F8FD` | Cyan-white core of glowing objects |
| Glow, main | `#00A2F5` | Electric blue |
| Glow, deep | `#0061BC` | Shadowed side of glowing objects |

### Topic accents (only inside the stock image, never on the text)
Most images are blue or cyan. These accents show up for certain topics:
- **Stablecoins:** gold coins
- **Solana and other chains:** purple or magenta
- **RWA / tokenized funds:** blue-violet
- **Formal verification / security:** warm orange-red (rare)
- **Ethereum upgrade:** the only light background (pale blue)

### Extended tokens (Antier Figma variables, for UI and overlays)
navy `#001A36 #002245 #0B3A66 #1E5B8F #4A89B9 #8FB4D8` · cyan `#087FB0 #0C9EDA #2BB4E6 #5CC9EE #8CDDF5 #E6F6FD` · indigo `#3D34D9 #4F46E5 #6C63EC #8B85F3 #B7B4FA`

---

## 3. Typography

> ### 🔒 Headline font rule (fixed)
> **Almarai · Regular (400) · 34 px · letter spacing 4%** · white `#FFFFFF`.
> Use this exact setting for every blog banner headline. Don't change the size, weight or tracking.

| Setting | Value |
|---|---|
| **Font family** | **Almarai** (Google Fonts, weights 300 / 400 / 700 / 800) |
| Headline weight | **Regular 400** (thin, clean: not bold) |
| Colour | `#FFFFFF`, a single colour with no highlighted words |
| Size | **34 px** (fixed, at the 931 × 551 canvas) |
| Line height | ~1.25–1.3 |
| Letter spacing | **4%** |
| Alignment | Left |
| Lines | **2** preferred, 3 at most |
| Line length | ≤ ~32 characters per line (the live line "Choosing a Blockchain Partner?" ≈ 500 px) |
| Text block | Starts at x = 34 px (same as the logo); vertically centred, slightly above the middle (live: y 232–304 at 551 height) |
| Case | Normal sentence or title case as written. Questions end with "?", statements end with "." when there are two sentences. |

Rules:
- Exactly one text element: the **banner line** from the brief. No subtitle, category, date, CTA or URL.
- No text box, panel or gradient card behind the text. The stock image must give a dark, quiet area on the left.
- Check punctuation: no "??", no missing colon or full stop between two clauses.
- Break lines for meaning, e.g. `Choosing a Blockchain Partner?` / `Look Deeper.`

---

## 4. Layout

Canvas: **931 × 551 px, fixed** (~1.69:1), the live blog size. The exported file is exactly 931 × 551 px.

```
┌───────────────────────────────────────────────────────────┐
│ [logo 40px] ← 34px from the top and left                   │
│                                                           │
│                                 ╱╱  stock 3D subject      │
│ Headline line one?           ╱╱  ███ glowing hero         │
│ Headline line two.          ╱╱   ███ object, right 50–60% │
│                                                           │
│ (left ~45%: dark, low-detail area for the text)           │
└───────────────────────────────────────────────────────────┘
```

- **Left ~45%:** text-safe area. It must be dark and low in contrast so white text reads (aim for WCAG contrast ≥ 4.5:1).
- **Right ~55%:** the hero subject (the glowing object), usually right of centre and often cropped by the edge.
- The image fills the whole canvas (full-bleed) with no border or rounded corners.
- **No other sizes.** All blog images stay 931 × 551 (see the fixed-size rule at the top).

---

## 5. Stock imagery style

The live blog uses **premium 3D / CGI stock renders** (the AI-3D style found on Magnific / Freepik).
They are not illustrations, icons, flat vectors or people.

### Signature look
- **Dark, moody scene** (near-black, deep navy or charcoal) with **one bright glowing hero object**.
- **Electric blue / cyan light** is the main glow, from inside the object or as rim light.
- **Material contrast:** rough or matte surfaces (concrete, stone, metal) against glowing glass, crystal or light.
- **Strong perspective and depth:** diagonal beams, tunnels, rings or pillars leading toward the subject.
- Cinematic lighting, shallow depth of field, very little clutter, nothing that looks cartoonish.

### Subject types seen on the live blog
| Type | Live examples |
|---|---|
| Glowing geometric object | Cyan glass cube on concrete beams ("Choosing a Blockchain Partner"), glowing blue card |
| Crypto symbol in 3D | Solana coin with reflection, crystal Ethereum octahedron |
| Coins / tokens | Gold coins floating on blue (stablecoins) |
| Abstract light structures | Fibre-optic strands, data-particle tunnel, concentric light rings, curved ribbons |
| Data and finance | 3D waveform rings, trading candles with glowing panels |
| Real-world photo (industry topics only) | Glass office at night (enterprise), container ship from above (logistics) |

### Picking an image (checklist)
1. Landscape, at least 1862 px wide (so a 931 × 551 crop stays sharp), ideally ~1.7:1
2. Subject sits on the **right half**; the left ~45% is dark and plain
3. The blue / cyan family fits the brand. A topic accent (gold, purple) is fine if the overall mood stays dark.
4. No baked-in text, watermark, logos of other companies or people's faces
5. The subject makes sense for the topic at thumbnail size (~150 px wide on the listing grid)

### Search keyword formulas (Magnific / Freepik stock)
`[topic object] + 3d render + dark background + blue neon glow + cinematic`

| Topic | Search terms |
|---|---|
| Identity / KYC / ERC-3643 | `glowing digital identity shield 3d dark blue`, `holographic id card neon blue 3d`, `fingerprint glass cube glow` |
| Tokenization / RWA | `glowing token coin on pedestal dark 3d`, `glass cube building token blue neon` |
| Stablecoins / payments | `gold coins floating dark blue 3d`, `digital currency flow light trails` |
| DeFi / smart contracts | `glowing blue cube concrete beams 3d`, `abstract blockchain blocks neon dark` |
| Wallets / cards | `glowing blue credit card 3d dark`, `digital wallet light tunnel` |
| Security / audits | `glass shield neon blue dark 3d`, `glowing lock cube dark` |
| Exchanges / trading | `trading candles neon blue 3d dark`, `stock chart holographic panels` |
| Chains (Ethereum, Solana…) | `ethereum crystal 3d dark`, `solana coin purple glow reflection` |
| Infrastructure / enterprise | `server data tunnel blue light`, `glass skyscraper night reflection` |

### Avoid
- Flat illustrations, isometric cartoons, emoji-style icons
- Ring-of-icons diagrams (icon bubbles around a coin). They aren't used on the live blog.
- Bright or white backgrounds (except a rare light one like the Ethereum image)
- Busy detail behind the headline area
- Reusing the same stock image for two posts

---

## 6. Brief format (input)

Each blog brief (a Google Doc) gives:
```
BLOG TITLE- <long title written for search>     → shown under the card on the site, NOT on the image
BANNER- <short hook line>                       → the only text on the image
```
Example: `BLOG TITLE- ERC-3643 Explained: The Evolution of Compliance-Enabled Tokenization`
`BANNER- Bringing Identity and Compliance On-Chain With ERC-3643`
→ Image text: `Bringing Identity and Compliance` / `On-Chain With ERC-3643`

---

## 7. Deliverables per post

| File | Size | Text | Used for |
|---|---|---|---|
| `banner.png` | **931×551** | Logo + banner line | Blog card, spotlight and social sharing |
| `banner-clean.png` | **931×551** | Logo only | Optional thumbnail without text |

Before exporting, check:
- [ ] Canvas and exported file are exactly **931 × 551 px**
- [ ] Almarai Regular, white, one size, 2 lines
- [ ] Logo is correct (quarter circles, not a full circle), 4.3% of width, 34 px margin at 931
- [ ] The headline and logo share the same left edge
- [ ] The left side is dark enough; the headline is readable at 300 px wide
- [ ] Punctuation and casing match the brief
- [ ] The stock image is licensed (Magnific / Freepik) and has no watermark

---

## 8. In-article diagrams (light theme)

Banners are dark. **Diagrams inside the article are light**, using a soft Antier gradient.
Reference: `outputs/erc-3643/diagram-erc-3643-architecture.png` (Figma: Blogs images → `Diagram · ERC-3643 Architecture`).

| Element | Spec |
|---|---|
| Canvas | **931 × 551 px, fixed** (same as banners). Fit the content to this size; don't grow the canvas |
| Background | Diagonal gradient `#F3FBFE` (cyan wash) → `#FFFFFF` → `#EEEDFD` (lilac soft), plus two large blurred glows: cyan `#8CDDF5` top-right and lilac `#B7B4FA` bottom-left |
| Logo | `brand/logo/antier-mark.svg` (navy), 40 px at 44 px from the top and left |
| Title | The doc's `DIAGRAM HEADING`, Almarai ExtraBold 40, `#002245` |
| Subtitle | One line, Almarai Regular 18, `#475569` |
| Hero node | Gradient `#0C9EDA` → `#4F46E5`, radius 20, white text, soft indigo shadow |
| Cards | White, radius 14, border `#E2E8F0`, shadow 0/4/14 navy 6%. Icon in a 40 px `#E6F6FD` box, stroke `#0C9EDA`. Title Almarai Bold 16 `#002245`; description Regular 13/140% `#475569` |
| Layer panels | White at 62% with a background blur, radius 22, a cyan or lilac border, numbered step badge, an uppercase layer label (ExtraBold 13, +8% tracking) and a question-style caption |
| Chips | Pill, Almarai Bold 12. Cyan tone `#E6F6FD`/`#087FB0`; indigo tone `#EEEDFD`/`#3D34D9` |
| Connectors | 2 px, cyan `#0C9EDA` / indigo `#4F46E5`; a dashed line for branching; chevron arrowheads |
| Status | Success `#047857` on `#E7F8F1`; error `#B91C1C` on `#FDECEC`. Only for outcomes |
| Footnote | Almarai Regular 13 `#64748B` with an accuracy disclaimer |

Reusable Figma components: `Diagram/Contract card` (Title, Description, Icon swap), `Diagram/Chip` (Tone = Cyan / Indigo / OnDark), `Icon/*` (section "Components · ERC-3643 diagram").
