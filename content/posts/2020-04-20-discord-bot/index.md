---
title: "Tidbit: A Discord Bot That Searches Twitter"
date: 2020-04-20
draft: false
---

I built **Tidbit**, a lightweight Discord bot that listens for mentions and turns your words into smart Twitter searches. By pulling the ten longest words in a message, Tidbit queries Twitter (via the API) and replies with the most relevant tweet it finds—URLs stripped for clarity. The project is fully containerized with Docker, uses `discord.js v14` and the `twitter-api-v2` library, and is easily configurable through environment variables. Tidbit is released under the **GNU General Public License v3 (GPL-3.0)**, so you are free to use, modify, and share it under the same terms.

![Discord chat screenshot](example.png)

Check out the [source on GitHub](https://github.com/neilspink/Tidbit-Doctor-Strew) and feel free to run it in your own server or extend it with new features.
