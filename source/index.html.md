---
title: API Reference

# language_tabs: # must be one of https://git.io/vQNgJ
#   - shell
#   - ruby
#   - python
#   - javascript

toc_footers:
  - <a href='https://www.employher.com' target='_blank'>Powered by <span style='color:#ff0990'>employHER</span> ©</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the employHER API!

### API Endpoint
`https://api-xda.employher.com/api`

<!-- Sample Section Starts -->
# Authentication

## Login

> Response (Status 200)

```json
{
  "status": 200,
  "message": "Login successful",
  "data": {
    "token": "secret_token"
  }
}
```

This endpoint lets you login into the portal.

### HTTP Request

<span class="http-req"><span class="post-method">POST</span> /session/login</span>

### Parameters

Parameter | Type | Default | Description
--------- | ------- | ------- | -----------
email | string | - | Email address
password | string | - | Your secret password
<!-- Sample Section Ends -->

# Video Studio

## List all Videos

> Response (Status 200)

```json
{
  "status": 200,
  "message": "Success",
  "pagination": {
    "totalPages": 1,
    "pageRecords": 1,
    "page": 1,
    "pageSize": 20
  },
  "data": [
    {
      "id": 1,
      "title": "My First video",
      "description": "This video is about me talking about my recent project",
      "video_file": "path to video file",
      "created_at": "2021-07-11 19:43:00"
    },
    {...}
  ]
}
```

Retrieve all the video list of candidate.

### HTTP Request

<span class="http-req"><span class="get-method">GET</span> /video-studio</span>

### Parameters

Parameter | Type | Default | Description
--------- | ------- | ------- | -----------
page | integer | 1 | The page number to retrieve list
pageSize | integer | 20 | How many records per page

## Add/Create a new Video

> Response (Status 200)

```json
{
  "status": 200,
  "message": "Video submitted successfully"
}
```

This endpoint lets you add new video into video studio list.

### HTTP Request

<span class="http-req"><span class="post-method">POST</span> /video-studio</span>

### Parameters

Parameter | Type | Default | Description
--------- | ------- | ------- | -----------
title | string | - | Title of video
description | string | - | Video description
file | binary | - | Binary data of file
