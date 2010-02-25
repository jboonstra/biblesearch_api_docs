---
layout: default
title: Notes
---

# Notes

Notes are annotations you apply to selected Bible verses.  Notes belong to users.  All notes retrieved via API will also include the verse references to which they refer.

## List

### GET /user/notes.xml

Returns all of your notes.

## Show

### GET /notes/1.xml

Returns your note identified by ID=1.  

## Create

### POST /notes.xml

Creates a note resource for the verse reference you pass to it in the body of your XML request.

The verse references must have both a start and an end node, each representing a verse id marking the start and end of the passage you would like to tag.  To tag a single verse, submit the same verse id as both the start and end values.

    <notes>
      <note>
        <title>Some Title</title>
        <content>Some body text.</content>
        <references>
          <reference>
            <start>GCEVNU:Acts.8.34</start>
            <end>GCEVNU:Acts.8.36</end>
          </reference>
        </references>
      </note>
    </notes>

## Update

### PUT /notes/1.xml

Updates the note identified by ID=1 with content of the submitted XML.

    <notes>
      <note>
        <title>New Title</title>
        <content>New body text.</content>
        <references>
          <reference>
            <start>GCEVNU:Acts.8.34</start>
            <end>GCEVNU:Acts.8.36</end>
          </reference>
        </references>
      </note>
    </notes>

## Delete

### DELETE /notes/1.xml

Deletes the note identified by ID=1.

*Please note:* The content-type header is not needed for DELETE requests, since you are not sending any XML to the ABS API.