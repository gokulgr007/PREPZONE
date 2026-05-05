# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is enabled on this template. See [this documentation](https://react.dev/learn/react-compiler) for more information.

Note: This will impact Vite dev & build performances.

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

**Render Deployment**

- **Quick (Static Site)**: This project builds to a static `dist` folder with `npm run build` and can be deployed to Render as a Static Site.
	- Build command: `npm ci && npm run build`
	- Publish directory: `dist`
	- A `render.yaml` manifest is included at the repository root to simplify Render service creation.
	- Add any runtime environment variables (API endpoints, feature flags) via the Render Dashboard under the service's Environment section.

- **Commands to preview locally**:

```bash
npm install
npm run build
npx serve dist
```

- **Optional: Fullstack (Frontend + Express backend)**
	- If you need to run an Express backend (e.g. for server-side APIs or MongoDB access), you can either:
		- Host just the frontend as a Static Site on Render and host the backend as a separate Web Service (or use Render Managed Databases).
		- Or provide a `Dockerfile` and deploy a single Web Service that serves both frontend and backend. Ask me and I can add a `Dockerfile` + `render.yaml` variant for a web service.

If you'd like, I can add the Dockerfile+manifest now, or finalize environment-variable guidance for Render. 
