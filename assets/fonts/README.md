# Self-hosted fonts

## TeX Gyre Pagella (`texgyrepagella-*.woff2`)

Palatino, to match the CV. The CV's PDF embeds `URWPalladioL-Roma` and
`URWPalladioL-Bold` (LaTeX's `mathpazo`/`palatino` package); TeX Gyre Pagella is
GUST's Unicode-extended version of that very same URW Palladio L design, so the
site and the CV render from the same typeface.

**Licence:** GUST Font License (GFL) — an LPPL-style free licence that
explicitly permits redistribution and web embedding.
<https://www.gust.org.pl/projects/e-foundry/licenses>

Note that macOS also ships a `Palatino.ttc`, but that is Apple's licensed system
font and must **not** be converted or self-hosted. It is only ever used via the
system font stack, off the visitor's own disk.

### How these are loaded

`_sass/_variables.scss` lists system Palatino first:

    "Palatino Linotype", "Palatino", "Book Antiqua", "URW Palladio L", "TeX Gyre Pagella", Georgia, serif

so macOS and Windows visitors render from disk and download nothing. Only
visitors without a local Palatino fetch these files. They are intentionally not
`<link rel="preload">`ed, since preload fetches unconditionally and would charge
every visitor for a font most of them already have.

### Regenerating

Source: <https://www.gust.org.pl/projects/e-foundry/tex-gyre/pagella>
(`qpl2_501otf.zip`). Requires `fonttools` and `brotli`.

    RANGES="U+0000-00FF,U+0100-017F,U+0180-024F,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+2000-206F,U+2070-209F,U+20A0-20BF,U+2100-214F,U+2190-2193,U+2212,U+2215,U+FEFF,U+FFFD"
    for s in regular italic bold bolditalic; do
      pyftsubset "texgyrepagella-$s.otf" \
        --unicodes="$RANGES" \
        --layout-features='kern,liga,clig,calt,onum,pnum,frac' \
        --flavor=woff2 \
        --output-file="texgyrepagella-$s.woff2"
    done

Subsetting to Latin + Latin Extended takes the four faces from 864K of OTF to
144K of WOFF2. The range covers the accented names that appear in the
publication lists (Zsolt István, Nathanaël Cheriere, and so on).
