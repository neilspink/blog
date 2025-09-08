---
title: "Recaptures: a one‑minute screen capture journal (C#)"
date: 2020-05-14
tags: ["csharp", "windows", "automation", "screen-capture", "fluentftp", "serilog", "privacy", "productivity"]
summary: "A tiny Windows utility that snapshots your screen every minute and ships it to storage—useful for a visual work log."
---

## Why I built it

In 2020, *everyone* was home; Parents, kids, teachers. My son had school on the computer and I had work. Like many parents, “Trust is good, control is better,” my wife said, so I built a way to see what my son was actually doing.  

I wanted a **visual record of work** without manual logging—something I could glance back on to reconstruct what he did.  So I wrote **Recaptures**, a tiny Windows app that **screenshots once per minute** and **uploads the JPEG** to remote storage.

- Language: **C# / .NET (WinForms host)**
- Packages: **FluentFTP** for FTPS, **Serilog** for logs
- Strategy: minimal timer + full-screen capture + JPEG quality control

Repo: `https://github.com/neilspink/recaptures`


### Prolog

My son hated it. When he was caught not working on school stuff, he quickly discovered why: the app. :) It was fun (for me) watching him try to hack it in real time.  

For him, it was surveillance. For me, it was peace of mind. But I’ll give him credit: it **raised his IT game**, and that, in a way, was also part of the lesson.
