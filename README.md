# Cultivation — Fundraising Pipeline Tracker

A visual fundraising pipeline management tool for nonprofits.

## 🚀 Quick Deploy Options

### Option 1: Netlify Drop (Fastest — 2 minutes)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `index.html` file onto the page
3. Done! You'll get a URL like `https://random-name-123.netlify.app`

**To get a custom URL:**
- Create a free Netlify account
- Go to Site settings → Domain management → Change site name
- Change to something like `my-org-cultivation.netlify.app`

---

### Option 2: GitHub Pages (Better for version control)

1. **Create a new GitHub repository**
   - Go to github.com → New repository
   - Name it `cultivation` (or whatever you like)
   - Make it Public
   - Check "Add a README file"

2. **Upload the file**
   - Click "Add file" → "Upload files"
   - Upload `index.html`
   - Commit changes

3. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: `main` / `root`
   - Click Save

4. **Access your site**
   - URL will be: `https://YOUR-USERNAME.github.io/cultivation/`
   - May take 1-2 minutes to go live

---

## ⚙️ Configuration

Click the **⚙️ Settings** button in the app to configure:

- **Annual Goal** — Your total fundraising target
- **Fiscal Year Start** — Which month your fiscal year begins
- **Current Month** — Which month of the fiscal year you're in

All data is saved in your browser's localStorage and persists between sessions.

---

## 📦 Features

- **Drag & drop** opportunities between stages and months
- **Campaigns** that span multiple months with prorated contributions
- **Proportional sizing** — bigger gifts = bigger blocks
- **Progress tracking** with baseline + secured + pipeline fills
- **Export/Import** data as JSON backup

---

## 💾 Data Storage

**For Alpha Testing:**
- Data is stored in browser localStorage
- Each user/browser has their own data
- Data persists until browser data is cleared
- Use Export to backup, Import to restore

**For Production (future):**
- Would need Supabase or similar backend
- Enables multi-user collaboration
- Real-time sync across devices

---

## 🔧 Customization

To change the default configuration, edit the `DEFAULT_CONFIG` object near the top of the JavaScript:

```javascript
const DEFAULT_CONFIG = {
  annualGoal: 400000,        // Total annual fundraising goal
  fiscalStartMonth: 6,       // 0=Jan, 6=Jul, etc.
  fiscalStartYear: 2025,     // Starting year
  currentMonthIndex: 1,      // Which month is "current" (0-indexed)
  defaultTarget: 30000,      // Default monthly target
  defaultBaseline: { name: 'Recurring', recurring: 4000, earned: 2000 }
};
```

---

## 📱 Browser Support

Works best in modern browsers:
- Chrome (recommended)
- Firefox
- Safari
- Edge

Mobile support is limited — desktop recommended for full functionality.

---

## 🐛 Known Limitations (Alpha)

1. **Single user** — Each browser has its own data
2. **No real-time sync** — Changes don't sync between devices
3. **localStorage limits** — ~5MB max (plenty for most use cases)
4. **No undo** — Be careful with deletions!

---

## 📝 Feedback

This is an alpha prototype! Please share feedback on:
- Bugs or broken features
- Confusing interactions
- Missing functionality
- Design suggestions

---

## License

MIT — Free to use and modify.
