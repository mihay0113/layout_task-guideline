# Guideline how to implement solution for Layout tasks 
1. **Fork** the repo.
2. **Clone** the forked one. (The project link should have your name but not `mate-academy`).
3. Go to create folder by running `cd your-project-name`.
4. Run `npm install` (or just `npm i`).
5. Run `npm start` to check if it works.
6. Open one more terminal window for the next steps
7. Create `develop` branch `git checkout -b develop`
8. Open code editor and replace `<your_account>` with your Github username in the `DEMO LINK` and `TEST REPORT LINK` of `readme.md`
9. Write you code in `index.html`, `style.css` inside `src` folder
10. Run `npm test` to check if you solved the task (and fix all errors if any).
    - Run `npm run lint` if you don't see the diff in browser and fix code style errors.
    - Run `npm start` if reference is empty in browser diff.
11. Commit and push your changes.
    - Run `git commit -am "write a short description of the changes you made"` to commit changes.
        - If you created new files additionally run `git add path/to/file1 path/to/file2`.
    - Run `git push origin develop` to push your changes to the GitHub.
    - Run `npm run deploy` to deploy changes to GitHub pages (use Git Bash when working on Windows). 
12. Create a Pull Request (PR) from your branch `develop` to branch `master` of original repo.
13. Copy `DEMO LINK` and `TEST REPORT LINK` from `readme.md` to the PR description.
14. Check your work using checklist (look for it in the root directory of the project) before submitting it for review.

> To update you PR repeat steps 9-11

## Linux users
> If you use _linux_ please make sure you adjusted writing permissions to let 
scripts work without `sudo`. Correct permissions means you don't see errors like
`permission denied` after running commands in CLI.

## NPM commands
- `npm install` installs the project dependencies and runs `postinstall`
  - which create reference files for pixel perfect and tests 
- `npm start` runs the server required for development and tests
- `npm test` runs linter and tests
  - `npm run lint` runs linter (code style check)
  - `npm run test:only` runs pixel perfect tests
- `npm run deploy` publishes the page and test report to `gh-pages` 

## Video guides
- [How to solve HTML tasks](https://youtu.be/haCRZ3gNjOs)
- [How to use pixel perfect extension](https://youtu.be/zqRko57AurU)

## Useful links
- [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- [Working with figma](./figma.md)
- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)
