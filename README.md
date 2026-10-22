# Accessible Scroll Motion

Source for [accessible-scroll-motion.thally.app](https://accessible-scroll-motion.thally.app),
a small documentation site about adding GSAP scroll animation to a Next.js App
Router site in a way that respects readers who need less motion.

The site is built with [Thally](https://thally.io) and published by Thally
Cloud. Every push to `main` triggers a managed production deployment.

## What's here

| Path | Purpose |
| --- | --- |
| `src/content/introduction.mdx` | What the pattern is and who it's for |
| `src/content/quickstart.mdx` | From `create-next-app` to a scroll-triggered fade-up |
| `src/content/guides/reduce-motion-toggle.mdx` | Add an on-site Reduce motion toggle, plus troubleshooting |
| `src/content/reference/motion-helpers.mdx` | Reference for `motionAllowed()`, `fadeUp()`, and `settleAnimations()` |
| `src/content/build-with-thally.mdx` | Article: how this site was built and published with Thally Cloud |
| `src/content/changelog.mdx` | Changes to the docs |
| `docs.json` | Tabs, sidebar groups, and page order |
| `src/data/site.ts` | Site name, description, and links |

Everything else is the Thally runtime, which arrives through the **Update
Thally framework** workflow. Don't edit it by hand.

## Work on the docs locally

Requires Node.js 20.19+, 22.14+, or 24+.

```bash
npm ci
npm run dev
```

The site runs at http://localhost:3040.

Before you push, check the content and build the site:

```bash
npx --yes @thallylabs/cli@latest check
npm run build
```

On Windows, if `check` fails with `'C:\Program' is not recognized as an
internal or external command`, run the same check through its underlying
package instead:

```bash
npx --yes create-thally-docs@latest check . --ci
```

## Code samples

Every sample was run in a fresh `npx create-next-app@latest --yes` project at
the versions listed on the introduction page. Re-test a sample before changing
it.
