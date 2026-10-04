# Changelog

Every released version of Rashnova, newest first. Installers and their SHA-256 are attached to
each [release](https://github.com/sathvik-zoldyck/rashnova/releases).

## 1.1.0 (2026-10-05)

Rashnova keeps a sealed, tamper-evident record of what happens on your Windows PC, so you can
check afterwards what was done while someone else had it: at a repair shop, a service desk,
or with anyone you hand it to. Black Box is now called Rashnova.

This release is the free local recorder. Everything is recorded and kept on your computer,
and no account is needed.

### What's in it

- **Repair Mode.** Start a watched session before you hand the PC over. When you get it back,
  you get a summary and a report of what was opened, copied, renamed and deleted, which
  programs ran, and which USB devices were plugged in, every file copied to them included.
- **Always-on recording, if you choose it.** Off until you turn it on. It keeps the
  irreversible and the alarming (permanent deletions, sensitive-looking files, anything
  moving onto a removable drive), not your everyday use of your own files. You can turn it
  off in one click, and turning it off never needs your PIN.
- **A record you can check.** Everything is written to a hash chain on this computer: you can
  tell if the record was altered or has gaps.
- **Reports** as PDF, web page (HTML) or spreadsheet (CSV), from the session summary or the
  dashboard. What you save is a copy; the original stays where Rashnova keeps it.
- **The Readout:** your week, in one verdict.
- **Monitor Now:** 30 seconds of live file activity, whenever you want a look.
- **Your PIN** is needed to start and end a Repair session, open the Readout or your past
  sessions, export a report and delete data. Switching always-on recording off never needs it.

### New since 1.0.1

- **Far fewer false alarms.** Everyday activity is no longer flagged as critical. Replayed over
  real logs from a working PC, the share of events rated critical fell from 43% with the
  previous rules to under 0.5%.
- **No account.** 1.1.0 needs no sign-in at any point.
- **An installer that does the whole job.** Setup installs Microsoft's .NET 8 Desktop Runtime
  first if your PC doesn't have it. If Rashnova's background service can't start, the
  installation is undone completely instead of leaving a half-working copy behind.
- **A Windows setting, stated plainly.** When recording is first switched on, Rashnova turns on
  Windows' PowerShell script logging, and records what the setting was before. It never
  switches off a setting that someone else turned on.
- **Update notices.** Once a day the app checks for a newer version and tells you. You
  download and install it yourself; your record, PIN and settings are kept.
- **Privacy.** With cloud backup off (the only option in 1.1.0), nothing from your record
  leaves the computer. The app makes two small requests, neither carrying anything from the
  record: the daily update check, and a check of the time against Microsoft's time server
  during a Repair session.

### Coming later

USB storage blocking arrives in an update shortly after launch. Cloud backup, recovery from
another device, location recording and the paid plan come in 1.2.

### Known limits

See [KNOWN_LIMITS.md](KNOWN_LIMITS.md).

### Upgrading from 1.0.1

Download and install 1.1.0.

## 1.0.1 (2026-05-14)

The first public release, under the name BlackBox. Superseded by 1.1.0; its page remains at
[black-box-v1.0.1](https://github.com/sathvik-zoldyck/black-box-v1.0.1).
