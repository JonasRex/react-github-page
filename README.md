# How to deploy to GitHub Pages

## With vite

### vite.config.js defineConfig

add this to the export file:
`export default defineConfig({ base: '/[repo]/', })`

### package.json

add this to the scripts:
`"deploy": "vite build && gh-pages -d dist"`

### Add deploy.sh to root

with this:

```
#!/usr/bin/env sh

# abort on errors
set -e

# build
npm run build

# navigate into the build output directory
cd dist

# if you are deploying to a custom domain
# echo 'www.example.com' > CNAME

git init
git checkout -B main
git add -A
git commit -m 'deploy'

# if you are deploying to https://<USERNAME>.github.io
# git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git main

# if you are deploying to https://<USERNAME>.github.io/<REPO>
# git push -f git@github.com:<USERNAME>/<REPO>.git main:gh-pages

cd -
```

### commit and push

### Install gh-pages package

`npm install gh-pages --save-dev`

### Deploy to GitHub Pages

`npm run deploy`

Done!

## With create react app

### Install github-pages package

`npm install gh-pages --save-dev`

### Add homepage to package.json

`"homepage": "http://[username].github.io/[repo]"`

### Add deploy script to package.json

`"scripts": { "predeploy": "npm run build", "deploy": "gh-pages -d build" }`

### Deploy to GitHub Pages

`npm run deploy`

### For more information

[GitHub Pages](https://pages.github.com/)
