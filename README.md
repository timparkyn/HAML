# HAML ===>> HTML Abstraction Markup Language

HAML is a templating language used with Rails. 
Essentially, it's a series of abbrevations that convert to HTML tags


Benefits of HAML
* User-friendly markup
* DRYer code
* Cleanly rendered HTML, with proper indentation
* easier to read?

View pages can be quickly changed HAML by changing the extention from .erb to .haml


Criticisms of HAML
* harder to read?
* pages can break if indentation and tabbing not followed consistently

Some code examples
```  
%head
    %title r-Blog
    %meta{"http-equiv" => "Content-Type", :content => "text/html; charset=utf-8"}
    %link{"rel" => "stylesheet", "href" => "main.css", "type" => "text/css"}
%body
#header
  %h1 Some good stuff
  %h2 And some even better stuff
#content
  - @posts.each do |entry|
    .post
      %h3.title= post.title
      %p.body= post.body 
      %p.date= post.created_at.strftime("%A, %B %d, %Y")
```

Converts to:

  ```<head>
    <title>r-Blog</title>
    <meta content='text/html; charset=utf-8' http-equiv='Content-Type' />
    <link href="/stylesheets/main.css" media="screen" rel="Stylesheet" type="text/css" />
  </head>
  <body>
    <div id='header'>
      <h1>Some good stuff</h1>
      <h2>And some even better stuff</h2>
    </div>
    <div id='content'>
      <div class='post'>
        <h3 class='title'>Such a great post</h3>
        <p class='body'>You're going to love this post. It's a terriffic post. A wonderful post. You're going lto love this post so much you'll be tired of posting
        </p>
        <p class='date'>Monday, June 19th, 2017</p>    
      </div>
```
