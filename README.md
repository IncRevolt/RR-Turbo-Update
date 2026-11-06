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

## Scope

This tool keeps the **OS** current. It does not add the local-AI stack — that's
a separate upgrade (see the RR AI download). Learn more at
[renewablerevolt.org](https://renewablerevolt.org).

## License

[Apache License 2.0](LICENSE) — © 2026 Renewable Revolt, Inc. "Renewable
Revolt" and "RR Turbo" are trademarks of Renewable Revolt, Inc.
