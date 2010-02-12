---
layout: default
title: Notes
---

# Notes

Notes are annotations you apply to selected Bible verses.  Notes belong to users.  All notes retrieved via API will also include the verses to which they refer.

## List

### GET /user/notes.xml

Returns all of your notes.

## Show

### GET /notes/1.xml

Returns your note identified by ID=1.  

## Create

### POST /notes.xml

Creates a note resource for the verse(s) you pass to it in the body of your XML request.

    <notes>
      <note>
        <title>Some Title</title>
        <body>Some body text.</body>
        <verses>
          <verse id="1" />
          <verse id="3" />
          <verse id="5" />
        </verses>
      </note>
    </notes>

## Update

### PUT /notes/1.xml

Updates the note identified by ID=1 with content of the submitted XML.

    <notes>
      <note>
        <title>New Title</title>
        <body>New body text.</body>
        <verses>
          <verse id="1" />
          <verse id="3" />
          <verse id="4" /> 
        </verses>
      </note>
    </notes>

## Delete

### DELETE /notes/1.xml

Deletes the note identified by ID=1.

*Please note:* The content-type header is not needed for DELETE requests, since you are not sending any XML to the ABS API.