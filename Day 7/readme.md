# Day 7; Intro to backend and API's

Now we know how HTTP works, and how to host sites it's time to look at creating more in-depth backends. In this session we will get more specific with HTTP and look at examples of using it. Additionally we will look at creating and consuming API's which will make communicating between sites possible!

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/11rxddvSzH_xCEhj9S1IA2prXLg6NhsA4w37Ex4I_UmI/edit?usp=sharing)

### Table of contents

- [HTTP requests/responses](#http-requestsresponses)
    - [Request](#request)
    - [Post example](#post-example)
    - [JSON Post example](#json-post-example)
    - [Responses](#responses)
    - [HTML example](#html-example)
    - [JSON example](#json-example)
        - [Error Example](#error-example)
        - [Error example w/html](#error-example-whtml)
- [HTTPIE](#httpie)
- [Pages on pages on pages](#pages-on-pages-on-pages)
- [How you should probably do this (multiple fetches)](#how-you-should-probably-do-this-multiple-fetches)
- [Ezcv flask integration](#ezcv-flask-integration)


### HTTP requests/responses

#### Request

A header at the end of the day is just text, and it looks like this:

```http
GET /beginner HTTP/1.1
Host: schulichignite.com
```

The first thing is the method, then the slug, then the HTTP version, then the host, then all the other header info


##### Post example

When sending data via a POST request, you also have a body, here’s an example of a form submission

```http
POST /form HTTP/1.1
Host: example.com
Content-Type: application/x-www-form-urlencoded
Content-Length: <needs to be calculated>

name=kieran&age=24
```

*The Content-Type is a [MIME type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)

##### JSON Post example

When sending data via a POST request, you also have a body, here’s an example of a JSON body

```http
	POST /calgary HTTP/1.1
	Host: weather.com
	Content-Type: application/json
	Content-Length: <needs to be calculated>

	{“date”:”11/29/2022”}
```

*The Content-Type is a [MIME type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)

#### Responses

##### HTML example

The first line is the status code, and status message. Then come the response headers, then the response body after 1 line of nothing!

```http
200 OK
Date: Tue, 29 Nov 2022 20:34:20 GMT
Content-Type: text/html; charset=utf-8
Server: cloudflare

<!doctype html><html><head></head><body><h1>Hello World</h1></body></html>
```

##### JSON example

Basically the same as the HTML example, except a different MIME type

```
200 OK
Date: Tue, 29 Nov 2022 20:34:20 GMT
Content-Type: text/json; charset=utf-8
Server: cloudflare

{"name":"kieran", "age":24}
```

###### Error Example

Error states 400-599, will often have no response body. They can sometimes have pages to handle errors that are HTML pages, but not always

```http
404 Not Found
Date: Tue, 29 Nov 2022 20:34:20 GMT
```

###### Error example w/html


Here’s an example with HTML


```http
404 Not Found
Date: Tue, 29 Nov 2022 20:34:20 GMT
Content-Type: text/html; charset=utf-8
Server: cloudflare

<!doctype html><html><head></head><body><h1>She's broken bud :(</h1></body></html>
```

### HTTPIE

[HTTPie](https://httpie.io/) is a great testing tool for creating HTML requests and reading responses!


### Pages on pages on pages
Iframes create a WHOLE NEW DOCUMENT inside the current one. This document has all the same capabilities as a normal one.

A similar effect can be achieved with this JS

```javascript
html = "<head></head><body><p id='text'>Hello!</p></body>"
parser = new DOMParser(); // Parses HTML
doc = parser.parseFromString(html, 'text/html');

// Use the document and parse it like we normally do in JS
text = doc.getElementByID("text")
console.log(text.innerHTML) // logs 'Hello!'
```

### How you should probably do this (multiple fetches)

This code will basically collect all of the requests together and parallelize them 

So now the alex request and megan request happen simultaneously instead of one after the other!

```javascript
users = [] // Initialize empty array

// Get the promise from the initial requests
const alexRequest = fetch(`https://kieranwood.ca/session-8-api/json/users/alex.json`
    ).then((response) => 
    response.json()
)

const meganRequest = fetch(`https://kieranwood.ca/session-8-api/json/users/megan.json`
    ).then(
        (response) => response.json()
)

// Process promises asynchronously
users = await Promise.all([alexRequest, meganRequest])

console.log(users)
```

### Ezcv flask integration
You can initialize ezcv to where ezcv generates the HTML and then flask serves it. You can do this by

```bash
ezcv init <name> --flask
```


