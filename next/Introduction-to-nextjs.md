 beginner-friendly article introducing Next.js. It explains why Next.js exists(react using react you have to install third part libring for routing), its core features, how to create a new project, the basic project structure, a simple "Hello, World!" example, and the tradeoffs of using the framework.
Your main content. Explain the pattern, technique, or approach.

# Introduction to Next.js

> **Topic:** Next.js · **Level:** Beginner · **Author:** [@geliettech](https://github.com/geliettech)

<!--
How to use this template:
1. Copy this file into the relevant folder (e.g. react/, performance/)
2. Rename it using kebab-case: e.g. error-boundaries-in-practice.md
3. Use the sections below if applicable or add any sections that are necessary for your article
4. Add a link to your article in the folder's README.md index
-->

## The Problem

What problem does this solve? Why should the reader care?

Describe the situation a developer is in when they need this knowledge. Make it concrete.
what react can't solve

## The Solution


```tsx
// Keep code examples focused and production-oriented.
// Show the relevant part, not the whole app.
```

If you're demonstrating an improvement, show **before** and **after**:

```tsx
// Before
```

```tsx
// After
```

## Tradeoffs

No solution is free. Be honest about the costs:

- **When this shines:** ...
- **When to avoid it:** ...
- **What you give up:** ...

## Key Takeaways

- 3–5 bullet points the reader should remember
- Each should stand on its own
- Think: "what would I tell a teammate in 30 seconds?"

## References *(optional)*

- [Link to docs, talks, or articles that go deeper](https://example.com)




















# Introduction to Next.js

> **Topic:** Next.js · **Level:** Beginner · **Author:** [@geliettech](https://github.com/geliettech)

## The Problem

React is one of the most popular libraries for building user interfaces. It makes it easy to create reusable components and interactive web applications.

However, React only focuses on building the **UI (User Interface)**. It doesn't provide everything you need to build a complete production-ready application.

When building a real-world application with React, you'll often need to figure out things like:

- Routing between pages
- Server-side rendering (SSR)
- Static site generation (SSG)
- Search Engine Optimization (SEO)
- Image optimization
- API endpoints
- Code splitting and performance optimization
- File-based project organization

To solve these problems, developers usually install and configure several libraries such as React Router, Express, Vite plugins, image optimization libraries, authentication solutions, and more.

As an application grows, managing all these tools can become difficult and time-consuming.

This is where **Next.js** comes in.

Next.js is a React framework that provides many of these features out of the box, allowing developers to focus more on building applications instead of configuring tooling.

---

## The Solution

### What is Next.js?

Next.js is an open-source framework built on top of React by **Vercel**.

It extends React with features that make building production-ready web applications much easier.

Some of its most popular features include:

- File-based routing
- Server-side rendering (SSR)
- Static Site Generation (SSG)
- Incremental Static Regeneration (ISR)
- API Routes
- Built-in image optimization
- Automatic code splitting
- Metadata management for SEO
- TypeScript support
- Fast Refresh during development

Instead of spending hours configuring your project, Next.js gives you sensible defaults that work immediately.

---

## Creating Your First Next.js Project

You can create a new Next.js application using the following command:

```bash
npx create-next-app@latest
```

Or using npm:

```bash
npm create next-app@latest
```

The installer will ask a few questions:

```text
✔ What is your project named?
✔ Would you like to use TypeScript?
✔ Would you like to use ESLint?
✔ Would you like to use Tailwind CSS?
✔ Would you like to use the App Router?
```

After installation, navigate into the project:

```bash
cd my-next-app
```

Start the development server:

```bash
npm run dev
```

Open your browser and visit:

```
http://localhost:3000
```

You should see your new Next.js application running.

---

## Understanding the Project Structure

A new Next.js project contains several folders and files.

```text
my-next-app/
│
├── app/
│   ├── layout.tsx
│   ├── page.tsx
│
├── public/
│
├── components/
│
├── styles/
│
├── package.json
└── next.config.ts
```

### Important folders

#### `app/`

This is where your application pages live when using the App Router.

Every folder inside `app` can represent a route.

Example:

```text
app/
    page.tsx
    about/
        page.tsx
```

Creates:

```
/
```

and

```
/about
```

---

#### `public/`

Stores static assets such as:

- images
- videos
- icons
- fonts

Example:

```text
public/logo.png
```

Can be accessed with:

```tsx
<img src="/logo.png" alt="Logo" />
```

---

#### `components/`

A common place to keep reusable UI components.

Example:

```text
components/
    Button.tsx
    Navbar.tsx
    Footer.tsx
```

---

#### `package.json`

Contains project information and dependencies.

---

#### `next.config.ts`

Used to configure Next.js behavior.

---

## Your First Page

Inside the `app` folder you'll find:

```tsx
export default function Home() {
  return <h1>Hello, World!</h1>;
}
```

Visiting:

```
http://localhost:3000
```

renders:

```text
Hello, World!
```

That's your first Next.js page.

---

## File-Based Routing

One of Next.js's biggest advantages is that routing is based on the file system.

Instead of writing route configurations manually, you simply create folders.

For example:

```text
app/
    about/
        page.tsx
```

Automatically creates:

```
/about
```

Another example:

```text
app/
    contact/
        page.tsx
```

Creates:

```
/contact
```

No additional router configuration is needed.

---

## Example: React vs Next.js Routing

### Before (React)

In a typical React application, you usually configure routes yourself.

```tsx
import { BrowserRouter, Routes, Route } from "react-router-dom";

<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
  </Routes>
</BrowserRouter>;
```

### After (Next.js)

Simply create the folder structure:

```text
app/
    page.tsx
    about/
        page.tsx
```

Next.js automatically creates the routes for you.

---

## Why Developers Like Next.js

Next.js reduces the amount of setup required for modern web applications.

Instead of combining many separate libraries, it provides a complete framework with features such as:

- Better SEO through server rendering
- Faster page loading
- Optimized images
- Built-in routing
- API endpoints
- Automatic performance optimizations
- Excellent developer experience

These features make it suitable for blogs, portfolios, dashboards, e-commerce websites, company websites, SaaS applications, and many other types of projects.

---

## Tradeoffs

No solution is perfect.

### **When this shines:**

- Building production-ready React applications
- Applications that need SEO
- Content-heavy websites
- E-commerce platforms
- Marketing websites
- Dashboards and SaaS products

### **When to avoid it:**

- Small learning projects where plain React is enough
- Applications that don't need server rendering or SEO
- Teams that only need a simple client-side application

### **What you give up:**

- More concepts to learn compared to React alone
- Build and rendering strategies (SSR, SSG, ISR, CSR)
- A framework with opinions about project structure
- Slightly larger learning curve for beginners

---

## Key Takeaways

- React builds user interfaces, while Next.js provides a complete framework for building production-ready React applications.
- Next.js includes features like routing, rendering strategies, image optimization, API routes, and SEO support out of the box.
- File-based routing makes creating pages simple—adding a folder with a `page.tsx` file automatically creates a route.
- Creating a new Next.js project is quick with `create-next-app`, allowing you to start building immediately.
- Next.js is an excellent choice for applications where performance, SEO, and developer productivity are important.

---

## References *(optional)*

- https://nextjs.org/docs
- https://nextjs.org/learn
- https://react.dev