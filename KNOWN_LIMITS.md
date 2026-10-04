# Rashnova 1.1.0: known limits

What Rashnova 1.1.0 does not do, or does not do yet. Each entry says what the limit is, why, and
what is planned. We publish this so you can decide with the facts; if a limit changes, it changes
here first.

---

## Installing

**The installer is not code-signed yet.**
Windows SmartScreen shows "Windows protected your PC" and "Unknown publisher" when you run
it. To continue, choose "More info", then "Run anyway". Before you do, you can check that the
file is the one we published: its SHA-256 is listed next to the download link.
*Why:* we do not have a code-signing certificate yet.
*Planned:* a signed installer once we do. Until then the warning stays: Windows does not
build up trust for an unsigned installer over time.

**Windows only, 64-bit.**
Rashnova 1.1.0 is built for 64-bit Windows 10 and 11, and has been tested on Windows 10.
It needs Microsoft's .NET 8 Desktop Runtime, which the installer downloads from Microsoft and
installs first if it is missing.
*Planned:* nothing announced for other systems in this version.

## Your PIN

**A forgotten PIN cannot be recovered.**
Not by us, and not by signing in. Starting a Repair session, exporting a report and deleting
data need the PIN. Turning recording off never needs it, so a forgotten PIN can never keep
you being recorded.
*Why:* a way to recover the PIN would be a way around it for anyone who has the computer.
*Planned:* nothing; this is deliberate.

## Who can read the record

**The record can be read by the account that set the PIN, and by administrators.**
The record on this computer can be read by the Windows account that set the Rashnova PIN and
by every administrator account on this computer. Other accounts cannot read it, and
restarting the computer or signing in with another account does not change that.
The second copy is encrypted, and Rashnova opens it only after your PIN is checked. The
computer's administrators can still read it.
*Why:* an administrator can change any permission on Windows, so no program can keep its files
from one.
*Planned:* nothing; this is how Windows works.

## What is recorded

**Nothing can be recorded while the computer is off, asleep or restarting.**
A Repair session ends only when you end it with your PIN. If the computer restarts, is switched
off or goes to sleep, or Rashnova's recorder is stopped during a session, recording pauses and
resumes by itself as soon as the computer starts or wakes again, before anyone signs in. The
session's report shows each interruption and how long it lasted. Nothing done in that time can be recorded, including
anything done by starting the computer from another drive. After such a restart, Rashnova's
encrypted copy of the record stays paused until you enter your PIN.
*Why:* nothing runs while the computer is off, and Rashnova opens the encrypted copy only after
your PIN is checked.
*Planned:* nothing; this is a deliberate trade.

**A crash or power cut can lose the last few seconds.**
Some activity is held for a few seconds before it is written: repeated events are grouped
into one entry, and a rename, a new file or a program's save is held briefly so it can be
written down correctly (with the file's new name, or as one save instead of several steps).
Everything held is written when Rashnova stops normally and at the end of every Repair
session. If Windows crashes or the power is cut, the last few seconds of activity may be
missing from the record.
*Why:* writing each step at once would record an editor's save as several confusing entries
and a rename without its new name.
*Planned:* nothing; this is a deliberate trade.

**Changes to Windows settings (the registry) cannot be attributed to a person.**
They are recorded, with the setting and the time, but Windows does not say which program or
account made the change. Wherever the report shows one, it says so.
*Why:* a limit of what Windows reports.
*Planned:* no fix in sight.

## Not in this version

**USB storage blocking.**
Rashnova 1.1.0 records every USB storage device that is plugged in and every file copied to
one, but does not block them. The switch in Settings says "Coming soon".
*Planned:* an update shortly after launch.

**Cloud backup, sign-in, recovery from another device, location recording and the paid
plan.**
1.1.0 is the free local recorder: everything is recorded and kept on this computer, with no
account. These features appear in Settings as "Coming soon".
*Planned:* a later version.

## Updates

**Updates are not installed automatically.**
Once a day the app checks alcyonesecure.com for a newer version and tells you when there is
one; you download and install it yourself. Your record, PIN and settings are kept across an
update.
*Planned:* nothing at present.
