# Interactive Learning Hub

## Overview

The Interactive Learning Hub is a full-stack web application that enables educators to create, manage, and deliver interactive learning modules. Built with React on the frontend and Express.js on the backend, it provides a visual editor for creating interactive content with hotspots, timelines, and multimedia elements.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for client-side routing
- **State Management**: Zustand with temporal middleware for undo/redo functionality
- **UI Components**: Radix UI primitives with custom styling using Tailwind CSS
- **Data Fetching**: TanStack React Query for server state management
- **Bundler**: Vite for development and production builds

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Runtime**: Node.js 20
- **Database**: PostgreSQL with Drizzle ORM
- **API Design**: RESTful architecture with JSON responses
- **Session Management**: Express sessions with PostgreSQL store
- **Development**: Hot reload with Vite middleware integration

## Key Components

### 1. Editor System
- **Canvas Editor**: Visual drag-and-drop interface for placing hotspots on background images
- **Properties Panel**: Form-based configuration for hotspot properties and interactions
- **Visual Timeline**: Step-by-step interaction sequencing with different action types
- **Undo/Redo**: Temporal state management for editor actions

### 2. Viewer System
- **Guided Mode**: Step-by-step navigation through learning content
- **Explore Mode**: Free exploration of interactive elements
- **Hotspot Interactions**: Support for messages, quizzes, audio, zoom, and highlighting
- **Responsive Design**: Mobile-friendly interface for content consumption

### 3. Project Management
- **Dashboard**: Overview of all learning projects with statistics
- **Project Cards**: Visual representation of projects with preview images
- **Admin Toggle**: Switch between viewer and admin modes
- **Share Functionality**: Generate shareable links and embed codes

## Data Flow

### Project Creation Flow
1. User navigates to editor from dashboard
2. Creates new project or loads existing project
3. Configures project settings (title, description, pages)
4. Adds background images and places interactive hotspots
5. Defines timeline events and interactions
6. Saves project to database via REST API

### Viewing Flow
1. User accesses project through dashboard or direct link
2. Viewer modal loads project data
3. Interactive elements are rendered on background image
4. User can navigate through guided timeline or explore freely
5. Interactions trigger appropriate responses (messages, quizzes, etc.)

## External Dependencies

### Frontend Dependencies
- **UI Library**: Radix UI for accessible component primitives
- **Styling**: Tailwind CSS for utility-first styling
- **Icons**: Lucide React for consistent iconography
- **Date Handling**: date-fns for date manipulation
- **Carousel**: Embla Carousel for image galleries
- **Validation**: Zod for runtime type checking

### Backend Dependencies
- **Database**: Neon serverless PostgreSQL
- **ORM**: Drizzle ORM for type-safe database operations
- **Session Store**: connect-pg-simple for PostgreSQL session storage
- **Validation**: Zod for schema validation
- **ID Generation**: nanoid for unique identifier generation

## Deployment Strategy

### Development Environment
- **Platform**: Replit with integrated PostgreSQL
- **Hot Reload**: Vite development server with Express middleware
- **Database**: Automatic schema migrations with Drizzle Kit
- **Port Configuration**: Frontend on port 5000, mapped to external port 80

### Production Build
- **Frontend**: Vite build process generates optimized static assets
- **Backend**: esbuild bundles server code for Node.js deployment
- **Static Files**: Served through Express static middleware
- **Database**: Environment-based connection string configuration

### Deployment Configuration
- **Autoscale**: Configured for automatic scaling based on demand
- **Health Checks**: Port-based health monitoring
- **Environment Variables**: DATABASE_URL for database connection
- **Build Process**: Automated build pipeline with npm scripts

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes

✓ **June 16, 2025** - Initial Interactive Learning Hub setup with modern glass-effect UI
✓ **June 16, 2025** - Modernized interface with visual controls:
  - Replaced text inputs with dropdowns, color pickers, and button groups
  - Created visual timeline with step markers and hotspot indicators
  - Fixed hover states for better icon visibility
  - Simplified interaction selector to single dropdown
  - Repositioned timeline to span only under canvas area

## User Preferences

**UI Design**: Prefers modern, visual interfaces with minimal text input. Favors dropdowns, buttons, chips, and visual timeline representations over text-heavy forms.

**Layout**: Timeline should be positioned under the image/canvas area only, not extending through the properties panel.