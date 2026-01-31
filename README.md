# AETERNITAS - Luxury Watch Brand Website

A high-end, cinematic luxury brand website for AETERNITAS Swiss Haute Horlogerie. Built with Next.js, Three.js, and GSAP for an immersive premium experience.

![AETERNITAS Preview](https://images.unsplash.com/photo-1524592094714-0f0654e20314?w=1200)

## ✨ Features

### Visual Design
- **Ultra-premium aesthetic** with black, gold (#C9A962), and elegant typography
- **Cormorant Garamond** serif for headlines + **Inter** sans-serif for body text
- **Custom gold gradient text** with shimmer animations
- **Noise texture overlays** for tactile luxury feel
- **Custom scrollbar** and cursor styling

### 3D Graphics (Three.js + React Three Fiber)
- **Hero Section**: Interactive 3D luxury watch with mouse-follow animation
- **Signature Experience**: Immersive 3D scene with floating golden spheres, particle field, and animated torus portal
- **Smooth mouse interactions** for parallax effects
- **Optimized lighting** with warm gold directional lights

### Animations (GSAP + ScrollTrigger)
- **Cinematic entrance sequence** with staggered character reveals
- **Scroll-triggered animations** throughout all sections
- **Parallax scrolling effects** on images and content
- **3D card tilt effects** on product hover
- **Smooth page transitions** and loading screen

### Sections
1. **Hero** - Full-screen cinematic intro with 3D watch
2. **Brand Story** - Philosophy, heritage timeline, and craftsmanship
3. **Product Showcase** - Luxury watch collections with 3D hover effects
4. **Signature Experience** - Immersive 3D visual experience
5. **Why AETERNITAS** - Value propositions with animated stats
6. **CTA** - Private consultation booking form
7. **Footer** - Premium footer with newsletter signup

## 🚀 Tech Stack

- **Framework**: [Next.js 16](https://nextjs.org/) (App Router)
- **Language**: TypeScript
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)
- **3D Graphics**: [Three.js](https://threejs.org/) + [React Three Fiber](https://docs.pmnd.rs/react-three-fiber)
- **Animations**: [GSAP](https://greensock.com/gsap/) + [ScrollTrigger](https://greensock.com/scrolltrigger/)
- **Icons**: [Lucide React](https://lucide.dev/)

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/aeternitas.git
cd aeternitas

# Install dependencies
npm install

# Run development server
npm run dev

# Open http://localhost:3000
```

## 🏗️ Project Structure

```
my-app/
├── app/
│   ├── globals.css          # Global styles, animations, custom properties
│   ├── layout.tsx           # Root layout with fonts and metadata
│   └── page.tsx             # Main page composition
├── components/
│   ├── Navigation.tsx       # Fixed navigation with scroll effects
│   ├── Watch3D.tsx          # Hero 3D watch component (Three.js)
│   ├── Experience3D.tsx     # Signature Experience 3D scene
│   ├── ui/                  # shadcn/ui components
│   └── sections/
│       ├── Hero.tsx         # Hero section with intro animation
│       ├── BrandStory.tsx   # Brand philosophy and timeline
│       ├── ProductShowcase.tsx  # Product grid with 3D cards
│       ├── SignatureExperience.tsx  # 3D immersive section
│       ├── WhyThisBrand.tsx # Value propositions
│       ├── CTA.tsx          # Contact/consultation form
│       └── Footer.tsx       # Premium footer
├── lib/
│   └── utils.ts             # Utility functions (cn helper)
├── public/                  # Static assets
├── next.config.ts           # Next.js configuration
├── tailwind.config.ts       # Tailwind configuration
└── package.json
```

## 🎨 Key Components

### Watch3D
Interactive 3D luxury watch rendered with Three.js:
- Realistic watch geometry (case, bezel, dial, hands, crown)
- Mouse-follow rotation animation
- Gold and black materials with proper lighting
- Floating animation with GSAP Float

### Experience3D
Immersive 3D scene for the Signature Experience section:
- Animated torus knot portal
- Floating golden spheres
- Particle field with gold accents
- Light rings with slow rotation
- Mouse-interactive camera

### Product Cards
Premium product showcase cards:
- 3D tilt effect on hover (mouse position tracking)
- Specs reveal animation
- Gold border glow on hover
- Image parallax effect

## ⚡ Performance Optimizations

- **Dynamic imports** for 3D components (SSR disabled)
- **Lazy loading** with loading spinners
- **Optimized Three.js rendering**:
  - Reduced polygon counts
  - Efficient material reuse with `useMemo`
  - Limited particle counts (50-200)
- **DPR (Device Pixel Ratio)** capped at 2 for performance
- **Will-change CSS property** for smooth animations
- **Passive event listeners** for scroll and mouse events

## 🔧 Configuration

### Next.js Config
```typescript
// next.config.ts
const nextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: "https",
        hostname: "images.unsplash.com",
      },
    ],
    unoptimized: true, // Required for static export with external images
  },
};
```

### Tailwind Custom Properties
Key CSS variables in `globals.css`:
```css
--color-gold: #C9A962;
--color-gold-light: #D4BC7E;
--color-luxury-black: #0A0A0A;
--color-luxury-dark: #111111;
```

## 🌐 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

**Note**: 3D graphics require WebGL support. Falls back gracefully on unsupported devices.

## 📱 Responsive Breakpoints

- **Mobile**: < 640px
- **Tablet**: 640px - 1024px
- **Desktop**: > 1024px
- **Large Desktop**: > 1280px

## 🎭 Animation Specifications

| Animation | Duration | Easing | Trigger |
|-----------|----------|--------|---------|
| Hero Text Reveal | 1.4s | power3.out | Load |
| Character Stagger | 0.03s | - | Load |
| Scroll Parallax | scrub | none | Scroll |
| Card 3D Tilt | 0.4s | power2.out | Hover |
| Section Reveal | 1s | power3.out | ScrollTrigger |

## 📝 License

© 2026 AETERNITAS. All rights reserved.

This project is created for demonstration purposes. Brand name, imagery, and design are fictional.

## 🙏 Credits

- **Fonts**: Google Fonts (Cormorant Garamond, Inter)
- **Images**: Unsplash
- **3D Environment**: React Three Fiber Drei
- **Animations**: GreenSock (GSAP)

---

Built with ❤️ for luxury brand experiences.
