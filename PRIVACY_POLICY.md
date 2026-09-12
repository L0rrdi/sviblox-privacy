# SviBlox Beta Privacy Policy

Effective date: September 12, 2026

SviBlox Beta is a browser extension that adds quality-of-life features to the Roblox website, including home page sections, friend-tile stats, badge display tools, server filters, profile mutuals comparisons, in-page mirrors of the community-maintained Ultra Hard Badge List and Badger Hub, a personal badge watchlist, a local playtime activity view, custom themes, RoPro playtime import, optional local playtime tracking, dev products on the Store tab, subplaces on the Servers tab, an optional Robux-to-currency converter, an optional per-experience total-spent display, and an optional Marketplace source-file download.

## Data SviBlox Stores

SviBlox stores the following data in Chrome extension storage in the user's browser profile:

- Extension settings, such as theme selection, currency selection, and playtime tracking preference.
- Roblox game IDs, friend IDs, and other Roblox metadata used to display extension features.
- User-defined game folders for home-page tile sorting.
- Imported playtime data provided manually by the user.
- Optional extension-tracked playtime while the browser is open.
- Cached Roblox API responses used to reduce repeated requests, including cached transaction summaries when the total-spent feature is enabled.
- Locally cached copies of the public community Ultra Hard Badge List and Badger Hub spreadsheets, refreshed periodically.
- Badge-ownership results: which of the listed badges the signed-in user owns, and — when the optional friends leaderboard is used — how many each of the user's own Roblox friends owns. Stored locally so the pages can be reopened without rescanning.
- The user's own badge watchlist and its sections.
- Last-seen timestamps for the user's own Roblox friends, computed locally from Roblox presence data and used to show "last online" labels on friend profiles.
- Custom theme colors and user-selected theme background images or videos. Background videos are stored locally in the browser's IndexedDB; they are never uploaded anywhere.
- Private per-user notes, nicknames, and friend categories the user creates, plus user-curated Badger Hub annotations. All stored locally.

## Data SviBlox Reads

SviBlox may read the following data from Roblox endpoints using the user's existing Roblox browser session:

- The current Roblox user ID from the authenticated user endpoint.
- Public Roblox data such as game metadata, thumbnails, favorites, public creations, badge ownership, dev products, friends lists, groups, inventory, limiteds, and the list of places in an experience.
- Optional Roblox presence information (online / in-game / studio) when the user enables the local playtime tracking feature, and periodic presence snapshots of the user's friends for the "last online" labels.
- The user's own purchase history from the Roblox transactions endpoint when the user enables the optional Total Spent or Account Value features. This is used to compute, in the user's browser, how much Robux the user has spent on the currently visible experience, or an estimated account value. This data is read on demand, processed locally, and is never transmitted to the developer or any third party.
- For the Mutuals tab on a profile's Friends page: the friend list, favorite games, groups, inventory items, and limiteds of the viewed user and of the signed-in user. These are intersected locally in the browser to produce the "mutual" lists shown on screen.
- For the Ultra Hard Badge List, Badger Hub, and Badge Watchlist pages: the signed-in user's own list of awarded badges (against the badges listed on the page) to mark which ones the user has earned. The user's Roblox user ID is sent to Roblox's own badge endpoints to compute this.
- For the optional UHBL friends leaderboard, and for an explicit player lookup by username: the same badge-ownership check run against the user's own Roblox friends, or against the looked-up player. Their user IDs come from Roblox's own friends and user-search endpoints, the requests go to Roblox, and the results are ranked locally in the browser and stored locally so the board can be reopened without rescanning.

SviBlox uses the user's existing Roblox browser session through normal browser requests. SviBlox does not ask for, store, log, export, or collect Roblox passwords, session tokens, `.ROBLOSECURITY`, PINs, or other authentication secrets.

## Data Sharing

SviBlox does not sell, transfer, or share user data with third parties.

SviBlox does not send user data to the developer.

SviBlox does not use analytics, advertising trackers, or third-party telemetry services.

## Network Requests

SviBlox communicates with `roblox.com` and Roblox-owned subdomains declared in the extension's host permissions. These requests are used only for the extension's visible Roblox website features.

In addition, SviBlox issues anonymous reads against `docs.google.com` to fetch the public community badge spreadsheets — the Ultra Hard Badge List (as CSV) and the Badger Hub workbook (as XLSX). These requests are sent without authentication, without Roblox session cookies, without user identifiers, and without a request body. Google's Sheets export endpoint redirects to a temporary `googleusercontent.com` URL to serve the bytes, which is why that host is also listed in the extension's host permissions. Nothing about the user or their Roblox account is sent to Google.

When the user explicitly clicks "Download source" on a Marketplace catalog item, SviBlox fetches that asset (and its first-level linked assets) from Roblox's asset-delivery service, which redirects to Roblox's content CDN (`*.rbxcdn.com`, also declared in host permissions), and saves the files to the user's Downloads folder using the browser's downloads permission. This only happens on an explicit click and only fetches files the user's existing Roblox session is already permitted to retrieve.

SviBlox uses the browser's webNavigation permission to notice when a tab navigates to a Roblox profile URL. Roblox answers a request for a terminated or banned account with a redirect to a generic error page that no longer carries the account's ID, so the extension records that numeric ID from the outgoing URL in order to rebuild a readable profile view on the page the user actually lands on. Only the URL of the top-level frame is read, only the numeric profile ID is kept, it is held in memory for that tab alone, and it is discarded when the tab navigates elsewhere or closes. Nothing is written to disk and nothing is transmitted.

## User-Provided Content

If a user uploads a custom theme background image or video, that file is stored locally (images in Chrome extension storage, videos in the browser's IndexedDB). SviBlox does not upload custom theme backgrounds to any server.

## Data Removal

Users can remove SviBlox data by clearing the extension's storage or uninstalling the extension from Chrome. Users can also reset extension-tracked playtime from the SviBlox Options page. The user can disable any optional feature (including the total-spent feature) from the SviBlox popup, which stops the corresponding network requests immediately.

## Disclaimer and Trademarks

SviBlox is an independent, community-made browser extension. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation. "Roblox" is a trademark of Roblox Corporation, used only to describe the website the extension enhances. SviBlox is provided "as is", without warranty of any kind; you use it at your own risk.

## Changes

This policy may be updated when SviBlox changes. The latest version is published at the privacy policy URL used in the Chrome Web Store listing.

## Contact

For privacy questions, contact the SviBlox developer through the support contact listed on the Chrome Web Store item, or message `l0rrdi` on Discord.
