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

# CSS

Cascade Style Sheets is broken down in to sections, first we have to tell the browser what we want to change. Then we tell the browser how we want that thing changed.

Example 

```
body{
  color: red;
  font-weight: bold;
}
```

If we break that down a bit the word body is telling CSS what to change. 
The color:red; is telling CSS how to change that. In addition to the how and the want, we have some syntax requirements as well. Let's add in another change to the body. Change the code in the CSS tab to say. 

## Selecting elements

If we wanted only our header to be red, but the rest of the body to be black all to do is change the "what" in our CSS. So we need to change the "body" to H1.

```
h1 { 
  color: red;
}

p {
  font-weight: bold;
}
```

If you want to customize some texts you can also use the "id" selector to just change some items. 

## Deep on CSS Selectors

1. Review Type Selector
2. Review Class Selector
3. Review ID Selector
4. Review Compound Selector
5. Review Descendent Selector
6. Review Child
7. Review Adjacent Sibling
8. Review General Sibling 
9. Review Universal
10. Review Attribute Selectors
11. Review Pseudo Selectors 

### Selectors

CSS gives us variety of ways to select different elements and style with them.  

#### 1) Select by Type
This selects an specific element selected with his element name.

```
p {
  color: red;
}
```

#### 2) Select by Class
This selects an element matching class attribute name. This selector indicated by the preceeding . dot (period)

```
.container {
  font-weight: bold;
}
```

Additionaly you can apply a class name to as many elements as you like across any pages in your website. This is a good selector for Sprinkling the same style to many different elements. 

You can also apply more than one class to the same element. For example, let's apply two classes to the same paragraph. 


```
<span class="thick alert"> Warning... </p>
```

```
.thick{
  font-weight: bold;
}

.alert {color: red;}

```

#### 3) Select by ID

This selects an element with matching id attribute name. This selector is indicated by the preceeding hashtag symbol.

```
<div id="box"> I'm a cajita :v </div>
```
```
#box {
  background: blue;
}
```

A single Id name should only be applied to one element per page. 

#### 4) Compound

This selects all matched elements in the compound set. This selector is indicated by a "," separating the selectos of the set. Each element within the comma separated list will be styled the same.

```
<h1>Heading</h1>
<h2>Subheading</h2>
<div id="box"> I'm a box </div>
```

```
h1, h2, #box { 
  font-family: Arial, Helvetica, sans-serif;
}
```

#### 5) Descendent

This selects an element that is nested inside of a specific parent element. This selector is indicated by a "space" keyboard between the parent and the child to be selected. 

```
<ul id="nav">
  <li>Child</li>
</ul>
```

```
#nav li{ 
  background: blue; 
}
```

#### 6) Child

This selects an element that is nested only one level deep inside of the specified parent element. It only selects direct children and not grandchildren. This selector is indicated by a > (greater than) symbol between the parent and the child to be selected.

```
<ul id="list">
  <li>child</li>
  <li>child
    <ul>
      <li>grand child</li>
    </ul>
  </li>
</ul>
```

```
#list > li {
  border: 1px solid black;
}
```

#### 7) Adjacent Sibling

This selects an element that appears directly after the former element assuming they are both siblings (in the same level of nesting, in the same parent). 
This selector is indicated by a + symbol between the former sibling and the selected element that follows.

```
<h3>Heading</h3>
  <p>
    I'm a paragraph that is selected Because I come directly after an H3.
  </p>
  <p>
    I'm not selected ;(
  </p>
```

```
h3 + p {
  color: green;
}
```

#### 8) General Sibling 

This selects all elements that appear directly after the former element. This selector is indicated by a ~ tilde symbol between the former sibling and the selected element that follows it.

```
<h2>Sub Heading</h2>
  <p>
    I'm selected because I appear after an h2.
  </p>
  <p>
    I'm also selected for the same reason, in fact any paragraphs on the rest of the page after the h2 I will be selected. :) 
  </p>
```

```
h2 ~ p {
  color: black;
}
```

#### 9) Universal

This selects elements where the properties specified have not been styled by any other selectors. This selector is indicated by an * asterik symbol. 

``` 
* {
  color: orange;
}
```
```
<h5> I was selected because I haven't specified a color style for h5 anywhere else yet on our CSS so they will get the color orange now being covered under the universal selector. 
```

#### 10) Attribute  

This selects an element with a matching attribute value. This selector is indicated by square brackets : [], followed by the attribute property and value of the selected element within the brackets. 

```
<img src="myimage.png" alt="Cat"> 
```

```
img[alt="Cat"] {
  border: 1px solid black; 
}
```

**Other Attribute Selectors Include**

```
a[href^="http"] The ^= caret symbol and equals sign select elements that start with the matching value, such as <a href="http://google.com">google</a>.

p[class$="dog"] The $= dollar and equals signs select elements that end with the matching value, such as <p class="bigbdog">...</a>.

img[alt*="love"] The *= asterisk and equals sign select elements that have the matched characters appearing anywhere within the value, such as <img src="myimage.jpg" alt="I love you.">.

p[class~="monkey"] The ~= tilde symbol and equals sign select elements that contain the term within a space separated value, such as <p class="zoo monkey details">...</p>.

p[class|="birds"] The |= pipe symbol selects elements that contain the term within a dash separated value, such as <p class="new-birds-today">...</p>.

```

#### 11) Pseudo Class

This selects an element based on the unique relationship or state described in the selector. This selector is indicated by the : (colon symbol), followed by the pseudo class that describes the element's state or positioning amongst other elements.

```
<a href="about.html">About</a>
```
```
a:link {
  text-decoration: none;
}
```
```
Other Pseudo Class Selectors Include:
a:link selects links in their default state before the visitor has interacted with them.

a:visited selects links after the user has already clicked on them and is visiting that page again.

a:hover selects links when the user is hovering their mouse over the link.

a:active selects links for only the moment when the mouse button is pressed when clicking on the link.

p:first-child selects elements that are the first child when appearing inside a common parent. Such as <div><p>I'm selected</p><p>I'm not</p><p>Neither am I</p></div>

p:last-child selects elements that are the last child when appearing inside a common parent. Such as <div><p>I'm not selected</p><p>Neither am I</p><p>I'm selected</p></div>

These are just a few pseudo selectors, but there are many additional ones you can explore in the resource links provided at the bottom of this lesson.
```

# JS And the Web

## This is Alice Example.

If you click on Alice, you'll notice that Alice has some behavior. If you click on her she starts spinning and she doesn't stop unless clicked again. It's not very nice to make a kitten spin based on the whims of someone's mouse click.

## Discovering JavaScript's Powers 

In previous lessons, you've seen that HTML structures the content of a webpage. Now JavaScript is a language that adds behavior to a website. What do we mean by that? 
When we say JS adds behavior to our HTML we mean that it selects HTML, listens to events such as mouse clicks, and adds, modifies or removes HTML.
In this case, the behavior that JavaScript added was it listened to the click event, and then modified the HTML of alice, If you look at the JS tab, you can see that the code is almost readable.


script.js
```
function toggleClass(){
  if(image.className == 'image'){
      image.className = ''
  } else {
      image.className = 'image'
  }
}
```

index.html
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="css/main.css">
  </head>
  <body>
    <div class="container">
        <h1>Click me</h1>
        <img id="kitten" class="" src="http://makeameme.org/media/templates/120/grumpy_cat.jpg" alt="" width="150" height="150">
        <script src="js/script.js"></script>
    </div>
  </body>
</html>

```

main.css
```
#kitten{
  border-radius: 50%;
}

.container{
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100px;
  height: 120px;
  margin:-60px 0 0 -60px;
}

.container > h1 {
  color: gray;
  text-align: center;
}
.image {
-webkit-animation:spin 4s linear infinite;
-moz-animation:spin 4s linear infinite;
animation:spin 4s linear infinite;
}

@-moz-keyframes spin { 100% { -moz-transform: rotate(360deg); } }
@-webkit-keyframes spin { 100% { -webkit-transform: rotate(360deg); } }
@keyframes spin { 100% { -webkit-transform: rotate(360deg); transform:rotate(360deg); } }

```

This code do: 
[]Find HTML.
[]-Allows you to find specific pieces of HTML so we can later change that HTML. Above we found the image of the cat.
[]Listen and respond to events.
[]JavaScript can listen to events like clicking or hovering over specific elements, the user pressing on specific keys, and much more.


# Introduction to the DOM

## Problem Statement.

We know how to write HTML and style it with CSS but if we want to do more with the content in our pages, such as adding or deleting elements or modifying them. 
It's time to move on to interactivity and understanding the **Document Object Model** or DOM

### The document Object Model

Just as your DNA represents a code based version of you, the DOM represents a code-based version of a web page. Because of this, when you change the DOM, you change what's displayed in the browser. Adding elements, removing, changing, etc. Thanks to the DOM and the way it creates a representative model of documents elements, we can use a language such as JavaScript to work with those elements and add to them, delete them or modify them. 

To see the DOM in action, let's take a look at the HTML that constructs every website we visit. 

#### Some useful resources

https://css-tricks.com/dom/

https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction

#### Conclusion

HTML is a markup language used to display content in a browser. When we change the appearance of a web page, what we are really changing is the Document Object Model, wich directly determines the appearance displayed in th browser.

We can view and manipulate the Document Object Model by opening our developer tools, but when we do so the HTML is not changed.

We can also view our Document Object Model by opening the console and typing the word "document"

We can select a specific piece of the DOM by using JS, such as Document.querySelector('header'), and we can also use JavaScript to alter our DOM with .remove().

# Selecting Single Elements Readme

Learn how to:

<> Use the developer tools to identify a particular element.
<> Use JavaScript's selector methods to select particular pieces of the DOM.
<> Learn about CSS selectors and use them to select elements by id, class or HTML tag.

## Intro.

We are going to take a little deeper look at how to retrieve information about a webpage by using JavaScript's "document object model API". 

## Get Started

Let's work with the "Ada Lovelace" Wikipedia Entry
```
We are going to identify were is her H1 element with the command document.querySelector('#firstHeading')
```
and you should see returned this: 

```<h1 id="firstHeading" class="firstHeading" lang="en">Ada Lovelace</h1>
```

### Other CSS Selectors

Using JavaScript we can "target" elements using the same syntax we "target" element in CSS. You've just used the first occurrence of an HTML tag match to "select" an HTML element.  Let's see some other ways to "select" elements.  For the moment, we'll step away from the `lovelace.html` document and look at a simple HTML snippet as a thought experiment. Beneath the snippet, find a table displaying different ways to select the paragraph element.

```html
<div>
	<p id="content" class="red"> Select this content!</p>
</div>
<ul>
	<li>Don't </li>
	<li>Select </li>
	<li>This </li>
</ul>
```

| Attribute     | CSS Selector  | querySelector Code |
| ------------- |:-------------:| -----:|
| id      	   | `#` 			  | `document.querySelector('#content')`|
| class      	   |`.`     		  |  `document.querySelector('.red')` |
| html tag      | 	         |    `document.querySelector('p')` |


So you can see that we prepend the `#` sign to the `id` attribute name to select an item by its `id.` We prepend the `.` to the class attribute name to select an item by its class name.  And we prepend nothing when selecting by tag name.

We can also select elements using other methods.  Let's add in those other methods to our chart.

| Attribute     | CSS Selector  | querySelector Code |Alternative Method |
| ------------- |:-------------:| -----:| -----:|
| id     	   | `#` 			  | `document.querySelector('#content')`|`document.getElementById('content')`|
| class      	   | `.`     		  |  `document.querySelector('.red')` |`document.getElementsByClassName('red')`|
| html tag      | 	         |    `document.querySelector('p')` | `document.getElementsByTagName('p')`|

> Notice that when we use a method like `getElementById` we do not need to start with a # sign.  This is because JavaScript already knows that we are selecting by the `id` attribute by virtue of using a method that only accepts an id.  Query selectors take different types of attributes, so there we do need to specify the type of attribute we are selecting by.

Let's turn back to our `lovelace.html` file.

### Selecting By Ancestry - And Solving a Problem

Let's look at some more content: links.

Links are defined in HTML with an `a` tag. Let's use what we know so far to try to access the link for the word "Marylebone" inside the "info box" or "gray inset" at the right. Inspect this element.  You'll see it has no `id` or `class` attribute.  To select it we can select the infobox and _then_ select a unique span with a class name and _then_ the first link within that span. That is, we will "chain" our calls to `document.querySelector`. Try this:

`document.querySelector(".infobox").querySelector("span.deathplace").querySelector("a")`

This code statement should make sense in English if you read it backward:

"Find the link that's within the span element with the class "deathplace" that's within some element with the class "infobox".

It's our opinion that having the mental flexibility to read backward and forward in different made-up languages might be the reason so many programmers are prone to puns, wordplay, and Lewis Carroll books.

### Retrieving Attributes

Now that we have selected the proper HTML element, let's save it to a variable and examine it "under a microscope."

```js
let maryleboneAnchor = document.querySelector(".infobox").querySelector("span.deathplace").querySelector("a")
maryleboneAnchor.constructor
// ƒ HTMLAnchorElement() { [native code] }
```

By calling the selected element's `constructor` property, we can see that we `maryleboneAnchor` is an "instance" of an `HTMLAnchorElement`.  Many methods on this instance correspond to the potential attributes of an HTML anchor.  For example, `maryleboneAnchor.href` returns `"/wiki/Marylebone"`, `maryleboneAnchor.text` returns `"Marylebone"`.

> **The magic of guessing:**
> Programmers guess a lot more than you might think.  The reason why is because the consequences guessing incorrectly are really low, and you can often quickly find out if you are right or wrong.  So if you're unsure if some code will work, just guess and try it.  The consequence of guessing incorrectly is that you learn something new about the language.

The methods we explored thus far like `href` and `text` make a lot of sense when we have an instance of an `HTMLAnchorElement`.  There are other methods you can reliably call on any instance of an element (or any HTML DOM node, to be technical) that you select.  We already saw a couple of them when exploring the DOM in previous lessons.  These methods can allow us to find information about other related nodes, like `children`, or `nextSibling`.  Some tell us attributes of element, like `attributes` to see attributes of the element, `classList` to see a list of classes associated with the element, and `style` which returns the associated CSS styles of a selected element. Explore these on the `maryleboneAnchor` element.

If `maryleboneAnchor` isn't providing anything interesting, use the "chained" `querySelector` method to find something more interesting. Don't forget the magic of guessing either, if there's a `next....` something there's probably also a `previous....` something. If a method doesn't return a String, what _does_ it return? This process of exploration and guess-and-check, optimized for speed, is how programmers avoid having to know books worth of knowledge: they don't memorize all the facts, they ask the _computer_ to teach them micro-lessons.

### Summary

In this section, we learned how to use JavaScript and our developer console to ask questions about our HTML. Here is our process:

1. From the browser, click inspect element on the HTML element you are interested in to find an identifying attribute to select the HTML.
2. Depending on the type of attribute, you can then use `document.querySelector()` method, and in the parentheses pass through the proper CSS selector in combination with the attribute name to select that element **OR** we can use a different JavaScript method like `document.getElementsByClassName()` to select the correct element.
3. Once you have properly targeted the element, you can then call other methods to identify attributes of that element e.g.`document.querySelector('a').text`

### Resources

[MDN Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)

<p class='util--hide'>View <a href='https://learn.co/lessons/selecting-single-elements-readme'>Selecting Single Elements Readme</a> on Learn.co and start learning to code for free.</p>

[static-lovelace-file]: https://learn-co-curriculum.github.io/selecting-single-elements-readme/lovelace.html

#Selecting Single Elements Lab 

