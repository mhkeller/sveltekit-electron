SvelteKit + Electron template
===

This repo contains two configurations for setting up SvelteKit with Electron. 

1. The `main` branch uses `mainWindow.loadFile`
2. The `serve` branch uses [electron-serve](https://github.com/sindresorhus/electron-serve)

Both rely on `prerender=true` and `ssr=true` in the Svelteit layout config. 

The `prerender=true` option creates the HTML on build and `ssr=true` tells SvelteKit which page to load. Without the `ssr` option, SvelteKit will rely on `location.pathname` to know which route it is loading when pointed to an arbitrary HTML file. The file protocol based route does not work well with this logic so you need the route-information to be rendered server-side.

```sh
npm i
```

```sh
npm run build:svelte
npm run dev:electron
```
