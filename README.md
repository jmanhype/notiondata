# NotionData

A modern web application built with Astro and TailwindCSS.

## 🚀 Project Overview

This project is built using [Astro](https://astro.build), a modern static site generator that delivers lightning-fast performance. The site includes:

- **Modern UI Components**: Pre-built navigation, hero section, footer, and card components
- **TailwindCSS Styling**: Utility-first CSS framework for rapid UI development
- **TypeScript Support**: Type-safe development experience
- **SEO-Friendly**: Optimized meta tags and semantic HTML

## 📁 Project Structure

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Card.astro         # Reusable card component
│   │   ├── Footer.astro       # Site footer
│   │   ├── HeroSection.astro  # Hero/landing section
│   │   └── NavBar.astro       # Navigation header
│   ├── layouts/
│   │   └── Layout.astro       # Base page layout
│   └── pages/
│       └── index.astro        # Home page
├── tailwind.config.cjs        # TailwindCSS configuration
├── astro.config.mjs           # Astro configuration
└── package.json
```

## 🛠️ Setup & Installation

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd notiondata
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Install Astro Tailwind Integration** (required for TailwindCSS)
   ```bash
   npm install @astrojs/tailwind
   ```

4. **Update `astro.config.mjs`** to enable Tailwind:
   ```javascript
   import { defineConfig } from 'astro/config';
   import tailwind from '@astrojs/tailwind';

   export default defineConfig({
     integrations: [tailwind()],
   });
   ```

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 🎨 Available Components

### NavBar
Navigation header with menu, product links, search, cart, and sign-in options.

### HeroSection
Landing page hero section with headline, description, and call-to-action button.

### Footer
Site footer with copyright and social media links.

### Card
Reusable card component for displaying links with title, description, and hover effects.

## 📝 Development Notes

- **TailwindCSS**: Components in `src/components/` use Tailwind utility classes. Ensure the Tailwind integration is properly configured.
- **TypeScript**: The project uses TypeScript for type safety. Component props are defined using interfaces.
- **Styling**: Mix of global styles in `Layout.astro` and component-scoped styles.

## 🔧 Configuration Files

- `tailwind.config.cjs`: TailwindCSS configuration with content paths
- `astro.config.mjs`: Astro build configuration
- `tsconfig.json`: TypeScript compiler options

## 📚 Learn More

- [Astro Documentation](https://docs.astro.build)
- [Astro Discord](https://astro.build/chat)
- [TailwindCSS Documentation](https://tailwindcss.com/docs)

## 🤝 Contributing

This project follows standard Astro development patterns. When contributing:

1. Follow existing code style and component patterns
2. Test changes locally with `npm run dev`
3. Ensure production build succeeds with `npm run build`
4. Keep components focused and reusable

## 📄 License

See the project repository for license information.
