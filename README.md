# DT-Iverta 1.0.0

**The app asks, you answer.** *Think it and Dream it to life.*

An issue tracker for Windows. An issue is anything that needs you: a bug in something you are
building, a repair, a renewal, a deadline, a letter that wants an answer. All of it in one place,
most pressing first, and every one of them yours to decide.

## What is here

| File | What it is |
|---|---|
| `DT-Iverta-1.0.0-x64.msi` | the installer: everything DT-Iverta is, in one file. It is the release's download (Releases, 1.0.0), not a file in the repository, which holds nothing over 100 MB |
| `SHA256SUMS` | the installer's SHA-256, to check the copy you have is this one |
| `LICENSE` | the MIT licence |
| `RELEASE-NOTES.md` | what is in 1.0.0, and its known limits |
| `THIRD-PARTY-NOTICES.md` | every component it is built from, and each one's terms |

## Installing

Download `DT-Iverta-1.0.0-x64.msi` from the 1.0.0 release and run it. Windows asks once for permission to install for everyone on the
computer. DT-Iverta goes into `C:\Program Files\DT-Iverta`, with DT-Iverta in the Start menu and
its folder on the PATH, so `DT-Iverta` works in any terminal opened after it. Settings, Apps takes
it away again; each person's own records, settings and keys stay where they are. Windows 10 or 11,
64-bit.

To check the installer before you run it, in PowerShell:

```
Get-FileHash .\DT-Iverta-1.0.0-x64.msi -Algorithm SHA256
```

and compare the hash with the one in `SHA256SUMS`.

It is not signed, so Windows may warn before its first start, and an antivirus may hold its first
run on a machine.

## Free, private, and yours

**Free.** DT-Iverta is free, under the MIT licence. Use it, share it, take it apart, change it,
and pass it on, changed or not. The one condition is that the copyright notice, the credit to its
original author, stays with every copy. Once you have downloaded it, your copy is yours.

**No support.** No technical assistance of any kind is offered. The guide inside the program
(`DT-Iverta help`, and Help in the window, F1) is all the documentation there is. DT-Iverta comes
as it is, with no guarantee of any kind; the licence says so in full. What you do with it is up to
you.

**No server, no collection.** There is no privacy policy, because there is nothing for one to
cover. DT-Iverta collects nothing about you and sends nothing to its author: no account, no
telemetry, no crash reports, no update checks, and no server of ours for anything to go to. It
needs no central server to work.

Nothing leaves your computer unless you switch on something that reaches the internet: a provider
for CoWork, a calendar or mail account, the weather, rates and prices, or the Browser. What that
sends goes to the company you chose, under that company's own terms, and DT-Iverta writes every
request in the send log before it goes. The switch "Nothing leaves this computer" stops all of it at
once.

Part of the point of DT-Iverta is to give power away. What you know carries some of that power, so
all of it stays with you.
