# HANDOFF — SD Certified Redesign Project

**Status: COMPLETE.** 20 designs built, verified, hosted.
Last updated: 2026-11-12 (Asia/Calcutta).

---

## 1. The original request (verbatim, as it evolved)

> **"Use graphify and analyse the SDCertified app… complete redesign of all the pages as a plain single html css file, with mock data, to show the client… completely different 10 designs… 10 html css files, add very good animations too, both desktop and mobile views, All should look premium, modern and engaging, all designs should be very different from each other… good images mock data"**

Requirements added across the session, in order:

1. **"SD Certified is an offering of Suresh Drives" must be prominent** on every page (nav, trust band, footer band).
2. **Welcome page first** — every design opens on a welcome/hero page; the flow starts there.
3. **Use local `assets/` images only** — no remote/placeholder image URLs.
4. **"No sub agents — My hardware can't handle it"** — sequential authoring, no subagents, no workflows; lightweight QA only (no Playwright/browser automation).
5. Each design grew from a single file into a **multi-page mini-app**: `styles.css` + 7 linked HTML pages, **zero JavaScript**, Google Fonts as the only external dependency, openable by double-click (`file://`).
6. **"also make 5 more totalling 15 designs with their red theme"** → designs 11–15, red-themed, each visually distinct.
7. **"My client prefers to see more similar designs like design 1 you made, with their red accent/Theme color, Create 5 more new designs similar to design 1, better UX if possible too"** → designs 16–20, all in the aurora-glass family of design 01, red variants, each distinct, with UX upgrades.
8. **"Host all these websites in my personal github account as a single website, list all designs in first page, click on each to see it in detail way"** → one GitHub Pages site: gallery front page + 20 clickable prototypes.
9. **"look at @Deploy Continue Minimal Backend for git details if needed"** — referred session (see §6).
10. **"Can you first confirm you can do the hoisting thing on your own..?"** — confirmed and done.

## 2. Referred website — the content source

**[https://sureshdrives.com](https://sureshdrives.com)** — the parent company. All trust content, contact details and the founder block are taken from this site. The brief in [`BRIEF.md`](BRIEF.md) captures the exact copy.

Key facts, used verbatim on every design:

- **Tagline / footer band (every page):** "**SD Certified is an offering of Suresh Drives** — India's first professional on-site car inspection company. 300+ point checks · AI-powered reports · 10+ years in the automobile industry, Kozhikode, Kerala."
- **Founder block:** Suresh Babu K, founder of Suresh Drives, with the quote *"If a flaw exists, it goes in the report. The buyer should see it before the deal, not after."* Badge "Suresh Drives · Since 2014".
- **Founder images (cropped from the website, stored in `assets/`):** `suresh-face.jpg` (1350×1350 crop), `suresh-founder-poster.jpg` (contact page bio).
- **Parent-company links (footer, every page, `target="_blank" rel="noopener"`):**
  [sureshdrives.com](https://sureshdrives.com) · [/pre-delivery-inspection](https://sureshdrives.com/pre-delivery-inspection) · [/quality-certification](https://sureshdrives.com/quality-certification) · [/sd-assure](https://sureshdrives.com/sd-assure)
- **Contact block:** +91 8330 881 213 (`tel:+918330881213`) · WhatsApp +91 98954 41213 (→ `wa.me/919895441213`) · sureshhdrives@gmail.com · HiLITE Business Park, Poovangal, Kozhikode 673014.
- **Three verbatim testimonials (contact page):** Ashar A. Latheef · Kiran Bose (BMW 530d) · Jayaram R Nair (Dubai).

## 3. Deliverables — where everything lives

| Path | What |
|---|---|
| `SDCertified-Redesigns/` (this folder) | Source of truth: 20 design folders, `assets/` (images), `BRIEF.md`, `_work/` tooling |
| `SDCertified-Redesigns/design-NN-name/` | Each design: `styles.css` + `index.html` + 6 generated pages + skeleton files `_nav.html`, `_foot.html`, `_head.html`, `_meta.txt` |
| `..\sdcertified-redesigns-site\` | Staging copy of the deployed site (git repo) |
| **Live site** | **https://aswinpg.github.io/sdcertified-redesigns/** |
| Repo | `AswinPG/sdcertified-redesigns` — public, branch `main`, GitHub Pages from root |

The front page lists all 20 designs in three groups (Original Ten 01–10, Red Themes 11–15, Aurora Glass · Red Edition 16–20); each card opens that design's welcome page, fully clickable.

## 4. The 20 designs

| # | Folder | Theme |
|---|---|---|
| 01 | `design-01-aurora-glass` | Light aurora glass, Sora+Inter (baseline the client liked) |
| 02 | `design-02-midnight-carbon` | Dark carbon + electric accent |
| 03 | `design-03-editorial-ivory` | Ivory editorial, quiet luxury |
| 04 | `design-04-race-stripe` | Motorsport stripes, condensed type |
| 05 | `design-05-neo-brutal` | Thick borders, hard offset shadows |
| 06 | `design-06-cyber-neon` | Neon-glow dark, grid |
| 07 | `design-07-swiss-mono` | Swiss grid, hairlines, cobalt #0033FF |
| 08 | `design-08-terracotta-clay` | Sand + terracotta, arched frames, Fraunces |
| 09 | `design-09-inspection-terminal` | Terminal-window hero, JetBrains Mono, data-first |
| 10 | `design-10-noir-gold` | Black + champagne gold shimmer |
| 11 | `design-11-crimson-heritage` | Burgundy bg, gold seals, Playfair |
| 12 | `design-12-signal-red-industrial` | Steel grey, safety red, hazard stripes |
| 13 | `design-13-vermilion-editorial` | Warm paper, vermilion, magazine layout |
| 14 | `design-14-scarlet-futurism` | Near-black, scarlet glow, Unbounded |
| 15 | `design-15-cherry-retro-pop` | Cream/cherry, sunburst, polaroid + sticker |
| 16 | `design-16-rose-aurora-glass` | **Red twin of 01** — rose blobs, light |
| 17 | `design-17-ember-dusk-glass` | Dark warm charcoal, ember glow |
| 18 | `design-18-wine-silk-glass` | Deep burgundy, silk bands, Fraunces serif |
| 19 | `design-19-sakura-bloom-glass` | Light sakura pink, drifting petals, pill shapes |
| 20 | `design-20-crimson-holo-glass` | Near-black holo, crimson glow, mono accents |

Every design implements the full shared CSS vocabulary used by the generated pages (see `_work/gen-pages.ps1` for exact markup): `.nav .nav-in .logo .links .menu-btn .menu-toggle .mobile-panel .btn .btn-blue .kick h2.sec .sub .page-hero .crumbs .browse-grid .rail .fg .fl .chips .chip .sortline .count .grid .g3 .car .ph .tagb .tg-plat .tg-gold .tg-silver .feat .body .meta .priceline .price .score .detail .d-img .d-head .d-price .d-cols .d-col .specbar .rep .st .pass .warn .bigscore .bar .wizbar .wstep .n .done .now .form-grid .field .photos .slot .filled .estimate .val .tiers .tier .medal .tagline .plans .plan .hot .pop .for .amt .faq details summary p .founder .founder-photo .frame-e .badge-sd .quote-line .contact-grid .ccard .ic .mapblock .pull .qmark cite footer .foot-grid .offering .foot-bottom .totop`.

**Animation toolkit (pure CSS, per design):** keyframe entrances, `@supports (animation-timeline: view())` scroll-driven bar fills/rises with fallbacks, Ken Burns "breathe" loops on hero images, hover effects gated by `@media (hover:hover) and (pointer:fine)`, and a `prefers-reduced-motion: reduce` kill-switch. Mobile nav is the CSS checkbox hack (see §7).

**UX upgrades in designs 16–20** (the "better UX" ask): `section{scroll-margin-top}` so anchor jumps land under the sticky nav, CSS-only back-to-top link in the footer (`href="#welcome"`), `:focus-visible` rings, ≥44px tap targets, hover-gated transforms, contrast-checked muted colors.

## 5. Mock content per page (identical across all designs, via the generator)

- **index.html (page 1, welcome):** hero + proof band (₹0 brokerage / 300+ points / AI report / 10+ yrs) → trust band ("An offering of Suresh Drives") → founder block (`suresh-face.jpg`) → how-it-works 3 steps → 6 featured cars → CTA strip (₹9,999 flat under ₹10L).
- **browse.html:** filter rail (brand, price, city, grade, fuel) + "16 of 1,248 certified cars" + 16 car cards.
- **vehicle.html:** Bentley Flying Spur 4.0 V8 — Lot SD-2481, Gold, 94/100, ₹3.40 Cr, EMI ₹4,98,500/mo, owner Ramesh K.; spec bars; 300-point report (structure/flood/DTC/road test PASS, paint 2 panels NOTE); score bar; 3 related cars.
- **sell.html:** 4-step wizard on step 2 (Details done / Photos now), KL 09 AB 2481, 15,800 km; photo slots (`bentley-spur-blue.jpg`, `showroom-hall.jpg` filled); estimate ₹3.40 Cr (band ₹3.10–3.65 Cr).
- **certification.html:** verbatim Platinum / Gold / Silver tier copy.
- **pricing.html:** ₹9,999 all-inclusive (₹5–10L) · Custom >₹10L · SD Prime Assist hands-free · 5 FAQs.
- **contact.html:** founder poster bio, 6 contact cards, map block, 3 testimonials.
- Featured cars (6, all designs): RR Phantom VIII ₹4.90 Cr 97/100 Platinum · Bentley Flying Spur ₹3.40 Cr 94 Gold · Maybach GLS 600 ₹2.45 Cr 95 Platinum · BMW X7 xDrive40i ₹1.95 Cr 93 Gold · Ford Mustang GT ₹72 L 93 Gold · Jeep Wrangler Rubicon ₹64 L 90 Gold.
- Nav labels: Home / Browse / Sell / Grades / Pricing / Contact; active link `class="active"`; mobile panel also links vehicle.html.
- Footer on every page: offering band + parent links + contact + "© 2026 SD Certified Cars · Suresh Drives" + Terms · Privacy · Refund & Cancellation.
- Images referenced only as `../assets/<name>` (site root uses `assets/<name>`). Verified asset list in BRIEF.md; all refs audited clean.

## 6. Git / hosting details

- **Referred session** "Deploy Continue Minimal Backend" — the E0ERP repo at `C:\Users\aswin\OneDrive\Documents\GitHub\E0ERP` (org `Epoch-Zero-LLP`). It supplied the git details needed here: the **`gh` CLI is authenticated to account `AswinPG`** (`gh auth status`), git user `Aswin P G` / `aswinpg@outlook.in`.
- Repo created with `gh repo create sdcertified-redesigns --public`; Pages enabled via `gh api repos/AswinPG/sdcertified-redesigns/pages -X POST --input <json-file>` (`{"source":{"branch":"main","path":"/"}}`).
- **gh gotcha:** `gh api --jq` mis-parses in this shell ("accepts 1 arg(s), received 3") — write the JSON to a file and use `--input`, pipe to `Out-String`, skip `--jq`.
- **Update workflow:** edit in `SDCertified-Redesigns/design-NN/` → copy changed files into `..\sdcertified-redesigns-site\design-NN\` → `git commit` + `git push` → Pages rebuilds in ~1 min. The staging folder excludes the `_`-prefixed skeleton files.
- CRLF warnings on commit are harmless.

## 7. Tooling & known gotchas (read before touching anything)

- **Generator:** `_work/gen-pages.ps1` holds the shared body templates ($BODIES for the 6 secondary pages, $CAR_FULL 16 cars, $CAR_3 related). Per-design skeletons: `_nav.html` with `{M-index}`/`{M-browse}`/… markers replaced by ` class="active"`; `_foot.html`; `_head.html` (font links); `_meta.txt` (8 lines: kick titles, crumb, map text, quotes heading).
- **Templates:** `_work/tpl-nav.html`, `tpl-foot.html`, `tpl-head.html` (`{FONTS}` placeholder).
- **Helpers:** `_work/prep.ps1` (BOM-prefix skeletons + generate pages for hand-written designs) and `_work/prep2.ps1` (`Invoke-Prep2 -Design 'name' -Fonts '<link…>'` → materializes tpl skeletons, BOMs them, generates the 6 pages). Run pattern:
  ```powershell
  $root = 'C:\Users\aswin\OneDrive\Documents\GitHub\SureshDrives\SDCertified-Redesigns'
  . "$root\_work\prep2.ps1"
  Invoke-Prep2 -Design 'design-NN-name' -Fonts '<link href="https://fonts.googleapis.com/css2?…" rel="stylesheet" />'
  ```
- **PowerShell 5.1 (`pwsh` here is Windows PowerShell 5.1.26100):** reads BOM-less files as cp1252 → any non-ASCII char in a `.ps1`/skeleton file breaks parsing and produces mojibake (`â€"`) in generated pages. **Keep UTF-8 BOM on `_nav/_foot/_head/_meta.txt` and `gen-pages.ps1`; never re-save without BOM.** `prep.ps1`/`prep2.ps1` handle BOM correctly (`[byte[]](0xEF,0xBB,0xBF)` cast is required — `@(0xEF…)` fails). Avoid non-ASCII in inline `pwsh -Command` strings; write files with the write tool.
- **CSS-only mobile menu rule (critical):** markup must be
  `<input type="checkbox" id="menu" class="menu-toggle">` … `<nav class="mobile-panel">` as **later siblings in the same parent**, and the CSS must be `.menu-toggle:checked ~ .mobile-panel{max-height:420px}`. A descendant form (`.menu-toggle:checked ~ .nav-in .mobile-panel` when the input is inside `.nav-in`) silently fails. **Fixed 2026-11-12 in design-01** — the last remaining instance of this bug.
- **One generator fix 2026-11-10:** inline `style="color:#3c3a33"` in vehicle.html text → `var(--ink)` (invisible on dark themes); all generated pages regenerated.
- **User-reported broken heroes fixed 2026-11-10:** design-11 `rr-cullinan-white.jpg`→`rr-cullinan-bronze.jpg`, design-12 `bentley-baturr.jpg`→`bentley-villa.jpg`, design-13 `rr-dawn-gray.jpg`→`rr-cullinan-road.jpg`. Always re-run the image audit after writing an index.html.

## 8. QA (all green)

- 140 pages (20 designs × 7): every page present, no mojibake, every `../assets/<file>` exists in `assets/`, every internal `href` target exists, encoding clean.
- Live site verified: gallery HTTP 200, design pages HTTP 200, content intact.

**QA command (lightweight, no browser):**
```powershell
$root = 'C:\Users\aswin\OneDrive\Documents\GitHub\SureshDrives\SDCertified-Redesigns'
$assets = (Get-ChildItem "$root\assets" -File).Name
$problems = 0
foreach ($d in (Get-ChildItem $root -Directory | Where-Object Name -match '^design-\d\d')) {
  $pages = Get-ChildItem $d.FullName -Filter *.html | Where-Object Name -notlike '_*'
  if ($pages.Count -ne 7) { "!! $($d.Name): $($pages.Count) pages"; $problems++ }
  foreach ($p in $pages) {
    $t = [System.IO.File]::ReadAllText($p.FullName)
    if ($t -match 'â€') { "!! MOJIBAKE $($d.Name)/$($p.Name)"; $problems++ }
    foreach ($m in [regex]::Matches($t, '\.\./assets/([A-Za-z0-9._-]+)')) { if (-not $assets.Contains($m.Groups[1].Value)) { "!! MISSING IMG $($d.Name)/$($p.Name) $($m.Groups[1].Value)"; $problems++ } }
    foreach ($m in [regex]::Matches($t, 'href="([a-z]+)\.html"')) { if (-not (Test-Path (Join-Path $d.FullName ($m.Groups[1].Value + '.html')))) { "!! BROKEN LINK $($d.Name)/$($p.Name)"; $problems++ } }
  }
}
if ($problems -eq 0) { 'QA PASS' }
```

## 9. Adding design 21+

1. Create `design-21-name/`, write `styles.css` covering the full shared vocabulary (§4) + your theme, write `index.html` (welcome, hero, proof band, trust band, founder, 3 steps, 6 cars, CTA strip, footer).
2. `Invoke-Prep2` (aurora family, tpl skeletons) or `Invoke-Prep` (hand-written skeletons) to generate the 6 secondary pages.
3. Run the §8 QA.
4. Copy the folder (minus `_`-files) into the site repo, commit, push.
5. Add a card to the site's front-page `index.html` grid.

## 10. Standing constraints from the user

No subagents/workflows (weak hardware) · local `assets/` images only · welcome-first · "offering of Suresh Drives" prominent · premium/modern/engaging · designs must look very different from each other · client presentation is the purpose, so copy comes from sureshdrives.com verbatim.
