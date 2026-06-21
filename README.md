# Meridian Journal — Travel Blog

A professional, multi-page travel blog built with pure HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies — open the file and it works.

---

## Features

- **4 pages** — Home, Destinations, About, and Contact — built as a single-page app (SPA) with JS-powered navigation
- **6 full articles** with rich editorial content including pull quotes, tips, and section headings
- **Live search** — filters articles in real time as you type
- **Region tabs** — filter stories by Asia, Europe, Africa, Americas, and Oceania
- **Dynamic article renderer** — each article is stored as structured data and rendered on the fly
- **Destinations page** — organised by continent with 16 destinations across 4 regions
- **Contact form** with validation and a success message on submit
- **Newsletter signup** with basic email validation
- **Responsive layout** — works on desktop, tablet, and mobile with a hamburger menu

---

## Tech Stack

| Layer | Detail |
|-------|--------|
| HTML | Semantic, single-file structure |
| CSS | Custom properties (variables), Flexbox, CSS Grid, responsive breakpoints |
| JavaScript | Vanilla JS, no libraries or frameworks |
| Fonts | Google Fonts — Playfair Display (display) + Inter (body) |

---

## Project Structure

Everything lives in one file: `travel-blog.html`

```
travel-blog.html
├── <style>
│   ├── CSS custom properties (color palette, typography)
│   ├── Navigation
│   ├── Home page (hero, cards, sidebar, featured strip)
│   ├── Destinations page
│   ├── Article page
│   ├── About & Contact pages
│   ├── Newsletter bar & Footer
│   └── Responsive breakpoints (@media)
│
├── HTML
│   ├── <nav> — sticky top bar with search input
│   ├── #page-home — hero section, trending strip, article grid, sidebar
│   ├── #page-destinations — continents + destination cards
│   ├── #page-article — dynamically populated by JS
│   ├── #page-about — team grid, stats
│   ├── #page-contact — form with validation
│   ├── Newsletter bar
│   └── Footer with column links
│
└── <script>
    ├── articles[] — data array for all 6 articles
    ├── renderArticleCards() — filter and render card grid
    ├── setTab() — region tab switching
    ├── handleSearch() — real-time search filtering
    ├── showPage() — SPA page navigation
    ├── showArticle() — dynamic article page renderer
    ├── filterRegion() — trending strip quick filter
    ├── toggleMobileMenu() — hamburger nav for mobile
    ├── subscribeNewsletter() — newsletter input validation
    └── submitForm() — contact form handling
```

---

## Pages

### Home
- Full-width dark hero with headline and CTA
- Gold trending strip with region quick-filters
- Editor's Pick featured article (large card)
- Tabbed article grid filterable by region
- Sidebar: popular destinations, travel quote, trip planner widget

### Destinations
- Organised by continent (Asia, Africa, Americas, Europe)
- 16 destination cards with emoji, description, and category tag
- Clicking a card opens the related article if one exists

### About
- Team stats (countries, writers, stories, years)
- Editorial philosophy section
- 4-person team grid with roles and countries covered

### Contact
- Form with name, email, subject dropdown, and message fields
- Success message on valid submission
- Sidebar with alternative contact emails and a pitch guide

---

## Design

The design uses an editorial palette inspired by print journalism:

| Token | Value | Use |
|-------|-------|-----|
| `--ink` | `#1A1A18` | Body text, dark backgrounds |
| `--gold` | `#B8860B` | Accent, CTAs, highlights |
| `--gold-light` | `#F5EFD6` | Soft background tints |
| `--paper` | `#FAFAF7` | Page background |
| `--white` | `#ffffff` | Cards, nav |

Typography pairs **Playfair Display** (serif, for headings and display text) with **Inter** (sans-serif, for body and UI).

---

## How to Use

1. Download `travel-blog.html`
2. Open it in any browser
3. No server, no install, no build step required

To add a new article, add an object to the `articles` array in the `<script>` section:

```js
{
  id: 'unique-id',
  region: 'asia',              // asia | europe | africa | americas | oceania
  regionLabel: 'Asia · Japan',
  title: 'Your Article Title',
  excerpt: 'Short summary shown on the card.',
  author: 'Author Name',
  authorInitials: 'AN',
  date: 'June 20, 2025',
  readTime: '7 min',
  emoji: '🏯',
  bg: 'linear-gradient(135deg, #color1, #color2)',
  lead: 'Opening paragraph shown in italic at the top of the article.',
  content: [
    { type: 'p', text: 'A paragraph of body text.' },
    { type: 'h2', text: 'A section heading' },
    { type: 'pullquote', text: 'A standout quote.' },
    { type: 'tip', title: 'Tip Label', text: 'Practical tip text.' }
  ]
}
```

---

## License

Free to use and modify for personal and commercial projects.
