# Security policy

Rashnova's job is to keep an honest record, so we take reports about its security seriously and
we thank the people who send them.

## Supported versions

| Version | Supported |
| --- | --- |
| 1.1.x | Yes |
| 1.0.x (BlackBox) | No. Please install the latest release. |

## Reporting a vulnerability

**Please do not open a public issue for a security problem.** Report it privately, in either of
these ways:

- **GitHub:** use [Report a vulnerability](https://github.com/sathvik-zoldyck/rashnova/security/advisories/new)
  on this repository's Security tab.
- **Email:** contact@alcyonesecure.com, with "Security" in the subject.

Please include:

- the Rashnova version, and the Windows version and edition;
- what an attacker can do, and what access they need to begin with;
- the steps to reproduce it, and a proof of concept if you have one;
- whether you would like to be credited, and under what name.

Never send us anyone's real record or personal files. If a report needs evidence, describe it or
make it from a test machine.

## What happens next

- We acknowledge new reports within **72 hours**.
- We keep you informed while we investigate and fix.
- We follow coordinated disclosure: please give us a reasonable time to ship a fix before you
  publish, typically up to **90 days** from your report. If a fix ships sooner, we can agree to
  publish sooner.
- Fixes are released here, with the change described in the release notes. With your permission,
  we credit you.

## Scope

In scope:

- the installer (`Rashnova-Setup-*.exe`, `Rashnova-*.msi`) and the programs it installs;
- the Rashnova app and its background recorder, including how the app talks to the recorder;
- the integrity of the record: a way to change, remove or add entries without it showing;
- the PIN: a way to get past it, or to use Rashnova's functions that need it without it;
- the update check.

Out of scope:

- anything that needs administrator rights on the computer to begin with. An administrator can
  change any permission on Windows; this is stated in our [known limits](KNOWN_LIMITS.md);
- what cannot be recorded while the computer is off, asleep, restarting, or started from another
  drive (also a stated limit; the record shows each such interruption);
- problems in Windows, in the .NET runtime, or in other software Rashnova does not ship;
- reports from automated scanners with no demonstrated impact.
