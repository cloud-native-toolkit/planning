# Contributing

## Requirements

Set up your SSH Key GitHub account and install node.js 4 or higher.

- [Generating SSH Keys - GitHub](https://help.github.com/articles/generating-ssh-keys/)
- [`nvm` (Node Version Manager)](https://github.com/creationix/nvm) to use the
  `Node 6`.


## Start contributing

### 1. Fork the repo:

Go to [carbon-components](https://github.com/IBM/carbon-components) and click
the `Fork` button in the top-right corner.

### 2. Clone your fork:

1.  Go to your [GitHub Repositories](https://github.com/settings/repositories).
1.  Click on `[your_github_username]/carbon-components`.
1.  Click on the `Clone or Download` button and copy the URL from the
    `Clone with SSH` option. It should start with `git@github.com...`

In your terminal:

```sh
git clone git@github.com:[your_github_username]/carbon-components.git
cd carbon-components
```

See [GitHub docs](https://help.github.com/articles/fork-a-repo/) for more
details.

### 3. Add upstream remotes

When you clone your forked repo, doing a `git remote -v` will show that the
`origin` remote is set up for you already by default. This should be pointing to
your forked repo.

Add the `IBM/carbon-components` repo to your remote (this can be useful to
update your fork of new changes down the road):

```sh
# Add the upstream remote to your repo
git remote add upstream git@github.com:IBM/carbon-components.git

# Verify the remote was added
git remote -v
```

When you do `git remote -v`, you'll see these remotes:

- `origin`: connection to your fork
- `upstream`: connection to the original repo.

### 4. Work in a branch

- Always work in a branch.
- Submit pull requests from a branch.
- All commits must follow the convention outlined
  [here](https://github.com/conventional-changelog/conventional-changelog/blob/v0.5.3/conventions/angular.md).

### 5. Start the server

```sh
npm run dev

# or

yarn dev
```

Once it's done building, you can start editing source code or creating new
components. The system is set up to automatically bundle your changes/additions.
Visit http://localhost:3000 to see the changes happen on the fly.

Options:

- `-b`: Enable breaking changes for the next release
- `-e`: Enable experimental features

### 6. Test your JavaScript code

If you're contributing to our JavaScript code, test your changes by running our
test commands:

```sh
gulp test:unit
```

If you add any features to our JavaScript code, make sure to add tests so that
your code is covered. Tests are written in
[Mocha](https://mochajs.org)/[Chai](http://chaijs.com). You can see if your code
is covered by looking at carbon-components/tests/coverage/\*/index.html after
running test.

If your change may hit some browser quirks, use `-b` option, like:

```sh
gulp test:unit -b IE -b Firefox
```

(Other browsers tests can run with are: `Safari`, `Chrome` and `ChromeHeadless`)

If you are very sure that your change affects a specific set of components, you
can use `-f` option, like:

```sh
gulp test:unit -f tests/spec/fab_spec.js
```

Other options for testing are:

- `-d`/`--debug`: Stop generating code coverage report. Useful to debug your
  code when running test.
- `-k`/`--keepalive`: Keep running test runner even after test ends. Test will
  restart running when you make changes to any test files or any files under
  test.
- `-v`/`--verbose`: Let Karma emit detailed log.

### 7. Test your HTML/CSS code for a11y

If you're contributing to our HTML/CSS code, a11y compliance of your code should
be tested.

To do so, you can test your changes by running our test commands:

```sh
gulp test:a11y
```

If you are very sure that your change affects a specific set of components, you
can use `--name` option, like:

```sh
gulp test:a11y --name dropdown
```

The a11y test may report potential issues that should be handled in
application-level, not in carbon-components code. In such case, you can ignore
those issues by adding an item to `shouldIssueBeIgnoredForRule` table in
[tests/a11y/global-ignore-aat-issues.js](https://github.com/IBM/carbon-components/blob/master/tests/a11y/global-ignore-aat-issues.js).
The table is keyed by something like `wcag20.tech.h59.linkValid` which helps
identifying what RPT rule to ignore. You can specify `true` to the value which
ignores all violations of the rule, or a function which takes the DOM element
violating the rule and returns `true` if such violation should be ignored.

### 8. Make a pull request

**Note:** Before you make a pull request,
[search](https://github.com/IBM/carbon-components/issues) the issues to see if a
similar issue has already been submitted. If a similar issue has been submitted,
assign yourself or ask to be assigned to the issue by posting a comment. If the
issue does not exist, create a new issue.

When you're at a good stopping place and you're ready for feedback from other
contributors and maintainers, **push your commits to your fork**:

#### Commit tip

> **Writing commit messages**
>
> - `<type>` indicates the type of commit that's being made. This can be:
>   `feat`, `fix`, `perf`, `docs`, `chore`, `style`, `refactor`
> - `<scope>` The scope could be anything specifying place of the commit change
>   or the thing(s) that changed.
>
> **Commit message format:**

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

_Do not submit pull requests from the `master` branch of your fork._

```
git checkout -b { YOUR_BRANCH_NAME }
git add .
git commit -m "fix(table): IE11 positioning error" -m "Fixes #34"
```

- [Close a commit via commit message](https://help.github.com/articles/closing-issues-via-commit-messages/)

```
git push origin { YOUR_BRANCH_NAME }
```

In your browser, navigate to
[IBM/carbon-components](https://github.com/IBM/carbon-components) and click the
button that reads `Compare & pull request`

> **Is it a Breaking Change?**

> We want to respect semver. It's important to discern whether your pull request
> contains breaking changes or not. Sometimes, renaming or removing things in
> the code can result in breaking changes.

> Here are some examples of breaking changes... changing, renaming or removing
> any of the following:
>
> - HTML attributes
> - Folders or Files
> - Any SCSS `@mixin`, `$variable` or `function`
> - Any JS `function` or `class`

> We also practice **graceful deprecation** when something is slated to be
> removed -- we mark it as deprecated in the current version and remove it in
> the next major version.

Before you create a pull request, change the base branch depending on what kind
of change you're submitting.

- Pull requests with **non-breaking changes** like patches and minor updates use
  the `master` as the base branch.
- Pull requests with **breaking changes** use the latest `major version number`
  branch as the base branch (i.e. `7.0.0` or whatever the next major version
  is).

Write a title and description then click `Create pull request`

- [How to write the perfect pull request](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)

### 9. Updating a pull request

Stay up to date with the activity in your pull request. Maintainers from the
Design System team will be reviewing your work and making comments, asking
questions and suggesting changes to be made before they merge your code.

:tada: You no longer need to squash commits :tada:

When you need to make a change, add, commit and push to your branch normally.

Once all revisions to your pull request are complete, someone from Design
Systems will squash and merge your commits for you.
