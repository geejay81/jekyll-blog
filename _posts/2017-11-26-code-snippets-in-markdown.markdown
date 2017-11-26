---
layout: "post"
title: "Code Snippets in Markdown"
date: "2017-11-26 19:54:00"
categories: Jekyll Markdown
---

As I'm just getting started with Jekyll, I'm looking in to the different things you can do, and thought it would be worth sharing what I have learnt. To start with, I am testing the markdown in the posts. Here is an example of embedding code samples in the blog - this shows the CLI snippet required to create a new Jekyll site once Jekyll has been installed:

```
jekyll new my-blog-name
```

In order to embed code snippets, you can enter three back ticks (`) above and below your code snippet.

````
```
jekyll new my-blog-name
```
````
> *Tip:* You may have noticed that above I have included the back ticks with in the code block - so it has nested back ticks. How can we prevent the nested backticks from closing the code block?
> This was acheived by opening and closing the code block with 4 back ticks instead of 3.

## Code Formatting
It is also possible to show colouring and formatting for specific programming languages by including a reference to the language after the opening 3 back ticks:

````
``` javascript
var el = document.getElementById('element');
```
````

This will render with language formatting and colours, as shown below:

``` javascript
var el = document.getElementById('element');
```
