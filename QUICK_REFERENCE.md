# Active Residents - Quick Reference Card

## 🚀 Getting Started in 5 Minutes

### 1. Test Your Website Locally

```bash
# Open in default browser (macOS)
open index.html

# Or just double-click these files:
- index.html (landing page)
- support.html (support center)
- privacy.html (privacy policy)
- test-functionality.html (testing dashboard)
```

### 2. Test Mobile Menu

1. Open any page in browser
2. Press `F12` → Click device icon (phone/tablet)
3. Click hamburger menu (☰)
4. ✓ Menu should slide down
5. ✓ Icon changes to X
6. Press `ESC` to close

### 3. Test Search (Support Page Only)

1. Open `support.html`
2. Type in search box: "password"
3. ✓ Should show results instantly
4. Click a result to navigate

### 4. Test Dark Mode

1. Click moon/sun icon in header
2. ✓ Page switches to dark theme
3. Reload page
4. ✓ Theme persists

### 5. Add Google Analytics

**File to edit:** `index.html`
**Line number:** 691
**Find:** `const GA_ID = 'G-XXXXXXXXXX';`
**Replace with:** `const GA_ID = 'G-YOUR-ACTUAL-ID';`

---

## 📁 File Structure

```
/active residents website/
├── index.html              # Landing page
├── support.html           # Support/Help center
├── privacy.html           # Privacy policy
├── sitemap.xml           # SEO sitemap
├── robots.txt            # Search engine instructions
├── test-functionality.html # Testing dashboard
├── SETUP_GUIDE.md        # Complete setup guide
└── QUICK_REFERENCE.md    # This file
```

---

## 🔗 Important URLs (After Deployment)

| Page | URL |
|------|-----|
| Home | https://www.activeresidents.co.uk/ |
| Support | https://www.activeresidents.co.uk/support.html |
| Privacy | https://www.activeresidents.co.uk/privacy.html |
| Sitemap | https://www.activeresidents.co.uk/sitemap.xml |
| Robots | https://www.activeresidents.co.uk/robots.txt |

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Tab` | Navigate through page |
| `Enter` | Activate button/link |
| `ESC` | Close menu/search/banner |
| `Space` | Toggle checkbox/button |
| `F12` | Open browser dev tools |
| `Cmd+Shift+M` | Toggle device emulation (macOS) |
| `Ctrl+Shift+M` | Toggle device emulation (Windows/Linux) |

---

## 🎨 Design System

### Colors
- **Primary Blue:** #3B82F6
- **Primary Hover:** #2563EB
- **Background Light:** #F0F7FF (or #F4F7FE for privacy page)
- **Background Dark:** #0F172A
- **Text Light:** #1E293B (#333344 for privacy page)
- **Text Dark:** #F8FAFC

### Fonts
- **Display (Headings):** Merriweather
- **Body Text:** Inter

### Border Radius
- Default: 1rem (16px)
- XL: 1.5rem (24px)
- 2XL: 2rem (32px)
- 3XL: 3rem (48px)

---

## 🐛 Troubleshooting

### Mobile menu not working
```javascript
// Check console (F12) for errors
// Make sure JavaScript is enabled
// Try clearing browser cache (Cmd+Shift+R or Ctrl+F5)
```

### Search not working
```javascript
// Only works on support.html
// Make sure you're typing 2+ characters
// Check console for JavaScript errors
```

### Dark mode not persisting
```javascript
// Clear localStorage: localStorage.clear()
// Toggle dark mode again
// Reload page to test
```

### Cookie banner not appearing
```javascript
// Clear localStorage: localStorage.clear()
// Wait 1.5 seconds after page load
// Should appear automatically
```

---

## 📤 Deployment Checklist

### Before uploading:
- [ ] Google Analytics ID added
- [ ] Test all features locally
- [ ] No console errors
- [ ] All images load
- [ ] All links work

### Upload these files to your web server root:
- [ ] index.html
- [ ] support.html
- [ ] privacy.html
- [ ] sitemap.xml
- [ ] robots.txt

### After uploading:
- [ ] Test on live URL
- [ ] Verify sitemap: yourdomain.com/sitemap.xml
- [ ] Verify robots: yourdomain.com/robots.txt
- [ ] Submit sitemap to Google Search Console
- [ ] Wait 24-48 hours for Google Analytics data

---

## 🔍 SEO Checklist

### Google Search Console
1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add property: `https://www.activeresidents.co.uk`
3. Verify ownership (HTML file or meta tag)
4. Submit sitemap: `sitemap.xml`

### Google Analytics
1. Go to [analytics.google.com](https://analytics.google.com)
2. Create property for your website
3. Copy Measurement ID (G-XXXXXXXXXX)
4. Add to index.html line 691

### Check Indexing (After 1-2 weeks)
```
Google Search: site:www.activeresidents.co.uk
```
Should show all your pages.

---

## 🧪 Testing Tools

### Browser DevTools
- **F12** - Open dev tools
- **Console** - Check for errors
- **Network** - Check load times
- **Lighthouse** - Performance audit

### External Tools
- [PageSpeed Insights](https://pagespeed.web.dev/)
- [Mobile-Friendly Test](https://search.google.com/test/mobile-friendly)
- [Rich Results Test](https://search.google.com/test/rich-results)
- [XML Sitemap Validator](https://www.xml-sitemaps.com/validate-xml-sitemap.html)

---

## 📱 Mobile Testing

### Resize Browser Method
1. Open page in Chrome/Firefox
2. Press `F12`
3. Click device toolbar icon
4. Select device (iPhone 12, iPad, etc.)
5. Test all features

### Real Device Method
- Test on actual iPhone/Android
- Test on actual iPad/Tablet
- Check all features work
- Verify text is readable
- Ensure buttons are tappable

---

## 💡 Tips & Best Practices

### Dark Mode
- Respects system preference on first visit
- Stores user preference in localStorage
- Synced across all pages

### Cookie Consent
- Shows once per browser
- "Accept All" = enables analytics
- "Essential Only" = no tracking
- Fully GDPR compliant

### Search Feature
- Minimum 2 characters to search
- Real-time results
- Searches FAQ and content
- Keyboard navigable

### Accessibility
- All interactive elements keyboard accessible
- Proper ARIA labels throughout
- Screen reader friendly
- Proper heading hierarchy

---

## 🆘 Need Help?

### Check the Console
1. Press `F12`
2. Click "Console" tab
3. Look for red errors
4. Copy error message

### Common Issues

**"Cannot read property of undefined"**
- JavaScript error
- Check if element IDs match
- Verify file loaded correctly

**"Failed to fetch"**
- Network/CORS error
- Test on actual web server, not file://
- Check file paths

**Styles not loading**
- Clear cache (Cmd+Shift+R)
- Check if Tailwind CDN loads
- Verify no CSS errors in console

---

## 📊 Analytics Events Tracked

Once Google Analytics is set up, these events are tracked:

- **Page Views** - Automatic
- **Cookie Consent** - When user accepts/declines
- **Link Clicks** - External links (if configured)
- **Search Queries** - Support page searches (if configured)

---

## ✅ Pre-Launch Final Check

Run through this before going live:

- [ ] All pages open without errors
- [ ] Mobile menu works on phone screen size
- [ ] Search works on support page
- [ ] Dark mode toggles correctly
- [ ] All links navigate correctly
- [ ] Images load properly
- [ ] Favicon shows in tab
- [ ] Cookie banner appears on first visit
- [ ] Google Analytics ID is correct
- [ ] Sitemap.xml is accessible
- [ ] Robots.txt is accessible
- [ ] No JavaScript errors in console
- [ ] Pages load in under 3 seconds
- [ ] Test on iPhone Safari
- [ ] Test on Android Chrome

---

**Last Updated:** December 23, 2025
**Version:** 1.0

For detailed setup instructions, see `SETUP_GUIDE.md`
For interactive testing, open `test-functionality.html`
