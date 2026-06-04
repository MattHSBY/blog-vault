# Building a Static Blog with Obsidian and GitHub Pages

*June 2026 · Category: Projects*

Here's how I set up a blog site that publishes straight from my Obsidian vault.

## The Stack

- **[Obsidian](https://obsidian.md/)** for writing
- **[Git plugin](https://publish.obsidian.md/git-doc/)** for syncing
- **[GitHub Pages](https://docs.github.com/en/pages)** for hosting
- **Vanilla JS** for rendering


## How It Works

Every `.md` file I write in my vault gets committed and pushed to a [vault repo](https://github.com/MattHSBY/blog-vault) on GitHub. A small JavaScript function in the site repo crawls the GitHub API to find all those files, reads their content, and renders them with marked.js.

The result is a fully static site that updates whenever I push from Obsidian.

## Lessons Learned

Keeping the vault separate from the site scaffolding was the right call. I can use obsidian how I normally would — I don't have to worry about HTML/CSS files for the site and no config files polluting my notes.

The only convention I follow: put a `# Title` as the first line, and optionally a date on the second line with `*Month Year*`.
