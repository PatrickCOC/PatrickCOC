# ReadBar privacy policy

Last updated: 29 September 2026

ReadBar is a Chrome extension for reading your own notes and text files, and headlines and stock quotes from sources you choose, in a small bar on the current page. It has no account, advertising, analytics, or developer-operated server.

## Data on your device

Memos, imported text, reading positions, preferences, keyboard shortcuts, saved news and API bookmarks, API keys, and cached headlines and quotes are stored in your Chrome browser profile with `chrome.storage.local`. Linked local novels stay in their original files; Chrome stores their file handles and reading indexes in extension IndexedDB and their progress in local storage. ReadBar does not upload your notes or novels to us.

You can change or delete saved items in Options. You can download a JSON backup and restore it. API bookmarks and keys are excluded from a backup unless you explicitly select the option to include them; when included, they are plain text in the downloaded file. A backup is created in your browser and saved wherever your browser downloads it. Removing the extension removes its browser-profile data; any backup file you downloaded stays where you saved it.

## Requests to sites you choose

ReadBar accesses the active tab only when you invoke the extension, to display the bar. It does not record your browsing history or send the page you are reading to us.

When you add a news site or feed, ReadBar asks Chrome for access to that site's HTTPS origin, then requests its feed and caches headlines. If you open a headline within ReadBar, it may request the article page to extract readable paragraphs. The original page may be on another origin and requires its own permission. ReadBar can open the original article in a new tab at your request.

When you configure a news API, its key is sent only to the endpoint you specified, using the header or query parameter you selected. A query parameter can appear in that provider's request logs. When you add a US stock symbol, ReadBar requests Yahoo Finance's chart endpoint for that symbol; Yahoo's service may log the request. These sites and API providers process requests under their own policies. ReadBar does not sell or share your stored notes, novels, keys, or reading positions with them.

## Permissions

- `activeTab`: temporary access to the tab on which you invoke the bar.
- `scripting`: insert the bar in that tab after invocation.
- `storage`: save your content, settings, progress, and source caches in this browser profile.
- Optional HTTPS site access: requested for each user-selected news site, feed, article origin, API endpoint, or the Yahoo quote endpoint. You may decline it; that source will not load.

For privacy questions, open an issue at https://github.com/PatrickCOC/readbar/issues .
