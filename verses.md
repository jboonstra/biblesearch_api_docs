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

## Searching

### GET /verses.xml?#{OPTIONS}

You may append a number of querystring options to filter the verses returned:

* *keyword:* the words(s) you are searching for
* *precision:* may be "all" to return search results with all keywords or "any" to return search results where any keywords appear
* *exclude:* any keywords that *should not* appear in the search results
* *version:* may be one or several of the [version][version] "version" values
* *language:* may be one or several of [version][version] "language" values
* *testament:* may be one or several of the [book][book] "testament" values
* *book:* may be one or several of the [book][book] "abbreviation" values
* *sort_order:* may be either "canonical" or "relevance"

A sample search URL:

    /verses.xml?keyword=love+peace&precision=all&testament=OT

## Show

### GET /verses/1.xml

Returns the specific verse resource with ID=1.

[version]: /versions.html "Versions"
[book]: /books.html "Books"