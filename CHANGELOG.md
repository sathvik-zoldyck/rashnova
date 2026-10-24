# Changelog

Every released version of Rashnova, newest first. Installers and their SHA-256 are attached to
each [release](https://github.com/sathvik-zoldyck/rashnova/releases).

## 1.3.0 (2026-10-25)

The biggest update yet: a new design across every screen, proofs you can make of any file, Origin
to check where a file came from, and more of what happens during a session in the record.

The recorder is still free and still works without an account. Your record is kept on your
computer.

### New in 1.3.0

- **A new look.** One calm design across the whole app. The sidebar has three groups: Watch
  (Repair Mode, Handover Mode, Monitor Now, Live log, Sessions), the Readout, and Proof (Proofs,
  Origin).
- **Proofs.** Make a proof of any file: it fixes exactly what the file is and when it existed,
  witnessed by independent time stamp authorities and the Bitcoin blockchain. Only a salted
  fingerprint is sent to them, never the file. Anyone can check a proof later in a browser, without
  Rashnova, with the checker inside every proof or at [alcyonesecure.com/proof/verify.html](https://www.alcyonesecure.com/proof/verify.html). Each
  proof comes with a certificate (three designs free). Proofs are free, as many as you like.
  **Prove this session** and **Prove the report** make a proof of a session's or the Readout's report
  in one click.
- **Origin.** Drop a file and Rashnova says where it came from, whether it changed, and when it
  existed, from what the file and its proofs carry: Content Credentials (C2PA), photo details, RFC
  3161 time stamps, OpenTimestamps and Rashnova proofs. It is read on your computer; nothing is
  uploaded.
- **More in the record during a session:**
  - folders opened in File Explorer;
  - browser tab titles (the title only, never the address or the page; a private window is noted
    without its title);
  - Wi-Fi and other networks joined and left;
  - covering tracks: Windows' recent files list cleared, the Recycle Bin emptied, restore points,
    backups or event logs deleted, deleted files wiped from free space;
  - screenshots saved and screen snips started;
  - Windows' own security alerts, kept as Windows wrote them: Microsoft Defender finding something
    or being turned off, Windows Firewall turned off, an event log cleared, a new service installed,
    someone added to Administrators.

  A program reading files for itself (a build tool, a sync app) is no longer shown as a person
  opening them.
- **Wrong PINs are recorded**, naming the Windows account they came from. Wrong PINs tried from
  another Windows account no longer make you wait.
- **You choose how it records** when you set it up: Always On, or only during a session.
- **Handover Mode keeps a custody ticket:** who the computer went to, their role and why. Taking it
  back needs your PIN, and past handovers are listed.
- **Monitor Now** runs for as long as you pick, from 30 seconds to 1 hour, and keeps going while
  you use the rest of the app.
- **Sessions** shows every Repair and Handover session on a calendar, each with its verdict.
- **Notifications only when it matters:** a USB drive during a session, the recorder not answering,
  Monitor Now finished, and a proof's Bitcoin time confirmed. Each can be turned off in Settings.
- **Updates shown inside the app.** When a new version is out, the app and the tray say so, with
  what changed and the file's SHA-256. You install it yourself. Settings has **Check now**.
- **An optional account.** Sign in with an email and password, in the app or through your browser.
  Everything in the recorder works without one.
- **Uninstall from the app:** keep the record (the default) or remove everything.
- **Fixes:** after a restart, entering your PIN now waits for the recorder to be ready instead of
  failing; the live feed can no longer hold up the record; signing out forgets that account's plan.

### What leaves your computer

Nothing from your record. Rashnova makes a few small requests that carry nothing from it: a daily
check for a newer version; during a session, a check of the time, so a changed clock shows in the
record; when you make a proof, a salted fingerprint (never the file) to the time stamp services and
the Bitcoin calendars; in Origin, a Bitcoin block number, only when you ask; and only if you sign
in, your sign in and your plan.

### Known limits

- **The installer is not code-signed yet.** Your browser and Windows SmartScreen may warn about it.
  On Windows 11, Smart App Control may hold back a brand new version until Microsoft has checked
  it; we send every version to Microsoft when we publish it.
- **Not open yet:** the cloud copy and buying the Personal plan. Both appear in the app as coming.
- See [KNOWN_LIMITS.md](KNOWN_LIMITS.md).

### Upgrading

**From 1.2.1, 1.2.0 or 1.1.0:** download and install 1.3.0 over it. Your record, PIN and settings
are kept.

**From BlackBox 1.0.1:** Rashnova is BlackBox's new name. Download and install 1.3.0.

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
