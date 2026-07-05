# Gnana Vriksha - AI Career Guidance Platform

**Empowering Indian students to discover their ideal career path through AI-guided exploration.**

## Overview

Gnana Vriksha is a premium, fast-loading career guidance platform designed specifically for Class 10 students in India. Built with a focus on performance, accessibility, and user experience, it combines anime-inspired design aesthetics with modern web technologies.

**Key Features:**
- AI-powered career recommendations
- Comparison of educational pathways (Diploma, Intermediate, ITI)
- Personalized career roadmaps
- Scholarship finder
- Interactive career explorer
- Mobile-first responsive design
- Glassmorphism UI with smooth animations
- Zero touch/interaction issues

## Design Philosophy

**Ethereal Minimalism with Anime-Inspired Depth** — The platform balances peaceful aesthetics with intelligent functionality. Every design decision prioritizes clarity, accessibility, and performance while maintaining a premium, award-winning visual quality.

**Color Palette:**
- Deep Sky Blue: `oklch(0.55 0.15 260)` — Primary, trust, education
- Cyan: `oklch(0.65 0.12 200)` — Innovation, AI elements
- Emerald Green: `oklch(0.60 0.10 140)` — Nature, growth

**Typography:**
- Display: Poppins (700 weight) — Modern, friendly
- Body: Inter (400–500 weight) — Clean, readable

## Tech Stack

- **Frontend:** React 19 + TypeScript
- **Styling:** Tailwind CSS 4 + Custom CSS
- **Animations:** CSS-first (GPU-accelerated)
- **UI Components:** shadcn/ui
- **Icons:** Lucide React
- **Routing:** Wouter (lightweight)
- **Build:** Vite 7
- **Package Manager:** pnpm

## Project Structure

```
gnana_vriksha/
├── client/
│   ├── public/              # Static files (favicon, robots.txt)
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   │   ├── Sections.tsx # Career, stats, testimonials sections
│   │   │   └── ui/          # shadcn/ui components
│   │   ├── pages/           # Page-level components
│   │   │   ├── Home.tsx     # Main landing page
│   │   │   └── NotFound.tsx # 404 page
│   │   ├── lib/
│   │   │   ├── utils.ts     # Utility functions
│   │   │   └── touch-utils.ts # Touch & accessibility utilities
│   │   ├── contexts/        # React contexts
│   │   ├── hooks/           # Custom hooks
│   │   ├── App.tsx          # Root component & routing
│   │   ├── main.tsx         # React entry point
│   │   └── index.css        # Global styles & design tokens
│   └── index.html           # HTML template
├── server/                  # Express server (placeholder)
├── PERFORMANCE.md           # Performance optimization guide
├── ideas.md                 # Design philosophy & approach
└── package.json             # Dependencies & scripts
```

## Getting Started

### Prerequisites
- Node.js 18+
- pnpm 10+

### Installation

```bash
# Install dependencies
pnpm install

# Start development server
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview

# Type check
pnpm check

# Format code
pnpm format
```

The development server runs at `http://localhost:3000/`.

## Performance Optimizations

**Fast Loading:**
- Single hero image (reused across sections)
- CSS-only animations (no JavaScript overhead)
- Lazy loading for images
- Minimal bundle size

**Smooth Interactions:**
- GPU-accelerated animations (transform + opacity only)
- 100–250ms animation durations
- Debounced scroll events
- No layout thrashing

**Touch-Friendly:**
- All interactive elements 44px+ (WCAG AA)
- No hover-only interactions
- Visible focus indicators
- Keyboard navigation fully supported

**Accessibility:**
- WCAG AA color contrast (4.5:1 text)
- Semantic HTML structure
- ARIA labels where needed
- Respects `prefers-reduced-motion`

See [PERFORMANCE.md](./PERFORMANCE.md) for detailed optimization strategies.

## Design System

### Colors

| Name | Value | Usage |
|------|-------|-------|
| Primary | `oklch(0.55 0.15 260)` | Buttons, links, accents |
| Secondary | `oklch(0.65 0.12 200)` | Cyan elements, AI features |
| Accent | `oklch(0.60 0.10 140)` | Emerald highlights |
| Background | `oklch(0.98 0.001 0)` | Off-white page background |
| Foreground | `oklch(0.235 0.015 65)` | Text color |

### Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| H1 | Poppins | 700 | 48px |
| H2 | Poppins | 700 | 32px |
| H3 | Poppins | 700 | 24px |
| Body | Inter | 400 | 16px |
| Small | Inter | 400 | 14px |

### Spacing

- Base unit: 4px
- Padding: 16px (mobile), 24px (tablet), 32px (desktop)
- Gap between sections: 64px (mobile), 96px (desktop)

### Animations

| Name | Duration | Easing | Use Case |
|------|----------|--------|----------|
| `animate-float` | 3s | ease-in-out | Floating elements |
| `animate-drift` | 6–14s | ease-in-out | Particle movement |
| `animate-slide-up` | 150ms | ease-out | Card entrance |
| `animate-fade-in` | 500ms | ease-out | General fade |
| `animate-glow-pulse` | 2s | ease-in-out | Glowing effects |

## Components

### Reusable Sections

**ComparisonSection:** Displays Diploma, Intermediate, and ITI pathway comparison with features and CTAs.

**StatsSection:** Shows key metrics (50K+ students, 200+ paths, 95% success rate).

**TestimonialSection:** Displays student, parent, and counselor testimonials with avatars.

**FAQSection:** Expandable FAQ items with smooth animations.

## Key Features

### Hero Section
- Anime-inspired landscape background with parallax effect
- Student illustration with glowing AI pathway
- Gradient text "Build Tomorrow"
- Dual CTA buttons with hover effects

### Navigation
- Floating glassmorphic navbar
- Smooth scroll transitions
- Mobile-responsive menu
- Logo with brand mark

### Quick Access Cards
- 6 feature cards with icons
- Staggered entrance animation
- Hover lift effect
- Touch-friendly (44px+ targets)

### Search Bar
- AI-powered search placeholder
- Voice search icon
- Filter options
- Glassmorphic design

### Sections
- Pathway comparison
- Statistics display
- Success testimonials
- FAQ accordion

## Accessibility

**Keyboard Navigation:**
- Tab through all interactive elements
- Enter/Space to activate buttons
- Escape to close modals
- Focus indicators visible on all elements

**Screen Readers:**
- Semantic HTML structure
- ARIA labels on icons
- Heading hierarchy (h1 → h6)
- Alt text on images

**Visual Accessibility:**
- 4.5:1 color contrast on text
- No color-only information
- Readable font sizes (16px minimum)
- Sufficient spacing between elements

**Motion:**
- Respects `prefers-reduced-motion` setting
- Animations can be disabled
- No auto-playing content

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari 14+, Chrome Android 90+)

## Deployment

The website is deployed on Manus with automatic scaling. To publish:

1. Create a checkpoint: `webdev_save_checkpoint`
2. Click the **Publish** button in the Management UI
3. Configure custom domain in Settings → Domains

## Future Enhancements

- AI career recommendation quiz
- User authentication & profiles
- Personalized learning roadmaps
- College recommendation engine
- Scholarship finder integration
- Resume builder
- Dark mode support
- Multi-language support (Hindi, Tamil, Telugu, etc.)

## Contributing

When making changes:
1. Follow the design philosophy (see [ideas.md](./ideas.md))
2. Maintain performance standards (see [PERFORMANCE.md](./PERFORMANCE.md))
3. Test on mobile devices
4. Ensure WCAG AA accessibility
5. Use CSS animations (not JavaScript)

## License

© 2026 Gnana Vriksha. All rights reserved.

## Support

For issues or questions, contact the development team or submit feedback through the Management UI.

---

**Built with ❤️ for Indian students. Empowering careers, one student at a time.**
