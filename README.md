# Aditya Agarwal — The Digital Wardrobe 🧥

> *A bespoke single-file portfolio website crafted with code, data, creativity & intelligence.*

---

## 🧥 Overview

**The Digital Wardrobe** is a fully self-contained single-file HTML portfolio for **Aditya Agarwal**, a B.Tech CSE (AI & ML) student at AKTU, Python Developer, and Co-Founder of PANKH. The site uses a wardrobe/tailoring atelier metaphor throughout — every section, animation, and interaction is woven around the craft of bespoke tailoring as a parallel to software craftsmanship.

---

## 🗂️ Live Sections

| Section | Wardrobe Name | Description |
|---|---|---|
| Hero | The Wardrobe | Curtain-reveal entrance with animated name stitching |
| About | The Tailor's Studio | Bio, stats, and timeline of experience |
| Education | Folded Fabrics of Knowledge | Degrees, CGPA, and certifications |
| Skills | The Wardrobe of Skills | Tabbed skill panels with animated progress bars |
| Projects | Garments of Code | Project cards hung on wardrobe hangers |
| Contact | The Fitting Room | Contact info + EmailJS-powered mail form |

---

## ✨ Features

- **Curtain reveal hero** — two fabric panels part on load, revealing the portrait and name
- **Custom tailor-needle cursor** — animated needle with a trailing bronze thread
- **Name stitch animation** — each letter of "ADITYA AGARWAL" stitches in individually
- **Floating particles** — subtle linen-toned dust motes drifting upward
- **Wardrobe skill tabs** — five panels (Web Dev, Data Science, ML, AI & GenAI, Vibe Coding) with live progress bar fills and "Stitching" badges for skills in progress
- **Project garment cards** — each project hangs on a rendered clothes hanger
- **Contact form** with EmailJS integration, field validation, `.com` email check, and a bronze particle burst on success
- **Footer curtain close** — curtains draw shut as the footer enters view
- **Hero tilt** — subtle 3D parallax tilt on mouse movement
- **Scroll reveal** — all sections animate in on scroll via IntersectionObserver

---

## 🛠️ Tech Stack

| Layer | Used |
|---|---|
| Structure | HTML5 (single file) |
| Styling | CSS3 — custom properties, clip-path, keyframe animations |
| Fonts | Google Fonts — Cinzel, Lato, Crimson Pro |
| Interactivity | Vanilla JavaScript (no frameworks) |
| Email | [EmailJS](https://www.emailjs.com/) `@emailjs/browser@4` |
| Rendering | Canvas API (cursor thread + particles) |

---

## 🚀 Setup & Deployment

This is a **zero-dependency single-file site** — no build step, no npm, no bundler.

### 1. Clone / Download
```bash
git clone https://github.com/AdityaAg7/digital-wardrobe.git
# or just download final_website.html
```

### 2. Configure EmailJS

The contact form uses [EmailJS](https://www.emailjs.com/) to send mail without a backend. Before deploying, replace the three placeholders in `final_website.html`:

```js
// Near the bottom of the file — EmailJS init
emailjs.init({
    publicKey: "YOUR_PUBLIC_KEY",   // ← Your EmailJS Public Key
});

// Inside the sendBtn click handler
emailjs.send(
    "YOUR_SERVICE_ID",              // ← Your EmailJS Service ID
    "YOUR_TEMPLATE_ID",             // ← Your EmailJS Template ID
    { ... }
)
```

**How to get these values:**
1. Sign up at [emailjs.com](https://www.emailjs.com/)
2. Create an **Email Service** (Gmail, Outlook, etc.) → copy the **Service ID**
3. Create an **Email Template** with variables `{{from_name}}`, `{{from_email}}`, `{{subject}}`, `{{message}}` → copy the **Template ID**
4. Go to **Account → API Keys** → copy your **Public Key**

### 3. Deploy

Drop `final_website.html` anywhere:

| Platform | How |
|---|---|
| **GitHub Pages** | Push to repo → Settings → Pages → Deploy from branch |
| **Netlify** | Drag & drop the file at [netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | `vercel --prod` in the folder |
| **Any static host** | Upload the single `.html` file — done |

---

## ✏️ Customisation

Everything lives in one file. Key spots to update:

| What | Where in file |
|---|---|
| Name, tagline, bio | `#hero` and `#about` sections in HTML |
| Profile photo | Replace the emoji `🧵` in `.portrait-img-wrap` with an `<img>` tag |
| Timeline / experience | `.timeline-rope` items in `#about` |
| Projects | `.project-garment` cards in `#projects` |
| Skills & percentages | `--skill-pct` values on `.skill-patch` elements |
| Colour palette | `:root` CSS variables at the top of `<style>` |
| Contact details | `.contact-line` items in `#contact` |

---

## 🎨 Color Palette

| Token | Hex | Role |
|---|---|---|
| `--linen` | `#D2B8A3` | Body text, muted elements |
| `--warm-brown` | `#A68773` | Labels, secondary text |
| `--fabric-white` | `#E8DDD3` | Primary text |
| `--bronze` | `#B87333` | Accents, borders, highlights |
| `--dark-shadow` | `#4E342E` | Mid-depth backgrounds |
| `--deep` | `#2A1A14` | Page background |
| `--thread` | `#C8913A` | Cursor thread, glow effects |

---

## 📬 Form Validation

The contact form validates:
- **Name & Email** — required; shows browser native tooltip *"This field can't be empty"* with red border on empty submit
- **Email format** — must end in `.com`; shows tooltip *"Please use an email address ending in .com"*
- **Sending state** — button animates with spinning needle + pulsing glow
- **Success** — bronze particle burst + styled confirmation banner
- **Error** — graceful red-toned "Thread Snapped" message with retry

---

## 🌐 Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Custom cursor is desktop-only; falls back to default on touch devices.

---

## 👤 Author

**Aditya Agarwal**
B.Tech CSE (AI & ML) · AKTU · Co-Founder @ PANKH

- GitHub: [github.com/AdityaAg7](https://github.com/AdityaAg7)
- LinkedIn: [linkedin.com/in/aditya-agarwal-b32523302](https://www.linkedin.com/in/aditya-agarwal-b32523302/)
- Email: agarwal.aditya.7026@gmail.com

---

*Crafted with Code, Data, Creativity & Intelligence.*
