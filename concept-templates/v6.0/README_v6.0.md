# xsvStudio Email Signatures v6.0

## 📦 Package Contents

### Signature Files (HTML)
- `signature-executive-base64_v6.0.html` - Ian Martin (CEO) with base64 icons
- `signature-executive-hosted_v6.0.html` - Ian Martin with hosted icon URLs
- `signature-division-base64_v6.0.html` - Halie Martin (Office Manager) with base64 icons
- `signature-division-hosted_v6.0.html` - Halie Martin with hosted icon URLs
- `signature-division-halie-martin_v6.0.html` - Halie alternative version

### Icon Source Files (SVG)
Located in `icons-svg/` folder:
1. `verification.svg` - Checkmark badge (16×16 display)
2. `email.svg` - Envelope icon (12×12 display)
3. `phone.svg` - Phone icon (12×12 display)
4. `globe.svg` - Globe icon for contact (12×12 display)
5. `globe-social.svg` - Globe icon for social row (16×16 display)
6. `linkedin.svg` - LinkedIn logo (16×16 display)
7. `youtube.svg` - YouTube logo (16×16 display)
8. `github.svg` - GitHub logo (16×16 display)
9. `instagram.svg` - Instagram logo (16×16 display)

## ✅ What's New in v6.0

### Spacing Improvements
- Verification badge moved closer to name (2px gap, like "Example*")
- Name/title/logo stack tightened (0px margins between)
- Overall signature height reduced ~12px

### Icon Formats
- **base64 versions**: Icons embedded in HTML (portable but may fail in Gmail)
- **hosted versions**: Icons reference URLs (better Gmail compatibility)
- **SVG sources**: For converting to PNG in GIMP

## 🎨 GIMP PNG Conversion Guide

### Why Convert to PNG?
Gmail strips inline SVG and sometimes base64. PNG files hosted on GitHub work reliably.

### Step-by-Step GIMP Workflow

#### 1. Open SVG in GIMP
```
File → Open → Select [icon-name].svg
Import Settings:
  - Width: 64 pixels (for 2x retina sharpness)
  - Height: 64 pixels
  - Resolution: 300 PPI
```

#### 2. Check Transparency
```
Layer → Transparency → Add Alpha Channel
(Ensures transparent background)
```

#### 3. Export as PNG
```
File → Export As
Filename: [icon-name].png
Export Options:
  ✅ Compression level: 9
  ✅ Save color values from transparent pixels
  ❌ Save Exif data (uncheck)
  ❌ Save thumbnail (uncheck)
```

#### 4. Recommended Export Sizes
Different icons need different sizes:

**Contact Icons** (email, phone, globe):
- Export: 24×24px (for 12×12 display @ 2x)
- Or: 32×32px (more headroom)

**Social Icons** (linkedin, youtube, github, instagram, globe-social):
- Export: 32×32px (for 16×16 display @ 2x)
- Or: 48×48px (crisper)

**Verification Badge**:
- Export: 32×32px (for 16×16 display @ 2x)

### 5. Batch Export All Icons
In GIMP:
```
Filters → Batch Processing → David's Batch Processor
(Or manually export each with consistent settings)
```

## 📤 Upload to GitHub

### After Converting SVGs to PNGs:

1. Create `/icons/` folder in your repo root
2. Upload all PNG files:
   ```
   /icons/verification.png
   /icons/email.png
   /icons/phone.png
   /icons/globe.png
   /icons/globe-social.png
   /icons/linkedin.png
   /icons/youtube.png
   /icons/github.png
   /icons/instagram.png
   ```

3. Get raw GitHub URLs:
   ```
   https://raw.githubusercontent.com/xBlynd/xsvStudio-Email-Signature/main/icons/[filename].png
   ```

4. Update signature HTML files to use these URLs instead of base64

## 🔧 SVG vs Base64 vs Hosted PNG

### SVG (Source Files)
- **Pros**: Vector, scales perfectly, small file size
- **Cons**: Gmail blocks inline SVG, doesn't work in email clients
- **Use**: Source files for conversion only

### Base64 Embedded
- **Pros**: Self-contained HTML, no external dependencies
- **Cons**: Gmail strips base64 images on save, icons disappear
- **Use**: Testing only, not production

### Hosted PNG (RECOMMENDED)
- **Pros**: Works in ALL email clients including Gmail
- **Cons**: Requires external hosting (GitHub/your server)
- **Use**: Production signatures after PNG conversion

## 📋 Version Control

### Current Version: v6.0
- Date: January 23, 2026
- Changes: Tight spacing, verification badge positioning

### Next Version: v6.1
When making updates, create new files:
- `signature-executive-base64_v6.1.html`
- Update README to `README_v6.1.md`
- Tag in Git: `git tag v6.1`

## 🚀 Gmail Installation (After PNG Upload)

1. Convert SVGs to PNGs in GIMP (see guide above)
2. Upload PNGs to GitHub `/icons/` folder
3. Update signature HTML with GitHub raw URLs
4. Open signature HTML in browser
5. Select All (Ctrl+A) → Copy (Ctrl+C)
6. Gmail Settings → Signature → Paste
7. Save

## 🐛 Troubleshooting

**Icons not showing in Gmail?**
- Use PNG files, not SVG or base64
- Host on GitHub raw URLs or your server
- Check icon URLs load directly in browser

**Spacing looks wrong?**
- Make sure you're using v6.0 files (tight spacing applied)
- Check browser zoom is 100%

**Badge too far from name?**
- This is fixed in v6.0 (2px gap)
- If still wrong, manually adjust `padding-right` in HTML

---

**Repository**: https://github.com/xBlynd/xsvStudio-Email-Signature
**Support**: Check repo issues or README updates
