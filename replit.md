# Overview

This is a statically generated blog built with Next.js 15, TypeScript, and Markdown. The application demonstrates Next.js's Static Site Generation (SSG) capabilities by using Markdown files as the content source. Blog posts are stored as `.md` files with front matter metadata and are processed at build time to generate static HTML pages. The project includes a clean, responsive design with dark mode support and focuses on performance through static generation.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: Next.js 15 with App Router architecture
- **Language**: TypeScript for type safety
- **Styling**: Tailwind CSS with custom design tokens for consistent theming
- **Components**: Modular React components organized by functionality
- **Dark Mode**: Client-side theme switching with system preference detection and local storage persistence

## Static Site Generation
- **Content Source**: Markdown files stored in `_posts` directory with YAML front matter
- **Processing Pipeline**: 
  - `gray-matter` parses front matter metadata from Markdown files
  - `remark` and `remark-html` convert Markdown content to HTML
  - Static generation occurs at build time for optimal performance
- **Routing**: Dynamic routes using Next.js file-based routing (`/posts/[slug]`)

## Content Management
- **Post Structure**: Each post contains title, excerpt, cover image, date, author, and content
- **Data Layer**: File-system based API functions in `/lib/api.ts` handle post retrieval and sorting
- **Type Safety**: TypeScript interfaces define Post and Author data structures

## Performance Optimizations
- **Static Generation**: All pages pre-rendered at build time
- **Image Optimization**: Next.js Image component with responsive loading
- **Caching**: Custom cache headers configured to prevent caching during development
- **Build Tool**: Turbopack enabled for faster development builds

## Design System
- **Typography**: Inter font family with custom size scales
- **Color Palette**: Neutral grays with accent colors and success states
- **Responsive Design**: Mobile-first approach with breakpoint-based layouts
- **Custom Styling**: CSS modules for component-specific styles (theme switcher, markdown content)

# External Dependencies

## Core Framework
- **Next.js 15.0.2**: React framework with SSG capabilities
- **React 19 RC**: UI library (release candidate version)

## Content Processing
- **gray-matter**: YAML front matter parsing from Markdown files
- **remark**: Markdown processor for content transformation
- **remark-html**: Plugin to convert Markdown AST to HTML strings

## Styling and UI
- **Tailwind CSS**: Utility-first CSS framework
- **PostCSS**: CSS processing with Autoprefixer
- **classnames**: Dynamic CSS class composition utility

## Utilities
- **date-fns**: Date formatting and manipulation
- **TypeScript**: Static type checking and development tooling

## Development Tools
- **Autoprefixer**: CSS vendor prefix automation
- **ESLint**: Code linting (configured via Next.js)
- **Hot Reload**: Development server with fast refresh