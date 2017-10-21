---
title: SciBowlDB
image: scibowldb.png
links:
- title: Website
  url: http://www.scibowldb.com/
- title: Github Repo
  url: https://github.com/CQCumbers/scibowldb
---

SciBowlDB is the largest database of high school science bowl questions available anywhere, with over 16,000 unique toss-up and bonus questions (about 9000 are publicly available), all labelled with correct answer, category, and source. Questions are compiled from freely available online sources including 1998 and 2005 nationals rounds, as well as from question exchanges and my high school archives. The website allows one to fuzzy search and filter for specific questions to study, simulate infinite toss-up practice rounds, and create randomized sets of 25 questions for use in invitationals or formal practices. Technology-wise, SciBowlDB is built with Python, Flask, and SQLite on Heroku. It is used extensively by many high school science bowl participants across the country for study and practice.

This project was initially inspired by the many hours I have spent digging through filing cabinets and binders full of collected science bowl rounds, trying to find ones to use to study or practice. When the teacher whose room these records were stashed in left and we had to clean up and reduce the amount of space we used, I got to work digitizing our massive collection of questions, and adding it to exchange questions and official resources available online. I wanted to create a centralized repository for questions that could be used for self-study and team practice sessions, so everyone interested in Science Bowl could more easily get access to a large database of questions to practice with. I also wanted to practice building a simple webapp with flask (I had finished a school course in python the year before and wanted to actually apply it to something). The questions are stored an encrypted SQL database with over 8000 rows, each containing data - source, category, etc. - for a pair of toss up and bonus questions. The website allows random browsing of practice questions as well as fuzzy searching and filtering of questions, and has different levels of security to allow us to keep some digitized rounds confidential. As far as I no there is no comparable system in terms of size - it catalogs more than 3 times as many questions as anything else I have seen. The service is very useful for us and other schools for science bowl practices.
