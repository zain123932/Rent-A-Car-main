# 🚗 Rent a Car

A responsive, multi-page car rental website built with **HTML, CSS and JavaScript**. It showcases a premium and vintage fleet, customer reviews, blog stories and a login/sign-up flow, with a dark/light theme switcher and smooth animations throughout.

> **Note:** This is a front-end project. There is no backend or database, so login, booking, reviews and the newsletter are UI demonstrations only (see [Known Limitations](#-known-limitations)).

---

## 📑 Table of Contents

- [Features](#-features)
- [Pages](#-pages)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Theming](#-theming)
- [Responsive Design](#-responsive-design)
- [Known Limitations](#-known-limitations)
- [Roadmap](#-roadmap)
- [Team](#-team)
- [License](#-license)

---

## ✨ Features

- **Dark / Light theme** with a custom animated sun-and-moon toggle. The choice is saved in `localStorage`.
- **Hero image slider** on the home page, with auto-play and fade transitions (Slick Carousel).
- **3D flip "Top Picks" cards** that open like a book to reveal car specs and a rent button.
- **Fleet catalogue** with category tags (Vintage, Luxury, SUV, Economical), specs and daily/monthly prices in PKR.
- **Customer reviews** page with a rating summary, review cards and an interactive star-rating form.
- **Blog** with a featured story and "Read More / Read Less" expandable articles.
- **Login / Sign-up** page with a glassmorphism card, a looping video background and a form toggle.
- **Embedded Google Map** and contact details on the home page.
- **Fully responsive layout** with a hamburger menu for tablets and phones.
- **Shared header and footer** design across all pages, including a newsletter sign-up field.

---

## 📄 Pages

| Page | File | Description |
| --- | --- | --- |
| Home | `index.html` | Hero section, car slider, "Find Us" map and contact details |
| Cars | `cars.html` | Top Picks 3D cards and the full car grid |
| About | `about.html` | Company story, stats bar and team section |
| Reviews | `review.html` | Rating summary, customer reviews and a review form |
| Blogs | `blog.html` | Featured story and expandable articles |
| Login | `login.html` | Log In and Sign Up forms over a video background |

---

## 🛠 Tech Stack

| Category | Technology |
| --- | --- |
| Markup | HTML5 |
| Styling | CSS3 (Flexbox, Grid, CSS variables, media queries, 3D transforms, glassmorphism) |
| Scripting | JavaScript (ES6), jQuery 3.7.1 |
| Slider | [Slick Carousel](https://kenwheeler.github.io/slick/) 1.9.0 |
| Icons | [Font Awesome](https://fontawesome.com/) 6.5.1 |
| Font | [Montserrat](https://fonts.google.com/specimen/Montserrat) (Google Fonts) |
| Maps | Google Maps Embed |

All libraries are loaded from CDNs, so there is **nothing to install or build**.

---

## 📁 Project Structure

```
rent-a-car/
├── index.html
├── cars.html
├── about.html
├── review.html
├── blog.html
├── login.html
├── script.js              # Slider, theme switcher, mobile menu, login/signup logic
├── README.md
│
├── styles/
│   ├── style.css          # Global reset, fonts, home page hero and location section
│   ├── theme.css          # Colour variables (dark/light) and theme toggle styles
│   ├── navbar.css         # Header, navbar and page-specific header overrides
│   ├── footer.css         # Footer and newsletter styles
│   ├── slider.css         # Slick slider fixes
│   ├── responsive.css     # Media queries for all pages
│   ├── cars-style.css     # Cars page styles
│   ├── about-style.css    # About page styles
│   ├── review-style.css   # Reviews page styles
│   ├── blog-style.css     # Blog page styles
│   └── login-style.css    # Login page styles
│
└── assets/                # Images, car photos, icons and loginbg.mp4
```

---

## 🚀 Getting Started

### Prerequisites

A modern web browser (Chrome, Edge, Firefox or Safari) and an internet connection, since the fonts, icons and libraries load from CDNs.

### Run locally

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<your-repo>.git

# 2. Go into the project folder
cd <your-repo>

# 3. Open the site
# Double-click index.html, or use a local server (recommended):
npx serve .
# or with the VS Code "Live Server" extension: right-click index.html → Open with Live Server
```

### Deploy

Because the site is fully static, it can be hosted for free on **GitHub Pages**, **Netlify** or **Vercel**. Just point the host at the project's root folder.

---

## 🎨 Theming

Colours are controlled by CSS variables defined in `styles/theme.css`. Dark mode is the default. Adding the `light-mode` class to `<body>` switches every variable to its light value.

```css
:root            { --primary-color: #fff;     --background-color: #15173a; }
body.light-mode  { --primary-color: #1d1f2c;  --background-color: #f4f6f8; }
```

The theme toggle in `script.js` adds or removes `light-mode` and stores the preference under the `theme` key in `localStorage`.

To change the brand colours, edit these values in `styles/style.css`:

```css
--secondary-color: #ed1329;   /* Red accent */
--tertiary-color:  #ff8938;   /* Orange accent */
```

---

## 📱 Responsive Design

Breakpoints are defined in `styles/responsive.css`:

| Breakpoint | Behaviour |
| --- | --- |
| ≤ 1024px | Hero stacks vertically, map and details stack |
| ≤ 992px | Hamburger menu replaces the navbar, footer becomes 2 columns |
| ≤ 900px | About, Reviews and Blog layouts switch to a single column |
| ≤ 600px | Car grid, review grid and Top Picks become single column |
| ≤ 576px | Footer becomes a single column |
| ≤ 500px | Login card and form rows adjust for small phones |

---

## ⚠️ Known Limitations

This project is a front-end demo. Please be aware of the following:

- **Login and sign-up are simulated.** Any phone number and password will "log in", and no data is stored or verified. Do **not** enter real personal data such as a real CNIC or address.
- **Booking buttons** ("Rent" and "Book Now") do not open a booking flow yet.
- **Review form** does not save or display new reviews. Existing reviews are sample content.
- **Newsletter forms** do not submit anywhere.
- **Placeholder content:** reviews, prices and car details are sample data for demonstration.

---

## 🗺 Roadmap

- [ ] Booking form with date picker and price calculator
- [ ] Real authentication with a backend (Node.js / Firebase)
- [ ] Save and display reviews dynamically
- [ ] Search, filter and sort on the Cars page
- [ ] Prevent the theme "flash" on page load by applying the saved theme in `<head>`
- [ ] Load the shared header and footer from a single file
- [ ] Form validation with proper accessibility labels
- [ ] Multi-language support (English / Urdu)

---

## 👥 Team

| Name | Role |
| --- | --- |
| Ms. Sara Mishal Sajid | Project Instructor |
| Mahad Abbas | Founder and Designer |
| Zaryab Khan | Technical Lead |
| Sheeri Abid | Web Manager |

---

## 📜 License

Add your preferred license here (for example, MIT) and include a `LICENSE` file in the repository.

---

<p align="center">Made with ❤️ for car lovers · © 2025 Rent a Car</p>