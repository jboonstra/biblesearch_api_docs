---
layout: default
title: Tags
---

# Tags

Tags are annotations applied to selected Bible verses.  Tags belong to users.  Individual tags retrieved via API will also include the verse references to which they refer.                                                                             

## List

### GET /tags.xml

Returns all, site-wide tags.  

*Please note:* This request for all tags *will not* include their verse references.

### GET /user/tags.xml

Returns a list of tags for your user.

*Please note:* This request for all tags *will not* include their verse references.

## Show

### GET /tags/1.xml

Returns the tag identified by ID=1.  

### GET /tags/tagname.xml

For convenience, you may also retrieve tags by name.  If the tag includes multiple words, please replace the spaces in the tags with the plus symbol like: love+and+understanding

## Create

Create (POST) requests are not allowed for tag resources.  To create a tag you must create a tagging resource.

## Update

Update (PUT) requests are not allowed for tag resources.  To edit a tag, you must make a request to its tagging resource.

## Delete

Delete (DELETE) requests are not allowed for tag resources.  To delete a tag, you must delete its corresponding tagging resource.
