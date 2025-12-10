# TypeScript Starter Template

**For extremely basic (no build) frontend projects only**

## Install

- Visit the GitHub repo for this template
- click "Use this template" > "Create a new repository"
- follow the GitHub instructions to clone the new repo to your local system.
- cd into the new repo's project folder
- run `npm install`

## Usage

- to write TypeScript, go to `src/script.ts`
- to write HTML, go to `public/index.html`
- to write CSS, go to `public/link.css`
- for local development, run `npm run dev`
- compiled JavaScript files can be found in `dist/`
- drag the index.html file from your file explorer to your browser

## My notes on how I created the starter template

```
mkdir typescript-starter-project
cd typescript-starter-project
mkdir src/ dist/ public/
npm init -y

npm install --save-dev eslint @eslint/js typescript typescript-eslint
npm install --save-dev --save-exact prettier

touch public/index.html public/link.css src/script.ts

# create tsconfig.json

# create eslint.config.mjs

# create empty Prettier config file
node --eval "fs.writeFileSync('.prettierrc','{}\n')"

# create prettierignore file
node --eval "fs.writeFileSync('.prettierignore','# Ignore artifacts:\nbuild\ncoverage\n')"

# compile ts
npx tsc

# alternative compile for dev setup
npx tsc --watch

# run eslint
npx eslint .

# run prettier
npx prettier . --write
```