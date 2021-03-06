---
title: SpotSkim API Reference

language_tabs:
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - authentication
  - user
  - location
  - asset
  - versioning
  - errors

search: true
---
# Introduction
All SpotSkim APIs return JSON data objects for developers to parse. This is the preferred encoding and decoding method supported. Unless otherwise specified the `content-type` must be set to `application/json`

SpotSkim currently supports two types of APIs. They are tailored for the following use cases

###[Web API](#web-api)
Typical users of this API would be partners that are integrating with SpotSkim from their own portals. Functionality such as "Add a Location", or "Add a User" are supported. Eventual goal of this API is to provide our partners all the API functionality that is used by SpotSkim Portal to build a custom portal if they so choose.  

###[Phone API](#phone-api)
Typical users of this API, are partners that are trying to support SpotSkim on devices that are not supported out of the box. For example, you could be writing custom software to support Windows CE Devices in stores. 
This API is exactly the same API that is used by the SpotSkim Application, so any future changes will be documented and available to our partners as well

Most of the functionality supported by the APIs are authenticated. You will need to either perform `Login` using the API itself and store the token, or alternatively use your console to [obtain the API token](#obtaining-tokens)

If a call is authenticated, you must make sure to set the `Authorization` header to `ApiKey user@spotskim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8`

More generically the Authorization header must have the format 
`ApiKey (space)username:(colon)API-key`
