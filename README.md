# Overview
The icanhazdadjoke API endpoint enables you to reach a set of daily
jokes on the icahazdadjoke.com web page. With queries as part of the
Search function, you can use keywords to browse through a list of jokes.

This documentation includes three parts:
* an Overview of the icanhazdadjoke API endpoint
* a step-by-step tutorial for using the icanhazdadjoke API endpoint, and
* the reference the OpenAPI specification for the icanhazdadjoke API endpoint.

# Step-by-Step Tutorial
You can use the icanhazdadjoke API with the command line or with an API platform, for example, Postman. This section explains both methods.
## API Structure
### Method
GET 
### Request Headers
* Accept - application/json
* User-Agent: ILF Test (https://github.com/username/repo)
## cURL Command
```
curl [options] [URL...]
```
* URL -  https://icanhazdadjoke.com/search
### Query Parameters
* **term** - the keyword to do a search on the array of jokes.
* **limit** - the maximum number of jokes shown per page.
* **page** - the current page number, e.g., 1, 2.

## Windows Command Line
1. Open a CMD Window.
2. Type the cURL command as follows.
```
curl -H "Accept: application/json" -H "User-Agent: ILF Test (https://github.com/username/repo" https://icanhazdadjoke.com/search
```
3. Observe the output as an aray of jokes per the ID (id) of each. There are 744 jokes and 38 pages.

```
{"current_page":1,"limit":20,"next_page":2,"previous_page":1,"results":[{"id":"0189hNRf2g","joke":"I'm tired of following my dreams. I'm just going to ask them where they are going and meet up with them later."},{"id":"08EQZ8EQukb","joke":"Did you hear about the guy whose whole left side was cut off? He's all right now."},{"id":"08xHQCdx5Ed","joke":"Why didn\u2019t the skeleton cross the road? Because he had no guts."},{"id":"0DQKB51oGlb","joke":"What did one nut say as he chased another nut?  I'm a cashew!"},{"id":"0DdFQZgyXnb","joke":"Where do fish keep their money? In the riverbank"},{"id":"0DdaxAX0orc","joke":"I accidentally took my cats meds last night. Don\u2019t ask meow."},{"id":"0DtrrOZDlyd","joke":"Chances are if you' ve seen one shopping center, you've seen a mall."},{"id":"0L6MexPukjb","joke":"Dermatologists are always in a hurry. They spend all day making rash decisions. "},{"id":"0LuXvkq4Muc","joke":"I knew I shouldn't steal a mixer from work, but it was a whisk I was willing to take."},{"id":"0gFdFBsWDd","joke":"I won an argument with a weather forecaster once. His logic was cloudy..."},{"id":"0ga2EdN7prc","joke":"How come the stadium got hot after the game? Because all of the fans left."},{"id":"0ga2wsPZgib","joke":"\"Why do seagulls fly over the ocean?\" \"Because if they flew over the bay, we'd call them bagels.\""},{"id":"0oO71TSv4Ed","joke":"Why was it called the dark ages? Because of all the knights. "},{"id":"0oz51ozk3ob","joke":"A steak pun is a rare medium well done."},{"id":"0ozAXv4Mmjb","joke":"Why did the tomato blush? Because it saw the salad dressing."},{"id":"0wcFBQfiGBd","joke":"Did you hear the joke about the wandering nun? She was a roman catholic."},{"id":"189xHQ7pOuc","joke":"What creature is smarter than a talking parrot? A spelling bee."},{"id":"18Elj3EIYvc","joke":"I'll tell you what often gets over looked... garden fences."},{"id":"18h3wcU8xAd","joke":"Why did the kid cross the playground? To get to the other slide."},{"id":"1DIRSfx51Dd","joke":"Why do birds fly south for the winter? Because it's too far to walk."}],"search_term":"","status":200,"total_jokes":744,"total_pages":38}
```
**Note**: You can use the -o option in the cURL command to put the output to a file for better formatting.
```
curl http://{one,two}.site.com -o "file_#1.txt"
```

### Example using cURL with the Term "Meow"
To get and then show all of the jokes with the keyword "meow" type the command that follows.
```
curl -H "Accept: application/json" -H "User-Agent: ILF Test (https://github.com/username/repo" https://icanhazdadjoke.com/search?term=meow
```
Example Output
```
{"current_page":1,"limit":20,"next_page":1,"previous_page":1,"results":[{"id":"0DdaxAX0orc","joke":"I accidentally took my cats meds last night. Don\u2019t ask meow."},{"id":"BQfaxsHBsrc","joke":"What do you call a pile of cats?  A Meowtain."}],"search_term":"meow","status":200,"total_jokes":2,"total_pages":1}
```

### Example using cURL with Two Query Parameters
Append this to the end of the cURL command:
```
?[param1]=value,[param2]=value
```
```
curl -H "Accept: application/json" -H "User-Agent: ILF Test (https://github.com/username/repo" https://icanhazdadjoke.com/search?limit=10,page=1
```
## IntelliJ IDE
You can set up the IntelliJ IDE with the [ReST Console plugin](https://plugins.jetbrains.com/plugin/8114-rest-console) to run the Request and get a Response (body).
1. Install the ReST Console Plugin.
2. Open the ReST Console.
3. For the **Method**, select GET.
4. In the **URL** box, enter "icanhazdadjoke.com/search".
5. In the **User-Agent** box, enter "https://github.com/username/repo".
6. For the **Content-Type** Header, select "appication/json".
7. For the **Accept Content-Type** Header, select "application/json".
8. In the **Query Parameters Area**, click the "+" sign and add "term" for the Key and "meow" for the Value (keyword).
9. Click the **SUBMIT** button to get a response.
10. Example response: see the next section, "Example Response Body".
11. Click **Response > Headers** to view the response header output as follows for example.
```
Date: Mon, 08 May 2023 12:04:45 GMT
Content-Type: application/json
Transfer-Encoding: chunked
Connection: keep-alive
access-control-allow-headers: User-Agent, Content-Type
access-control-allow-methods: GET
access-control-allow-origin: *
access-control-max-age: 86400
access-control-request-method: GET
Cache-Control: max-age=0, must-revalidate, no-cache, no-store, public, s-maxage=0
retry-after: 60
x-frame-options: DENY
x-ratelimit-limit: 100
x-ratelimit-remaining: 99
x-ratelimit-reset: 1683547546
x-xss-protection: 1; mode=block
CF-Cache-Status: DYNAMIC
Report-To: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v3?s=fQKk5x5uLlhWAiJYfxTrlk038ef9P4bV1%2F0eeHCKIp%2BaZILZu5n%2BI1IASJGgPzUAJ0E5RTCbw172O8YbztFvp4oNn4lq1nSWoI3sZpUptMEr5eHubETOXN4urPg25Y1KpuVBios%3D"}],"group":"cf-nel","max_age":604800}
NEL: {"success_fraction":0,"report_to":"cf-nel","max_age":604800}
Strict-Transport-Security: max-age=15552000; includeSubDomains
X-Content-Type-Options: nosniff
Server: cloudflare
CF-RAY: 7c4191296c85457c-ATL
alt-svc: h3=":443"; ma=86400, h3-29=":443"; ma=86400
OkHttp-Sent-Millis: 1683547486622
OkHttp-Received-Millis: 1683547486678
```

### Example Reponse Body
```
{
  "current_page": 1,
  "limit": 30,
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



# OpenAPI Specification
The following contains the OpenAPI 3.1.0 endpoint documenation. The [APIMATIC SDK](https://www.apimatic.io/) generated the OpenAPI 3.1.0 documentation
in YAML format.

```
openapi: 3.1.0
info:
  title: ICANHAZDADJOKE
  contact: {}
  version: '1.0'
jsonSchemaDialect: https://json-schema.org/draft/2020-12/schema
servers:
- url: https://icanhazdadjoke.com
  variables: {}
paths:
  /search:
    get:
      tags:
      - Misc
      summary: GetNewRequest
      description: New Request
      operationId: GetNewRequest
      parameters:
      - name: Accept
        in: header
        description: ''
        required: true
        style: simple
        schema:
          type: string
          examples:
          - application/json
      - name: term
        in: query
        description: meow
        required: true
        style: form
        explode: true
        schema:
          type: string
      - name: User-Agent
        in: header
        description: ''
        required: true
        style: simple
        schema:
          type: string
          examples:
          - ILF Test (https://github.com/username/repo
      responses:
        default:
          description: ''
          headers: {}
          content: {}
        '200':
          description: OK
          headers:
            Date:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - Sun, 07 May 2023 20:18:57 GMT
                    contentMediaType: text/plain
                  example: Sun, 07 May 2023 20:18:57 GMT
            Transfer-Encoding:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - chunked
                    contentMediaType: text/plain
                  example: chunked
            Connection:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - keep-alive
                    contentMediaType: text/plain
                  example: keep-alive
            access-control-allow-headers:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - User-Agent, Content-Type
                    contentMediaType: text/plain
                  example: User-Agent, Content-Type
            access-control-allow-methods:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - GET
                    contentMediaType: text/plain
                  example: GET
            access-control-allow-origin:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '*'
                    contentMediaType: text/plain
                  example: '*'
            access-control-max-age:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '86400'
                    contentMediaType: text/plain
                  example: '86400'
            access-control-request-method:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - GET
                    contentMediaType: text/plain
                  example: GET
            Cache-Control:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - max-age=0, must-revalidate, no-cache, no-store, public, s-maxage=0
                    contentMediaType: text/plain
                  example: max-age=0, must-revalidate, no-cache, no-store, public, s-maxage=0
            retry-after:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '60'
                    contentMediaType: text/plain
                  example: '60'
            x-frame-options:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - DENY
                    contentMediaType: text/plain
                  example: DENY
            x-ratelimit-limit:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '100'
                    contentMediaType: text/plain
                  example: '100'
            x-ratelimit-remaining:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '99'
                    contentMediaType: text/plain
                  example: '99'
            x-ratelimit-reset:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - '1683490798'
                    contentMediaType: text/plain
                  example: '1683490798'
            x-xss-protection:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - 1; mode=block
                    contentMediaType: text/plain
                  example: 1; mode=block
            CF-Cache-Status:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - DYNAMIC
                    contentMediaType: text/plain
                  example: DYNAMIC
            Report-To:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - endpoints:
                      - url: https://a.nel.cloudflare.com/report/v3?s=fUpkuPKeZ4bMHMJmyDp%2FOZfopvt6S7BV7uDbWemuPqTQsbOCRcNu%2FoimSLldnHsemVqf3NSVEl3vQtuW86U%2BH%2FzM40xVnsnEUOaJy54fLpo9EWcNqaEIHqvsCVUAmAV%2FLnlCL34%3D
                      group: cf-nel
                      max_age: 604800
                    contentMediaType: text/plain
            NEL:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - success_fraction: 0
                      report_to: cf-nel
                      max_age: 604800
                    contentMediaType: text/plain
                  example:
                    success_fraction: 0
                    report_to: cf-nel
                    max_age: 604800
            Strict-Transport-Security:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - max-age=15552000; includeSubDomains
                    contentMediaType: text/plain
                  example: max-age=15552000; includeSubDomains
            X-Content-Type-Options:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - nosniff
                    contentMediaType: text/plain
                  example: nosniff
            Server:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - cloudflare
                    contentMediaType: text/plain
                  example: cloudflare
            CF-RAY:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - 7c3c27b4ca5e6fd9-IAD
                    contentMediaType: text/plain
                  example: 7c3c27b4ca5e6fd9-IAD
            Content-Encoding:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - br
                    contentMediaType: text/plain
                  example: br
            alt-svc:
              content:
                text/plain:
                  schema:
                    type: string
                    examples:
                    - h3=":443"; ma=86400, h3-29=":443"; ma=86400
                    contentMediaType: text/plain
                  example: h3=":443"; ma=86400, h3-29=":443"; ma=86400
          content:
            application/json:
              schema:
                allOf:
                - $ref: '#/components/schemas/NewRequest'
                - examples:
                  - current_page: 1
                    limit: 20
                    next_page: 2
                    previous_page: 1
                    results:
                    - id: 0189hNRf2g
                      joke: I'm tired of following my dreams. I'm just going to ask them where they are going and meet up with them later.
                    - id: 08EQZ8EQukb
                      joke: Did you hear about the guy whose whole left side was cut off? He's all right now.
                    - id: 08xHQCdx5Ed
                      joke: Why didn’t the skeleton cross the road? Because he had no guts.
                    - id: 0DQKB51oGlb
                      joke: What did one nut say as he chased another nut?  I'm a cashew!
                    - id: 0DdFQZgyXnb
                      joke: Where do fish keep their money? In the riverbank
                    - id: 0DdaxAX0orc
                      joke: I accidentally took my cats meds last night. Don’t ask meow.
                    - id: 0DtrrOZDlyd
                      joke: Chances are if you' ve seen one shopping center, you've seen a mall.
                    - id: 0L6MexPukjb
                      joke: 'Dermatologists are always in a hurry. They spend all day making rash decisions. '
                    - id: 0LuXvkq4Muc
                      joke: I knew I shouldn't steal a mixer from work, but it was a whisk I was willing to take.
                    - id: 0gFdFBsWDd
                      joke: I won an argument with a weather forecaster once. His logic was cloudy...
                    - id: 0ga2EdN7prc
                      joke: How come the stadium got hot after the game? Because all of the fans left.
                    - id: 0ga2wsPZgib
                      joke: "\"Why do seagulls fly over the ocean?\" \"Because if they flew over the bay, we'd call them bagels.\""
                    - id: 0oO71TSv4Ed
                      joke: 'Why was it called the dark ages? Because of all the knights. '
                    - id: 0oz51ozk3ob
                      joke: A steak pun is a rare medium well done.
                    - id: 0ozAXv4Mmjb
                      joke: Why did the tomato blush? Because it saw the salad dressing.
                    - id: 0wcFBQfiGBd
                      joke: Did you hear the joke about the wandering nun? She was a roman catholic.
                    - id: 189xHQ7pOuc
                      joke: What creature is smarter than a talking parrot? A spelling bee.
                    - id: 18Elj3EIYvc
                      joke: I'll tell you what often gets over looked... garden fences.
                    - id: 18h3wcU8xAd
                      joke: Why did the kid cross the playground? To get to the other slide.
                    - id: 1DIRSfx51Dd
                      joke: Why do birds fly south for the winter? Because it's too far to walk.
                    search_term: ''
                    status: 200
                    total_jokes: 744
                    total_pages: 38
                contentMediaType: application/json
      deprecated: false
      security: []
    parameters: []
components:
  schemas:
    NewRequest:
      title: NewRequest
      required:
      - current_page
      - limit
      - next_page
      - previous_page
      - results
      - search_term
      - status
      - total_jokes
      - total_pages
      type: object
      properties:
        current_page:
          type: integer
          contentEncoding: int32
        limit:
          type: integer
          contentEncoding: int32
        next_page:
          type: integer
          contentEncoding: int32
        previous_page:
          type: integer
          contentEncoding: int32
        results:
          type: array
          items:
            $ref: '#/components/schemas/Result'
          description: ''
        search_term:
          type: string
        status:
          type: integer
          contentEncoding: int32
        total_jokes:
          type: integer
          contentEncoding: int32
        total_pages:
          type: integer
          contentEncoding: int32
      examples:
      - current_page: 1
        limit: 20
        next_page: 2
        previous_page: 1
        results:
        - id: 0189hNRf2g
          joke: I'm tired of following my dreams. I'm just going to ask them where they are going and meet up with them later.
        - id: 08EQZ8EQukb
          joke: Did you hear about the guy whose whole left side was cut off? He's all right now.
        - id: 08xHQCdx5Ed
          joke: Why didn’t the skeleton cross the road? Because he had no guts.
        - id: 0DQKB51oGlb
          joke: What did one nut say as he chased another nut?  I'm a cashew!
        - id: 0DdFQZgyXnb
          joke: Where do fish keep their money? In the riverbank
        - id: 0DdaxAX0orc
          joke: I accidentally took my cats meds last night. Don’t ask meow.
        - id: 0DtrrOZDlyd
          joke: Chances are if you' ve seen one shopping center, you've seen a mall.
        - id: 0L6MexPukjb
          joke: 'Dermatologists are always in a hurry. They spend all day making rash decisions. '
        - id: 0LuXvkq4Muc
          joke: I knew I shouldn't steal a mixer from work, but it was a whisk I was willing to take.
        - id: 0gFdFBsWDd
          joke: I won an argument with a weather forecaster once. His logic was cloudy...
        - id: 0ga2EdN7prc
          joke: How come the stadium got hot after the game? Because all of the fans left.
        - id: 0ga2wsPZgib
          joke: "\"Why do seagulls fly over the ocean?\" \"Because if they flew over the bay, we'd call them bagels.\""
        - id: 0oO71TSv4Ed
          joke: 'Why was it called the dark ages? Because of all the knights. '
        - id: 0oz51ozk3ob
          joke: A steak pun is a rare medium well done.
        - id: 0ozAXv4Mmjb
          joke: Why did the tomato blush? Because it saw the salad dressing.
        - id: 0wcFBQfiGBd
          joke: Did you hear the joke about the wandering nun? She was a roman catholic.
        - id: 189xHQ7pOuc
          joke: What creature is smarter than a talking parrot? A spelling bee.
        - id: 18Elj3EIYvc
          joke: I'll tell you what often gets over looked... garden fences.
        - id: 18h3wcU8xAd
          joke: Why did the kid cross the playground? To get to the other slide.
        - id: 1DIRSfx51Dd
          joke: Why do birds fly south for the winter? Because it's too far to walk.
        search_term: ''
        status: 200
        total_jokes: 744
        total_pages: 38
    Result:
      title: Result
      required:
      - id
      - joke
      type: object
      properties:
        id:
          type: string
        joke:
          type: string
      examples:
      - id: 0189hNRf2g
        joke: I'm tired of following my dreams. I'm just going to ask them where they are going and meet up with them later.
tags:
- name: Misc
  description: ''
```



    
         





