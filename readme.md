# seb-52-hoot

Mono-repo approach -> 2 folders

## Init

From empty folder -> `hoot`

- git init
- touch .gitignore
- - [Contents](https://www.toptal.com/developers/gitignore/api/windows,osx,node,visualstudiocode)
- git add .
- git commit

## Commit lint

Idea is to enforce commit messages to start with `feat:`

Need something to let us know when we are committing

something -> git hooks -> husky is JS git hook manager

```bash
echo "export default { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
mv commitlint.config.js commitlint.config.mjs
npm install --save-dev husky
npx husky init
echo "npx --no -- commitlint --edit \$1" > .husky/commit-msg
```
