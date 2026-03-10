# Gatsby + Contentful Demo Project (Reference Implementation)

## ℹ️ Overview

This repository is a **streamlined demonstration project** built to document and preserve a working setup for a **Gatsby + Contentful** website.

**Objective:**

- Capturing a minimal, repeatable setup
- Serving as a personal reference for future projects
- Demonstrating integration patterns without production complexity

This is intentionally a **demo and learning artifact**, not a full-featured application.

## 📄 What This Project Demonstrates

- Static site generation with **Gatsby**
- Headless CMS integration using **Contentful**
- Type-safe React components with **TypeScript**
- Modern styling using **Tailwind CSS**
- Image and Markdown rendering via Gatsby plugins
- Environment-based configuration for local and hosted builds
- Netlify deployment configuration

## 🛠 Tech Stack

- React
- Gatsby
- TypeScript
- ESLint
- Jest (unit testing)
- Tailwind CSS + PostCSS
- Heroicons
- Lodash (debouncing)
- Gatsby plugins for images and Markdown
- Netlify (hosting & CI)


## 📁 Project Structure Highlights

- `src/pages/index.tsx`
    - Generates the homepage

- `gatsby-node.ts`
    - Dynamically creates pages at build time

- `src/templates/ProfilePageTemplate.tsx`
    - Template used for Contentful-driven pages

## 🚀 Running the Project Locally

### 1. Environment Variables

Create an environment file:

```bash
.env.development
```

Copy contents from `_env.sample` and populate:

```text
CONTENTFUL_SPACE_ID=
CONTENTFUL_ACCESS_TOKEN=
```

You may also create `.env.production` for production builds.

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development Server

```bash
npm run dev
```

## 🛠 Available Scripts

```
npm run dev
npm run build
npm run serve
npm run clean
npm run test
npm run lint
npm run typecheck
```

## 📦 Contentful Data Model

This demo uses a small, opinionated Contentful schema.

### Content Model: Skill

- **Name**
    - Short text
    - Entry title
    - Required

### 📦 Content Model: Consultant

Includes fields for:

- Activation status
- Slug-based routing
- Contact information
- Location
- Profile image
- Markdown bio
- Related skills
- Availability window
- Hourly fee

This model is intentionally verbose to demonstrate:

- Field validation
- Reference fields
- Date handling
- Markdown rendering

> After creating models, add a placeholder entry named **PLACEHOLDER** and mark inactive where applicable.

## 🚀 Deployment Notes

- Environment variables must be configured in Netlify
- Builds are triggered automatically on push
- Gatsby build output is served as a static site

## 💡 Scope & Intent

This project is intentionally limited in scope:

- No authentication
- No mutations or CMS write access
- No advanced state management

Its purpose is to act as a **clear, minimal reference** for:

- Gatsby + Contentful wiring
- Static site generation workflows
- CMS-driven page creation

## 📄 License

MIT
