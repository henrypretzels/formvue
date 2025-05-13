formvue

This template should help get you started developing with Vue 3 in Vite.
Recommended IDE Setup

    VSCode + Volar (and disable Vetur).

Type Support for .vue Imports in TS

    TypeScript cannot handle type information for .vue imports by default, so we replace the tsc CLI with vue-tsc for type checking.
    In editors, we need Volar to make the TypeScript language service aware of .vue types.

Customize configuration

    See Vite Configuration Reference.

Project Setup

sh

npm install

Compile and Hot-Reload for Development

sh

npm run dev

Type-Check, Compile and Minify for Production

sh

npm run build

Lint with ESLint

sh

npm run lint

Initialize Local Server (with json-server)

This project uses json-server to simulate a REST API for development purposes. The server runs at http://localhost:3000.
Setup

    Install json-server globally:

sh

npm install -g json-server

    Or as a development dependency:

sh

npm install --save-dev json-server

    Create a db.json file in the root of your project with some mock data. Example:

json6 lines
Click to expand

{
"users": [
...

Run the Server

    Start the server on port 3000:

sh

json-server --watch db.json --port 3000

    Access the API at: http://localhost:3000
