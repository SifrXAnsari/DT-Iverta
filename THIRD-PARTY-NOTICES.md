# Third-party notices

DT-Iverta is MIT licensed. What follows is everything else it is built with or can use, and the
terms each comes under. One library sits in the source tree, because documents cannot be read
without it; the build fetches the rest, and the model files are downloaded by whoever runs it.

## Built into the program

**md4c** — MIT License. Copyright © 2016-2026 Martin Mitáš.
https://github.com/mity/md4c — release v0.6.0 (commit 7fc1815a), in `third_party/md4c` with its
own `LICENSE.md`. It reads the Markdown documents are kept in.

**AvaloniaEdit** — MIT License. Copyright (c) 2017 Eli Arbel; the AvalonEdit code it was ported
from is Copyright (c) 2014 AlphaSierraPapa for the SharpDevelop Team, under the same terms.
https://github.com/AvaloniaUI/AvaloniaEdit — package `Avalonia.AvaloniaEdit` 11.4.1, fetched by
the build. It is the doc writer's editor.

**llama.cpp** — MIT License. Copyright (c) 2023-2024 The ggml authors.
https://github.com/ggml-org/llama.cpp — pinned in `third_party/llama.cpp.pin`. It carries
**ggml**, under the same MIT terms, and the CPU, CUDA and Vulkan backends built from it.

**Avalonia** — MIT License. Copyright 2013-2025 © The AvaloniaUI Project.
https://github.com/AvaloniaUI/Avalonia — packages `Avalonia`, `Avalonia.Win32`, `Avalonia.Skia`,
`Avalonia.Themes.Fluent` and `Avalonia.Remote.Protocol` 11.3.7, fetched by the build. The window is
drawn with it.

**MicroCom.Runtime** — MIT License. Copyright 2021 © Nikita Tsukanov. Package 0.11.0, which
Avalonia uses to call Windows' COM interfaces.

**SkiaSharp** — MIT License. © Microsoft Corporation. Package 2.88.9, with **Skia** (BSD
3-Clause, Google) in `libSkiaSharp.dll`, and the libraries Skia is built with, each named with its
terms in the `THIRD-PARTY-NOTICES.txt` the package ships.

**HarfBuzzSharp** — MIT License. © Microsoft Corporation. Package 8.3.1.1, with **HarfBuzz** (the
"Old MIT" licence, Behdad Esfahbod and others) in `libHarfBuzzSharp.dll`, as its own notices file
sets out.

**ANGLE** — BSD 3-Clause License. Copyright 2018 The ANGLE Project Authors. In
`av_libglesv2.dll`, from the package `Avalonia.Angle.Windows.Natives` 2.1.25547.20250602.

**The .NET runtime** — MIT License. © Microsoft Corporation. Compiled into `DT-Iverta.exe` ahead
of time by the package `runtime.win-x64.Microsoft.DotNet.ILCompiler` 10.0.12, whose
`THIRD-PARTY-NOTICES.TXT` names what the runtime itself is built from.

**The WebView2 SDK** — BSD 3-Clause License. Copyright (C) Microsoft Corporation. From the package
`Microsoft.Web.WebView2` 1.0.4191.47: its header, compiled into the program, and its loader,
`WebView2Loader.dll`, which ships beside it. The engine the loader starts, Microsoft Edge WebView2,
is part of Windows (the Evergreen runtime) and is not redistributed here.

The build copies every licence and notice file these packages ship, from the exact versions it
took, into `notices\` beside the program, and lists every component and version in
`components.cdx.json` (CycloneDX 1.5). Those files are the full terms; this page is the summary.
The full MIT text is the same as `LICENSE` in this repository, with the copyright lines above.

## Photographs, in the Hawaii theme

Eight photographs, each dedicated to the public domain by the person who took it, under the
Creative Commons CC0 1.0 Universal dedication: nothing is owed for using them, and each is credited
here and wherever the program shows it all the same. They were published on Unsplash and are kept
on Wikimedia Commons, where these copies came from; each was made 2,560 pixels wide and saved again
without the camera's data, and the program is built only with the bytes whose SHA-256
`themes/hawaii/theme.json` records.

- **The Nā Pali coast from the sea**, Kauaʻi. Christian Joudrey.
  https://commons.wikimedia.org/wiki/File:Na_Pali_Coast_(Unsplash).jpg
- **Hanauma Bay**, Oʻahu. Matty Adame.
  https://commons.wikimedia.org/wiki/File:Paradise_(Unsplash).jpg
- **A headland in the evening sun**, Maui. Luca Bravo.
  https://commons.wikimedia.org/wiki/File:Maui,_Hawaii_(Unsplash).jpg
- **Nā Mokulua at dawn, from Lanikai**, Oʻahu. Christian Joudrey.
  https://commons.wikimedia.org/wiki/File:Two_island_silhouettes_(Unsplash).jpg
- **The Nā Pali coast from the Kalalau Trail**, Kauaʻi. Josh Austin.
  https://commons.wikimedia.org/wiki/File:NaPali_Coast_(Unsplash).jpg
- **Palms at sunset**, Maui. Ethan Robertson.
  https://commons.wikimedia.org/wiki/File:Palm_trees_and_the_ocean_(Unsplash).jpg
- **The coast north of Mākaha at dusk**, Oʻahu. Jeremy Bishop.
  https://commons.wikimedia.org/wiki/File:Side_of_the_mountain_(Unsplash).jpg
- **Haleakalā's crater above the clouds**, Maui. delfi de la Rua.
  https://commons.wikimedia.org/wiki/File:Haleakal%C4%81_National_Park_-_Delfi_de_la_Rua_2016-06-04_(Unsplash).jpg

## Graphics libraries, on a machine built with CUDA

NVIDIA's **CUDA runtime** (`cudart64_12.dll`) and **cuBLAS** (`cublas64_12.dll`,
`cublasLt64_12.dll`) ship beside the program. They come from the CUDA Toolkit 12.9 and are
redistributed under the NVIDIA CUDA Toolkit End User License Agreement, whose Attachment A lists
the CUDA Runtime and the CUDA BLAS Library as distributable; the build copies that agreement into
`notices\cuda`. They are loaded only when the local model first uses the card.

## Runtimes for code, beside the program

`DT-Iverta code` runs Python and C#, each a program of its own in `runtimes\`, never linked into
DT-Iverta.exe.

- **Python 3.14.7**, the embeddable distribution for Windows x64 from python.org, unchanged,
  under the Python Software Foundation License Version 2; its own `LICENSE.txt` sits in
  `runtimes\python` and is copied into `notices\python`. The build checks the download against the
  SHA-256 `runtimes\languages.json` records.
  https://www.python.org/ftp/python/3.14.7/python-3.14.7-embed-amd64.zip
- **Roslyn's scripting API** (Microsoft.CodeAnalysis.CSharp.Scripting 5.9.0 and the packages it
  needs), MIT, the .NET Foundation, and the **.NET runtime** the C# runner is published with, MIT,
  Microsoft. Their licence and notice files are copied into `notices\`, and each is listed with its
  version in `components.cdx.json`.

## Parts of Windows that DT-Iverta calls

These ship with the operating system and are used through their public interfaces. They are not
redistributed here.

- **winsqlite3** — Windows' own build of SQLite, used for the search index. SQLite is in the
  public domain.
- **CNG, NCrypt and DPAPI** — hashing, signatures, AES-GCM and the sealing of secrets.
- **WinHTTP** — the only way DT-Iverta speaks to the internet, used only by its network broker.
- **SAPI** — reading aloud, with the voices already installed.
- **Windows.Media.Ocr and Windows.Data.Pdf** — reading text off a page, through C++/WinRT
  (which is part of the Windows SDK).
- **DXGI** — asking what graphics card is present and how much memory it has.
- **AppContainer and job objects** — the sandboxes the local model, the page reader, the
  network broker and code typed at `DT-Iverta code` run in.
- **Microsoft Edge WebView2** — the Browser's full-service engine, kept up to date by Windows.
- **The Segoe UI typeface** — the window writes in Windows' own interface font; no font ships.

## Models, if you choose to use one

No model is included. DT-Iverta is pointed at a file you downloaded, and the terms are the
model's own. The one DT-Iverta was tested with:

- **Qwen3-4B** (GGUF, Q4_K_M) — Apache License 2.0, Alibaba Cloud.
  https://huggingface.co/Qwen/Qwen3-4B-GGUF

## Providers, if you choose to use one

Claude (Anthropic), OpenAI and Microsoft 365 Copilot are reached through their public APIs with
a key or token you supply. Their terms, billing and data handling are between you and them;
DT-Iverta only writes down exactly what it sent.
