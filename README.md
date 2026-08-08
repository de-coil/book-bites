# Book Bites

A personal library of book reviews and inspiring quotes, built with Astro and deployed on Cloudflare.

## Features

- **Book Reviews** - Browse and read detailed reviews of books with ratings and summaries
- **Inspiring Quotes** - Collection of quotes fetched from an external API
- **Dark/Light Theme** - Toggle between themes with preference saved to localStorage
- **Responsive Design** - Works on all device sizes
- **Static Site Generation** - Fast loading with Astro's SSG
- **Server-Side Rendering** - Quotes page uses SSR for dynamic content

## Tech Stack

- **Framework**: [Astro 7](https://astro.build)
- **UI**: React components with Astro islands
- **Styling**: CSS custom properties for theming
- **Deployment**: Cloudflare Pages
- **Content**: Markdown files with content collections

## Project Structure

```
src/
├── components/
│   ├── BookCard.astro      # Book card component
│   ├── Likes.tsx           # React like button component
│   └── ThemeToggle.tsx     # Theme toggle with localStorage
├── content/
│   └── books/              # Markdown book reviews
├── layouts/
│   └── BaseLayout.astro    # Main layout with navbar
├── pages/
│   ├── index.astro         # Homepage
│   ├── about.astro         # About page
│   ├── books/
│   │   ├── index.astro     # Books listing
│   │   └── [id].astro      # Individual book review
│   └── quotes/
│       └── index.astro     # Quotes page (SSR)
└── styles/
    └── global.css          # Theme variables and global styles
```

## Getting Started

### Prerequisites

- Node.js >= 22.12.0
- pnpm (recommended)

### Installation

```bash
pnpm install
```

### Development

```bash
pnpm dev
```

Starts the development server at `http://localhost:4321`.

### Build

```bash
pnpm build
```

Builds the project for production to the `dist/` directory.

### Preview

```bash
pnpm preview
```

Previews the production build locally.

## Adding Books

Add a new markdown file to `src/content/books/` with the following frontmatter:

```markdown
---
title: "Book Title"
author: "Author Name"
summary: "Brief summary of the book"
rating: 8
---

Your review content here...
```

## Theme System

The site uses CSS custom properties for theming. Theme preference is saved to localStorage and applied on page load to prevent flash of unstyled content.

- **Light theme**: Cream background with golden yellow accents
- **Dark theme**: Dark brown background with warm gold accents

## License

MIT License - see [LICENSE](LICENSE) file for details.
