# responsive-images

## Overview

This is the repository for my course "Mastering responsive HTML images 🌉". It contains the
following resources for students of the course:

1. The source code for each video to code along with is located in folder `code-along`.
2. The course slides I use in the videos are located in folder `slides`.

## Tech stack for the slides

- Animotion `@animotion/core` for the slide logic.
- SvelteKit v2.
- Svelte v5.
- TypeScript.
- Components shared among slides are located in `slides/src/lib/components`.
- Tailwind v4 for styling.

## Tech stack for the code-along folder

- Each sub-directory contains a self-contained Vite project.
- Anything in a `public` folder is available at the root URL.

## Code style

- Always use Svelte v5 syntax.
- Always use TypeScript.
- In Svelte components, create an interface `Props` for the component's props.
- Use TailwindCSS for styling and tailwind-merge for class merging.
- Comments use proper punctuation and end with a period.
