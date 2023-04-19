# How to deploy to GitHub Pages

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
