# Bluedee

A browser-game library with a tabbed, browser-style layout. Search for a game, browse by category, save favorites and switch themes.

## Features

- **90 games.** 48 are hosted in this repository and 42 link out to their original sites.
- **Hosted games keep working.** They live in [`games/`](./games), load nothing from other sites, and also run from an `about:blank` tab.
- **Search and categories:** Arcade, Puzzle, Racing, Sports, Classic and Sandbox.
- **Favorites** are saved in your browser's local storage.
- **Four themes:** Light, Graphite, Midnight and Monochrome.
- **Open games** either inside the site (in a tab) or in a new `about:blank` tab, using the selector at the top right. Linked games open the same way, but some sites refuse to be shown inside another page. For those, use the **Open game in a new tab** button (or the button shown in the about:blank tab).
- **No analytics or tracking.**

## Run it locally

Any static file server works:

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Pushing to `main` publishes the site to GitHub Pages using [`.github/workflows/pages.yml`](./.github/workflows/pages.yml). In the repository settings, set **Pages → Source** to **GitHub Actions**.

## Add a game

1. Put the game in `games/<name>/index.html`. If it uses the shared language file, include `../i18n.js`.
2. Add a line to the `games` list near the top of the script in `index.html`: `["Name","Category","Short description","games/<name>/index.html"]`.
3. Make sure you have the right to redistribute the game, and keep its licence next to it.

## Hosted games and licences

The 48 hosted games and the shared `i18n.js` come from [mashukui/web-games](https://github.com/mashukui/web-games), released under the MIT License. The licence text is kept in [`games/LICENSE`](./games/LICENSE), and each game page keeps its author credit. See [`games/README.md`](./games/README.md) for the list and for the small changes made to the upstream files.

## Linked games

The other 42 games are hosted by their original providers. Bluedee only links to them, so a link may stop working or change at any time, and Bluedee has no control over those sites. Sites that block embedding will show a blank or "refused to connect" frame; only hosting a game here (when its licence allows) makes it work everywhere.
