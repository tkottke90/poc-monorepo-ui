# Setup

This document outlines the steps I took to setup this repository.

## Repository Setup

To get started knew I was going to use [NX]() for managing the repository,  I initialized the NX repo using the init command:

```sh
npx nx@latest init
```

Then, I needed to add some additional NX packages specifically for what I was building:

```sh
npm install -D @nx/js @nx/react
```

## Application Setup

The main application shell was the next thing I setup.  This was created in the `apps/` directory.  Using the `@nx/react` package I setup and installed it will the following flags for bundling, linting, routing, and unit tests:

```sh
npx nx g @nx/react:application apps/main --bundler=vite --linter=eslint --unitTestRunner=vitest --useReactRouter=true
```

## Module Setup

