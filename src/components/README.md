# Components Documentation

This directory contains reusable Astro components for the NotionData application.

## 📦 Available Components

### Card.astro

A reusable card component for displaying linked content with hover effects.

**Props:**
- `title` (string, required): The card title
- `body` (string, required): The card description text
- `href` (string, required): The URL the card links to

**Usage:**
```astro
<Card
  href="https://example.com"
  title="Example Title"
  body="This is a description of what the card links to."
/>
```

**Features:**
- Hover animation with gradient effect
- Accessible link wrapper
- Responsive design
- Arrow indicator on hover

---

### NavBar.astro

Navigation header component with menu, product links, and user actions.

**Props:** None (currently static)

**Structure:**
- Menu icon/button
- Product navigation links (Product, Pricing, Contact us)
- User actions (Search, Cart, Sign in)

**Usage:**
```astro
import NavBar from '../components/NavBar.astro';

<NavBar />
```

**Note:** This component uses Tailwind classes. Ensure Tailwind integration is configured.

---

### HeroSection.astro

Landing page hero section with headline, description, and call-to-action.

**Props:** None (currently static)

**Content:**
- Badge: "Backed by Y Combinator"
- Headline: "Make OpenAI enterprise ready."
- Description: Value proposition text
- CTA Button: "Contact sales"

**Usage:**
```astro
import HeroSection from '../components/HeroSection.astro';

<HeroSection />
```

**Customization:**
To customize content, you can convert the static text to props:
```astro
interface Props {
  badge?: string;
  headline: string;
  description: string;
  ctaText?: string;
}
```

---

### Footer.astro

Site footer with copyright and social media links.

**Props:** None (currently static)

**Content:**
- Copyright notice: "© 2023 Bricks Cloud Technologies, Inc. All rights reserved."
- Social media icons (Twitter, Facebook, LinkedIn)

**Usage:**
```astro
import Footer from '../components/Footer.astro';

<Footer />
```

**Future Enhancement:**
Consider making the year dynamic:
```astro
<p>© {new Date().getFullYear()} Bricks Cloud Technologies, Inc. All rights reserved.</p>
```

---

## 🎨 Styling Notes

### Component Scoped Styles
Most components use scoped `<style>` tags, meaning styles only apply within that component.

### TailwindCSS Classes
Several components (NavBar, HeroSection, Footer) use Tailwind utility classes. Ensure the Tailwind integration is properly installed:

```bash
npm install @astrojs/tailwind
```

And configured in `astro.config.mjs`:

```javascript
import tailwind from '@astrojs/tailwind';

export default defineConfig({
  integrations: [tailwind()],
});
```

### Global Styles
Global CSS variables are defined in `Layout.astro`:
- `--accent`: Primary accent color (136, 58, 234)
- `--accent-light`: Light accent color (224, 204, 250)
- `--accent-dark`: Dark accent color (49, 10, 101)
- `--accent-gradient`: Gradient using accent colors

---

## 🔧 Customization Guide

### Making Components More Flexible

**1. Add Props Interface**
```astro
---
interface Props {
  myProp: string;
  optionalProp?: number;
}

const { myProp, optionalProp = 42 } = Astro.props;
---
```

**2. Support Slots**
```astro
<div class="component">
  <slot />
</div>
```

**3. Conditional Rendering**
```astro
{someCondition && <div>Conditional content</div>}
```

---

## 🧪 Best Practices

1. **Type Safety**: Always define Props interfaces for type checking
2. **Accessibility**: Include ARIA labels and semantic HTML
3. **Responsive Design**: Use mobile-first CSS or Tailwind responsive classes
4. **Performance**: Keep components lightweight; avoid heavy client-side JavaScript
5. **Reusability**: Make components configurable via props rather than hardcoding content

---

## 📚 Learn More

- [Astro Components](https://docs.astro.build/en/core-concepts/astro-components/)
- [Astro Props](https://docs.astro.build/en/core-concepts/astro-components/#component-props)
- [Astro Styling](https://docs.astro.build/en/guides/styling/)
