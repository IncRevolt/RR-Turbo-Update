# RR Turbo — Update

Keeps your **RR Turbo** PC on a current, **security-supported** version of
Windows. A veteran-owned 501(c)(3) nonprofit —
[Renewable Revolt](https://renewablerevolt.org).

## Why this exists

Windows ships feature versions (24H2, 25H2, 26H2…) and **retires security
updates** for the older ones. Windows 11 **24H2 stopped receiving security
updates in October 2026.** This tool moves your RR Turbo machine up to the
current version so it keeps getting patched — **without reinstalling Windows
or touching your RR Turbo setup.**

Each step is a small **enablement package**: it flips features that are
already on the machine (24H2 build 26100 → 25H2 build 26200). It is not a
reinstall, so nothing we removed comes back and nothing you set is lost.

## How it works (and why it's safe)

- It downloads **Microsoft's own signed package** straight from Microsoft.
  We host nothing and modify nothing.
- It **verifies the Microsoft signature** before installing.
- If Microsoft ever rotates the download link, it **fails loudly** and walks
  you through getting the file from Microsoft's own Update Catalog — it never
  leaves you stuck or silently installs the wrong thing.

## How to run it (current step: 24H2 → 25H2)

Open the **`24H2-to-25H2`** folder from the download, then:

1. Double-click **`Run-Step1-Download.bat`** — downloads + verifies the package.
2. Double-click **`Run-Step2-Install.bat`** — installs it (click **Yes** at the
   admin prompt), then restart when it offers.
3. After the restart: open Start, type **`winver`**, confirm the build starts
   with **26200**. Done.

If the install reports **"not applicable,"** the machine usually just needs its
pending monthly Windows updates first — install those, then run Step 2 again.

## Releases = OS-currency stages

This repo advances in stages, one release each:

- **`v24H2-to-25H2`** — current.
- **`v25H2-to-26H2`** — next, when Microsoft ships 26H2 as an enablement
  package (lands in `future-stages/`).

Always grab the release that matches where your machine is now.

## RR Tune-Up (bonus tool)

`RR Tune-Up` is a separate one-shot tool in this repo's releases. It runs on any
Windows 11 machine and does two things:

1. **SearchHost WebView2 fix (always runs).** Windows' Start/taskbar search
   quietly spawns a hidden Edge WebView2 to render Bing/web results — ~360 MB of
   idle RAM on the machines we measured. This removes it (local search still
   works) and installs a tiny logon guard that re-applies the fix after Windows
   updates. Browser-safe: it only ever touches the Windows search package's
   WebView2, never your web browser.
2. **The Renewable Revolt look (optional — it asks Y/N).** Press Enter to skip,
   or type Y for a dark/grey theme, a decluttered taskbar, no Bing/web in Start
   search, and the RR wallpaper. All reversible in Windows Settings.

**Before you run it,** consider creating a System Restore Point (Start → type
"restore" → **Create a restore point** → Create) so you can roll back if you ever
want to.

Grab it from the **`rr-tuneup`** release, **unblock the zip** (right-click →
Properties → Unblock), extract, and double-click **`RUN - RR Tune-Up.bat`**.
Restart when it finishes so the WebView2 fix takes effect.

## Scope

This tool keeps the **OS** current. It does not add the local-AI stack — that's
a separate upgrade (see the RR AI download). Learn more at
[renewablerevolt.org](https://renewablerevolt.org).

## License

**[PolyForm Noncommercial License 1.0.0](LICENSE)** — free for personal and
nonprofit, noncommercial use (running it on your own PC counts).  You may use
and share it; you may **not** sell it, repackage it for payment, or rebrand it.
© 2026 Renewable Revolt, Inc. "Renewable Revolt" and "RR Turbo" are trademarks
of Renewable Revolt, Inc.
