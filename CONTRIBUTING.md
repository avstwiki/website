# Contributing to Avstwiki

This guide explains how to contribute, whether you're a developer or editing content for the first time.

## Ground rules

- **Never push directly to `main`.** All changes go through a pull request (PR) that gets reviewed before merging.
- **One topic per PR.** If you're working on two different pages, make two separate PRs.
- **Assign yourself a page** before starting, so two people don't port the same content at the same time – coordination via group chat.

## For content contributors (no developer experience needed)

You can do everything in your browser — no need to install anything.

### Editing an existing page

1. Navigate to the file you want to edit on GitHub (Markdown files live in `docs/`).
2. Click the **pencil icon** (top right of the file view).
3. Make your changes. The files use Markdown — see the [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/) if you need help with formatting.
4. When you're done, click **"Commit changes..."** (the green button).
5. In the dialog that appears, select **"Create a new branch for this commit and start a pull request."**
6. Name your branch following the pattern `content/short-description`, for example `content/visa-application` or `content/health-insurance`.
7. Click **"Propose changes"**, then **"Create pull request"** on the next page.

That's it. Vercel will automatically build a preview of the site with your changes — you'll see a link appear in the PR after a minute or two. Use it to check that everything looks right.

### Creating a new page

1. Navigate to the `docs/` folder on GitHub.
2. Click **"Add file" → "Create new file"**.
3. Type the file name including any subfolder, for example `docs/studying/nostrification.md`.
4. Add your content in Markdown.
5. Follow steps 4–7 above to propose the change as a PR.

### Tips for porting from Google Sites

- Copy the text content, but don't worry about matching the exact layout — Docusaurus handles styling.
- Convert links to Markdown format: `[link text](https://example.com)`.
- If a page has images, ask one of the developers to help add them, or note it in the PR description. Maybe you can also add them yourself via the web interface (supports uploading files into a folder directly, images live in `static/img/`), needs to be tested.

## For developers

### Local setup

```bash
git clone git@github.com:avstwiki/website.git
cd website
npm install
npm start
```

This starts a local dev server at `http://localhost:3000` with hot reloading.

### Branch naming

- Content porting: `content/page-name`
- Bug fixes: `fix/short-description`
- New features or structural changes: `feature/short-description`

### Before opening a PR

1. Make sure the site builds without errors: `npm run build`
2. Check your changes locally in the browser.
3. Keep PRs focused — don't mix unrelated changes.

## Review process

Every PR needs at least one approving review before it can be merged. When you open a PR:

1. Write a short description of what you changed.
2. Wait for the Vercel preview build to finish and check the preview link.
3. A maintainer will review your PR and may request changes.
4. Once approved, a maintainer will merge it.

## Questions?

Open an issue on GitHub or ask in the group chat. There are no stupid questions — talking is better than fixing mistakes later.

## License

By contributing, you agree that your contributions will be licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
