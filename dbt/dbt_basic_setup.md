---
title: Basic Setup for DBT
layout: default
parent: DBT For Beginners
---

When I started in DBT, I was intimiated with all the features - sources, tests, models, connections, jinja, and what not.

But now i setup DBT projects in couple of hours. In the simplest cases, I use DBT just to schedule queries in an order. Nothing more.

To do this, 
- simply create a DBT account
- connect it to your database with a service account and a JSON key
- select 'managed' for repository
- In Develop IDE, paste your query and save it as 'table_name.sql' in the models folder
- Go to Deploy
- Create an environment for production
- Create a job, run it.
- If it works, schedule it.

That's it, you are done.
