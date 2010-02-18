---
layout: default
title: Versions
---

# Versions

Versions are the specific editions of the Bible such as the New International Version (NIV) or King James Version (KJV).  Versions have many books.

## List

### GET /versions.xml

Returns a list of all available versions.

### Get /versions/#{version_id}/books.xml

Returns a list of all books for the specified version.

## List with Language

### GET /versions.xml?language=eng

Returns a list of all versions specified by the language parameter.  Use an [ISO 639-2][iso] abbreviation as the language parameter.
  
## Show
    
### GET /versions/NASB.xml

Returns a specific version with ID=NASB.