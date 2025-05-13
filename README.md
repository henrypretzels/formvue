# formvue

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking.  
In editors, we need [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) to make the TypeScript language service aware of `.vue` types.

## Customize Configuration

See the [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
##Compile and Hot-Reload for Development

npm run dev

##Type-Check, Compile and Minify for Production

npm run build

##Lint with ESLint

npm run lint

##Initialize Local Server (with json-server)

##This project uses json-server to simulate a REST API for development purposes. The server runs at http://localhost:3000.
Setup

##Install json-server globally:

npm install -g json-server

##Or install it as a development dependency:

npm install --save-dev json-server

##Run the Server

##Start the server on port 3000:

json-server --watch db.json --port 3000

##Access the API at: http://localhost:3000

