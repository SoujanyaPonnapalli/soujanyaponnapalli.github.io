# CV page images (`cv1.png` … `cv4.png`)

These are the pages of `soujanya-cv.pdf`, shown on `/cv/`. Regenerate them
whenever the CV changes, in two steps.

## 1. Render each page

```bash
pdftoppm -png -scale-to-x 1554 -scale-to-y -1 soujanya-cv.pdf /tmp/cv
```

1554px wide keeps the images at the size the page has always used. Add or
remove `cvN.png` files if the CV gains or loses a page, and update the
`<img>` list in `_pages/cv.md` to match.

## 2. Trim the vertical page margins

Each PDF page carries roughly 150-175px of white at the top and bottom. Left
as-is, two of those margins stack between consecutive images and the page
reads as a series of separated sheets rather than one continuous document.
Trim them to a uniform 40px, keeping the full width so the text columns stay
aligned across pages:

```python
from PIL import Image
PAD = 40
for i in (1, 2, 3, 4):
    im = Image.open(f'/tmp/cv-{i}.png')
    g = im.convert('L'); w, h = im.size; px = g.load()
    ink = lambda y: any(px[x, y] < 245 for x in range(0, w, 3))
    top = 0
    while top < h and not ink(top): top += 1
    bot = h - 1
    while bot > top and not ink(bot): bot -= 1
    im.crop((0, max(0, top - PAD), w, min(h, bot + 1 + PAD))).save(f'images/cv{i}.png')
```

Only the height changes; every image stays 1554px wide.
