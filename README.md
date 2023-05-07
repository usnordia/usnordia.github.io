# Overview
The icahazdadjoke API endpoint enables you to reach a set of daily
jokes on the icahazdadjoke.com web page. With queries as part of the
Search function, you can use keywords to browse through a list of jokes.

This documentation includes three parts:
* an Overview of the icahazdadjoke API endpoint
* the OpenAPI specification for the API endpoint, and
* a step-by-step tutorial for using the API endpoint.

single page overview that outlines the concepts and
functionality of the API

# OpenAPI specification for the search endpoint

# Step-by-Step tutorial for using the API endpoint
The language of choice is the ReST Console plugin (link) intstalled
within the
Intellij IDE (link).

500-1000 word step-by-step tutorial for using the API endpoint
using the programming
language of your choice.

The ReST Console is an HTTP Client in IntelliJ IDEA for
RESTful Web Services.
## How to Install the ReST Console
The easiest way to install Ruby and Jekyll is by using the RubyInstaller for Windows.
https://jekyllrb.com/docs/installation/windows/
https://rubyinstaller.org/downloads/

# Example Response Body

```json

{
  "current_page": 1,
  "limit": 20,
  "next_page": 1,
  "previous_page": 1,
  "results": [
    {
      "id": "0DdaxAX0orc",
      "joke": "I accidentally took my cats meds last night. Don’t ask meow."
    },
    {
      "id": "BQfaxsHBsrc",
      "joke": "What do you call a pile of cats?  A Meowtain."
    }
  ],
  "search_term": "meow",
  "status": 200,
  "total_jokes": 2,
  "total_pages": 1
}

```




