# Developing

## Setup

```shell
yarn
```

## Submitting Pull Requests

**Please follow these basic steps to simplify pull request reviews.**

- Please rebase your branch against the current main.
- Run the `Setup` command to make sure your development dependencies are up-to-date.
- Please ensure the test suite passes before submitting a PR.
- If you've added new functionality, **please** include tests which validate its behavior.
- Make reference to possible [issues](https://github.com/phat-arrow/ngos/issues) on PR comment.

## Submitting bug reports

- Search through issues to see if a previous issue has already been reported and/or fixed.
- Provide a _small_ reproduction using a [StackBlitz project](https://stackblitz.com/) or a GitHub repository.
- Please detail the affected browser(s) and operating system(s).
- Please be sure to state which version of Angular, node (or yarn) and npm you're using.

## Submitting new features

- We value keeping the API surface small and concise, which factors into whether new features are accepted.
- Submit an issue with the prefix `RFC:` with your feature request.
- The feature will be discussed and considered.
- Once the PR is submitted, it will be reviewed and merged once approved.

## <a name="commit"></a> Commit Message Guidelines

We have very precise rules over how our git commit messages can be formatted. This leads to **more
readable messages** that are easy to follow when looking through the **project history**. But also,
we use the git commit messages to **generate the NgOS changelog**.

### Commit Message Format

Each commit message consists of a **header**, a **body** and a **footer**. The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

The footer should contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages/) if any.

Samples:

```
docs(changelog): update changelog to beta.5
```

```
fix(release): change menu component to on push

Improve performance of menu rendering based on active application switching.
```

### Revert

If the commit reverts a previous commit, it should begin with `revert:`, followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type

Must be one of the following:

- **build**: Changes that affect the build system or external dependencies (example scopes: cli, yarn)
- **ci**: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- **docs**: Documentation only changes
- **feature**: A new feature
- **fix**: A bug fix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **code-style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.)
- **test**: Adding missing tests or correcting existing tests (example scopes: spec, e2e)

### Scope (projects)

The scope should be the name of the project affected (as perceived by the person reading the changelog generated from commit messages).

The following are some examples of project scopes:

- **ngos-app**
- **my-weather**

### Subject

The subject contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize the first letter
- no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

Example:

```
feat(scope): commit message

BREAKING CHANGES:

Describe breaking changes here

BEFORE:

Previous code example here

AFTER:

New code example here
```

_____
*Inspired by [CHANGELOG.md](https://raw.githubusercontent.com/ngrx/platform/master/CONTRIBUTING.md) from the NgRx platform repo.*