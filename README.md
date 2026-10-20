# create-quiet-on-set

Start a new project from [quiet-on-set](https://github.com/felton/quiet-on-set), a ready-to-shoot Vite starter with React Router, shadcn/ui and Tailwind CSS.

```bash
pnpm create quiet-on-set my-app
cd my-app
pnpm install
pnpm dev
```

`npm create quiet-on-set@latest my-app` and `bunx create-quiet-on-set my-app` work too. The project itself uses pnpm.

It downloads the latest template release into `my-app`, then runs the template's `pnpm make-it-yours`, which asks for the site's name, description and public URL and sets the copy up as your project.

## Options

| Option                 | Default            | Effect                                       |
| ---------------------- | ------------------ | -------------------------------------------- |
| `--template <tag>`     | the latest release | Template release, such as `v1.2.0`           |
| `--name <name>`        | the directory name | Site name                                    |
| `--description <text>` | empty              | One-line description                         |
| `--url <url>`          | empty              | Public address, including any subpath        |
| `-y`, `--yes`          |                    | Don't ask; use defaults for anything not given |

For coding agents and CI, pass the values and `--yes`:

```bash
pnpm create quiet-on-set my-app --name "Bakery Co" --description "Fresh bread daily" --yes
```

Releases from v1.2.0 on are supported, since that's the first with `make-it-yours`.

Docs: [felton.github.io/quiet-on-set](https://felton.github.io/quiet-on-set/)

## License

[MIT](LICENSE)
