# LifeOS / LifeOS Projects — Privacy Policy

**Effective date:** October 20, 2026  
**Products:** LifeOS for Windows (preview) and the optional LifeOS Projects browser extension  
**Data inquiries:** [GitHub Issues](https://github.com/valmasone/LifeOS-releases/issues) — do not post secrets or private conversations.

[Русская версия](PRIVACY.md) · [LifeOS overview](README.en.md)

## Purpose

LifeOS is a local-first tool for tracking active computer time, projects and breaks. LifeOS Projects is an optional browser extension that helps map the currently active browser tab to a project after the user has enabled local browser recognition.

## Data processed

The Windows application stores activity intervals, breaks, project/task records, confirmed context-to-project links and user preferences. With browser recognition enabled, the extension inspects the active tab of the focused browser window and extracts a limited set of structured values such as the hostname, supported repository/issue identifiers, work-channel or conversation identifiers, and tab-group names.

The extension may parse a page's URL in memory to extract those values, but **does not transmit or persist the full URL with query parameters** in its Native Messaging payload or LifeOS history. It does not read webpage text, chat messages, cookies, passwords, form values or keystrokes, does not use the `chrome.history` API, and does not request the `history` permission.

Some structured identifiers may be sensitive even without full page content. They are used only for the enabled local functionality. LifeOS keeps only limited, sanitized active-browser snapshots on the user's computer.

## Where the data goes

The extension communicates with `LifeOSBrowserBridge.exe` on the **same computer** using Chromium Native Messaging. Local activity records and project preferences are stored in the user's Windows profile, usually under `%LOCALAPPDATA%\LifeOS`, in SQLite and small local files. Confirmed project mappings may store hashes of context identifiers.

**LifeOS Projects does not send browser work context, page content or chat content to third-party cloud AI systems, advertising networks or analytics services.** The web browser and visited websites still communicate with their own services independently.

## Network use and updates

The Windows application may contact the LifeOS release delivery infrastructure (GitHub Releases / Cloudflare) to check for signed releases and download update packages. It does not attach work history to these requests. The delivery infrastructure may observe standard network metadata such as the device's IP address.

## Storage, security and deletion

User settings and history remain stored locally across program updates. The current LifeOS SQLite database **is not encrypted by LifeOS itself**. Windows account access control and disk encryption matter. Disabling the browser extension stops new browser-context capture; it does not automatically remove previous Windows LifeOS history. After exporting information you wish to keep and fully closing LifeOS, you can manually remove its local user-data directory to delete its stored history and backups.

## Extension permissions

- `tabs` — inspect metadata for the active browser tab.
- `tabGroups` — read the title of its group when available.
- `nativeMessaging` — communicate with the locally installed Windows program.
- `alarms` — update the current signal periodically.
- `storage` — locally remember the opt-in state and connection status.

The extension has no remotely hosted code, page-reading content scripts, advertising trackers or browser-history permission.

## Changes

We will update this policy when the data-processing behavior changes materially. Cloud synchronization or reading message bodies is not part of the currently released preview and would require separate disclosures and consent.
