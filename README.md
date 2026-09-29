# Speech Grid GitHub Pages demo

This build uses sample accounts and in-memory demo data. There is no Python server, real inference, or permanent storage. The waveform plays an eight-second synthetic signal, not a recording. Pipeline editing is available; execution explains that a backend is required. Do not use real credentials or confidential audio in a demo.

## Build

Requires Node.js 22 and npm. Run from this frontend directory:

```powershell
npm ci
npm run build:demo
```

`build:demo` uses `.env.demo`, relative asset URLs and hash routes so subdirectory hosting and refresh work on GitHub Pages. The ordinary `npm run build` keeps the backend-enabled configuration and browser routes.

Publish the contents of `dist/` and an empty `.nojekyll` file to the `main` branch of the dedicated `speechgrid-demo` repository. Configure Pages to deploy from `main` and `/ (root)`. Only compiled website assets are published. Backend files, model weights, original user data and source maps are excluded.

## Sample login

The researcher account is prefilled. Click Login, or select Admin demo first.

| Role | Username | Demo password |
| --- | --- | --- |
| Researcher | pm@speechgrid.com | pm123 |
| Administrator | admin@speechgrid.com | admin123 |

Project lists, uploads and administration use example data. Changes may reset when the page reloads. Real registration and analysis require a separately deployed backend.
