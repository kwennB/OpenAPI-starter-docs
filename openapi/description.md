# Overview

The Random API provides a free service to generate random user data for application testing.  (check other docs and get ideas to add)

Software teams test better with the Random API 
Deliver numerous data about a random user that cuts across all teams from the name, gender, location, timezone,  and more.

With random user data crafted for diverse use cases, you can test better with ready-made user data across your project. 

## Who is the Random User API for

The audience for https://randomuser.me/ is developers, data analysts, and researchers who need a quick and easy way to generate realistic mock user data for their applications or studies. This API generates random user profiles with diverse personal information, including name, gender, location, email address, and profile picture. It may also apply to UI/UX designers for placeholder data in designing user interfaces.

# Getting Started 

## Base URL

https://randomuser.me/   


## Using Code
You can call the Random API using various programming languages which include;

### JavaScript (jQuery)
```
var settings = {
  "url": "https://randomuser.me/api/",
  "method": "GET",
  "timeout": 0,
};


$.ajax(settings).done(function (response) {
  console.log(response);
});
```



### JavaScript (fetch)
```
var requestOptions = {
  method: 'GET',
  redirect: 'follow'
};


fetch("https://randomuser.me/api/", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```


### Python (request)
```
import requests


url = "https://randomuser.me/api/"


payload={}
headers = {}


response = requests.request("GET", url, headers=headers, data=payload)


print(response.text)
```


### Node JS (axios)
```
var axios = require('axios');


var config = {
  method: 'get',
maxBodyLength: Infinity,
  url: 'https://randomuser.me/api/',
  headers: { }
};


axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});
```

### PHP  
```
<?php


$curl = curl_init();


curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://randomuser.me/api/',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'GET',
));


$response = curl_exec($curl);


curl_close($curl);
echo $response;
```


### Ruby
```
require "uri"
require "net/http"


url = URI("https://randomuser.me/api/")


https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true


request = Net::HTTP::Get.new(url)


response = https.request(request)
puts response.read_body
```



# Authentication

Authorization (authentication) is not required to use the Random API; only GET requests are allowed now. 


# Error Handling

In the event that an error occurs, the API will return a JSON response with an "error" field containing a description of the error. The HTTP status code will also indicate the type of error.

## HTTP and Error Codes

The Random API returns HTTP status code and error code messages.


| HTTP Code     | Message | Description |
| -------- | --------| --------------- |
| 200  | OK    | The request was successful |
| 400 | Bad Request     | The request was invalid or missing a required parameter.|
| 404    | Not Found    |  The requested resource not found.|
|500     | Internal Server Error | An error occurred on the server |



# API Reference

## List and explanation of the flags

The Random User Generator API (https://randomuser.me/) is a free, open-source API that provides randomly generated user data. Here are the flags you can use with the API:

**gender**

You can define the gender of the user you want to generate with this flag. To get users of any gender, you can set this flag to male, female, or random (the default).

**seed**

This flag allows you to specify a seed value for the random number generator. Using a specific seed value ensures that you get the same set of users each time you request that seed value. It is very functional if you intend to generate the same kinds of users multiple times.

**nat**

This flag allows you to specify the nationality of the user you want to generate. You can set this flag to a two-letter country code (e.g., us for the United States, GB for Great Britain) to get users from a specific country. You get users from diverse nationalities if you don't give value to this flag.

**inc**

This flag specifies the user data fields you want to include in the response. You can set this flag to a comma-separated list of field names to include only those fields in the response. For example, inc=name,email would add only the name and email fields in the response.

**exc** 

This flag specifies the user data fields you want to exclude from the response. You can set this flag to a comma-separated list of field names to exclude those fields from the result. For example, exc=login,id would exclude the login and id fields from the response.

**results**

This flag specifies the amount users to generate in a single request. You can set this flag to any number between 1 and 5000 (the default is 1). 

**page**

This flag specifies which page of results to return. You can set this flag to any positive integer (default is 1) for a specific page. (It is very functional if you want to retrieve large numbers of users in multiple requests.)

These flags provide flexibility in generating random user data and customizing the response to meet specific requirements.


# Usage Limits


# Examples


# Support

If you encounter any errors when using the API, please reach us at support@randomuser.me with the error details, including the HTTP status code and error message. We'll do our best to resolve the issue as quickly as possible.

# Issues

* The endpoint is just one - /api
* The reason we can’t precisely specify the exact location when calling the API is that the data of users are random - so you will always get a random location regardless of the one you specify.
The only parameters you can correctly get is the (/gender and nationality (/nat) parameters)





