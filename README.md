# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## New Project(done)

```log
$ npx nuxi@latest init . --force

❯ Which package manager would you like to use?
● npm
○ pnpm
○ yarn
○ bun
◐ Installing dependencies...

> postinstall
> nuxt prepare

✔ Types generated in .nux

added 736 packages, and audited 738 packages in 2m

122 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
✔ Installation completed.

❯ Initialize git repository?
● Yes / ○ No
ℹ Initializing git repository...

hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
Initialized empty Git repository in /workspaces/nuxt-sample-todo-app/.git/

✨ Nuxt project has been created with the v3 template. Next steps:
 › Start development server with npm run dev
```

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm run build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm run preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
