# Guideline how to implement solution for Layout tasks 
1. Fork the repo and clone the forked one.
2. Run `npm install` (or just `npm i`)
3. Run `npm start`. (Open one more terminal window for the next steps)
4. Write you code in `index.html`, `style.css` inside `src` folder
5. Run `npm test` to check if you solved the task. (Fix all errors if any)
    - Run `npm run lint` if you don't see the diff in browser and fix code style errors.
    - Run `npm start` if reference is empty in browser diff.
6. Run `npm run deploy` to share your solution
7. Create a Pull Request (PR) from your branch `develop` to branch `master` of original repo.
8. Copy `DEMO LINK` and `TEST REPORT LINK` to the PR description

> To update you PR repeat steps 5 and 6

## Useful links
- [Working with figma](figma.md)
- [Pixel perfect extension](https://www.youtube.com/watch?v=zqRko57AurU&list=PL7FuXFaDeEX15gwtyUNTuHHori210Nqol)
- [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)
- `NodeJS`, `npm` [download](https://nodejs.org/en/) or [read installation guide](https://nodejs.org/en/download/package-manager/)
- `git` [download](https://git-scm.com/downloads) or [read installation guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Linux users
> If you use _linux_ please make sure you adjusted writing permissions to let 
scripts work without `sudo`. Correct permissions means you don't see errors like
`permission denied` after running commands in CLI.

## NPM commands
- `npm install` installs the project dependencies and runs `postinstall`
  - `git checkout -b develop` is executed under the hood to create a `develop` branch and switch on it.
  - `npm run css:reference` create reference files for pixel perfect and tests 
- `npm start` runs the server required for development and tests
- `npm test` runs linter and tests
  - `npm run lint` runs linter (code style check)
  - `npm run css:test` runs linter (code style check)
- `npm run deploy` save the changes, push them to github and published to `gh-pages`
  - `git add .`, `git commit -m 'solution'` and `git push origin develop` are executed under the hood
  - `npm run publish` publishes the page and test report to `gh-pages` 
