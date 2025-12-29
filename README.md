# 🥤 Fizzi App

A modern, interactive soda brand website built with Next.js, featuring stunning 3D graphics, smooth animations, and a headless CMS integration. Experience the fizzy world of Fizzi with immersive 3D soda cans, dynamic animations, and a beautiful user interface.

## ✨ Features

### 3D Graphics & Interactions
- **🎮 3D Soda Cans**: Interactive 3D soda can models using React Three Fiber
- **🎨 Multiple Flavors**: Support for 5+ flavors (Black Cherry, Lemon Lime, Grape, Strawberry, Watermelon)
- **💫 Floating Animations**: Smooth floating and rotation animations for 3D objects
- **🌊 Bubble Effects**: Animated bubble particles in the hero section
- **📐 HDR Environment**: High Dynamic Range lighting for realistic 3D rendering

### Content Management
- **📝 Prismic CMS**: Headless CMS integration for easy content management
- **🧩 Slice Machine**: Visual content editor with customizable slices
- **🔄 Preview Mode**: Real-time content preview functionality
- **📄 Dynamic Pages**: Dynamic page routing with UID-based URLs

### Animations & Effects
- **🎬 GSAP Animations**: Smooth scroll-triggered animations
- **📜 Scroll Animations**: Parallax and scroll-based effects
- **✨ Text Animations**: Character and word-level text animations
- **🎯 Interactive Elements**: Hover effects and interactive components

### UI Components
- **🏠 Hero Section**: Immersive hero with 3D scene and animated text
- **🎠 Carousel**: Image carousel with navigation
- **📝 Big Text**: Large typography sections
- **🔄 Alternating Text**: Dynamic text animations
- **🪂 Sky Dive**: Unique scroll-based animation section

### Design & Styling
- **🎨 Tailwind CSS**: Utility-first CSS framework
- **🔤 Custom Fonts**: Alpino variable font family
- **📱 Responsive Design**: Mobile-first responsive layout
- **🌈 Color Scheme**: Vibrant yellow and sky blue color palette

## 🛠️ Technologies Used

### Core Framework
- **Next.js 14**: React framework with App Router
- **React 18**: UI library
- **TypeScript**: Type-safe JavaScript

### 3D Graphics
- **React Three Fiber**: React renderer for Three.js
- **@react-three/drei**: Useful helpers for R3F
- **Three.js**: 3D graphics library
- **GLTF Models**: 3D model format for soda cans

### Animation
- **GSAP**: Professional animation library
- **@gsap/react**: React hooks for GSAP
- **ScrollTrigger**: GSAP plugin for scroll-based animations

### Content Management
- **Prismic**: Headless CMS
- **@prismicio/client**: Prismic JavaScript client
- **@prismicio/react**: React components for Prismic
- **Slice Machine**: Visual content editor

### Styling
- **Tailwind CSS**: Utility-first CSS framework
- **PostCSS**: CSS processing
- **Autoprefixer**: CSS vendor prefixing

### State Management
- **Zustand**: Lightweight state management

### Development Tools
- **ESLint**: Code linting
- **Prettier**: Code formatting
- **Concurrently**: Run multiple scripts simultaneously

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

1. **Node.js** (v18.x or higher)
   - Download from [nodejs.org](https://nodejs.org/)
   - Verify: `node --version`

2. **npm** (comes with Node.js) or **yarn**
   - Verify: `npm --version`

3. **Prismic Account** (for CMS)
   - Sign up at [prismic.io](https://prismic.io/)
   - Create a new repository

## 🚀 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/Afreen4115/Fizzi.git
cd Fizzi
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Set Up Prismic

1. **Create a Prismic Repository**:
   - Go to [prismic.io](https://prismic.io/)
   - Create a new repository
   - Copy your repository name

2. **Configure Environment Variables**:
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_PRISMIC_ENVIRONMENT=your-repository-name
   ```

3. **Set Up Content**:
   ```bash
   npm run set-up-content
   ```

### Step 4: Start Development Server

```bash
npm run dev
```

This will start:
- Next.js development server on `http://localhost:3000`
- Slice Machine on `http://localhost:9999`

Or run them separately:

```bash
# Next.js only
npm run next:dev

# Slice Machine only
npm run slicemachine
```

## 📖 Usage Guide

### Development Workflow

1. **Start Development**:
   ```bash
   npm run dev
   ```
   This runs both Next.js and Slice Machine concurrently.

2. **Edit Content**:
   - Open Slice Machine at `http://localhost:9999`
   - Edit slices and content visually
   - Changes sync automatically

3. **Preview Changes**:
   - View changes in real-time at `http://localhost:3000`
   - Use Prismic preview mode for draft content

### Building for Production

```bash
npm run build
npm start
```

### Code Formatting

```bash
npm run format
```

### Linting

```bash
npm run lint
```

## 📁 Project Structure

```
Fizzi/
├── public/
│   ├── fonts/
│   │   └── Alpino-Variable.woff2    # Custom font
│   ├── hdr/
│   │   ├── field.hdr               # HDR environment maps
│   │   └── lobby.hdr
│   ├── labels/
│   │   ├── cherry.png              # Soda can labels
│   │   ├── grape.png
│   │   ├── lemon-lime.png
│   │   ├── strawberry.png
│   │   └── watermelon.png
│   ├── Soda-can.bin                # 3D model binary
│   └── Soda-can.gltf               # 3D model GLTF
├── src/
│   ├── app/
│   │   ├── [uid]/
│   │   │   └── page.tsx            # Dynamic page routes
│   │   ├── api/
│   │   │   ├── exit-preview/        # Preview API routes
│   │   │   ├── preview/
│   │   │   └── revalidate/
│   │   ├── layout.tsx               # Root layout
│   │   ├── page.tsx                 # Homepage
│   │   └── slice-simulator/         # Slice simulator
│   ├── components/
│   │   ├── Bounded.tsx              # Container component
│   │   ├── Button.tsx               # Button component
│   │   ├── CircleText.tsx           # Circular text component
│   │   ├── FizziLogo.tsx            # Logo component
│   │   ├── FloatingCan.tsx          # Floating 3D can
│   │   ├── Footer.tsx               # Footer component
│   │   ├── Header.tsx               # Header/Navbar
│   │   ├── SodaCan.tsx              # 3D soda can component
│   │   ├── TextSplitter.tsx         # Text animation utility
│   │   └── ViewCanvas.tsx           # 3D canvas wrapper
│   ├── hooks/
│   │   ├── useMediaQuery.ts         # Media query hook
│   │   └── useStore.ts              # Zustand store
│   ├── slices/
│   │   ├── AlternatingText/         # Alternating text slice
│   │   ├── BigText/                 # Big text slice
│   │   ├── Carousel/                # Carousel slice
│   │   ├── Hero/                    # Hero slice with 3D
│   │   ├── SkyDive/                 # Sky dive animation slice
│   │   └── index.ts                 # Slice exports
│   └── prismicio.ts                 # Prismic client config
├── customtypes/
│   └── page/                         # Prismic page type
├── next.config.mjs                   # Next.js config
├── tailwind.config.js                # Tailwind config
├── slicemachine.config.json          # Slice Machine config
├── package.json
└── README.md
```

## 🏗️ Architecture

### Component Hierarchy

```
App (Layout)
├── Header
├── Main Content
│   ├── Hero (with 3D Scene)
│   ├── Carousel
│   ├── BigText
│   ├── AlternatingText
│   └── SkyDive
├── ViewCanvas (3D Canvas)
└── Footer
```

### 3D Graphics Pipeline

1. **ViewCanvas**: Main Three.js canvas container
2. **View.Port**: React Three Fiber viewport
3. **SodaCan**: 3D model component with textures
4. **FloatingCan**: Animation wrapper for floating effects
5. **Scene**: 3D scene setup with lighting and environment

### Content Flow

1. **Prismic CMS**: Content stored in Prismic
2. **Prismic Client**: Fetches content via API
3. **SliceZone**: Renders slices dynamically
4. **Components**: Each slice maps to a React component

## 🎨 Customization

### Adding New Soda Flavors

1. Add label image to `public/labels/`:
   ```bash
   public/labels/your-flavor.png
   ```

2. Update `SodaCan.tsx`:
   ```typescript
   const flavorTextures = {
     // ... existing flavors
     yourFlavor: "/labels/your-flavor.png",
   };
   ```

3. Use in components:
   ```tsx
   <SodaCan flavor="yourFlavor" />
   ```

### Creating New Slices

1. **Using Slice Machine**:
   - Open Slice Machine at `http://localhost:9999`
   - Click "Create Slice"
   - Configure fields and variations
   - Generate code

2. **Manually**:
   - Create folder in `src/slices/YourSlice/`
   - Add `index.tsx`, `model.json`, `mocks.json`
   - Export in `src/slices/index.ts`

### Modifying Colors

Edit `tailwind.config.js`:
```javascript
theme: {
  extend: {
    colors: {
      'fizzi-yellow': '#FDE047',
      'fizzi-green': '#D9F99D',
      // Add your colors
    }
  }
}
```

### Customizing Animations

Edit GSAP animations in slice components:
```typescript
useGSAP(() => {
  gsap.from(".element", {
    opacity: 0,
    y: 50,
    duration: 1
  });
});
```

## 🧪 Testing

### Running Tests

```bash
npm test
```

### Testing 3D Components

- Ensure WebGL is supported in your browser
- Test on different devices for performance
- Check mobile responsiveness

### Testing Prismic Integration

1. **Preview Mode**:
   - Use Prismic preview URLs
   - Test draft content visibility

2. **Content Updates**:
   - Make changes in Slice Machine
   - Verify updates appear on site

## 🚀 Deployment

### Deploy to Vercel

1. **Connect Repository**:
   - Push code to GitHub
   - Import to Vercel

2. **Environment Variables**:
   - Add `NEXT_PUBLIC_PRISMIC_ENVIRONMENT` in Vercel dashboard

3. **Deploy**:
   - Vercel will auto-deploy on push

### Deploy to Other Platforms

1. **Build**:
   ```bash
   npm run build
   ```

2. **Start**:
   ```bash
   npm start
   ```

3. **Configure**:
   - Set environment variables
   - Configure Prismic webhooks for revalidation

## 🐛 Troubleshooting

### Common Issues

#### 1. Prismic Connection Error
**Error**: `Failed to fetch from Prismic`

**Solutions**:
- Verify `NEXT_PUBLIC_PRISMIC_ENVIRONMENT` is set
- Check Prismic repository name is correct
- Ensure internet connection is active
- Verify Prismic API endpoint

#### 2. 3D Models Not Loading
**Error**: Models don't appear or show errors

**Solutions**:
- Ensure GLTF files are in `public/` directory
- Check file paths in `SodaCan.tsx`
- Verify WebGL is supported in browser
- Check browser console for errors

#### 3. Slice Machine Not Starting
**Error**: Slice Machine won't start

**Solutions**:
- Check port 9999 is available
- Verify `slicemachine.config.json` exists
- Reinstall dependencies: `npm install`
- Check for port conflicts

#### 4. Build Errors
**Error**: Production build fails

**Solutions**:
- Check for TypeScript errors: `npm run lint`
- Verify all imports are correct
- Ensure all assets are in `public/`
- Check environment variables are set

#### 5. Animations Not Working
**Error**: GSAP animations don't trigger

**Solutions**:
- Verify GSAP plugins are registered
- Check ScrollTrigger is imported
- Ensure elements have correct classes
- Check browser console for errors

#### 6. Performance Issues
**Issue**: Slow loading or laggy animations

**Solutions**:
- Optimize 3D models (reduce polygon count)
- Use lower DPR settings
- Reduce particle counts
- Enable code splitting
- Use image optimization

## 🔒 Performance Optimization

### Current Optimizations
- Code splitting with dynamic imports
- Image optimization with Next.js Image
- GLTF model preloading
- Suspense boundaries for 3D components
- Lazy loading for slices


## 🚧 Future Enhancements

Potential improvements for the project:

- [ ] E-commerce integration
- [ ] Product customization tool
- [ ] User accounts and favorites
- [ ] Social sharing functionality
- [ ] Multi-language support
- [ ] Advanced 3D interactions (rotation, zoom)
- [ ] AR/VR support
- [ ] Product finder/locator
- [ ] Newsletter subscription
- [ ] Blog section
- [ ] Recipe section
- [ ] Sustainability information
- [ ] Interactive flavor selector
- [ ] Sound effects
- [ ] Advanced analytics
- [ ] A/B testing
- [ ] Progressive Web App (PWA)

## 📱 Browser Support

- ✅ Chrome (latest) - Full support
- ✅ Firefox (latest) - Full support
- ✅ Safari (latest) - Full support
- ✅ Edge (latest) - Full support
- ⚠️ Internet Explorer - Not supported

**Note**: WebGL support required for 3D graphics

## 📝 Available Scripts

```bash
npm run dev              # Start dev server + Slice Machine
npm run next:dev         # Start Next.js only
npm run slicemachine     # Start Slice Machine only
npm run build            # Build for production
npm start                # Start production server
npm run lint             # Run ESLint
npm run format           # Format code with Prettier
npm run set-up-content   # Set up Prismic content
```


## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing framework
- [Prismic](https://prismic.io/) for the headless CMS
- [React Three Fiber](https://docs.pmnd.rs/react-three-fiber/) for 3D graphics
- [GSAP](https://gsap.com/) for animations
- [Tailwind CSS](https://tailwindcss.com/) for styling
- Contributors and users of this project



## 🔗 Useful Links

- [Next.js Documentation](https://nextjs.org/docs)
- [Prismic Documentation](https://prismic.io/docs)
- [React Three Fiber Docs](https://docs.pmnd.rs/react-three-fiber/)
- [GSAP Documentation](https://gsap.com/docs/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Three.js Documentation](https://threejs.org/docs/)

## 🎯 Key Features Explained

### 3D Soda Cans
- Uses GLTF 3D models
- Supports multiple flavor textures
- Floating and rotation animations
- Realistic metal materials
- HDR environment lighting

### Prismic CMS
- Headless content management
- Visual slice editor
- Preview mode for drafts
- Type-safe content queries
- Automatic revalidation

### GSAP Animations
- Scroll-triggered animations
- Text character splitting
- Timeline-based sequences
- Performance optimized
- Mobile-responsive

---

**Stay Fizzy! 🥤✨**
