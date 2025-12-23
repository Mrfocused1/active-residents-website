# Active Residents Website - Setup & Testing Guide

## 📊 Step 1: Set Up Google Analytics

### Option A: If you already have a Google Analytics account

1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account
3. Click **Admin** (gear icon in bottom left)
4. Under **Property**, click **Data Streams**
5. Click **Add stream** → **Web**
6. Enter your website URL: `https://www.activeresidents.co.uk`
7. Enter stream name: `Active Residents Website`
8. Click **Create stream**
9. Copy the **Measurement ID** (starts with `G-`)

### Option B: If you need to create a new Google Analytics account

1. Go to [Google Analytics](https://analytics.google.com/)
2. Click **Start measuring**
3. **Account Setup:**
   - Account name: `Active Residents`
   - Check all the data sharing settings (recommended)
   - Click **Next**
4. **Property Setup:**
   - Property name: `Active Residents Website`
   - Reporting time zone: `United Kingdom`
   - Currency: `Pound Sterling (£)`
   - Click **Next**
5. **Business Information:**
   - Industry: `Government and Public Services` or `Technology`
   - Business size: Select your size
   - Click **Next**
6. **Business Objectives:**
   - Select `Get baseline reports`
   - Click **Create**
7. Accept the Terms of Service
8. **Set up data collection:**
   - Platform: **Web**
   - Website URL: `https://www.activeresidents.co.uk`
   - Stream name: `Active Residents Website`
   - Click **Create stream**
9. Copy the **Measurement ID** (looks like `G-XXXXXXXXXX`)

### Step 1.3: Add the ID to your website

Once you have your Measurement ID, I'll help you add it to the website.

**Your Measurement ID:** (save it somewhere safe)
```
G-________________
```

---

## 📱 Step 2: Testing the Mobile Menu

### Desktop Testing (Resize Browser)

1. Open `index.html` in a web browser
2. Press `F12` to open Developer Tools
3. Click the **Device Toolbar** icon (or press `Ctrl+Shift+M` / `Cmd+Shift+M`)
4. Select a mobile device (e.g., "iPhone 12 Pro")

### What to Test

#### ✅ Basic Functionality
- [ ] Hamburger menu icon appears on mobile (below 768px width)
- [ ] Desktop navigation is hidden on mobile
- [ ] Clicking hamburger opens the menu
- [ ] Menu slides down smoothly
- [ ] Icon changes to "X" when menu is open

#### ✅ Navigation
- [ ] All menu links are visible
- [ ] Clicking a link closes the menu
- [ ] Clicking a link navigates to correct section/page

#### ✅ Keyboard Navigation
- [ ] Can tab to hamburger button
- [ ] Pressing Enter opens/closes menu
- [ ] Can tab through menu items
- [ ] Pressing ESC closes the menu

#### ✅ Dark Mode
- [ ] Menu works in both light and dark mode
- [ ] Toggle dark mode button visible and functional

### Test on Real Devices (if possible)

- [ ] iOS Safari (iPhone)
- [ ] Android Chrome
- [ ] iPad Safari

---

## 🔍 Step 3: Testing the Search Feature (Support Page)

### How to Test

1. Open `support.html` in your browser
2. Scroll to the search bar at the top
3. Click in the search input

### Test Scenarios

#### ✅ Basic Search
- [ ] Type "password" → Should show FAQ about password reset
- [ ] Type "location" → Should show FAQ about location services
- [ ] Type "edit" → Should show FAQ about editing reports
- [ ] Type "photo" → Should show "How to use" section about photos

#### ✅ Search Behavior
- [ ] Results appear as you type (after 2 characters)
- [ ] Results update in real-time
- [ ] Shows "No results found" for gibberish text
- [ ] Clicking a result navigates to that section
- [ ] Search results close after clicking a result

#### ✅ Quick Search Links
- [ ] Click "Password Reset" → Populates search with "password"
- [ ] Click "Track Report" → Populates search with "track"
- [ ] Click "Notification Settings" → Populates search with "notification"

#### ✅ Keyboard Navigation
- [ ] Can tab to search input
- [ ] Type and see results
- [ ] Press ESC to close results
- [ ] Can tab through result links
- [ ] Press Enter on a result to navigate

#### ✅ Edge Cases
- [ ] Type 1 character → No results (minimum 2 chars)
- [ ] Click outside search → Results close
- [ ] Type in uppercase → Still finds results (case insensitive)

---

## ⌨️ Step 4: Keyboard Navigation Testing

### Complete Keyboard Navigation Checklist

Use only your keyboard (no mouse!):

#### Index Page (index.html)

**Header Navigation**
- [ ] Tab to logo → Press Enter → Goes to home
- [ ] Tab to "How it Works" → Press Enter → Scrolls to section
- [ ] Tab to "Features" → Press Enter → Scrolls to section
- [ ] Tab to "Stories" → Press Enter → Scrolls to section
- [ ] Tab to "Coverage" → Press Enter → Scrolls to section
- [ ] Tab to dark mode toggle → Press Enter → Toggles theme
- [ ] Tab to "Download App" button → Press Enter → Scrolls to download section

**Mobile Menu** (resize to mobile)
- [ ] Tab to hamburger → Press Enter → Opens menu
- [ ] Tab through menu links
- [ ] Press ESC → Closes menu

**Main Content**
- [ ] Tab to app store buttons → Visible focus ring
- [ ] Tab through testimonial cards
- [ ] Tab through FAQ accordion → Press Enter → Expands/collapses

**Cookie Banner**
- [ ] Tab to "Accept All" → Press Enter → Saves preference
- [ ] Tab to "Essential Only" → Press Enter → Saves preference
- [ ] Press ESC → Closes banner

#### Support Page (support.html)

**Search**
- [ ] Tab to search input → Type → See results
- [ ] Tab through results
- [ ] Press Enter on result → Navigates to section
- [ ] Press ESC → Closes results

**FAQ Accordion**
- [ ] Tab to question → Press Enter → Expands answer
- [ ] Tab to thumbs up/down → Press Enter → Registers feedback

**Contact Buttons**
- [ ] Tab to "Email Support" → Press Enter → Opens email
- [ ] Tab to "Live Chat" → Press Enter → Opens chat (when implemented)

#### Privacy Page (privacy.html)

**Table of Contents**
- [ ] Tab through TOC links
- [ ] Press Enter → Jumps to section
- [ ] Smooth scroll behavior works

**General**
- [ ] All links have visible focus states
- [ ] No keyboard traps (can tab out of everything)
- [ ] Logical tab order (top to bottom, left to right)

---

## 🚀 Step 5: Deploy Sitemap & Robots.txt

### Local Testing First

1. Open Terminal/Command Prompt
2. Navigate to your website folder:
   ```bash
   cd "/Users/paulbridges/active residents website"
   ```
3. Check files exist:
   ```bash
   ls -la sitemap.xml robots.txt
   ```

### Upload to Your Web Server

**Method 1: Using FTP/SFTP Client (FileZilla, Cyberduck, etc.)**

1. Open your FTP client
2. Connect to your web server
3. Navigate to the **root directory** (usually `public_html`, `www`, or `htdocs`)
4. Upload these files to the root:
   - `sitemap.xml`
   - `robots.txt`
5. Verify by visiting:
   - `https://www.activeresidents.co.uk/sitemap.xml`
   - `https://www.activeresidents.co.uk/robots.txt`

**Method 2: Using cPanel File Manager**

1. Log in to your hosting cPanel
2. Click **File Manager**
3. Navigate to `public_html` or your root directory
4. Click **Upload**
5. Upload `sitemap.xml` and `robots.txt`
6. Verify they're in the root directory

**Method 3: Using Git (if using version control)**

```bash
git add sitemap.xml robots.txt
git commit -m "Add sitemap and robots.txt for SEO"
git push origin main
```

### Verification

Visit these URLs to confirm they're accessible:
- https://www.activeresidents.co.uk/robots.txt
- https://www.activeresidents.co.uk/sitemap.xml

---

## 🔎 Step 6: Submit to Google Search Console

### Create Google Search Console Account

1. Go to [Google Search Console](https://search.google.com/search-console/)
2. Sign in with the same Google account as Analytics
3. Click **Add Property**
4. Select **URL prefix**
5. Enter: `https://www.activeresidents.co.uk`
6. Click **Continue**

### Verify Ownership

**Recommended Method: HTML File Upload**

1. Download the verification file (looks like `google1234567890abcdef.html`)
2. Upload it to your website root directory (same as sitemap)
3. Click **Verify**

**Alternative Method: HTML Meta Tag**

I can add this to your HTML head if you prefer this method.

### Submit Your Sitemap

Once verified:

1. In Google Search Console, click **Sitemaps** in the left menu
2. Under "Add a new sitemap"
3. Enter: `sitemap.xml`
4. Click **Submit**
5. Status should change to "Success" after a few minutes

### Monitor Your Site

Google Search Console will now show you:
- How many pages are indexed
- Search performance (clicks, impressions)
- Mobile usability issues
- Security issues
- Manual actions

Check back in 24-48 hours to see data appearing.

---

## 🧪 Bonus: Browser Compatibility Testing

### Desktop Browsers
- [ ] Google Chrome (latest)
- [ ] Mozilla Firefox (latest)
- [ ] Safari (macOS)
- [ ] Microsoft Edge (latest)

### Mobile Browsers
- [ ] Safari (iOS)
- [ ] Chrome (Android)
- [ ] Samsung Internet (Android)

### Things to Check
- [ ] All pages load correctly
- [ ] Dark mode works
- [ ] Animations are smooth
- [ ] No console errors (F12 → Console tab)
- [ ] Images load properly
- [ ] Forms work (search, buttons)

---

## 📞 Need Help?

If you encounter any issues:

1. **Console Errors:** Press F12, check the Console tab for red errors
2. **Mobile Issues:** Test in browser DevTools device emulation first
3. **Analytics Not Working:** Wait 24 hours for data to appear
4. **Sitemap Errors:** Use [XML Sitemap Validator](https://www.xml-sitemaps.com/validate-xml-sitemap.html)

---

## ✅ Final Checklist

Before going live:

- [ ] Google Analytics ID added and tested
- [ ] Mobile menu tested on multiple devices
- [ ] Search feature working on support page
- [ ] All keyboard navigation working
- [ ] Sitemap uploaded and accessible
- [ ] Robots.txt uploaded and accessible
- [ ] Google Search Console verified
- [ ] Sitemap submitted to Search Console
- [ ] Cookie consent banner working
- [ ] All links working
- [ ] Dark mode working on all pages
- [ ] No console errors in browser
- [ ] Images loading correctly
- [ ] Page load speed acceptable

---

**Last Updated:** December 23, 2025
