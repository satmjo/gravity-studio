# 📷 Gravity Studio — Photo Showcase Website

A dark, cinematic photography portfolio built for **Gravity Studio**.  
Hosted for free on **Vercel**. No coding experience needed after setup.

---

## 📁 Project Structure

```
gravity-studio/
├── index.html          ← Main website page
├── photos.json         ← 📌 YOUR PHOTO LIST (edit this to add photos)
├── vercel.json         ← Vercel hosting config
├── css/
│   └── style.css       ← All visual styles
├── js/
│   └── app.js          ← Gallery logic
└── photos/
    ├── portraits/      ← Put portrait JPGs here
    └── wedding/        ← Put wedding JPGs here
```

---

## 🚀 First-Time Setup (Do Once)

### Step 1 — Install Git
Download from https://git-scm.com/downloads and install.

### Step 2 — Create a GitHub account
Go to https://github.com and sign up (free).

### Step 3 — Create a new GitHub repository
1. Click the **+** icon → "New repository"
2. Name it: `gravity-studio`
3. Keep it **Public**
4. Click **Create repository**

### Step 4 — Upload this project to GitHub
Open Terminal (Mac/Linux) or Git Bash (Windows) inside your `gravity-studio` folder:

```bash
git init
git add .
git commit -m "Initial: Gravity Studio website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gravity-studio.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

### Step 5 — Deploy to Vercel
1. Go to https://vercel.com and sign up with your GitHub account
2. Click **"Add New Project"**
3. Select your `gravity-studio` repository
4. Click **Deploy** — done! ✅

Your site will be live at: `https://gravity-studio.vercel.app`

---

## 📸 How to Add Your Own Photos

### Step 1 — Prepare your photos
- Save photos at **2K resolution** (2000–2560px wide)
- Format: **JPG** recommended (smaller file size, faster loading)
- Name files clearly: `portrait-aasha-01.jpg`, `wedding-sharma-ceremony.jpg`

### Step 2 — Put photos in the right folder
```
photos/portraits/   ← Portraits & People photos go here
photos/wedding/     ← Wedding photos go here
```

### Step 3 — Add entries to photos.json
Open `photos.json` and add a new entry inside the `"photos": [ ]` array.

**Template to copy:**
```json
{
  "id":       "p7",
  "category": "portraits",
  "title":    "Your Photo Title",
  "location": "Kathmandu, Nepal",
  "year":     "2025",
  "thumb":    "photos/portraits/your-photo.jpg",
  "full":     "photos/portraits/your-photo.jpg"
}
```

> 💡 **Pro tip:** You can use the same file for both `thumb` and `full`.
> The browser loads the image at different display sizes automatically.
> For best performance, optionally save a separate compressed thumb at ~800px wide.

**For wedding photos**, change `"category": "wedding"` and path to `photos/wedding/`:
```json
{
  "id":       "w7",
  "category": "wedding",
  "title":    "The First Dance",
  "location": "Hyatt Regency, Kathmandu",
  "year":     "2025",
  "thumb":    "photos/wedding/first-dance.jpg",
  "full":     "photos/wedding/first-dance.jpg"
}
```

**Categories available:**
- `"portraits"` → shows under Portraits tab
- `"wedding"` → shows under Wedding tab

### Step 4 — Publish to the web

After adding your photos and updating `photos.json`, run:

```bash
git add .
git commit -m "Add new photos — [date]"
git push
```

Vercel automatically detects the push and **redeploys in ~30 seconds**. 🎉

---

## 🔧 Customization

### Change your email address
Open `index.html`, find this line and replace with your email:
```html
<a href="mailto:hello@gravitystudio.com" class="contact-cta">hello@gravitystudio.com</a>
```

### Change the footer location text
Search for `Kathmandu, Nepal` in `index.html` and update as needed.

### Change accent color (gold)
Open `css/style.css`, find:
```css
--gold: #C9A84C;
```
Replace with any color you like.

### Add a custom domain (e.g. gravitystudio.com.np)
1. Buy a domain from a registrar (Namecheap, Google Domains, etc.)
2. In Vercel dashboard → your project → **Settings → Domains**
3. Add your domain and follow the DNS instructions

---

## 💡 Tips for Great Photos

- **Portrait orientation** (tall) photos create variety in the masonry grid
- Mix portrait and landscape orientations for a dynamic layout
- Aim for **consistent color grading** across your portfolio
- Keep file sizes under **3MB per photo** for fast loading (use tools like [Squoosh](https://squoosh.app))
- Add a **descriptive title** — it shows in the lightbox and adds elegance

---

## ❓ Troubleshooting

| Problem | Solution |
|---|---|
| Photos not showing | Check the file path in `photos.json` matches exactly (case-sensitive) |
| Site not updating | Wait 1 minute after `git push`, then hard-refresh (Ctrl+Shift+R) |
| Images slow to load | Compress photos using [Squoosh](https://squoosh.app) — aim for <2MB |
| Deploy failing | Check `photos.json` for missing commas using [JSONLint](https://jsonlint.com) |

---

## 📬 Support

Built with ♥ for Gravity Studio · Kathmandu, Nepal
