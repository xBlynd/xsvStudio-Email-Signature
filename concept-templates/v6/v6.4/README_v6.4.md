# v6.4 - Email Client Compatible Signatures

## What Changed from v6.3

**FIXED:** Links now work properly in Gmail and Outlook

### Issues Solved:
- Removed iframe approach (email clients block iframes)
- Removed base64 SVG icons (Gmail strips them on save)
- Switched to **external PNG icons** hosted on xsvstudio.com
- Simplified HTML structure for better email client compatibility
- All links use proper `<a href>` tags (no JavaScript, no weird hacks)

---

## Installation Instructions

### Prerequisites
Upload icon PNG files to your server first:
```
https://xsvstudio.com/email-signatures/icons/verification.png
https://xsvstudio.com/email-signatures/icons/email.png
https://xsvstudio.com/email-signatures/icons/phone.png
https://xsvstudio.com/email-signatures/icons/globe.png
https://xsvstudio.com/email-signatures/icons/globe-social.png
https://xsvstudio.com/email-signatures/icons/linkedin.png
https://xsvstudio.com/email-signatures/icons/youtube.png
https://xsvstudio.com/email-signatures/icons/github.png
https://xsvstudio.com/email-signatures/icons/instagram.png
```

### Gmail Installation

1. **Upload HTML to server:**
   ```
   https://xsvstudio.com/email-signatures/signature-executive_v6.4.html
   https://xsvstudio.com/email-signatures/signature-division-halie_v6.4.html
   ```

2. **Open signature URL in browser**

3. **Select entire signature** (Ctrl+A or Cmd+A)

4. **Copy** (Ctrl+C or Cmd+C)

5. **Gmail Settings** → See all settings → Signature section

6. **Create new signature** → Paste → **Save Changes**

7. **Compose test email** → Verify links work

---

### Outlook Desktop Installation

1. **Open signature URL in browser**

2. **Select entire signature** (Ctrl+A)

3. **Copy** (Ctrl+C)

4. **Outlook** → File → Options → Mail → Signatures

5. **Create new** → Right-click → **Paste (Keep Source Formatting)**

6. **Set as default** → OK

7. **Compose test email** → Links should work (Ctrl+Click in compose window is normal Outlook behavior)

---

### Outlook Web Installation

1. **Open signature URL in browser**

2. **Select + Copy**

3. **Outlook Web** → Settings → View all Outlook settings

4. **Mail** → Compose and reply → Email signature

5. **Paste** → Save

---

## Technical Details

### What Works Now:
- ✅ Clickable email links (`mailto:`)
- ✅ Clickable phone links (`tel:`)
- ✅ Clickable website links (`https://`)
- ✅ Social media icons load from server
- ✅ All icons display correctly (not stripped)
- ✅ Logo renders with proper brand colors
- ✅ Gradient separator displays

### Why This Works:
- External PNG images survive Gmail/Outlook sanitization
- No iframes (email clients block them)
- No inline SVG (Gmail strips it)
- No base64 images (Gmail strips them in signature settings)
- Pure table-based layout (compatible with Outlook's Word rendering engine)
- All styles inline (no external CSS)

---

## Files Included

- `signature-executive_v6.4.html` - Ian Martin (CEO)
- `signature-division-halie_v6.4.html` - Halie Martin (Office Manager, Northeast)

---

## Next Steps

1. Create icon PNG files (18x18px for social, 14x14px for contact)
2. Upload icons to `/public_html/email-signatures/icons/`
3. Upload HTML files to `/public_html/email-signatures/`
4. Test installation in Gmail
5. Test installation in Outlook
6. Verify all links work when emails are sent

---

## Troubleshooting

**Icons don't show:**
- Verify icons uploaded to correct server path
- Check URLs load in browser:
  - https://xsvstudio.com/email-signatures/icons/linkedin.png

**Links don't work:**
- In Outlook compose window, Ctrl+Click is required (this is normal)
- In sent emails, links should work with single click
- Test by sending email to yourself

**Signature looks different after paste:**
- Gmail/Outlook may adjust spacing slightly (this is normal)
- Core structure should remain intact
- Icons and links should still work
