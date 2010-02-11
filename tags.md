---
layout: default
title: Tags
---

# Tags

Tags are annotations you apply to selected Bible verses.  Tags belong to users.  All tags retrieved via API will also include the verses to which they refer.                                                                             

## List

### GET /tags.xml

Returns all, site-wide tags.

### GET /users/1/tags.xml

Returns a list of tags for the user resource with ID=1.  *Please note:* You may only view tags for your own user resource.

## Show

*Please tag:* You may only access the tags you have created yourself.  If you attempt to access a tag belonging to someone else, you will receive a "404 Not Found" error.

### GET /tags/1.xml

Returns the tag identified by ID=1.  

### GET /tags/tagname.xml

For convenience, you may also retrieve tags by name.  If the tag includes multiple words, please replace the spaces in the tags with the plus symbol like: love+and+understanding

## Create

### POST /tags.xml

Creates a tag resource for the verse(s) you pass to it in the body of your XML request.

    <tags>
      <tag>love</tag>
      <verses>
        <verse id="1" />
        <verse id="3" />
        <verse id="4" />
      </verses>
    </tags>

## Update

### PUT /tags/1.xml

Updates the tag identified by ID=1 with content of the submitted XML. You may also submit the request to /tags/love.xml.

    <tags>
      <tag>love</tag>
      <verses>
        <verse id="1" />
        <verse id="3" />
        <verse id="4" />
      </verses>
    </tags>


## Delete

### DELETE /tags/1.xml

Deletes the tag identified by ID=1.

*Please note:* The content-type header is not needed for DELETE requests, since you are not sending any XML to the ABS API.