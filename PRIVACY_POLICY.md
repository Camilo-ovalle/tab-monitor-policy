# Privacy Policy — Chrome Tab Monitor

**Last updated:** May 2026

## Overview

Chrome Tab Monitor is a browser extension that monitors and controls the number of open tabs and windows. This extension does **not** collect, store, transmit, or share any personal data or browsing information.

## Data Collection

Chrome Tab Monitor does **not** collect any data. Specifically:

- No personal information is collected
- No browsing history is tracked
- No data is sent to external servers
- No analytics or tracking tools are used
- No account or sign-in is required
- No cookies are used

The extension reads the browser's user-agent string locally to detect whether it is running in Google Chrome or Microsoft Edge and adapt its tab-closing behavior accordingly. This detection happens entirely on your device and the value is never stored or transmitted.

## Data Storage

All extension data is stored on your device and never transmitted to any server operated by this extension:

- **`chrome.storage.sync`** — Stores your configuration preferences (tab limits, window limits, auto-close settings). If browser sync is enabled (Chrome Sync with your Google account, or Microsoft Edge sync with your Microsoft account), the browser may synchronize these values across your devices through Google's or Microsoft's infrastructure. This is controlled entirely by your browser's sync settings and is not initiated by this extension.
- **`chrome.storage.managed`** — Read-only. In managed environments, your IT administrator may push policy values through this API. The extension reads these values but never writes to them.
- **`localStorage`** — Stores a single UI preference: your chosen color theme (`light` or `dark`). This value is scoped to the extension popup and is not accessible by any website or external service.
- **Activity log** — Stored in memory only. The log is lost when the browser service worker restarts and is never written to any persistent storage.

## Permissions Used

The extension requires the following permissions, used exclusively for its core functionality:

- **`tabs`** — To count open tabs in each window and close excess tabs when configured limits are exceeded.
- **`windows`** — To count open browser windows and close excess windows when configured limits are exceeded. On Microsoft Edge, the extension may also briefly open and immediately close a temporary helper window in order to close an excess tab, because Edge restricts closing new-tab pages directly.
- **`storage`** — To save your configuration preferences locally and read IT administrator policies in managed environments.
- **`notifications`** — To optionally notify you when tab or window limits are exceeded.

## Enterprise / Managed Environments (GPO)

Chrome Tab Monitor supports enterprise policy management on both Google Chrome and Microsoft Edge via Group Policy Objects (GPO) and the Windows Registry. If your organization deploys this extension through Chrome Enterprise or Microsoft Edge for Business, your IT administrator may pre-configure certain settings using `chrome.storage.managed`.

In this scenario:
- The extension **reads** policy values set by your administrator. It does **not** send any data back to your organization or any external server.
- Settings pushed via GPO appear as locked fields (marked **GPO**) in the extension popup and cannot be changed by the end user.
- No personal browsing data is shared with your organization through this mechanism.

## Third-Party Services

Chrome Tab Monitor does **not** use any third-party services, APIs, SDKs, or external network connections. No requests are made to external servers when using this extension.

## Changes to This Policy

If this privacy policy is updated, the changes will be reflected in this document with an updated date.

## Contact

If you have questions about this privacy policy, please open an issue on the [GitHub repository](https://github.com/Camilo-ovalle/Tab-Limiter-chrome-Extension/issues).

## Open Source

Chrome Tab Monitor is open source under the MIT License. You can review the complete source code at [https://github.com/Camilo-ovalle/Tab-Limiter-chrome-Extension](https://github.com/Camilo-ovalle/Tab-Limiter-chrome-Extension).
