---
layout: default
title: Taggings
---

# Taggings

Taggings associate users to tags.  Taggings belong to users and to tags.

*Please note:* You may only view or manipulate your own taggings.

## List                                       

### GET /user/taggings.xml

Returns all of your taggings.  All of your tags and tagged verses are included in the output of this request.

### GET /user/taggings.xml?tag=love

Returns all of your taggings for the supplied tag.  The supplied tag and all verses you have tagged with it are included in the output of this request.

## Show

### GET /taggings/1.xml

Returns the selected tagging with ID=1.  The associated tag and all verses are included in the output of this request.

## Create

### POST /taggings.xml

Creates a tagging resource for the tag and verse(s) you pass to it in the body of your XML request.  You may pass either the tag *name* node or *id* node with your request.

    <tagging>
      <tag>
        <name>love</name>
      </tag>      
      <verses>
        <verse id="1" />
        <verse id="3" />
        <verse id="5" />
      </verses>
    </tagging>

## Update

### Update /taggings/1.xml

Modifies a tagging resource identified by ID=1 with the tag and verse(s) you pass to it in the body of your XML request.  You may pass either the tag *name* node or *id* node with your request.

    <tagging>
      <tag>
        <name>love</name>
      </tag>      
      <verses>
        <verse id="1" />
        <verse id="3" />
        <verse id="5" />
      </verses>
    </tagging>

## Delete

### DELETE /taggings/1.xml

Deletes the tagging identified by ID=1.

*Please note:* The content-type header is not needed for DELETE requests, since you are not sending any XML to the ABS API.