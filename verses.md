---
layout: default
title: Verses
---

## Verses (belong to chapters)

Verses are the smallest unit of organization within the ABS Bible texts.  Verses belong to chapters.
    
## List

Book listings may only be requested in the context their chapter parent.

### GET /chapters/#{chapter_id}/verses.xml

Returns a list of all verses for the chapter resource specified by #{chapter_id}.

## Show

### GET /verses/1.xml

Returns the specific verse resource with ID=1.