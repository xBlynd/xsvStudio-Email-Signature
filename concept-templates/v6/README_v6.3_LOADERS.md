# xsvStudio Hosted Email Signatures v6.3

## 🎯 What This Is

Your signatures are now HOSTED on your website (like CustomEsignature):
- https://xsvstudio.com/email-signatures/signature-executive_v6.3.html
- https://xsvstudio.com/email-signatures/signature-division_v6.3.html
- https://xsvstudio.com/email-signatures/signature-division-halie_v6.3.html

Instead of pasting the FULL HTML into Gmail/Outlook (which strips links), you paste a TINY "loader" snippet that fetches it from your server.

---

## 📦 Files in This Package

### Loader Files (Full HTML Pages)
- `loader-executive_v6.3.html` - Full iframe wrapper for Ian
- `loader-division_v6.3.html` - Full iframe wrapper for Halie
- `loader-division-halie_v6.3.html` - Full iframe wrapper for Halie (alt)

### Paste Snippets (Copy These Into Email Clients)
- `PASTE-SNIPPET-executive_v6.3.html` - Code to paste for Ian
- `PASTE-SNIPPET-division_v6.3.html` - Code to paste for Halie
- `PASTE-SNIPPET-division-halie_v6.3.html` - Code to paste for Halie (alt)

---

## 🚀 Installation Instructions

### Step 1: Copy Snippet Code

1. Open `PASTE-SNIPPET-executive_v6.3.html` in text editor (Notepad, VS Code, etc.)
2. **Select ALL** text (Ctrl+A / Cmd+A)
3. **Copy** (Ctrl+C / Cmd+C)

### Step 2: Paste Into Gmail

1. Gmail → Settings ⚙️ → See all settings
2. Scroll to **Signature** section
3. Click in signature text box
4. **Paste** (Ctrl+V / Cmd+V) - you'll see an iframe box
5. **Save Changes**
6. Test: Compose new email → signature should load from server

### Step 3: Paste Into Outlook

1. Outlook → File → Options → Mail → Signatures
2. Click in signature editor
3. Switch to **HTML** view (if available)
4. **Paste** the snippet code
5. Save
6. Test: New email → signature should appear

---

## ⚠️ Known Issue: Email Clients Block Iframes

**Problem:** Gmail and Outlook may strip `<iframe>` tags for security.

**If that happens, I need to create a server-side renderer:**

### Alternative Solution (If Iframes Don't Work)

I'll create a PHP script on your Namecheap server:
```
/email-signatures/render.php
```

This script:
1. Fetches your signature HTML
2. Converts it to a PNG image
3. Returns the image with clickable map areas

Then you paste an `<img>` tag instead of iframe (much more reliable).

---

## 🐛 Troubleshooting

### Signature doesn't appear after pasting
**Cause:** Email client stripped iframe  
**Fix:** Use image-based loader (requires PHP script on your server)

### Links don't work
**Cause:** iframe is sandboxed  
**Fix:** Add `sandbox="allow-same-origin allow-top-navigation"` to iframe tag

### Signature looks wrong
**Cause:** iframe size too small  
**Fix:** Adjust width/height in loader snippet

---

## 📞 Next Steps

1. **Try the paste snippet first** (see if iframe works)
2. **If iframe is stripped**, I'll create the PHP image renderer
3. **If that doesn't work**, we'll use server-side email signature API (like CustomEsignature's backend)

---

## 🔧 Technical Details

### How CustomEsignature Does It

They use a combination of:
1. Hosted HTML signature (you've done this ✅)
2. Server-side image rendering with click map
3. Fallback to plain HTML if images blocked

For xsvStudio, the full solution needs:
- PHP script to render HTML → image
- Image map overlay for clickable links
- Fallback plain HTML version

I can build this on your Namecheap cPanel if iframe method fails.

---

**Try the paste snippet now and let me know if iframe loads or gets stripped.**
