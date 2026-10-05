# Changelog

Every released version of Rashnova, newest first. Installers and their SHA-256 are attached to
each [release](https://github.com/sathvik-zoldyck/rashnova/releases).

## 1.2.1 (2026-10-05)

A fix update for 1.2.0. It closes two ways someone with administrator rights could get around the
record, and makes uninstalling say what it does. Everything in 1.2.0 stays as it was.

It is still the free local recorder: everything is recorded and kept on your computer, and no
account is needed.

### Fixed in 1.2.1

- **A stopped recorder no longer passes for a power cut.** Rashnova now also checks Windows' own
  record of its recorder being stopped. If the recorder was killed and the computer was then
  switched off at the button, the session reads Compromised, as a stopped recorder should.
- **USB storage blocking switched off outside Rashnova is caught.** If its setting is changed outside
  Rashnova, that is recorded as tampering, the setting is put back, and USB storage stays blocked.
- **Uninstalling says uninstalling.** Every screen shown while Rashnova is removed now says so; none
  of them says "Install" or "Rashnova is installed" any more.
- **Upgrading from 1.1.0 tidies up fully.** Removing 1.1.0's old setup entry no longer stops partway
  if one of its leftover folders cannot be deleted.

### Known limits

See [KNOWN_LIMITS.md](KNOWN_LIMITS.md).

### Upgrading

**From 1.2.0 or 1.1.0:** download and install 1.2.1 over it. Your record, PIN and settings are kept.

**From BlackBox 1.0.1:** Rashnova is BlackBox's new name. Download and install 1.2.1.

## 1.2.0 (2026-10-05)

Rashnova keeps a sealed, tamper-evident record of what happens on your Windows PC, so you can
check afterwards what was done while someone else had it. This update adds Handover Mode and
USB storage blocking, and makes restarts during a session read as what they are.

It is still the free local recorder: everything is recorded and kept on your computer, and no
account is needed.

### New in 1.2.0

- **Handover Mode.** For the times someone else uses your computer for a while: family, a
  friend, a colleague. It records exactly what Repair Mode records, with the same sealed
  report, and only your PIN ends it. It has its own button on the dashboard, its own page and
  its own button in the quick panel, and past sessions say which mode each one was.
- **A restart is not tampering.** A restart, a shutdown, a power cut or sleep during a session
  is shown in the report with its length, and no longer marks the session Compromised. The
  recorder being stopped while Windows kept running is recorded as tampering, and the session
  reads Compromised.
- **USB storage blocking.** Switch it on in Settings with your PIN. Memory sticks and external
  disks no longer open, fast USB 3 drives included. A drive already plugged in keeps working
  until it is unplugged. If someone switches USB storage back on outside Rashnova, that is
  recorded as tampering and it is blocked again within seconds.
- **Start with Windows.** Choose always-on recording and Rashnova opens in the tray when you
  sign in, with no window, so Repair Mode and Handover Mode are a click away. It is its own
  switch in Settings too, and Windows lists it in its Startup apps, where you can turn it off.
- **PowerShell script logging only during a session.** Rashnova turns on Windows' PowerShell
  script logging when a Repair or Handover session starts and puts it back as it was when the
  session ends. 1.1.0 left it on between sessions.
- **Clearer words.** Change PIN says which step you are on. The Readout's cards say plainly
  what happened, every card can be opened, and a day marked partial is explained.
- **Smaller fixes.** A file at the top of a drive names the drive. Windows' own System Restore
  is no longer recorded as a person's program after the computer wakes. The tray icon uses far
  less of the processor.
- **One file that installs itself.** The download is now a single installer that brings
  everything Rashnova needs, including its own copy of .NET 10. Nothing else is downloaded
  during setup and nothing needs to be installed first. Microsoft supports .NET 10 until
  November 2028; support for .NET 8, which 1.1.0 used, ends in November 2026.

### Coming later

Cloud backup, recovery from another device, location recording and the paid plan come in a
later version.

### Known limits

See [KNOWN_LIMITS.md](KNOWN_LIMITS.md).

### Upgrading

**From 1.1.0:** Download and install 1.2.0 over 1.1.0. Your record, PIN and settings are kept. 1.1.0 was
installed through a separate setup program; its leftover entry in Windows' installed apps list
is removed, so Rashnova appears there once.

**From BlackBox 1.0.1:** Rashnova is BlackBox's new name. Download and install 1.2.0.

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
