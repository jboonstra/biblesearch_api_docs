---
layout: default
title: Verses
---

## Verses (belong to chapters)

Verses are the smallest unit of organization within the ABS Bible texts.  Verses belong to chapters.
    
## List

Book listings may only be requested in the context their chapter parent.

### GET /chapters/#{chapter_id}/verses.xml (with pagination: /verses.xml?n=#{offset})

Returns a list of all verses for the chapter resource specified by #{chapter_id}, paginated in groups of 500.

TODO: are there chapters with more than 500 verses?

## Show

### GET /verses/1.xml

Returns the specific verse resource with ID=1.

### GET /verses/1.xml?include=chapter

You may pass an *include* query parameter with value *chapter* with your request to retrieve the verse's parent chapter resource alongside the requested verse.