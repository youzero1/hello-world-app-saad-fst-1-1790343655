---
status: pending
title: Hello World App
---

1. Scaffold the base project files: `package.json`, `vite.config.ts`, `tsconfig.json`, `index.html`, and `src/main.tsx`. Configure the Vite plugins for Tailwind CSS v4 and the TanStack Router file-based route generator, and register the `@/` alias to `src/` in both `vite.config.ts` and `tsconfig.json`. Outcome: `npm run dev` starts a working dev server.

2. Create `src/styles/global.css` containing exactly the Tailwind v4 import line as its first line, and import it once from `src/main.tsx`. Outcome: Tailwind utility classes apply across the app.

3. Create the app shell at `src/routes/__root.tsx`: a root route rendering an `Outlet` inside a full-height wrapper with a light background (e.g. subtle neutral/slate tint) and default text color. Outcome: every page renders inside a consistent full-screen shell.

4. Create the home route at `src/routes/index.tsx` registered at path `/`. It renders a vertically and horizontally centered column containing a large responsive heading reading "Hello, World!" (scales from mobile to desktop via responsive text sizes, tight tracking, semibold/bold weight) and a smaller muted subtitle line beneath it. Outcome: visiting `/` shows the centered greeting on all screen sizes.

5. Extract the greeting UI into `src/components/Greeting.tsx`, accepting an optional `name` prop and rendering `Hello, {name}!` falling back to `World` when the name is empty or whitespace. Update `src/routes/index.tsx` to use it. Outcome: greeting markup is reusable and the route stays thin.

6. Optional enhancement — add local state in `src/routes/index.tsx` for the typed name and render a single labelled text input beneath the subtitle, styled with Tailwind (rounded border, padding, focus ring, centered text, constrained max width). Pass the value to `Greeting` so the heading updates live as the user types. Outcome: typing a name instantly personalises the greeting; clearing it returns to "Hello, World!".

7. Verify: run the dev server and check the page renders centered at mobile and desktop widths, the input is keyboard-focusable with a visible focus ring, and there are no TypeScript or console errors. Outcome: clean, responsive hello-world app ready to build on.
