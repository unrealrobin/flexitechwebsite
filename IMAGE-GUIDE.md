# Flexi Tech Website — Image Guide

## Logo

| File | Format | Notes |
|---|---|---|
| `images/logo.png` | **PNG with transparent background** | Ask whoever made the logo for the transparent version — the black background version will look bad on light pages |

---

## Hero / Background Images (one per page)

These go edge-to-edge behind text. They need to be wide and high-res.

| Page | Suggested Subject | Format | Min Size |
|---|---|---|---|
| Home (`index.html`) | Your most dramatic finished pool — aerial or wide-angle | JPEG | 1920×1080px |
| Services (`services.html`) | Any impressive pool shot | JPEG | 1920×1080px |
| Gallery (`gallery.html`) | Portfolio showstopper | JPEG | 1920×1080px |
| Contact (`contact.html`) | Clean, welcoming pool deck or backyard | JPEG | 1920×1080px |

---

## About / Feature Images

| Location | Suggested Subject | Format | Min Size |
|---|---|---|---|
| Home "About" section | Ken on a job site, or a team photo | JPEG | 800×600px |

---

## Service Detail Images (Services page)

One photo per service, displayed alongside the description text.

| Service | Suggested Shot | Format | Size |
|---|---|---|---|
| Custom Pool Construction | Wide shot of a completed new pool | JPEG | 800×500px |
| Spas & Hot Tubs | Close-up of a built-in spa | JPEG | 800×500px |
| Infinity / Zero-Edge | Dramatic angle showing the edge effect | JPEG | 800×500px |
| Pool Remodeling | Before/after, or a crisp remodeled pool | JPEG | 800×500px |
| Water Features | Waterfall, fountain, or grotto | JPEG | 800×500px |
| Decking & Hardscape | Travertine or paver deck around a pool | JPEG | 800×500px |

---

## Gallery Photos

Save all gallery photos to the `images/gallery/` folder.

**Minimum:** 12 photos to start. More is always better.

**File naming tip:** Use descriptive lowercase names — this helps with SEO.
Examples: `encino-pool-2024.jpg`, `pacific-palisades-spa.jpg`, `woodland-hills-infinity-pool.jpg`

### Category Filter Tags

Each photo in `gallery.html` has a `data-cat` attribute that controls which filter button shows it.

| Tag to use | Filter button it appears under |
|---|---|
| `pool` | Custom Pools |
| `spa` | Spas & Hot Tubs |
| `infinity` | Infinity Pools |
| `remodel` | Remodels |
| `hardscape` | Hardscape |

### How to Add a Gallery Photo

Copy and paste this block inside the `<div class="gallery-full" id="galleryGrid">` section of `gallery.html`, then fill in your details:

```html
<div class="gallery-full-item" data-cat="pool">
  <img src="images/gallery/your-photo.jpg" alt="Description of the pool" loading="lazy" />
  <div class="gallery-overlay">
    <div class="gallery-overlay-content">
      <span class="tag">Custom Pool</span>
      <h4>Your Project Title</h4>
      <p>Encino, CA</p>
    </div>
  </div>
</div>
```

### Layout Modifiers

Add these CSS classes to the `gallery-full-item` div to control the layout:

| Class | Effect | Best for |
|---|---|---|
| *(none)* | Standard square-ish cell | Any photo |
| `wide` | Spans 2 columns | Horizontal/landscape shots |
| `tall` | Spans 2 rows | Vertical/portrait shots |

Example of a wide item:
```html
<div class="gallery-full-item wide" data-cat="infinity">
```

---

## Folder Structure Summary

```
Flexi Tech/
├── index.html
├── services.html
├── gallery.html
├── contact.html
├── style.css
├── IMAGE-GUIDE.md        ← this file
└── images/
    ├── logo.png           ← transparent PNG logo
    ├── hero-home.jpg
    ├── hero-services.jpg
    ├── hero-gallery.jpg
    ├── hero-contact.jpg
    ├── about-team.jpg
    ├── service-pool.jpg
    ├── service-spa.jpg
    ├── service-infinity.jpg
    ├── service-remodel.jpg
    ├── service-water-features.jpg
    ├── service-hardscape.jpg
    └── gallery/
        ├── encino-pool-2024.jpg
        ├── pacific-palisades-spa.jpg
        └── ... (all your project photos)
```
