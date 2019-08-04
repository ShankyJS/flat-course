# flat-course
Public work on Flatiron School Bootcamp

# Getting Started with HTML

HTML is the "language" of the web, so as a user of the web, it's the language we have spent the majority of my time. 

## Anatomy of an HTML tag

The fundamental building block of HTML is a tag. 
Tags allows developers to tell things to the browser like "this text have to be a header and include an image". 

Tags all follow the same formate like this: 

```
<tag-text>
<br> #Create a new line. 
```
Most HTML tags work just like this:


[X]Opening tag, which states what kind of tag we’re using;
[Y]The text we want the tag to be applied to;
[Z]Closing tag, which makes sure the tag is limited to a certain piece of text.

## Basic HTML Document Structure.

```
<html> 
 <head>
 </head>
 <body>
   <h1>Profile</h1>
     Hello my name is Jhan.
   <br>
   <p>
     I've studying at The Flatiroon School for 1 hour. Be a good DevOps is my dream but I also want to be a Fullstack
     developer in Future. 
   </p>
 </body>
</html>
```

## Some useful resources
https://www.htmldog.com/references/html/tags/
https://developer.mozilla.org/en-US/docs/Web/HTML/Element

In this topic we cover the _img_ tag and the tags attributes. 

## Some useful resources for images
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img

# Undestanding Links in HTML
In HTML Links allows to connect our websites and pages to each other. They give the world wide web its power by simply allowing one document to lead to the next other.

```
<a href="http://example.com">
  <img src="myimage.jpg" alt="Alternate text">
</a>

This tells to your mail application to open.
<a href="mailto:webmaster@example.com">This is an email link</a>

<p id="tips">Useful Tips Section</p>
<a href="#tips">Jump to Useful Tips Section</a>

This tells to your phone that you can dial this num.
<a href="tel:555-555-5555">This is a phone number link</a>
```

## Relative and Absolute file paths.

There are to ways to express where we want to got. We can use either a relative file path or an absolute file path. 

## Relative 
```
about.html
```
Relative paths describe the location of resources whitin the same file system.

## Absolute

```
http://example.com/about.html
```
Absolute paths describe the location of resources on the entire internet at large. 

You should use the relative path when linking to content whitin your own website. Then use absolute paths when linking to content on other remote websites. 

## Sumary 

We can link to other pages either on our own website or on the internet as a whole by using the ```a``` tag and a ```href``` attribute, which specifies where we want the link to go. We use either a relative or absolute file path to determinate the link destination. 


