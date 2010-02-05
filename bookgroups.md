---
layout: default
title: Book Groups
---

# Book Groups

By convention, books of the Bible are often organized into groups, such as the Pentateuch or Gospels.  Groupings can vary for different versions of the Bible, and may contain a different sequence than appear in a complete <a href="books.html">book list</a>.  Book groups belong to a version and have many books.

## List

### Get /bookgroups.xml

Returns a list of all book groups in all versions.

## Show

### GET /bookgroups/1.xml

Returns the specified book grouping resource with ID=1.

### GET /bookgroups/1.xml?include=version

You may pass an *include* query parameter with value *version* with your request, to enclose your bookgroup resource in its parent version resource.

### GET /bookgroups/1.xml?include=books

You may pass an *include* query parameter with value *books* with your request, to include a list of the books resources it contains.