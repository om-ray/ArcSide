# ArcSide privacy policy

Effective November 3, 2026.

ArcSide is two parts that run on your Mac: the ArcSide extension for the Aside browser, and the ArcSide app, which draws the sidebar. Neither part collects data about you, and neither sends anything off your Mac.

## What the extension reads

To show your spaces, the extension reads these from Aside:

- Your open tabs: their titles, addresses, and whether each is active, pinned, playing sound, muted or asleep.
- Your tab groups: their names and colors. Each space is a tab group.
- Your bookmarks bar, and the folder it keeps for each space under Other bookmarks > Spaces. It looks at the top of Other bookmarks only to find that Spaces folder.
- The icons Aside has already saved for those pages. It reads them from Aside's own icon cache, so no website is contacted.
- The position and size of the Aside window, so the sidebar can sit beside it.

## What it saves

The extension saves its own data with Aside's extension storage (`chrome.storage.local` and `chrome.storage.session`), on your Mac only:

- Your spaces: their names, colors and order, and the tab you last used in each.
- Which tab belongs to which space, and which pinned tab it keeps open for each page on your bookmarks bar.

Session storage is cleared when Aside quits. Removing the extension removes all of it.

The app saves only its settings on your Mac: appearance, motion, sidebar width, whether opening at the edge, swiping and the menu bar icon are on, and which sections and bookmark folders you left open. It keeps your tabs and bookmarks in memory only while it runs.

The app changes no Aside settings. With your permission in Privacy & Security > Accessibility, it holds back the pointer moves that macOS sends to Aside within 12 points of an Aside window's left edge, so Aside's own tab strip doesn't open there together with the sidebar. To find those edges it reads where Aside's windows are on screen. It reads no keys, no clicks and nothing on the page, and keeps nothing from these events.

## Where data goes

The extension sends what it reads only to the ArcSide app on the same Mac, through Aside's native messaging. The app sends back what you asked for in the sidebar, such as switching a tab or moving a bookmark.

Neither part sends data to Om Ray or to anyone else:

- The extension makes no network requests of its own. Its code has no `XMLHttpRequest`, `WebSocket` or `EventSource`, and its one `fetch` call reads page icons from the extension's own icon address, which Aside answers from its cache.
- The app's one network request is its update check: once a day, and when you click Check for Updates, it downloads the list of ArcSide releases from GitHub (`github.com/om-ray/ArcSide`), and, when you choose to install one, the update itself. Like any download, that request carries your IP address and the app's name and version to GitHub. It sends nothing else, and the app sends no system profile.
- There are no analytics, no ads, no tracking, and no accounts.
- Nothing is sold or shared.

## Scripts in pages

The extension runs a script in a web page only in these cases:

- To keep track of the pinned tabs it opens for your bookmarks bar across restarts, it writes a random key into the history entry of each such tab, reads it back, and removes it from tabs that were copied from one. The script reads and changes only that key and returns nothing else from the page.
- When you click a bookmarklet (a bookmark whose address starts with `javascript:`) in the sidebar, it runs that bookmarklet in the current tab, as Aside's bookmarks bar would.

The extension loads no code from the internet. All of its code ships in the package.

## Contact

Questions about this policy: om@ray.vin.
