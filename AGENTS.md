## Project Configuration

- **Language**: TypeScript
- **Framework**: SvelteKit / Svelte 5
- **Package Manager**: bun
- **Add-ons**: prettier, eslint, vitest, playwright, tailwindcss, experimental, mcp
- **UI primitives**: bits-ui

---

## Project Conventions

### Layout / Blocks

- Use reusable `*Block` components for page sections.
- Most page sections should use `BlockWrapper`, which renders:
  - a full-width wrapper
  - `px-4 sm:px-8`
  - a centered Tailwind `container`
- Do not add extra `max-w-*` to block containers unless there is a specific design reason; Tailwind’s `container` handles page width.
- Full-width sections, like the hero image, can sit outside the container, but their text content should still use `BlockWrapper`.

### Rich Text / Prose

- Use `RichText` for Tailwind Typography prose styling.
- Do not put `max-w-none` on `RichText` by default; let the `prose` class control readable line length.
- For simple centered copy sections, use `ProseBlock`.
- Use the site/page wrapper’s `space-y-*` utilities for vertical rhythm between blocks.
- Do not put default vertical padding in block components, and do not pass default spacing classes at call sites.
- For content blocks, `class` should mean supplemental styling for the primary visible/content element, not block spacing.
- Use `wrapperClass` only as an escape hatch when a section needs explicit block-level spacing.
- `ProseBlock` should center the prose column with `mx-auto` and allow the container to remain full `container` width.
- Put headings directly inside prose content instead of passing separate header props/snippets; this keeps one convention for rich text structure.

### Components

Current shared components:

- `BlockWrapper` — standard full-width wrapper + centered container.
- `HeroBlock` — full-width image hero with overlay text inside `BlockWrapper`. Its `class` prop is for supplemental hero prose styling.
- `TextImageBlock` — 50/50 text/image section with optional `imagePosition="left" | "right"`. Its `class` prop is for supplemental prose styling.
- `ProseBlock` — simple centered prose section. Its `class` prop is for supplemental prose styling.
- `RatesBlock` — responsive rate/package cards. Its `class` prop is for supplemental card grid styling.
- `AccordionBlock` — FAQ accordion using `bits-ui` Accordion. Its `class` prop is for supplemental accordion root styling.
- `ContactBlock` — two-column contact details/form block. Use `detailsClass` and `formClass` for supplemental card styling.
- `Footer` — minimal site footer with contact/location details.
- `Image` — enhanced image wrapper. Pass imported `?enhanced` images via `src`; falls back to `https://placehold.co/{width}x{height}` when no `src` is passed.
- `RichText` — Tailwind prose wrapper.

### Copy / Content

- Use supplied client copy exactly where possible, lightly correcting obvious typos/punctuation only when helpful.
- Any copy or headings derived by us, and not present in the client’s original text, should be visibly marked in red for review.
  - For prose body text: `text-red-600`
  - For prose headings: include `prose-headings:text-red-600`
  - On dark hero gradients, use a lighter red such as `text-red-300`.
- Headers after the hero should be `h2`.
- Hero titles are `h1`; hero subtitles can be `h2`.

### Images

- Use images from `src/lib/assets/images` when a filename fits the section.
- Use Svelte enhanced images by importing local images with `?enhanced` and passing them to `Image`, `HeroBlock`, or image-based blocks.
- Placeholder URL format remains `https://placehold.co/600x400` or an appropriately sized variant when no local image is available.
- `HeroBlock` handles its own full-width image behavior.

### Brand Reference

Client brand colors for later design work:

- `#493931`
- `#F9FBEB`
- `#5B826B`
- `#E0B85C`
- `#255F7F`

The latter three are accent colors.

---

## Svelte MCP Instructions

You are able to use the Svelte MCP server, where you have access to comprehensive Svelte 5 and SvelteKit documentation. Here's how to use the available tools effectively:

### 1. list-sections

Use this FIRST to discover all available documentation sections. Returns a structured list with titles, use_cases, and paths.
When asked about Svelte or SvelteKit topics, ALWAYS use this tool at the start of the chat to find relevant sections.

### 2. get-documentation

Retrieves full documentation content for specific sections. Accepts single or multiple sections.
After calling the list-sections tool, you MUST analyze the returned documentation sections (especially the use_cases field) and then use the get-documentation tool to fetch ALL documentation sections that are relevant for the user's task.

### 3. svelte-autofixer

Analyzes Svelte code and returns issues and suggestions.
You MUST use this tool whenever writing Svelte code before sending it to the user. Keep calling it until no issues or suggestions are returned.

### 4. playground-link

Generates a Svelte Playground link with the provided code.
After completing the code, ask the user if they want a playground link. Only call this tool after user confirmation and NEVER if code was written to files in their project.
