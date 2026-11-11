# github-workflow-collab

GitHub Actions workflow practical (Lecture 2, Activities 1-5) for 43030.

On every push to `main`, `.github/workflows/main.yml` runs four steps:

1. **Checkout Repository** - clones the repo onto the runner.
2. **Update index.html** - works out a label from the pushing user and inserts a
   `<p>Updated by ... on ...</p>` line just before `</body>`.
3. **Update README** - appends a log line with the username, timestamp and short commit hash.
4. **Commit and Push Changes** - commits both files as `github-actions` and pushes back to `main`.

The page is published with GitHub Pages at
<https://quqerty.github.io/github-workflow-collab/>.

## Changes from the lecture version

- `actions/checkout@v4` instead of the slides' `@v2`, which is deprecated.
- Added `permissions: contents: write` at workflow level. The slides set this through
  Settings > Actions > General; declaring it in the file as well makes the requirement
  visible in the code.
- Built as a solo repository, so the username `case` has one named branch
  (`QUQerty` -> `Team Leader`) and falls back to the raw username for anyone else.

## Update log
### Updated by QUQerty on 2026-11-11 10:19:29 [Commit: 1e29fe3]
### Updated by QUQerty on 2026-11-11 10:20:08 [Commit: d349160]
