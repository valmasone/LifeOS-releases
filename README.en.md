<div align="center">

<img src="assets/lifeos.svg" width="92" alt="LifeOS" />

# LifeOS
### Work. Rest. Life.

**A local-first Windows companion for work time, projects and breaks.**

[Download Windows Preview](https://github.com/valmasone/LifeOS-releases/releases) · [Installation](INSTALL.md) · [Privacy](PRIVACY.md) · [Support](SUPPORT.md)

[Русский](README.md) · [English](README.en.md) · [简体中文](README.zh-CN.md) · [Español](README.es.md) · [Italiano](README.it.md) · [العربية](README.ar.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Português](README.pt.md) · [日本語](README.ja.md)

</div>

---

## Why LifeOS

Juggling multiple projects shouldn't require another manual timekeeping job. LifeOS records active computer time, helps attribute it to known projects and encourages regular breaks. **When project evidence is insufficient, an interval stays unassigned rather than being guessed.**

## Available functionality

| Feature | Current behavior |
| --- | --- |
| Active time | Windows foreground activity, with idle time and sleep excluded from active work. |
| Projects and tasks | Local project catalog and explicit context links; unknown intervals can be assigned manually. |
| Breaks | Adjustable work/rest rhythm, reminders, pause and resume. |
| Daily overview | Time totals and attribution to recognized projects. |
| Browser integration | Optional browser extension sends limited metadata about the active tab to a local LifeOS bridge after consent. |
| Updates | Signed-release verification, installation after approval and side-by-side versions for rollback. |

**Preview limits:** browser installation and reliable assignment for arbitrary chats are still being tested. LifeOS does not read Telegram/Mattermost message bodies, summarize private conversations with a language model, or claim to automatically identify every task.

## Download and install

1. Browse [Releases](https://github.com/valmasone/LifeOS-releases/releases). The current published update channel is **0.4.9 preview**; later work remains private until release approval.
2. Extract the **entire ZIP** to a dedicated folder and run `LifeOS.exe` on Windows. Where a verified LifeOS Setup installer is offered, prefer it for managed Launcher/OTA installations.
3. Choose work and rest intervals. Enable optional workspace recognition if desired.
4. Browser integration is optional. Installing a third-party CRX package may require an explicit browser-managed step until a verified store listing becomes available.

[Full install/update/data-preservation guide](INSTALL.md).

## Local-first privacy

Work history and project records stay in the Windows user profile and are **not uploaded to LifeOS servers**. The extension does not send webpage contents, chat messages, full URLs or browsing history to a cloud service. With consent, limited identifiers such as hostname, repository/issue, channel/conversation ID or tab group may be passed to the local native bridge. This metadata can itself be sensitive.

Update checks can contact release infrastructure, which may see the request's IP address. The local SQLite database is not encrypted by the application; Windows account access and disk encryption also matter.

[Detailed privacy policy](PRIVACY.en.md) · [Russian policy](PRIVACY.md).

## Project status

| Platform | Status |
| --- | --- |
| **Windows x64** | Preview for evaluation |
| **Browser extension** | Preparing for Opera Add-ons; store listing not yet verified |
| Android | Deferred until Windows 1.0 |
| Cross-device sync | Not implemented |

**This is not Windows 1.0 GA.** Security, accessibility, real-browser and longer-duration acceptance tests remain open. [Changelog](CHANGELOG.md) · [Known limitations and support](SUPPORT.md).

---

<div align="center">

**LifeOS — your time belongs to you.**

<sub>© 2026 LifeOS. Windows application source code is not distributed in this repository.</sub>

</div>
