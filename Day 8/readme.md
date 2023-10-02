# Day 8; Security

We can build apps! But people can steal our data :(

This session will cover security fundamentals and help you protect your projects!

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/1mITkYLOuPbeC6Pt63TuX2OJUUq9NPtGVBeeXVX9h7vw/edit?usp=sharing)

### Table of contents

- [Tweetdeck](#tweetdeck)
  - [Beautiful Soup 4](#beautiful-soup-4)
  - [More SQL](#more-sql)
  - [ORM’s](#orms)
  - [More advanced version of this attack](#more-advanced-version-of-this-attack)
  - [Repl.it](#replit)
  - [Diffie Hellman](#diffie-hellman)
  - [An example of CI/CD poisoning in practice](#an-example-of-cicd-poisoning-in-practice)
  - [Tools to do scanning](#tools-to-do-scanning)
  - [Recent example of session jacking](#recent-example-of-session-jacking)

### Tweetdeck

Tweetdeck was a platform for managing tweets. It had a vulnerability in it that allowed tweets to be treated as code. This meant users were exposed to anything possible in javascript when this vulnerability was discovered.

Details can be found here: [https://www.vox.com/2014/6/11/5800610/heres-how-that-major-tweetdeck-vulnerability-works](https://www.vox.com/2014/6/11/5800610/heres-how-that-major-tweetdeck-vulnerability-works)

### Beautiful Soup 4

Beautiful Soup 4 is a super handy package that lets us interact with, and find information from, web documents (like HTML) in our python code.

In the last slide we used it to compare tags in HTML code to a list of allowed tags, but it can also be used to scraping websites.

Knowing how tools like these can be used to scrape data can help you to make it easier (or more difficult) to scrape your own pages for data as well.

Learn more about bs4 [here](https://beautiful-soup-4.readthedocs.io/en/latest/).

### More SQL


We’re not going to cover SQL more, but this [site does a great job](https://www.w3schools.com/sql/)

Here are some good starting concepts:

-   How to [create tables](https://www.w3schools.com/sql/sql_create_table.asp)
-   The basic [Data types](https://www.w3schools.com/sql/sql_datatypes.asp)
-   How to [update rows](https://www.w3schools.com/sql/sql_update.asp)
-   How to [create new rows](https://www.w3schools.com/sql/sql_insert.asp)

### ORM’s

One way to combat **some** of these attacks is to use an ORM (object relational model).

This lets you access databases without SQL statements. 

But under the hood they still often use SQL, so you need to be careful no matter what you choose to do

### More advanced version of this attack

Here are some great videos that walk through more advanced versions of file-based attacks:

-   [https://www.youtube.com/watch?v=xZd1JWmLGLk](https://www.youtube.com/watch?v=xZd1JWmLGLk)
-   [https://www.youtube.com/watch?v=Ry_yb5Oipq0](https://www.youtube.com/watch?v=Ry_yb5Oipq0)

### Repl.it

A real world example of remote code execution (the concept, not the attack) is [repl.it](https://replit.com/), the site lets you spin up instances of programming languages, and run your code on their servers.

### Diffie Hellman

Here is an example of one of these public key systems

[https://github.com/descent098/diffie-hellman](https://github.com/descent098/diffie-hellman)

### An example of CI/CD poisoning in practice

The video below walks you through an example of doing this sort of thing

[Hacking CI/CD (Basic Pipeline Poisoning) - YouTube](https://www.youtube.com/watch?v=fcibOy-zoN8)

### Tools to do scanning

There are several good tools to do this. You can also add these to CI/CD pipelines in order to automatically check for vulnerabilities on an ongoing basis

-   [DeepSource: The Code Health Platform](https://deepsource.io/)
-   [Snyk | Developer security | Develop fast. Stay secure. | Snyk](https://snyk.io/)

### Recent example of session jacking

Great breakdown from hussein Nasser of a recent attack:

[https://www.youtube.com/watch?v=ASfMqrE0ISg](https://www.youtube.com/watch?v=ASfMqrE0ISg)
