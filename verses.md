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

## References

### GET /chapters/#{chapter_id}/verses.xml?start=1&end=14

Returns a collection of verses for the reference specified by the *start* and *end* querystring parameters.  Please note: start and end parameters represent the verse *number* attribute.

## Passages

### GET /verses.xml?passage=john+3:1&version=\#{VERSION}

### GET /verses.xml?passage=john+3:1-16&version=\#{VERSION} 

Returns a collection of verses for the passage specified by the *passage* querystring parameter.  The Bible *version* must also be specified using the [version][version] "version" value.  The passage request will be parsed, and misspelled book names or abbreviations will be corrected if possible.

Only a single version and passage may be requested.  If the BibleSearch application can find a passage matching the querystring parameters, it will perform a redirect to the canonical URL for the requested passage and respond with a a nested chapter and verse recordset.

## Searching

### GET /verses.xml?#{OPTIONS}

You may append a number of optional querystring parameters to filter the verses returned:

* *keyword:* the words(s) you are searching for.  **This parameter _must_ be provided.**
* *precision:* may be "all" to return search results with all keywords or "any" to return search results where any keywords appear
* *exclude:* any keywords that *should not* appear in the search results
* *spelling:* may be "yes" to search for keywords like the terms you submitted if your keywords return no results
* *version:* may be one or several of the [version][version] "version" values
* *language:* may be one or several of [version][version] "language" values
* *testament:* may be one or several of the [book][book] "testament" values
* *book:* may be one or several of the [book][book] "abbreviation" values
* *sort_order:* may be either "canonical" or "relevance"
* *offset:* may be an integer to request records returned after this number of records.  That is, if the offset is 1000, the records returned will start with the one thousand first record.
* *limit:* may be an integer to request a maximum number of records be returned.  If provided, *limit* must be less than or equal to 500.

A sample search URL:

    /verses.xml?keyword=love+peace&precision=all&testament=OT

## Show

### GET /verses/NASB:Acts.8.36.xml

Returns the specific verse resource with ID=NASB:Acts.8.36.

[version]: versions.html "Versions"
[book]: books.html "Books"