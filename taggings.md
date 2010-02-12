---
layout: default
title: Taggings
---

# Taggings

Taggings associate tags with verses and are owned by users.

*Please note:* You may only view or manipulate your own taggings.

## List                                       

### GET /user/taggings.xml

Returns all of your taggings.  All of your tags and tagged verses are included in the output of this request.

### GET /user/taggings/love

Returns all of your taggings for "love".  The supplied tag and all verses you have tagged with it are included in the output of this request.

## Show

### GET /user/taggings/1.xml

Returns the selected tagging with ID=1.  The associated tag and all verses are included in the output of this request.

## Create

### POST /user/taggings.xml

Creates a tagging resource for the tag and verse(s) you pass to it in the body of your XML request.  You must pass either the tag *name* node or *id* node with your request.

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

### PUT /user/taggings/1.xml

Modifies a tagging resource identified by ID=1 with the tag and verse you pass to it in the body of your XML request.  You may pass either the tag *name* node or *id* node with your request to update the tag used for the tagging.

    <tagging>
      <tag>
        <name>love</name> <!-- optional -->
      </tag>      
      <verses>
        <verse id="5" />
      </verses>
    </tagging>

## Delete

### DELETE /user/taggings/1.xml

Deletes the tagging identified by ID=1.

### DELETE /user/taggings/love.xml
                
You may also delete all of your tags for a give tag name by passing the name in the request URL.

*Please note:* The content-type header is not needed for DELETE requests, since you are not sending any XML to the ABS API.