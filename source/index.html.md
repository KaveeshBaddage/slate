---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/KaveeshBaddage/Tesseract-Web-App-Java-Backend'>Project Repository</a>


search: true
---

# Introduction

`Tesseract` is an open source text recognizer (OCR) Engine, available under the Apache 2.0 license. It can be used directly, or (for programmers) using an API to extract printed text from images. It supports a wide variety of languages.

`Tesseract OCR` is a Java web application which is implemented using Tesseract OCR Engine. It helps to convert

  - Images of typed text
  - Images of handwritten text  
  - Images of printed text into 
  
  a machine-encoded text. This web application uses Tesseract OCR Engine to do this conversion. 
  
  
  Its Java Backend exposes two REST API endpoints to access its functionality.

# Authentication

<aside class="success">
 Currently, this web application is in its initail state. So you don't need to do authentication to access its endpoints.
</aside>


# Extract What You Want

## Extract English text from an image

You can attach an image as a request body parameter and sent it to the backend to extract its text in English 

```shell
curl --location --request POST 'http://localhost:8090/getEnglishText' \
--form 'file=@<fileLocation>'
```


> The above cURL command will returns extracted text from given image in English.


### HTTP Request

`POST http://localhost:8090/getEnglishText`

### Request Body Parameters

Parameter |  Description
--------- |  -----------
file | Selected image file to extract the text

### Response

This HTTP request gives its response in text/plain format. 

<aside class="warning">Response content may include error messages which returns from Tesseract OCR Engine with extracted text. <br/>
Eg - Warning. Invalid resolution 0 dpi. Using 70 instead.
Estimating resolution as 297
</aside>


## Extract Sinhala text from an image

You can attach an image as a request body parameter and sent it to the backend to extract its text in Sinhala. 

```shell
curl --location --request POST 'http://localhost:8090/getSinhalaText' \
--form 'file=@<fileLocation>'
```


> The above cURL command will returns extracted text from given image in Sinhala.


### HTTP Request

`POST http://localhost:8090/getSinhalaText`

### Request Body Parameters

Parameter |  Description
--------- |  -----------
file | Selected image file to extract the text

### Response

This HTTP request gives its response in text/plain format. 

<aside class="warning">Response content may include error messages which returns from Tesseract OCR Engine with extracted text. <br/>
Eg - Warning. Invalid resolution 0 dpi. Using 70 instead.
Estimating resolution as 297
</aside>


<aside class="notice">
That is all about...!
</aside>


