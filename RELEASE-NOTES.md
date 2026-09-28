# DT-Iverta 1.0.0

Release notes, 28 September 2026. The first official release. It is not signed, so Windows may warn
before its first start and an antivirus may hold its first run on a machine.

## Installing it

`DT-Iverta-1.0.0-x64.msi` installs DT-Iverta for everyone on the computer, into
`C:\Program Files\DT-Iverta`, with DT-Iverta in the Start menu and its folder on the PATH. Windows
asks once for permission. Settings, Apps takes it away again, and leaves each person's own records,
settings and keys where they are. Windows 10 or 11, 64-bit.

DT-Iverta is one program, `DT-Iverta.exe`, with the few files beside it that it needs. Started from
the Start menu or Explorer it opens the window; in a terminal, `DT-Iverta help` lists everything,
and every screen in the window is a command first.

It writes to the workspace folders you start; to `%LOCALAPPDATA%\DT-Iverta`; to Windows' own key
store, where this machine's signing key lives (`DT-Iverta devices` names it); to the profiles
Windows keeps for its sandboxes (`%LOCALAPPDATA%\Packages\DT-Iverta.*`); and wherever you send an
export. Nothing else, and nothing starts with Windows unless you ask for it.

The guide, DT-Iverta's own documentation, is inside the program and needs no network:
`DT-Iverta help` at the command line, and Help in the window (F1, the rail, or Settings).

On a machine it has not run on before, three commands show how it stands there:

```
DT-Iverta version       which build this is
DT-Iverta ml probe      whether the model on this machine can use its graphics card
DT-Iverta where         where your work is kept, and what has left this computer
```

## Free, private, and yours

Free under the MIT licence: use it, share it, take it apart, change it, and keep the credit to its
original author with every copy. No technical assistance of any kind is offered. Nothing about you
is collected, and nothing is sent to its author. `DT-Iverta help free-and-yours` says it in full.

## What is in it

- **Issues**: notes, tasks and matters; statuses a kind chooses; priorities; deadlines as dates in
  a time zone; things that come round again; checklists; comments; links that block, supersede,
  duplicate or relate; why something ended; lists and tags; a list or a board; and the whole
  history of every change, to scroll back through or to see an issue as it stood on a day.
- **Documents**: a writer with letters, reports and meeting notes laid out; tables and charts;
  spelling by Windows' own checker; bringing in Word, OpenDocument, RTF, EPUB, PDF, web pages and
  Markdown, read in a sandbox; sending out as PDF, Word, OpenDocument, HTML, Markdown and text;
  converting files; handing a copy on through Windows' Share window; and every version of a text.
- **Home**: the calendar and the clock, the issues that need you, holidays and the seasons, and
  cards you choose: calendars from a link, Outlook.com, CalDAV and Google Calendar, Gmail, the
  weather, rates and prices.
- **The look**: Hawaii, with photographs of the islands, or Night; and your own photographs behind
  the window if you want them.
- **The Browser**: a reading view that makes any page a document, and, when you turn it on, the
  whole web in a WebView2 tab that keeps nothing between runs.
- **CoWork**: work handed over in your own words, planned as a checklist you can see and done a
  step at a time, never changing anything without the permission you chose, by the model on this
  computer in a sandbox with no network, or by a provider you switched on. Several tasks at once;
  a stop that cuts an answer off; what every task in a workspace is told first.
- **Automations**: scripts of commands in the workspace, run at a time of day, when a date passes
  or when a status changes, only on the machine that each names and only once allowed there.
- **Open data**: any list opened in a spreadsheet, and every table kept as plain files for Power
  BI's folder connector.
- **SippBucket**: when SippBucket runs on the machine, what another machine writes shows within
  seconds, and what this one writes leaves at once.

## What leaves the computer

Nothing, until you turn a feature on. Each feature that reaches the internet has its own switch,
off to start, says exactly what it sends, and writes every request in the send log before it goes.
The master switch, "Nothing leaves this computer", overrides them all. The model on this computer
runs in a Windows AppContainer with no capabilities at all, and the network broker in one whose
only capability is the internet as a client. Both have been tried from inside, asked to do what
their walls forbid, and every attempt was refused.

## Measured at size

On a six-core desktop with a GTX 1060 3 GB, a workspace of 5,000 issues, 1,000 links between them
and 1,000 documents, made from 27,269 changes, was timed:

| What | How long |
|---|---|
| A change, at full size as at the start | 8 ms |
| Opening it, every change read and replayed | 0.35 s, and 86 MB of memory |
| What a command that changed nothing pays as it ends | 65 ms |
| What a command that changed something pays as it ends | 0.34 s |
| A list of 3,750 issues | 24 ms |
| A search | 4 ms |
| The first time a machine writes the tables of a workspace this size | 23 s, once |

## Known limits

- It is not signed, so an antivirus may hold its first run on a machine.
- Signatures are ECDSA P-256, because Windows' key store has no Ed25519.
- Microsoft 365 Copilot's Chat API is a preview, for Copilot-licensed work accounts only.
- Skia, HarfBuzz, ANGLE and Microsoft's WebView2 loader, and on a machine with CUDA the graphics
  runtime, ship as DLLs beside the program: none is published in a form that links in with the
  program's own protections.
- The doc writer's page reads to a screen reader as an edit box with its text, not line by line
  or word by word, and a table as cells one by one: Avalonia offers no text or table patterns.
- File types are recognised from 254 kinds written here, not from The National Archives' full
  signature file.
- Outlook.com, Google Calendar and Gmail need a client ID you register yourself
  (`DT-Iverta help connectors` says how).

## What it is made of

`THIRD-PARTY-NOTICES.md` names every component and its terms, `notices\` beside the program holds
their licence files as the build took them, and `components.cdx.json` lists every component and
version (CycloneDX 1.5).
