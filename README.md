# Guideline how to implement solution for Github tasks
1. **Fork** the repo.
2. **Clone** the forked one. (The project link should have your name but not `mate-academy`).
3. Open the created folder in terminal by running `cd your-project-name`.
4. Run `npm install` (or just `npm i`).
5. Run `npm start` to check if it works.
    - At this point you should see the starting markup of the page at `http://localhost:8080/` opened in your Google Chrome
    - Update something in `src/index.html`. The change should be immediately updated in the browser.
    - If your URL has another port (not `:8000`) it means you already have a terminal with a running `npm start` command (maybe it is another project)
        - Stop the `npm start` command in current project by pressing `ctrl + c` (all operation systems)
        - Close the other terminal running `npm start`
        - Run the command again for your current project
        - The URL should be now `http://localhost:8080/`
6. Open one more terminal window for the next steps.
7. Create `develop` branch by running `git checkout -b develop`
    - If you see an error with `already exists` text it means you already have the `develop` branch. Just use it
8. Open code editor and replace `<your_account>` with your Github username in the `DEMO LINK` and `TEST REPORT LINK` of `readme.md`
9. Write you code in `index.html`, `style.css`, `main.js` inside `src` folder
10. Run `npm run lint` to check the code style.
    - Fix all the errors and run the command again
11. To check if your solution matches all the expectations you can run `npm test`
    - If you see a failing test you can click on it and see the difference by choosing `REFERENCE` and `TEST` at the top
    - If you see an `ENGINE ERROR: net::ERR_CONNECTION_REFUSED at http://localhost:8080/index.html` it means you don't have a running server
        - Open new terminal and run `npm start`
        - Check if the page is opened at `:8080` port (`http://localhost:8080/`)
        - Run `npm test` again to see the results
    - If test results are not opened in a browser, check if you fixed all the code style errors (`npm run lint`)
    - If you can't run tests for some weird reason just use a page screenshot from
      `backstop_data/bitmaps_reference/Entire_document.png` to ensure your page looks as expected. 
12. Commit and push your changes.
    - Run `git commit -am "write a short description of the changes you made"` to commit changes.
        - If you created new files additionally run `git add path/to/file1 path/to/file2`.
    - Run `git push origin develop` to push your changes to the GitHub.
    - Run `npm run deploy` to deploy changes to GitHub pages (use Git Bash when working on Windows).
        - project should be running at localhost:8080 during this step(`npm start`).
13. Create a Pull Request (PR) from your branch `develop` to branch `master` of original repo.
14. Copy `DEMO LINK` and `TEST REPORT LINK` from `readme.md` to the PR description.
15. Check your work using checklist (look for it in the root directory of the project) before submitting it for review.
16. To update you PR repeat steps 9-12 (no need to create the PR one more time).

> If you need an ADDITIONAL CODE REVIEW, click on re-request button at the PR page.
![Image of re-request button](https://user-images.githubusercontent.com/38065883/104471439-89929200-55c3-11eb-824a-596bfb8aa246.png)

## Linux users
> If you use _linux_ please make sure you adjusted writing permissions to let 
scripts work without `sudo`. Correct permissions mean you don't see errors like
`permission denied` after running commands in terminal.

## NPM commands
- `npm install` installs the project dependencies and runs `postinstall`
  - which create reference files for pixel perfect and tests 
- `npm start` runs the server required for development and tests
- `npm test` runs linter and tests
  - `npm run lint` runs linter (code style check)
  - `npm run test:only` runs pixel perfect tests
- `npm run deploy` publishes the page and test report to `gh-pages` 

## Useful links
- [NPM and GIT commands](https://mate-academy.github.io/fe-program/css/useful-commands)
- [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- [Working with figma](./figma.md)
- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)
- [How to use pixel perfect extension](https://youtu.be/zqRko57AurU)
