---
layout: default
title: Books
---

# Books

These are the books of the Bible belonging to the requested version.  Books belong to versions and to bookgroups, and books have many chapters.

## List

Book listings may only be requested in the context of version or bookgroup parents.

### GET /versions/NASB/books.xml

Returns a list of a books for the version resource with ID=NASB.

### GET /bookgroups/1/books.xml

Returns a list of all books for the bookgroup resource with ID=1.

### GET /versions/NASB/books.xml?testament=#{abbreviation}

Returns a list of only those books identified by the Testament abbreviation for the version resource with ID=1.  Valid abbreviations include NT (New Testament), OT (Old Testament) and DEUT (Deuterocanonical).

## Show

### GET /books/NASB:Acts.xml

Returns the specified book resource with ID=NASB:Acts.