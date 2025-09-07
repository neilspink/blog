+++
date = '2019-12-31'
draft = false
title = 'Map the metadata of your YAML'
description = 'This explains admonition shortcode implementation'
+++
# Have you ever had 1000+ YAML files and needed to know the common data structure?

## yaml-dredger

I thought it would be useful to analyze the structure of YAML files at scale.

YAML gets used for everything — APIs, configurations, Kubernetes, data specs — and often no one really knows what's in the files. This script crawls a folder of YAML and gives you a kind of map: what entities exist, what fields they have, and where they show up.

It's not pretty — but it works. And it’s fast enough for real datasets.

## Why I Built It

Back in 2001 at Swiss Re, I helped build a large reporting system on DB2. We relied heavily on metadata — not just to document views but to generate and trace them. That stuck with me.

Years later, while exploring Alibaba Cloud, I entered their **[Cricket, Wickets and Big Data](https://www.alibabacloud.com/blog/cricket-wickets-and-big-data_595336)** challenge. The contest involved analyzing over 1,400 international cricket matches using Alibaba’s big data tools. After completing the Big Data learning path, I was handed the dataset — mostly raw YAML.

This tool helped me break that down. I wanted to know: What entities exist? What the attributes are? Which files contain what?

The project is done in JavaScript, source code available on [Github](https://github.com/neilspink/yaml-dredger).
