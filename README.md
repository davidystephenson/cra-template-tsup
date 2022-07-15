# cra-template-tsup

Quickly publish Create React App with TypeScript to NPM.

## `yarn start`

Runs the app in the development mode at [http://localhost:3000](http://localhost:3000).

## `yarn build`

Builds the app for production to `/build`.

## `yarn pack`

Packages `src/App.tsx` for publishing to `/dist`.

## Publishing

1. Run `yarn pack` to package for publishing.
1. In package.json:
  1.1 Remove `"private": true` to allow public access.
  1.1 Add `"files": ["dist"]` to avoid ignoring.
  1.1 Add `"main": "dist/App.js"` as the entry point.
  1.1 Add `"types": "dist/App.d.ts"` as the type definitions.
1. Release with `npm publish`.
