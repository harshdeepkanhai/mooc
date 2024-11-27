https://scottmoss.notion.site/scottmoss/Intro-to-Node-js-V3-7c8e4ccaebf94b839f425fff13dcc44c

## Install node

- fnm/ NVM/

## Browser vs Node

- window in browser
- global in nodejs
- No DOM in nodejs
- We can create a server in Nodejs

# CLI

## Process & envrionmets

- process.argv
- process.env.NODE_ENV
- $env:NODE_ENV="Production"; node .\intro-node\index.js

## Custom CLI Setup

- npm init
- npm link

## Processing CLI Arguments

# Modules

## Modules Overview

- `"type": "module",` in `package.json`

## Importing & Exporting Modules

- `require` for CJS(Common JS)
- `exports.name` or `module.exports` in CJS
- `export const name` or `export default name` in MJS
- `import {name}` or `import name` in MJS

## Thinking in Modules

-

## Internal & 3rd-Party Modules

Internal modules

- `node:fs`
- `node:crypto`
- `node:http`
- `node:path`
- `node:os`
- etc

3rd Party modules

- `npm install <package-name>` installed in node_modules
- `npm install` if package.json is present.
- `npm uninstall <package-name>` to remove package
