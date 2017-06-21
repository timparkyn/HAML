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
```  %head
    %title BoBlog
    %meta{"http-equiv" => "Content-Type", :content => "text/html; charset=utf-8"}
    %link{"rel" => "stylesheet", "href" => "main.css", "type" => "text/css"}
  %body
    #header
      %h1 BoBlog
      %h2 Bob's Blog
    #content
      - @entries.each do |entry|
        .entry
          %h3.title= entry.title
          %p.date= entry.posted.strftime("%A, %B %d, %Y")
          %p.body= entry.body ```
