# Guideline how to implement solution for Layout tasks

 - [Video guide](https://youtu.be/-Elt79BhPiM)
 - [Pixel perfect extension](https://www.youtube.com/watch?v=zqRko57AurU&list=PL7FuXFaDeEX15gwtyUNTuHHori210Nqol)

Every task:
- Includes `eslint`
- Includes `stylelint`
- Includes `htmllint`
- includes `visual regression testing`
- Includes `pre-commit` hooks (eslint, stylelint, htmllint)
- Includes `ci` (travis-ci)

## Requirements

- `NodeJS`, `npm` [download](https://nodejs.org/en/) or [read installation guide](https://nodejs.org/en/download/package-manager/)
- `git` [download](https://git-scm.com/downloads) or [read installation guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Learn before writing solution

- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)
- If you use _linux_ please make sure you adjusted writing permissions to let 
scripts work without `sudo`. Correct permissions means you don't see errors like
`permission denied` after running commands in CLI.
- [Working with figma](figma.md)

## Workflow

- Fork the repository with task
- Clone forked repository 
    ```bash
    git clone git@github.com:<user_name>>/<task_repository>.git
    ```
- Create separate branch for the solution. Name of the branch should be the same 
as name of your channel in slack. 
    ```bash
    git checkout -b fs_on_apr19_sasha
    ```
- Run `npm install` to install dependencies
- Run `npm run css:reference` to get reference screenshots for your solution. 
After running this command you will be able to find reference screenshots in 
`backstop_data/bitmaps_reference/`
- Run `npm run start` to start `http-server` on `http://localhost:8080`
    When you run server the command line window will no longer be available for 
    writing commands until you stop server (`ctrl + c`). All other commands you 
    need to run in new command line window.
- Write `HTML` in `src/index.html`
- Write `CSS` in `src/style.css`
- Write `JS` in `src/main.js`
- Make sure the code is clean. Run linters (`npm run lint`)
- Follow [the simplified JS styleguide](https://mate-academy.github.io/style-guides/javascript-standard-modified)
- Follow [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- Use [pixel perfect extension](https://www.youtube.com/watch?v=zqRko57AurU&list=PL7FuXFaDeEX15gwtyUNTuHHori210Nqol) to check if your markup looks the same as the reference.
- Make sure the layout is correct. Open new command line window and run tests 
    `npm run css:test`. Your `http-server` which runs via `npm run start` must be 
    online for tests.
- Save the solution
   ```bash
   git add .
   git commit -m 'Solution'
   ```
- And push your branch to the repo 
    ```bash
    git push origin <branch_name>
    ```
- Run `npm run deploy` to deploy your layout and test result to `gh-pages`
- Add links to your demo and test report in `readme.md`
    - `[Demo link](https://<your_account>.github.io/<repo_name>/)` - this will 
    be a link to your `index.html`
    - `[Test report](https://<your_account>.github.io/<repo_name>/report/html_report/)` - 
    this will be a link to the test report which was created after running
     `npm run css:test` command and deployed to `gh-pages` via `npm run deploy` command
- Create `Pull Request` from forked repo (`<branch_name>`) to original repo (`master`)
- Add links to created `PR`. `PR` must include updated `readme.md` with `Demo` and `Test report`

## Scripts
- `npm run start` - start `http-server` on `http://localhost:8080`
- `npm run lint` - run linters (`CSS`, `HTML`, `JS`)
- `npm run css:reference` - get reference screenshots
- `npm run css:test` - run visual regression tests. `http-server` must be online for tests.
- `npm run deploy` - deploy layout and test-report to `gh-pages`
