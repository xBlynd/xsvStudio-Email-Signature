# xsvStudio Email Signatures v4.0
## CustomEsignatures.com Quality Standard

---

## 🎯 **LAYOUTS**

### **1. Executive Left Photo** (`executive-left-photo.html`)
**Photo Effect:** Gradient Ring (rotating border)
**Layout:** Photo LEFT | Info RIGHT
**Best For:** CEO, Executives, Principal
**Features:**
- 100px circular photo with animated gradient border
- Verification badge
- 5-icon social nav bar
- Gradient divider line
- Company tagline

---

### **2. Division Right Photo** (`division-right-photo.html`)
**Photo Effect:** Duotone Overlay (brand color filter)
**Layout:** Info LEFT | Photo RIGHT
**Best For:** Division VPs, Department Heads
**Features:**
- 90px rounded square photo with duotone overlay
- Division-specific logo color
- Division-specific accent colors
- 5-icon social nav bar
- Division tagline

---

### **3. Team Minimal** (`team-minimal.html`)
**Photo Effect:** None (no photo)
**Layout:** Single column, compact
**Best For:** Project Managers, Team Members
**Features:**
- Ultra-compact design
- 3 social icons (LinkedIn, Website, GitHub)
- Solid color divider
- Default tagline

---

## 🎨 **PHOTO EFFECTS REFERENCE**

### **Gradient Ring**
```html
<!-- Outer gradient border -->
<div style="position: absolute; top: -3px; left: -3px; width: 106px; height: 106px; border-radius: 50%; background: linear-gradient(135deg, #5c5edc 0%, #ff6b6b 100%); opacity: 0.8;"></div>
```

### **Duotone Overlay**
```html
<!-- Color filter layer -->
<div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(135deg, rgba(33,150,243,0.6) 0%, rgba(79,195,247,0.3) 100%); mix-blend-mode: multiply;"></div>
```

---

## 🔗 **SOCIAL MEDIA ICONS**

All layouts include:
- **LinkedIn** (Brand blue #0A66C2)
- **Website** (xsvStudio brand color)
- **YouTube** (Red #FF0000)
- **GitHub** (Black #181717)
- **Instagram** (Gradient overlay)

**Hover Effect:** `opacity: 0.7` (can be enhanced with email client CSS support)

---

## 📋 **CUSTOMIZATION INSTRUCTIONS**

### **Replace Photo Placeholder:**
```html
<!-- FIND THIS: -->
<div style="...">
    IM
</div>

<!-- REPLACE WITH: -->
<img src="https://your-photo-url.jpg" style="width: 100%; height: 100%; object-fit: cover;" alt="Your Name" />
```

### **Change Division Color:**
Replace all instances of `#2196f3` (Healthcare blue) with your division color:
- **Healthcare:** `#2196f3`
- **Industrial:** `#ff9800`
- **Technology:** `#9c27b0`
- **Legal:** `#f44336`
- **Real Estate:** `#4caf50`

### **Update Tagline:**
Edit the tagline div at the bottom:
```html
<div style="font-size: 10px; color: #999999; font-style: italic; margin-top: 10px;">
    Your Custom Tagline Here
</div>
```

---

## 🚀 **IMPLEMENTATION STEPS**

1. **Choose Your Layout** (Executive, Division, or Minimal)
2. **Open HTML File** in Chrome or Safari
3. **Select All** (Cmd+A / Ctrl+A)
4. **Copy** (Cmd+C / Ctrl+C)
5. **Gmail:** Settings → General → Signature → Paste
6. **Outlook:** Preferences → Signatures → Paste
7. **Apple Mail:** Mail → Preferences → Signatures → Paste

---

## ✅ **QUALITY STANDARDS MET**

- ✅ CustomEsignatures.com design quality
- ✅ Professional photo treatments
- ✅ Icon + text contact info
- ✅ 5-icon social nav bar with brand logos
- ✅ Gradient dividers and subtle shadows
- ✅ xsvStudio brand consistency
- ✅ Multiple layout options
- ✅ Mobile-responsive HTML tables
- ✅ Email client compatible (Gmail, Outlook, Apple Mail)

---

## 📖 **TAGLINE LIBRARY**

See `../v3/tagline-library.md` for all division-specific tagline options.

**Current Default:** *Solutions Evolved | Building What's Next*

---

**Version:** 4.0  
**Date:** January 16, 2026  
**Design Standard:** CustomEsignatures.com Professional Grade  
**Brand:** xsvStudio