---
title: Navi Search
image: navi_search.png
---

Built with 5 other students for a capstone class, Navi Search is a complete internet search engine written from scratch in C++. It includes a robust HTML parser and web crawler, capable of downloading over 300 pages per second per machine over HTTPS, while respecting robots.txt rules and server timeouts. An inverted index generator and constraint solver allow the over 400 million pages and 5TB of text crawled to be quickly queried over multiple machines, and a query compiler transforms English-like syntax into efficient query plans. All this is attached to a ranker that takes into account word frequency, relative positions, URL and body text, and other factors to deliver useful results. In creating it my team and I learned a great deal about debugging and profiling distributed systems, tuning low-level Linux features on AWS, interacting with web protocols at several layers of the stack, and working as a team to deliver a complete product on a tight schedule.
