# Manga Scraper

A Next.js web app for scraping manga chapters from online sources, downloading chapter images, and browsing them locally. Built with Mantine UI.

## Features

- **Scraping** — Fetch manga chapters and images from manga sites using Cheerio + Axios
- **Local storage** — Images are saved to `public/manga/{mangaName}/{chapterNo}/`
- **Browse UI** — View your manga library and chapters in a responsive web interface
- **Modern stack** — Next.js 15, React 18, Mantine 7, TypeScript

## Tech Stack

- [Next.js](https://nextjs.org/) 15
- [Mantine](https://mantine.dev/) 7
- [Cheerio](https://cheerio.js.org/) — HTML parsing for scraping
- [Axios](https://axios-http.com/) — HTTP requests

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) (or Node.js 18+)

### Installation

```bash
bun install
```

### Run development server

```bash
bun dev
```

Open [http://localhost:3000](http://localhost:3000).

### Build for production

```bash
bun run build
bun run start
```

## Project structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── home/               # Home page
│   ├── mangas/             # Manga list & chapter viewer
│   └── scraping/           # Scraping interface
├── components/             # Reusable UI components
├── server/
│   ├── routes/             # Server actions (manga listing)
│   └── utils/              # Scraping logic
└── constants.ts
```

## Usage

1. Run the scraper logic (see `src/server/utils/`) to fetch chapters and download images.
2. Images are stored in `public/manga/{mangaName}/{chapterNo}/`.
3. Visit `/mangas` to browse your manga and open chapters.

## License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.

You are free to:

- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material

**Restrictions:**

- **NonCommercial** — you may not use this material for commercial purposes
- **Attribution** — you must give appropriate credit and indicate if changes were made

See [LICENSE](LICENSE) for full terms, or [creativecommons.org/licenses/by-nc/4.0](https://creativecommons.org/licenses/by-nc/4.0/).
