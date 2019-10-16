# Guideline how to implement solution for Layout tasks 

## Video guides
- [How to solve HTML tasks](https://youtu.be/haCRZ3gNjOs)
- [How to use pixel perfect extension](https://youtu.be/zqRko57AurU)

## Instructions
1. **Fork** the repo.
2. **Clone** the forked one. (The project link should have your name but not `mate-academy`)
3. Run `npm install` (or just `npm i`)
    - if it fails rename `postinstall` command in `package.json` to `1postinstall` and run its parts separately.
4. Run `npm start`.
5. Open one more terminal window for the next steps
6. Replace `<your_account>` with your Github username in the `DEMO LINK` and `TEST REPORT LINK` of `readme.md`
7. Write you code in `index.html`, `style.css` inside `src` folder
8. Run `npm test` to check if you solved the task. (Fix all errors if any)
    - Run `npm run lint` if you don't see the diff in browser and fix code style errors.
    - Run `npm start` if reference is empty in browser diff.
9. Run `npm run deploy` to share your solution
    - this command saves changes and push them to github
    - if you don't have any changes you can run
        - `git push origin develop` - to send you code for PR
        - `npm run publish` - to publish you solution and test results on gh-pages
10. Create a Pull Request (PR) from your branch `develop` to branch `master` of original repo.
11. Copy `DEMO LINK` and `TEST REPORT LINK` from `readme.md` to the PR description

> To update you PR repeat steps 7-9

## Useful links
- [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- [Working with figma](./figma.md)
- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)

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
  - `npm run css:test` runs pixel perfect tests
- `npm run deploy` save the changes, push them to github and published to `gh-pages`
  - `git add .`, `git commit -m 'solution'` and `git push origin develop` are executed under the hood
  - `npm run publish` publishes the page and test report to `gh-pages` 
