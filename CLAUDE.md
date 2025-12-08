# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an AI consultancy website targeting small to medium-sized businesses (10-500 employees). The core services include:
- AI Prompt Engineering & Optimization (video, image, text content)
- Custom Software Development (low to mid-complexity applications)
- AI Integration Consulting

The business model focuses on practical, ROI-focused AI implementation for non-technical business leaders with transparent pricing and human-centric approach.

## Tech Stack

**Frontend**:
- Next.js 15 with App Router (TypeScript)
- Tailwind CSS + Framer Motion
- Radix UI primitives for accessibility
- React Hook Form + Zod for validation

**Backend & Infrastructure**:
- Vercel (hosting and deployment)
- Supabase (PostgreSQL database)
- Server actions for form handling
- Plausible Analytics (privacy-focused)

**Third-party Integrations**:
- Calendly (appointment booking)
- ConvertKit (newsletter)

## Getting Started

Initialize the project:
```bash
npx create-next-app@latest ai-consultancy --typescript --tailwind --app
cd ai-consultancy
npm install @radix-ui/react-dialog framer-motion lucide-react @hookform/resolvers zod
npm install -D @tailwindcss/typography @tailwindcss/forms
```

## Design System

### Color Palette (Tech Human Theme)

**Primary (Deep Space Navy)**: Authority and trust
- Primary shades: 900 (#0a0f1c) to 100 (#d3e6ff)
- Use for: Headlines, CTAs, navigation, trust elements

**Accent (Electric Cyan)**: Innovation and future
- Accent-500: #00f5ff (main)
- Use for: Interactive elements, highlights, tech references

**Warm (Amber)**: Human connection
- Warm-500: #ffb347 (main)
- Use for: Testimonials, human stories, warmth indicators

### Typography

- **Display**: 'Cal Sans' - Impactful headlines (weight: 400-700, line-height: 1.1)
- **Body**: 'Inter' - Readable content (weight: 300-600, line-height: 1.6)
- **Mono**: 'JetBrains Mono' - Code examples, technical terms

### Design Principles

1. Human-Centric Minimalism: Clean lines with human warmth
2. Data-Driven Layouts: Information hierarchy based on user behavior
3. Progressive Disclosure: Show complexity gradually
4. Inclusive Design: WCAG AA compliance required

## Key Features & Pages

### Business Audit Form (Critical Lead Capture)
The business audit form is the primary lead generation tool. Form fields:
- First Name (required, text)
- Last Name (required, text)
- Company Name (required, text)
- What Your Company Does (required, textarea)
- Email (required, email validation)
- Phone Number (optional, tel)
- Submit button: "AUDIT MY BUSINESS" (prominent green, all caps)

Must include privacy policy link and "no spam" trust indicators.

### Homepage Structure
1. Hero: "Transform Your Business with AI That Actually Works"
2. Value props (3-column): Fast Implementation, ROI-Focused, Human-Centric
3. Business Audit CTA section with form teaser
4. Social proof: Client logos, testimonials, metrics
5. Services preview cards
6. Secondary CTA: "Start Your AI Journey"

### Service Pages
1. AI Prompt Engineering - Before/after examples, pricing tiers
2. Custom Development - Tech stack options, process explanation
3. AI Integration Consulting - Assessment process, implementation timeline

### Content Strategy
- **Brand Voice**: Confident but approachable, expert but not elitist
- **Language**: Business-focused, outcome-oriented, jargon-light
- **Messaging**: Focus on practical applications and tangible business outcomes
- **Avoid**: AI buzzwords without substance, generic claims

## Architecture Decisions

### Avoid Over-Engineering
This is a consultancy website for SMBs, not enterprise software:
- Keep solutions simple and focused on immediate business needs
- Don't add abstractions for one-time operations
- Only validate at system boundaries (user input, external APIs)
- Trust internal code and framework guarantees

### Performance Targets
- Page load time: <2 seconds
- Mobile usability: 95%+ score
- SEO: Optimize for "AI consultancy [location]" keywords
- Accessibility: WCAG AA compliance mandatory

### SEO & Content
- Content-first approach
- Technical SEO from day 1
- Structured data for all service pages
- Blog system using MDX for case studies and tips

## Development Workflow

The project follows an MVP-first approach with fixed feature sets to avoid scope creep. Development is organized in phases (see PLAN.md for full details):

1. Foundation: Project setup, design system, homepage
2. Core Features: Service pages, contact forms, portfolio, about page
3. Advanced Features: Blog (MDX), service calculator, booking integration
4. Polish & Launch: Content optimization, A/B testing, analytics

## Form Handling Pattern

Use React Hook Form + Zod + Server Actions:
```typescript
// Typical form flow:
// 1. Define Zod schema for validation
// 2. Use useForm with zodResolver
// 3. Submit to server action
// 4. Store in Supabase
// 5. Provide user feedback
```

## Important Constraints

1. **Target Audience**: Non-technical business leaders - keep UI intuitive
2. **Pricing Transparency**: All pricing must be clear and upfront
3. **Mobile-First**: SMB decision-makers often browse on mobile
4. **Privacy**: GDPR compliant, privacy-focused analytics only
5. **Brand Consistency**: Maintain "Tech Human" theme throughout

## Competitive Differentiation

This is NOT a generic "AI solutions" company. Key differentiators:
- SMB specialization (not enterprise)
- Practical AI applications (not theoretical)
- Consultant relationship (not just vendor)
- Transparent pricing (no surprise fees)
- Fast execution (agile approach)
