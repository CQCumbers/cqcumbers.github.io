---
title: Dungeon Bot
image: dungeon_bot.png
links:
- title: Invite Link
  url: https://discordapp.com/oauth2/authorize?client_id=664915224595398666&scope=bot
- title: Github Repo
  url: https://github.com/CQCumbers/dungeon_bot
---

Dungeon Bot is a Discord bot interface for the popular game AI Dungeon 2, an open-ended text adventure based on OpenAI's GPT-2 language model. It is currently used by over 1000 servers, and provides a unique way to craft interesting narratives together with other users. An experiment in deploying large deep learning models on GPU servers, it relies on a central redis server to handle incoming requests, and spins up relatively inexpensive vast.ai GPU workers to generate interesting scenarios from free-form player inputs. While not as technically challenging as some of my other projects, through it I gained experience in deploying GPU-based deep learning models via Docker, as well as debugging distrubuted systems.
