<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, the black box for your laptop, by Alcyone Secure" width="100%">

# Rashnova

### A tamper-evident activity recorder for Windows

**Hand over your PC. Get back a sealed record of what was done with it.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**Download**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**Website**](https://www.alcyonesecure.com) ·
[**Known limits**](KNOWN_LIMITS.md) ·
[**Privacy**](#privacy) ·
[**Security**](SECURITY.md)

</div>

> **Languages** &nbsp;·&nbsp; **English** · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md) · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---


Rashnova records what happens on a Windows PC while someone else has it: at a repair shop, at an
IT desk, or with anyone you hand it to. Start a **Repair session** before the handover. When the PC
comes back, end it, and Rashnova gives you a verdict and a report of what was opened, copied,
renamed and deleted, which programs ran, and which USB drives were plugged in.

Every entry is sealed to the one before it, so the record shows if anything in it was altered or
removed, and it shows every stretch where nothing could be recorded. Everything stays on your
computer. No account, no cloud, no telemetry.


> [!NOTE]
> This repository is where Rashnova is **released**: installers, release notes, known limits and
> security policy. Rashnova is proprietary software by [Alcyone Secure](https://www.alcyonesecure.com);
> its source code is not published here.


## Contents

- [Why Rashnova exists](#why)
- [What it does](#what-it-does)
- [What it never records](#never)
- [How it works](#how)
- [Download and install](#download)
- [System requirements](#requirements)
- [Privacy](#privacy)
- [Known limits](#limits)
- [Updates](#updates)
- [Support and security](#support)
- [Licence](#licence)

<a name="why"></a>
## Why Rashnova exists

Aircraft, trains and ships carry a black box. A computer that leaves your hands carries nothing,
and the person holding it has full access to everything on it.

That access gets used. In a [2022 study by researchers at the University of Guelph](https://arxiv.org/abs/2211.05824)
(published at IEEE Symposium on Security and Privacy 2023), laptops were left overnight at 12 repair
shops with logging switched on. Technicians at six of them accessed the personal data on them, and
two copied data off the laptop. Antivirus and endpoint tools were never built to notice this: the
person was handed the keys.

Rashnova is not prevention. It is evidence, so that what happened can be checked rather than argued
about.

> *Trust is good. Proof is better.*

<a name="what-it-does"></a>
## What it does

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode.** A watched session, started with your PIN before the handover and ended with
your PIN when you get the PC back. It records files opened, created, renamed, copied and deleted,
programs started, PowerShell commands run, sign-ins, and USB storage plugged in, including every
file written to it. A restart, a shutdown or sleep never ends the session: the report shows each
interruption and how long it lasted.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="Session summary: a verdict, the most notable events and the chain check">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="Session explorer: every event over time, by program and by folder">

</td>
<td width="50%" valign="top">

**A record you can check.** Each session ends with a verdict and a report you can save as PDF, a
web page or a spreadsheet. The session explorer shows every event over time, by program and by
folder, and the chain check tells you whether the record is intact. What you save is a copy; the
original stays where Rashnova keeps it.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**The weekly Readout.** Your week in one verdict, with at most a few things worth a look. Mark
each one "that was me" or "that wasn't me". It also says, in plain words, what Rashnova can and
cannot see.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="The weekly Readout: a verdict for the week, items worth a look, activity by day">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="The choice between session-only and always-on recording">

</td>
<td width="50%" valign="top">

**Always-on recording, only if you choose it.** Off until you switch it on. It keeps the
irreversible and the alarming (permanent deletions, sensitive-looking files, anything moving onto
or off a removable drive), not your everyday use of your own files. Switching it off takes one
click from the tray or Settings, and never needs your PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**From the tray.** See that a session is recording, end it, run a 30-second spot check of live
file activity (Monitor Now), or open the last report.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="The quick panel in the Windows tray" width="70%">

</td>
</tr>
</table>

<sub>Screenshots show Rashnova with a sample session (a fictional user, "Riya").</sub>

<a name="never"></a>
## What it never records

Rashnova records **that** something happened, not what was on the screen. It does not record:

- keystrokes
- clipboard contents
- your screen, as pictures or video
- your camera or microphone
- the contents of your documents, photos, emails or messages
- the web pages you visit, or what is on them

Two things it does record are worth knowing. During a Repair session, PowerShell commands are
recorded as they run, and so is the full start-up line of each program a person starts, so a
browser opened from a link shows that link.

A report says, for example, that `Bank_Statement_Aug2026.pdf` was opened from
`Documents\Finance` by Microsoft Edge at 15:01:16. It does not say what the statement contained.

<a name="how"></a>
## How it works

1. **Install.** Setup installs Rashnova and its background recorder.
2. **Set a PIN.** The PIN is checked by the recorder, not by the app window.
3. **Before the handover:** **Repair Mode > Activate**, then your PIN.
4. **Hand it over.** Everything in "What it does" is written to a sealed record.
5. **Get it back:** **Deactivate**, then your PIN. You get a verdict, a report and the chain check.

The recorder runs as a Windows service, so it keeps recording whether or not anyone opens the
Rashnova window, and it starts again on its own after a restart.

**Every session ends with one of four verdicts:**

| Verdict | Means |
| --- | --- |
| **Quiet** | The record verifies, it is complete, and nothing of high importance happened. |
| **Notable** | At least one high or critical event: worth reading. |
| **Compromised** | The record has a gap inside the session (the computer was off, asleep or restarting, or monitoring was interrupted) or shows interference, so it cannot vouch for the whole session. |
| **Chain broken** | The record does not verify. Everything is still shown, marked as unverified. |

<a name="download"></a>
## Download and install

| File | Use it for |
| --- | --- |
| **`Rashnova-Setup-1.1.0.exe`** | Everyone. Installs Microsoft's .NET 8 Desktop Runtime first if your PC doesn't have it, then Rashnova. |
| `Rashnova-1.1.0.msi` | Administrators deploying with their own tools. Needs the .NET 8 Desktop Runtime already installed. |
| `SHA256SUMS.txt` | The SHA-256 of each file, to check your download. |

1. Download `Rashnova-Setup-1.1.0.exe` from the [latest release](https://github.com/sathvik-zoldyck/rashnova/releases/latest).
2. **Check the file** (recommended). In PowerShell:
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-Setup-1.1.0.exe"
   ```
   The hash must match the one in `SHA256SUMS.txt` and in the release notes, exactly.
3. Run it. Windows SmartScreen shows **"Windows protected your PC"** with an unknown publisher,
   because the installer is not code-signed yet (see [Known limits](KNOWN_LIMITS.md)). Choose
   **More info**, then **Run anyway**.
4. Accept the [licence terms](https://www.alcyonesecure.com/terms), install, and open Rashnova.
5. Set a PIN, and choose whether to keep session-only recording (the default) or switch on
   always-on recording.


> [!IMPORTANT]
> A forgotten PIN cannot be recovered, by us or anyone else. Write it down somewhere safe.
> Switching always-on recording off never needs the PIN.


**Coming from BlackBox 1.0.1?** Rashnova is BlackBox's new name. Download and install 1.1.0.

<a name="requirements"></a>
## System requirements

- Windows 10 or Windows 11, 64-bit (tested on Windows 10)
- Microsoft .NET 8 Desktop Runtime (Setup installs it if it is missing)
- Administrator approval to install, because the recorder runs as a Windows service

<a name="privacy"></a>
## Privacy

- **Local only.** The record is written and kept on your computer. There is no account and no
  cloud in 1.1.0, and Rashnova sends no usage data.
- **Two small requests,** neither carrying anything from your record: a daily check of
  alcyonesecure.com for a newer version, and, during a Repair session, a check of the time against
  Microsoft's time server.
- **Who can read the record.** The Windows account that set the PIN, and the computer's
  administrators. The second copy is encrypted, and Rashnova opens it only after your PIN is
  checked. The computer's administrators can still read it.
- **Tell the people who use your PC.** Always-on recording covers the whole computer, including
  people who never open Rashnova.
- **A Windows setting, stated plainly.** When recording is first switched on, Rashnova turns on
  Windows' PowerShell script logging, and records what the setting was before. It never switches
  off a setting someone else turned on.

<a name="limits"></a>
## Known limits

We publish what Rashnova does not do, so you can decide with the facts. The most important:

- **Nothing can be recorded while the computer is off, asleep or restarting.** The session goes
  on, and the report shows each interruption and its length.
- **Administrators can read the record.** No program can keep its files from a Windows administrator.
- **The installer is not code-signed yet,** so Windows SmartScreen warns before it runs.
- **USB storage blocking is not in 1.1.0.** Every USB drive and every file copied to one is
  recorded; blocking arrives in an update.

The full list, with the reason for each and what is planned: **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## Updates

Once a day Rashnova checks alcyonesecure.com for a newer version and tells you when there is one.
You download and install it yourself; your record, PIN and settings are kept. Every version is
published here, with its release notes and SHA-256. See the [changelog](CHANGELOG.md).

<a name="support"></a>
## Support and security

- **Help:** see [SUPPORT.md](SUPPORT.md), or write to **support@alcyonesecure.com**.
- **Bugs:** [open an issue](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). Never
  post your record, file names or anything personal in an issue.
- **Security vulnerabilities:** do not open a public issue. Follow [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## Licence

Rashnova is proprietary software, free for use on devices you own or are authorised to monitor.
See [LICENSE](LICENSE) and the [terms](https://www.alcyonesecure.com/terms). The documents and images
in this repository are © Alcyone Secure.

---

<div align="center">

<img src="assets/rashnova-icon.png" alt="Rashnova" width="72">

**Alcyone Secure** · Built in Bengaluru, India · [alcyonesecure.com](https://www.alcyonesecure.com)

*Security is not just prevention. Security is accountability.*

</div>
