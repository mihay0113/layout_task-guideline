# Guideline how to implement solution for Layout tasks

[Video guide](#) _in progress_

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
- `docker` [download](https://www.docker.com/products/docker-desktop)
    - [What is docker?](https://www.docker.com/why-docker)
    - [Solve virtualization issue on Windows](https://stackoverflow.com/questions/39684974/docker-for-windows-error-hardware-assisted-virtualization-and-data-execution-p)

## Learn before writing solution

- [Creating a pull request from a fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)

## Workflow

- Fork the repository with task
- Clone forked repository<br/> `git clone git@github.com:<user_name>>/<task_repository>.git`
- Create separate branch for the solution. Name of the branch should be the same as name of your channel in slack. <br/> e.g. `git checkout -b fs_on_apr19_sasha`
- Run `npm install` to install dependencies
- Run `npm run start` to start `http-server` on `http://localhost:8080`
- Write `HTML` in `src/index.html`
- Write `CSS` in `src/style.css`
- Write `JS` in `src/main.js`
- Make sure the code is clean. Run linters (`npm run lint`)
- Follow [the simplified JS styleguide](https://mate-academy.github.io/style-guides/javascript-standard-modified)
- Follow [HTML, CSS styleguide](https://mate-academy.github.io/style-guides/htmlcss.html)
- Make sure `docker` is online (you see the `docker` icon in tray on Windows or in toolbar on Mac)
- Make sure the layout is correct. Run tests (`npm run css:test`). Your `http-server` which runs via `npm run start` must be online for tests.
- If you don't see `reference` screenshots run `npm run css:reference` to update it.
- Save the solution <br/>
   ```
   git add .
   git commit -m 'Solution'
   ```
- And push your branch to the repo<br/> `git push origin <branch_name>`
- Run `npm run deploy` to deploy your layout and test result to `gh-pages`
- Update links in `readme.md`
    - `[Demo link](https://<your_account>.github.io/<repo_name>/)`
    - `[Test report](https://<your_account>.github.io/<repo_name>/report/html_report/)`
- Create `Pull Request` from forked repo (`<branch_name>`) to original repo (`master`)
- Add links to created `PR`, `Demo` and `Test report` to your table and send them you your coach or TA

## Scripts
- `npm run start` - start `http-server` on `http://localhost:8080`
- `npm run lint` - run linters (`CSS`, `HTML`, `JS`)
- `npm run css:test` - run visual regression tests. `http-server` must be online for tests.
- `npm run css:reference` - update reference screenshots
- `npm run deploy` - deploy layout and test-report to `gh-pages`
