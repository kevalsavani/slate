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

`POST /session/login`

### Parameters

Parameter | Type | Default | Description
--------- | ------- | ------- | -----------
email | string | - | Email address
password | string | - | Your secret password
