# AI Consultancy Website

Professional AI consultancy website for small to medium-sized businesses, specializing in prompt engineering, custom software development, and AI integration consulting.

## Project Overview

This website positions the consultancy as the go-to expert for AI integration, offering premium services with a focus on tangible business outcomes over buzzwords.

### Core Services

- **AI Prompt Engineering & Optimization** - Video, image, and text content prompts
- **Custom Software Development** - Low to mid-complexity AI-powered applications
- **AI Integration Consulting** - ROI-focused AI implementation roadmaps

### Target Audience

Small to medium businesses (10-500 employees), non-tech founders and executives seeking practical AI solutions.

## Tech Stack

- **Framework**: Next.js 15 (App Router) with TypeScript
- **Styling**: Tailwind CSS + Framer Motion
- **UI Components**: Radix UI primitives
- **Database**: Supabase (PostgreSQL)
- **Hosting**: Vercel
- **Analytics**: Plausible (privacy-focused)

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
# Initialize Next.js project
npx create-next-app@latest ai-consultancy --typescript --tailwind --app
cd ai-consultancy

# Install dependencies
npm install @radix-ui/react-dialog framer-motion lucide-react @hookform/resolvers zod
npm install -D @tailwindcss/typography @tailwindcss/forms
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the site.

## Design System

The site uses a "Tech Human" theme balancing technological innovation with human warmth:

- **Primary**: Deep Space Navy (#0a0f1c - #d3e6ff) for authority and trust
- **Accent**: Electric Cyan (#00f5ff) for innovation
- **Warm**: Amber (#ffb347) for human connection

## Project Structure

See [PLAN.md](./PLAN.md) for detailed development roadmap and [CLAUDE.md](./CLAUDE.md) for technical guidance.

## License

Proprietary - All rights reserved
