# Kris Rodriguez Portfolio v2

A modern, animated portfolio website built with Astro, featuring WebGL backgrounds, horizontal scrolling sections, and smooth GSAP animations.

## ✨ Features

- **WebGL Topographic Wave Background** - Interactive Three.js canvas with mouse-responsive wave effects
- **Horizontal Scroll Sections** - Smooth horizontal scrolling for About and Skills sections
- **Animated Hero Section** - Dynamic title zoom with letter-specific animations
- **Sticky Experience Cards** - Stacked card layout with blur effects on scroll
- **Magnetic Buttons** - Interactive magnetic hover effects on CTAs
- **Motion Path Animation** - Flying element following SVG bezier curves
- **Scroll-Triggered Animations** - GSAP ScrollTrigger for smooth reveal effects
- **Sanity CMS Integration** - Content management for projects, skills, experiences, and contacts
- **Fully Responsive** - Optimized for mobile, tablet, and desktop
- **3D Text Effects** - Layered text-shadow for depth on footer text

## 🚀 Project Structure

```text
/
├── public/
│   ├── cv.pdf                    # Your CV/Resume file
│   ├── favicon.svg
│   └── images/
│       └── projects/             # Project featured images
├── src/
│   ├── components/
│   │   └── ProjectCard.astro     # Reusable project card component
│   ├── content/                  # Content collections (if using)
│   ├── layouts/
│   │   └── Base.astro            # Main layout with header, footer, loader
│   ├── lib/
│   │   └── sanity.ts             # Sanity client configuration
│   ├── pages/
│   │   ├── index.astro           # Homepage with all sections
│   │   ├── about.astro
│   │   ├── contact.astro
│   │   └── work/
│   │       ├── index.astro       # Projects listing
│   │       └── [slug].astro      # Individual project pages
│   └── styles/
│       └── theme.css             # Global CSS variables and styles
├── astro.config.mjs              # Astro configuration
├── sanity.config.ts              # Sanity Studio configuration
└── package.json
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

## � Dependencies

### Core
- **Astro** - Static site framework
- **Three.js** - WebGL 3D graphics for wave background
- **GSAP** - Animation library with ScrollTrigger and MotionPath plugins
- **Sanity** - Headless CMS for content management

### Development
- **TypeScript** - Type safety
- **@types/three** - TypeScript definitions for Three.js

## 🎨 Sections

### Hero Section
- WebGL topographic wave background with mouse interaction
- Animated title with zoom effect on scroll
- Custom font mixing (Syne + Playfair Display italic)

### Horizontal Scroll (About + Skills)
- Pinned horizontal scrolling container
- Flying element animation along SVG path
- Fade-in animations for content
- Text scramble effect on About section

### Featured Work
- Timeline layout with dots and connecting lines
- Magnetic button with hover effect
- Project cards with featured images
- Sticky sidebar with section info

### Experience
- Sticky stacked cards with blur effect
- Vertical line background pattern
- Large background numbers
- Scroll-triggered fade animations

### Contact
- Two-column grid layout
- Hover effects on contact links
- Sticky sidebar positioning

### Footer
- 3D text effect on name
- Magnetic CV download button
- Social links (Email, GitHub, LinkedIn)
- Professional three-column layout

## 🎯 Content Management

Content is managed through Sanity CMS. The following content types are available:

- **Projects** - Portfolio work with images, descriptions, tags
- **Skills** - Technical skills with categories and levels
- **Experiences** - Work history with roles, companies, dates
- **Contacts** - Social links and contact methods
- **About** - Bio and introduction text
- **Settings** - Site title, tagline, and global settings

## 🔧 Configuration

### Sanity Setup
1. Create a Sanity project at [sanity.io](https://sanity.io)
2. Update `src/lib/sanity.ts` with your project ID and dataset
3. Configure schemas in Sanity Studio
4. Deploy Sanity Studio or run locally

### CV/Resume Download
1. Place your PDF file in `public/` folder (e.g., `public/cv.pdf`)
2. The footer button will automatically link to it
3. Update filename in `src/layouts/Base.astro` if needed

## 📱 Responsive Design

The site is fully responsive with breakpoints at:
- **Mobile**: < 640px
- **Tablet**: 640px - 768px
- **Desktop**: > 768px

Mobile optimizations include:
- Reduced font sizes with clamp()
- Single column layouts
- Disabled magnetic effects
- Simplified animations
- Full-width buttons

## 🎭 Animation Features

### GSAP Animations
- **ScrollTrigger** - Scroll-linked animations with scrub
- **MotionPath** - SVG path following for flying element
- **Timeline** - Sequenced animations for hero zoom
- **Magnetic Effect** - Mouse-following button interactions

### Three.js Effects
- Real-time wave generation
- Mouse position tracking
- Topographic contour lines
- Smooth camera positioning

## 🚢 Deployment

### Recommended Platforms

#### For a simple Astro portfolio:
I recommend **Vercel**.

**Reason:** Both offer:
- Zero-config deployment from Git
- Automatic builds on push
- Free SSL certificates
- CDN distribution
- Excellent performance for static sites
- Simple environment variable management

#### For Astro + EmDash CMS:
I recommend **Vercel**.

**Reason:**
- EmDash CMS is file-based (stores content in Git), so no external database needed
- Both platforms offer automatic rebuilds on Git commits
- Content changes trigger builds automatically when pushed to repository
- No need for webhooks or API keys (unlike headless CMS solutions)
- Preview deployments for content changes before merging
- Simple environment variable management if needed
- Excellent performance for static sites with file-based content
- Zero-config deployment experience

### Build Command
```bash
npm run build
```

### Output Directory
```
dist/
```

## 🎨 Customization

### Colors
Edit CSS variables in `src/styles/theme.css`:
```css
--color-bg: #0a0a0a;
--color-text: #f5f5f5;
--color-accent: #a78bfa;
```

### Fonts
Fonts are loaded from Google Fonts in `src/layouts/Base.astro`:
- **Syne** - Headings and titles
- **Anton** - Hero title
- **Playfair Display** - Italic accent letter
- **Space Mono** - Loader percentage

### Animations
Adjust animation timing in `src/pages/index.astro`:
- ScrollTrigger start/end points
- Animation durations
- Easing functions
- Stagger delays

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Kris Rodriguez**
- Portfolio: https://rodirguez-portfolio.vercel.app/
- GitHub: https://github.com/Rodriguez1718
- Email: krisjohn.rodriguez@gmail.com

## 🙏 Acknowledgments

- Astro team for the amazing framework
- GSAP for powerful animations
- Three.js for WebGL capabilities
- Sanity for flexible content management
