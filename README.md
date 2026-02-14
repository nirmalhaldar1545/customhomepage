# Custom Homepage

A stunning, personalized browser start page with an animated 3D shader background and quick-access shortcuts. Designed to replace your browser's default new tab or startup page with a classy, visually immersive experience.

![Preview](https://img.shields.io/badge/React-19-blue) ![Preview](https://img.shields.io/badge/Three.js-0.182-orange) ![Preview](https://img.shields.io/badge/GSAP-3.14-green) ![Preview](https://img.shields.io/badge/TailwindCSS-4.1-cyan) ![Preview](https://img.shields.io/badge/TypeScript-5.9-blue)

## 🌐 Live Demo

**Deployed on GitHub Pages:** [https://nirmalhaldar1545.github.io/customhomepage/](https://nirmalhaldar1545.github.io/customhomepage/)

## Features

- **Mesmerizing Shader Background** - Real-time animated 3D shader effect using Three.js and custom GLSL shaders
- **Smooth Animations** - Elegant entrance animations powered by GSAP with blur transitions
- **Quick Access Shortcuts** - One-click access to your most-used services:
  - Gmail
  - Google Drive
  - YouTube
  - ChatGPT
  - Coursera
- **Fancy Button Effects** - Interactive buttons with animated dot borders and hover states
- **Fullscreen Immersive Design** - Full viewport height layout with radial gradient overlay
- **Responsive** - Adapts to any screen size

## Tech Stack

- **[React 19](https://react.dev/)** - UI framework
- **[Vite](https://vitejs.dev/)** - Build tool and dev server
- **[Three.js](https://threejs.org/)** - 3D graphics and WebGL
- **[React Three Fiber](https://docs.pmnd.rs/react-three-fiber)** - React renderer for Three.js
- **[GSAP](https://greensock.com/gsap/)** - Professional-grade animations
- **[Tailwind CSS 4](https://tailwindcss.com/)** - Utility-first CSS
- **[Lucide React](https://lucide.dev/)** - Beautiful icons
- **[TypeScript](https://www.typescriptlang.org/)** - Type safety

## Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/nirmalhaldar1545/customhomepage.git
cd customhomepage
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open `http://localhost:5173` in your browser

### Build for Production

```bash
npm run build
```

The built files will be in the `dist/` folder.

## Deployment

### GitHub Pages (Recommended)

This project is configured for easy deployment to GitHub Pages:

```bash
npm run deploy
```

This command will:
1. Build the project (`npm run build`)
2. Deploy the `dist` folder to the `gh-pages` branch

The site will be available at: `https://[your-username].github.io/customhomepage/`

### Manual Deployment

For other hosting services (Vercel, Netlify, etc.):

1. Build the project:
   ```bash
   npm run build
   ```

2. Deploy the contents of the `dist/` folder to your hosting service

## Setting as Chrome Startup Page

### Method 1: Use GitHub Pages URL (Recommended)

1. Open Chrome and go to `chrome://settings/onStartup`

2. Select **"Open a specific page or set of pages"**

3. Click **"Add a new page"** and enter:
   ```
   https://nirmalhaldar1545.github.io/customhomepage/
   ```

### Method 2: Local File

1. Build the project:
   ```bash
   npm run build
   ```

2. Open Chrome and go to `chrome://settings/onStartup`

3. Select **"Open a specific page or set of pages"**

4. Click **"Add a new page"** and enter:
   ```
   file:///C:/Users/[YourUsername]/customhomepage/dist/index.html
   ```
   (Adjust the path to match your actual project location)

### Method 3: Development Server

For hot-reloading during development:

1. Start the dev server:
   ```bash
   npm run dev
   ```

2. Set your Chrome startup page to:
   ```
   http://localhost:5173
   ```

## Customization

### Changing Shortcuts

Edit [`src/components/ui/infinite-hero.tsx`](src/components/ui/infinite-hero.tsx) to modify the quick-access buttons:

```tsx
<a
  href="https://your-favorite-site.com"
  className="fancy-button"
>
  <div className="dots-border" />
  <YourIcon className="button-icon" />
  <span className="text-button">Your Site</span>
</a>
```

Available icons from [Lucide](https://lucide.dev/icons/):
- Import new icons: `import { YourIcon } from "lucide-react"`

### Modifying the Shader

The background shader can be customized in [`infinite-hero.tsx`](src/components/ui/infinite-hero.tsx). The fragment shader uses GLSL and creates the animated wave-like effect.

### Styling

- Global styles: [`src/index.css`](src/index.css)
- Button styles: [`src/components/ui/fancy-button.css`](src/components/ui/fancy-button.css)
- Tailwind configuration is built-in with v4

## Project Structure

```
customhomepage/
├── public/
│   └── favicon.png
│
├── src/
│   ├── assets/
│   │
│   ├── components/
│   │   └── ui/
│   │       ├── fancy-button.css
│   │       └── infinite-hero.tsx
│   │
│   ├── App.css
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
│
├── index.html
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |
| `npm run deploy` | Deploy to GitHub Pages |

## Browser Support

- Chrome 90+ (recommended)
- Edge 90+
- Firefox 90+
- Safari 15+

WebGL support is required for the shader background.

## Performance

The shader background uses raymarching with 256 steps, optimized for smooth performance on modern GPUs. The animation runs at 60fps on most devices.

## Repository

- **GitHub:** [https://github.com/nirmalhaldar1545/customhomepage](https://github.com/nirmalhaldar1545/customhomepage)
- **Live Site:** [https://nirmalhaldar1545.github.io/customhomepage/](https://nirmalhaldar1545.github.io/customhomepage/)

## License

MIT License - feel free to use and modify for your own custom homepage!

## Acknowledgments

- Shader effect inspired by [Shadertoy](https://www.shadertoy.com/) creations
- Button styling inspired by modern glassmorphism design trends
- Icons by [Lucide](https://lucide.dev/)

---

**Enjoy your new classy browser start page!**
