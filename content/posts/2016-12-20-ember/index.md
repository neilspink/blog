---
title: "Speed Comparison: Ember.js Client & Server Heat Test"
date: 2016-12-20
draft: false
tags: [JavaScript, Ember.js, Node.js, Google Cloud, performance]
---

Back in late 2016 I wanted to get my hands dirty with **Ember.js** and modern JavaScript frameworks, so I started a small side project called **Speed Comparison**. The idea was simple: measure website performance and make it easy to compare results.  

I split the work into **eight weekly sprints** so I could learn by shipping something small each week. The project ended up with two main parts:  

- **Client (Ember.js):** a responsive UI for visualizing the speed scores  
- **Server (Node.js):** hosted on **Google Cloud**, collecting and serving the performance data  

### The API

The server exposed a small **REST API** for pulling site performance scores. I documented it with **Swagger (OpenAPI 2.0)** so it was easy to test and extend. Here’s a slice of the spec:

```yaml
swagger: '2.0'
info:
  title: cloude.ch pagespeed API
  description: Use to call Google Pagespeed Insights
  version: "1.0.0"
host: api.clouded.ch
basePath: /api
paths:
  /sites:
    get:
      summary: Pagespeed insight
      parameters:
        - name: url
          in: query
          required: true
          type: string
      responses:
        200:
          description: pagespeed 0 to 100
```

That endpoint would hit Google Pagespeed Insights, crunch the result, and return a number between 0 and 100. Nothing fancy, but it got the job done.

### Stack & Hosting

The client was pure **Ember.js** (my first project with it), deployed on **Firebase Hosting**. The backend was a lightweight **Node.js** app (also my first time using Node), running on **Google Cloud**. That setup gave me a good crash course in getting a front end and an API out into the wild, not just running locally. It was the first time I stitched together a full stack on Google platforms, and it felt pretty satisfying to see the pieces talk to each other.

### The Code

If you want to check it out:

- Client (Ember.js): [speed-comparison-client](https://github.com/neilspink/speed-comparison-client) 
- Server: [speed-comparison-server](https://github.com/neilspink/speed-comparison-server)
