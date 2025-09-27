# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- **Start development server**: `npm run dev` - Runs Vite dev server at localhost:8080 with hot reload
- **Build for production**: `npm run build` - Creates optimized build in dist/ directory
- **Install dependencies**: `npm install` - Install project dependencies (run once initially)

## Project Structure

This is a Three.js Journey lesson codebase focused on learning Three.js concepts through hands-on exercises. The current lesson is "06-cameras" which demonstrates camera controls and interactions.

### Architecture
- **Vite-based setup**: Uses Vite for development server and build tooling with hot reload
- **Modular structure**: Each lesson is self-contained in its own directory
- **Source organization**:
  - `src/` contains the main lesson files
  - `static/` for static assets (currently empty but configured)
  - Entry point is `src/index.html` with `src/script.js` as the main Three.js code

### Key Configuration
- **Vite config**: Root set to `src/`, public directory is `../static/`, build output to `../dist/`
- **Three.js version**: Uses Three.js v0.174.0
- **Development**: Vite dev server opens to local network with auto-restart on static file changes

### Lesson Structure Pattern
- Each lesson follows consistent structure: package.json, vite.config.js, src/ directory
- Main Three.js code in `src/script.js` with standard scene, camera, renderer setup
- HTML canvas element with class "webgl" for Three.js rendering
- Current lesson demonstrates mouse-controlled camera movement and perspective vs orthographic cameras

### Development Notes
- Camera controls implemented via mouse cursor tracking with normalized coordinates
- Animation loop uses `requestAnimationFrame` with Three.js Clock for timing
- Scene includes a red cube mesh with subdivision for demonstrating camera effects