---
title: SciBowlDB
image: scibowldb.png
links:
- title: Website
  url: https://scibowldb.com/
- title: Github Repo
  url: https://github.com/CQCumbers/scibowldb
---

With over 16,000 categorized questions, ScibowlDB is the largest database of DOE Science Bowl questions available online, and an invaluable resource for high school science bowl teams across the US. Its web interface helps you search for specific questions to study, simulate infinite practice rounds, and create randomized questions sets for team meetings or scrimmages. SciBowlDB was built with Python, Flask, and SQL, and deployed on Heroku. As my first major web application, it taught me a great deal about full-stack web development and handling large, irregular data sets.

This project was initially inspired by the many hours I have spent digging through filing cabinets and binders full of collected science bowl rounds, trying to find ones to use to study or practice. When the teacher whose room these records were stashed in left and we had to clean up and reduce the amount of space we used, I got to work digitizing our massive collection of questions, and adding it to exchange questions and official resources available online. I wanted to create a centralized repository for questions that could be used for self-study and team practice sessions, so everyone interested in Science Bowl could more easily get access to a large database of questions to practice with. I also wanted to practice building a simple webapp with flask (I had finished a school course in python the year before and wanted to actually apply it to something). The questions are stored an encrypted SQL database with over 8000 rows, each containing data - source, category, etc. - for a pair of toss up and bonus questions. The website allows random browsing of practice questions as well as fuzzy searching and filtering of questions, and has different levels of security to allow us to keep some digitized rounds confidential. As far as I no there is no comparable system in terms of size - it catalogs more than 3 times as many questions as anything else I have seen. The service is very useful for us and other schools for science bowl practices.
