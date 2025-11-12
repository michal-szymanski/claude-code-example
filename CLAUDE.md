# Training App

A React-based web application for setting personal training goals and tracking progress over time.

## Project Overview

This is a training application where users can:
- Set personal training goals
- Track progress towards their goals
- Monitor their achievements and milestones

## General AI Rules

**CRITICAL:** These rules must be followed at all times when working on this codebase.

### Code Comments
- **NEVER generate comments within the code. No exceptions.**
- Code must be self-documenting through clear naming and structure

### File Naming
- **File names MUST be kebab-case**
- Examples: `goal-tracker.jsx`, `progress-chart.jsx`, `user-settings.js`
- Applies to all file types: JavaScript, CSS, configuration files, etc.

### TypeScript Conventions
- **ALWAYS use Types instead of Interface unless technically impossible**
- Prefer `type` declarations over `interface` declarations
- Only use `interface` when extending or merging declarations is required

### Rule Enforcement
- **Before making any edit, check if it violates these rules**
- If a rule conflict arises, ask the user for clarification rather than breaking the rule
- These rules take precedence over common conventions or defaults

### Agent Delegation

**CRITICAL:** Follow this workflow for all frontend development tasks.

#### Workflow for Frontend Tasks

1. **Frontend Development Phase**
   - **MUST invoke the frontend-expert agent** for any frontend work
   - Frontend tasks include: React components, TypeScript code, UI/UX work, styling, accessibility
   - Agent location: `.claude/agents/frontend-expert.md`
   - The frontend-expert writes code following all project rules and best practices

2. **Code Quality Enforcement Phase**
   - **MUST invoke the code-quality-enforcer agent** immediately after frontend-expert completes
   - Agent location: `.claude/agents/code-quality-enforcer.md`
   - This agent runs TypeScript and Prettier checks across the entire codebase
   - Fixes any type errors or formatting inconsistencies
   - Ensures code meets quality standards before completion

#### Agent Workflow Example
```
User Request (Frontend Task)
    ↓
Invoke frontend-expert agent
    ↓
Frontend code written/modified
    ↓
Invoke code-quality-enforcer agent
    ↓
TypeScript check → Fix errors
    ↓
Prettier format → Fix formatting
    ↓
Final verification → Task complete
```

**Important:** Never skip the code-quality-enforcer step after frontend work. This ensures consistent quality across the entire codebase.

## Technology Stack

### Core Technologies
- **React 19.2.0** - Modern UI library with latest features
- **Vite 7.2.2** - Fast build tool and development server with HMR
- **JavaScript (ES Modules)** - Primary development language

### Development Tools
- **ESLint 9.39.1** - Code quality and linting
- **Vite React Plugin** - Fast refresh and optimized React development
- **React Hooks** - Modern state management approach

### Styling
- **Pure CSS** - No framework dependencies
- **CSS Custom Properties** - Theme variables and consistent styling
- **Light/Dark Theme Support** - Automatic theme based on system preferences
- **Responsive Design** - Mobile-first approach with media queries

## Project Structure

```
training-app/
├── public/              # Static assets
│   └── vite.svg
├── src/                 # Source code
│   ├── assets/          # Images and media files
│   │   └── react.svg
│   ├── App.jsx          # Root component
│   ├── App.css          # Component-specific styles
│   ├── index.css        # Global styles and theme
│   └── main.jsx         # Application entry point
├── index.html           # HTML template
├── package.json         # Dependencies and scripts
├── vite.config.js       # Vite configuration
├── eslint.config.js     # ESLint configuration
└── .gitignore           # Git ignore rules
```

## Key Files

### Entry Points
- **index.html** - Root HTML file that loads the React application
- **src/main.jsx** - React entry point that mounts the App component
- **src/App.jsx** - Root React component (currently template code)

### Configuration Files
- **vite.config.js** - Vite build configuration with React plugin
- **eslint.config.js** - ESLint rules for code quality
- **package.json** - Project dependencies and npm scripts

## Development

### Prerequisites
- Node.js 20.12.2+ (currently using v20.12.2)
- npm 10.5.0+

### Getting Started

1. Install dependencies:
```bash
npm install
```

2. Start development server:
```bash
npm run dev
```

3. Open your browser to the URL shown in the terminal (typically http://localhost:5173)

### Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Create production build in `dist/` directory
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint to check code quality

## Current State

The project is currently in its **initial setup phase** with the default Vite React template.

### Implemented Features
- ✅ Basic React 19 project structure
- ✅ Vite build configuration
- ✅ ESLint setup for code quality
- ✅ Light/Dark theme support in CSS
- ✅ Hot Module Replacement (HMR) for fast development

### Pending Implementation
- ⏳ Goal creation and management
- ⏳ Progress tracking functionality
- ⏳ User interface for training app
- ⏳ Data persistence (localStorage or backend API)
- ⏳ Goal visualization and statistics
- ⏳ User authentication (if needed)

## Code Style

### React Patterns
- Functional components with hooks
- React 19's `createRoot` API for rendering
- Strict Mode enabled for development warnings

### Naming Conventions
- Components: PascalCase for component names (e.g., `App`, `GoalTracker`)
- Files: **kebab-case for ALL files** (e.g., `app.jsx`, `goal-tracker.jsx`, `user-utils.js`)
- CSS: kebab-case for class names
- Variables/Functions: camelCase
- Constants: UPPER_SNAKE_CASE

### ESLint Rules
- React Hooks rules enforced
- React Refresh compatibility for Vite HMR
- No warnings on unused vars for PascalCase names (components)

## Building for Production

1. Create production build:
```bash
npm run build
```

2. The optimized build will be in the `dist/` directory

3. Preview the production build:
```bash
npm run preview
```

## Future Enhancements

Potential features to implement:
- Goal categories (strength, cardio, flexibility, nutrition, etc.)
- Progress charts and visualizations
- Reminders and notifications
- Achievement badges and milestones
- Social sharing capabilities
- Export progress data
- Mobile-responsive design optimization
- Progressive Web App (PWA) capabilities

## Git Repository

This project is version-controlled with Git. The repository is initialized and ready for commits.

## Notes

- The project uses React 19.2.0, which includes the latest React features
- Vite provides extremely fast HMR and build times compared to traditional bundlers
- No TypeScript currently, but type definitions are available if migration is desired
- No state management library (Redux, Zustand) yet - will evaluate based on complexity needs
- No routing library yet - will add React Router if multi-page navigation is needed

## Contributing

When adding new features:
1. Create feature branch from main
2. Follow existing code style and conventions
3. Run `npm run lint` before committing
4. Test in both light and dark themes
5. Ensure responsive design works on mobile devices

---

**Last Updated:** 2025-11-12
**Status:** Initial Setup - Ready for Feature Development
