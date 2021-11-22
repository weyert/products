# Skill Recordings Projects

This is an exploratory project using Turborepo and pnpm to create a monorepo working environment for multiple applications and a shared common core library (or set of libraries.

## Get Started

You'll need [Yarn](https://classic.yarnpkg.com/lang/en/) installed.

```bash
yarn i
yarn turbo run build
```

This will build (and cache) the library packages and applications.

You can start the template next.js app:

```bash
cd apps/next-product-starter && yarn dev
```

## Adding a Project to Vercel

The build command needs to be scoped to the specific project so we aren't building all of the repos for every single run. The `-w` flag runs ppm in the root of the project so all projects are built.

`build`:

```
cd ../.. && yarn turbo run build --scope="rust-adventure" --includeDependencies
```

## Develop locally using vercel

Because of the way vercel handles monorepo projects, you can only have a single
project linked locally at a given time.

In the root of the project:

```bash
vercel link
vercel dev
```

Calling `vercel link` asks if you want to link the project (yes), has you pick the account (`skillrecordings`), and
finally you enter the project name for the project you are working on.

Repeat this process if you want to work on a different project.

## Tools Used

### Turborepo

> abstracting the complex configuration needed for most monorepos into a single cohesive build system

Turbo is the core of the developer experience that this playground is exploring and provides cohesive logical building of a monorepo that contains many apps and library packages.

It's a closed source paid product that we are excited to use and support.

### Changset

> 🦋 A way to manage your versioning and changelogs with a focus on monorepos

Changeset is an Atlassian library that makes releasing library versions a little nicer.

### pnpm

> Fast, disk space efficient package manager

performant npm is just what it says it is and a modern evolution of npm/yarn etc that follows the same conventions and gives efficiency in a monorepo environment and can shave a lot of time off of builds.

### cypress

for integration and e2e testing!

## Resources

Here's a general tour of Turborepo from Jared:

[![Jared Palmer gives Joel a tour of Turborepo - Watch Video](https://cdn.loom.com/sessions/thumbnails/6be074dc590d44b192ab7e126f04c36b-with-play.gif)](https://www.loom.com/embed/6be074dc590d44b192ab7e126f04c36b)

Some good examples and background in [Jared's TSDX monorepo platground](https://github.com/jaredpalmer/tsdx-monorepo).

[![vercel logo](https://raw.githubusercontent.com/skillrecordings/turbo-playground/6d8af460a9630edea33cbbeef2a2309189f95a64/1618983297-powered-by-vercel.svg)](https://www.vercel.com/?utm_source=[skillrecordings]&utm_campaign=oss)
