# cra-template-tsup

Quickly publish Create React App with TypeScript to NPM.

## `yarn start`

Start in development mode at [http://localhost:3000](http://localhost:3000).

## `yarn build`

Build for production to `/build`.

## `yarn pack`

Package `src/App.tsx` for publishing to `/dist`.

## Publishing

1. Package for publishing with `yarn pack`.
1. In package.json:

    1. Remove `"private": true` to allow public access.
    1. Move `"react-scripts"` to `"devDependencies"`.
    1. Move `"react"` and `"react-dom"` to `"devDependencies"`.
    1. Add `"files": ["dist"]` to avoid ignoring.
    1. Add `"main": "dist/App.js"` as the entry point.
    1. Add `"types": "dist/App.d.ts"` as the type definitions.

1. Release with `npm publish`.
