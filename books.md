---
layout: default
title: Books
---

# Books

These are the books of the Bible belonging to the requested version.  Books belong to versions and have many chapters.

## List

### Get /books.xml

Returns a list of all books for all versions.

## Show

### GET /books/1.xml

Returns the specified book resource.

## Show with Chapters

### GET /books/1.xml?include=chapters

You may pass an *include* query parameter with value *chapters* with your request to retrieve a list chapter resources belonging to each book (/books.xml request) or the specified version (for the /books/1.xml request).



