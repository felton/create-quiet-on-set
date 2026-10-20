# create-quiet-on-set

The `pnpm create quiet-on-set` CLI for the [quiet-on-set](https://github.com/felton/quiet-on-set) template. One file, `index.mjs`, with no dependencies.

- **Keep setup logic out of this repo.** The CLI only downloads a template release (GitHub API for the latest tag, the codeload tarball, the system `tar`) and runs that release's `scripts/make-it-yours.mjs`. Changes to what setting up a project means belong in the template repo.
- **Flags are passed through to make-it-yours** (`--name`, `--description`, `--url`, `--yes`). A new template flag needs adding to `parseArgs` and the pass-through list here.
- **`MIN_VERSION`** is the oldest template release the CLI accepts. Raise it if the CLI starts relying on something newer in the template.
- **No dependencies.** Use `node:` built-ins only.
- **Tests:** `pnpm test` (`node --test`). `index.test.mjs` runs the CLI as a child process, with `CREATE_QOS_SOURCE` pointing at a fake template, so nothing is downloaded. CI also creates a real project from the latest release on Linux and Windows.
- **Releases:** [Conventional Commits](https://www.conventionalcommits.org/). release-please opens release PRs, and merging one publishes to npm with provenance (npm trusted publishing). Don't edit `version` or `CHANGELOG.md` by hand.
