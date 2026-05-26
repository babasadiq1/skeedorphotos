# 🎯 SKEEDOR PHOTOS — COMPLETE BEGINNER'S GUIDE
### How to set up, customise, and publish the website (no coding experience needed)

---

## WHAT YOU HAVE

Inside your `skeedor-photos` folder you have **one file**:
```
skeedor-photos/
  └── index.html   ← This IS the entire website
```
That single file contains everything — the design, layout, animations, and logic.

---

## STEP 1 — PREVIEW THE WEBSITE ON YOUR COMPUTER

You don't need VS Code or any software to preview it.

1. Open the `skeedor-photos` folder on your computer
2. Double-click `index.html`
3. It will open in your browser (Chrome, Edge, Firefox — any works)
4. You'll see the full website!

> ⚠️ Note: The photos will show as brown colour blocks for now.
> You'll replace them with real photos in Step 3.

---

## STEP 2 — EDIT THE TEXT CONTENT

To edit any text, you need a simple text editor.

### Which editor to use (free, no installation needed on Windows):
- **Notepad** (already on your PC — search "Notepad" in the Start menu)
- Or download **Notepad++** from https://notepad-plus-plus.org (better, free)

### On Mac:
- Use **TextEdit** (comes built-in)

### How to open and edit:
1. Right-click on `index.html`
2. Click "Open with" → choose Notepad (or Notepad++)
3. Press **Ctrl + H** (Find & Replace) to change text easily

---

### THINGS TO CHANGE IN THE FILE:

Search for these and replace with your client's real info:

| Search for this | Replace with |
|---|---|
| `Bauchi · Nationwide` | Client's real city/location |
| `hello@skeedorphotos.com` | Client's real email |
| `+234 800 000 0000` | Client's real phone number |
| `@skeedorphotos` | Client's real Instagram handle |
| `Est.` year `2019` | Year Skeedor Photos was founded |
| `₦80,000` | Real portrait session price |
| `₦350,000` | Real wedding package price |
| Testimonial names and quotes | Real client testimonials |
| About section paragraphs | Real photographer bio |
| `© 2025 Skeedor Photos` | Current year if needed |

---

## STEP 3 — ADD REAL PHOTOS

### Prepare your photos:
- Get the photos from your client (WhatsApp, Google Drive, etc.)
- Save them into the **same folder** as `index.html`
- Rename them simply: `photo1.jpg`, `wedding1.jpg`, etc. (no spaces in names!)
- Recommended size: **1200px wide** is ideal (not too huge, not too small)

### Hero section (the 4-photo grid at the top):

Find this in the file (there are 4 like this):
```html
<div class="img-placeholder photo-a" style="height:100%"></div>
```

Replace each one with:
```html
<img src="your-photo-name.jpg" style="width:100%; height:100%; object-fit:cover;">
```

Example — to use a photo called `wedding1.jpg`:
```html
<img src="wedding1.jpg" style="width:100%; height:100%; object-fit:cover;">
```

### Portfolio grid (the masonry/column section):

Find lines like:
```html
<div class="masonry-photo photo-a" style="height: 380px"></div>
```

Replace with:
```html
<img src="portfolio1.jpg" class="masonry-photo" style="height:380px; object-fit:cover; width:100%;">
```

### About section (photographer photo on the left):

Find:
```html
<div class="about-photo"></div>
```

Replace with:
```html
<img src="photographer.jpg" style="width:100%; height:100%; object-fit:cover; min-height:600px;">
```

---

## STEP 4 — SET UP THE CONTACT FORM (Free, takes 5 minutes)

Right now the form doesn't send emails. Here's how to make it work for free:

1. Go to **https://formspree.io** in your browser
2. Click "Get Started" and sign up with an email
3. Click "New Form" and give it a name like "Skeedor Contact"
4. Formspree will give you a link that looks like:
   `https://formspree.io/f/abcdefgh`
5. Open `index.html` in Notepad
6. Find this line:
   ```html
   <form action="#" method="POST" id="contactForm">
   ```
7. Replace the `#` with your Formspree link:
   ```html
   <form action="https://formspree.io/f/abcdefgh" method="POST" id="contactForm">
   ```
8. Save the file. Done! Form submissions now go straight to your client's email.

---

## STEP 5 — PUBLISH THE WEBSITE ONLINE (Free)

### Option A — Netlify (EASIEST, recommended, 100% free)

1. Go to **https://www.netlify.com** and sign up (free)
2. After logging in, look for "Sites" on the left
3. At the bottom of the page it says **"drag and drop your site folder here"**
4. Drag your entire `skeedor-photos` folder into that box
5. Netlify gives you a live link like: `https://random-name.netlify.app`
6. Share that link with your client — the website is LIVE!

### To update the site later:
Just drag the folder again — Netlify replaces it automatically.

### Get a custom domain (e.g. www.skeedorphotos.com):
1. Buy a domain from **Namecheap** (https://namecheap.com) — costs around $10-15/year
2. In Netlify, go to Site Settings → Domain Management → Add custom domain
3. Follow the steps — Netlify walks you through it

---

### Option B — GitHub Pages (also free, slightly more steps)

1. Create a free account at **https://github.com**
2. Click the "+" button → "New repository"
3. Name it `skeedor-photos`, make it Public, click Create
4. Click "uploading an existing file" and upload your `index.html` and all your photo files
5. Go to Settings → Pages → Source: select "main" branch → Save
6. Your site will be live at: `https://yourusername.github.io/skeedor-photos`

---

## STEP 6 — SOCIAL MEDIA LINKS

In the footer, find these lines and replace `#` with real URLs:

```html
<a href="#" class="social-link" target="_blank">Instagram</a>
<a href="#" class="social-link" target="_blank">Pinterest</a>
<a href="#" class="social-link" target="_blank">TikTok</a>
```

Replace like this (example):
```html
<a href="https://www.instagram.com/skeedorphotos" class="social-link" target="_blank">Instagram</a>
```

---

## COMMON QUESTIONS

**Q: Why does the website look different from the preview Claude showed me?**
A: The brown colour blocks are placeholders for photos. Once you add real photos (Step 3), it will look great.

**Q: Can I change the gold colour to something else?**
A: Yes! In the CSS at the top of the file, find `--gold: #C4973A;` and change `#C4973A` to any colour code you want. Google "colour picker" to find hex codes.

**Q: How do I add more portfolio photos?**
A: Copy one of the `<div class="masonry-item">` blocks and paste it below the others. Change the photo source and category.

**Q: My client wants a WhatsApp button. How do I add one?**
A: Add this anywhere in the HTML (change the number):
```html
<a href="https://wa.me/2348000000000" style="position:fixed; bottom:24px; right:24px; background:#25D366; color:white; padding:14px 20px; border-radius:50px; text-decoration:none; font-size:13px; z-index:999;">
  💬 WhatsApp
</a>
```

**Q: How do I save my changes?**
A: In Notepad, press **Ctrl + S**. Then refresh the browser tab where the website is open.

**Q: The website looks broken. What happened?**
A: Most likely a missing `>` or `"` somewhere. Press **Ctrl + Z** in Notepad to undo your last changes, one by one, until it works again.

---

## QUICK CHECKLIST BEFORE SENDING TO CLIENT

- [ ] Client name "Skeedor Photos" appears correctly everywhere
- [ ] Real email address added
- [ ] Real phone number added
- [ ] Real location added
- [ ] Real photos added (no brown placeholders)
- [ ] Real prices updated
- [ ] Real testimonials added
- [ ] Social media links updated
- [ ] Contact form connected to Formspree
- [ ] Website published on Netlify (or GitHub Pages)
- [ ] Custom domain connected (if client wants one)

---

## NEED HELP?

Come back to Claude and describe what you're stuck on — paste the exact part of the code you're trying to change and ask for help. Claude can rewrite any part of the file for you.

---
*Guide created for Skeedor Photos website — built with HTML/CSS/JS, no frameworks needed.*
