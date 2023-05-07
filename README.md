# Overview
The icanhazdadjoke API endpoint enables you to reach a set of daily
jokes on the icahazdadjoke.com web page. With queries as part of the
Search function, you can use keywords to browse through a list of jokes.

This documentation includes three parts:
* an Overview of the icanhazdadjoke API endpoint
* a step-by-step tutorial for using the icahazdadjoke API endpoint, and
* the reference the OpenAPI specification for the icahazdadjoke API endpoint.

# Step-by-Step Tutorial

# OpenAPI specification the icanhazdadjoke search endpoint
The following contains the OpenAPI 3.1.0 endpoint documenation. The [APIMATIC SDK](https://www.apimatic.io/) generated the OpenAPI 3.1.0 documentation
in YAML format.

```json
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
                  example:
                    endpoints:
                    - url: https://a.nel.cloudflare.com/report/v3?s=fUpkuPKeZ4bMHMJmyDp%2FOZfopvt6S7BV7uDbWemuPqTQsbOCRcNu%2FoimSLldnHsemVqf3NSVEl3vQtuW86U%2BH%2FzM40xVnsnEUOaJy54fLpo9EWcNqaEIHqvsCVUAmAV%2FLnlCL34%3D
                    group: cf-nel
                    max_age: 604800
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
              example:
                current_page: 1
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



    
         





