# AI Spokesperson Application

## Overview

This is a modern web application that provides an AI-powered spokesperson system for events. The application features a 3D animated virtual face that can deliver speech with synchronized facial animations, visual effects control, and real-time system monitoring. It's built using a full-stack architecture with React Three Fiber for 3D graphics, Express.js backend, and PostgreSQL database.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a monorepo structure with clear separation between client, server, and shared code:

- **Frontend**: React 18 with TypeScript, using Vite for development and building
- **Backend**: Express.js server with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **3D Graphics**: React Three Fiber for WebGL-based 3D rendering
- **UI Components**: Radix UI with shadcn/ui component library
- **Styling**: Tailwind CSS with custom design system
- **State Management**: TanStack Query for server state and React hooks for local state

## Key Components

### Frontend Architecture
- **3D Viewport**: Uses React Three Fiber to render an animated AI face with audio-reactive animations
- **Control Panels**: Modular components for speech control, visual effects, event management, and system monitoring
- **Design System**: Custom dark theme with neon cyan/purple color palette and glass morphism effects
- **Responsive Layout**: Grid-based layout optimized for desktop use

### Backend Architecture
- **RESTful API**: Express.js routes for managing speech content, event sessions, and visual effects
- **Data Storage**: Currently using in-memory storage with interface designed for easy database integration
- **Error Handling**: Centralized error handling with proper HTTP status codes
- **Development Tools**: Hot reload with Vite integration for seamless development

### Database Schema
- **Speech Content**: Stores text, voice settings, and metadata for AI speech
- **Event Sessions**: Manages event information, duration tracking, and attendee counts
- **Visual Effects**: Configurable color schemes, animations, and mood presets

### Audio & Speech System
- **Web Speech API**: Browser-native text-to-speech with configurable voice, pitch, and speed
- **Audio Visualization**: Real-time audio level monitoring with animated feedback
- **Speech Synchronization**: Facial animations synchronized with speech output

## Data Flow

1. **Speech Generation**: User inputs text → Speech controller validates and stores → Web Speech API generates audio → 3D face animates
2. **Visual Effects**: User adjusts settings → API updates database → Real-time UI feedback
3. **Event Management**: Session tracking with automatic duration updates and attendee management
4. **System Monitoring**: Simulated real-time metrics for CPU, GPU, memory, and system health

## External Dependencies

### Core Framework Dependencies
- **React Ecosystem**: React 18, React Three Fiber, React Router (wouter)
- **UI Library**: Radix UI primitives, shadcn/ui components
- **Database**: Drizzle ORM with PostgreSQL support via Neon Database
- **Development**: Vite, TypeScript, ESBuild for production builds

### Specialized Libraries
- **3D Graphics**: Three.js via React Three Fiber for WebGL rendering
- **Audio**: Native Web Speech API for text-to-speech
- **State Management**: TanStack Query for server state caching
- **Styling**: Tailwind CSS with custom design tokens
- **Form Handling**: React Hook Form with Zod validation

## Deployment Strategy

### Development Environment
- **Vite Dev Server**: Hot module replacement for frontend development
- **Express Server**: Development mode with request logging and error overlays
- **Database**: PostgreSQL via environment variable configuration
- **Build Process**: TypeScript compilation with path mapping support

### Production Build
- **Frontend**: Vite production build with optimized assets
- **Backend**: ESBuild bundling for Node.js deployment
- **Database Migrations**: Drizzle Kit for schema management
- **Environment**: Production-ready Express server with static file serving

### Database Integration
- **Current**: In-memory storage for development and testing
- **Production Ready**: PostgreSQL with Drizzle ORM migrations
- **Schema**: Well-defined tables for speech content, events, and visual effects
- **Connection**: Neon Database serverless PostgreSQL with connection pooling

The application is designed for easy deployment to platforms like Replit, with proper environment variable configuration and database provisioning support.