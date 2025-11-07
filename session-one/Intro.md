# HTML - Intro

**HTML** is the foundation of the Worldwide Web.  With a limited set of rules, there is incredible power behind it which lets us craft documents, apps, and experiences.

HTML has succeeded because of a feature it provides us: **forgiveness**. There are some rules, right, but after you learn those, you have a lot of freedom. Browsers have learned to be resilient and to always try to do their best when parsing and presenting HTML to the users.

**Backwards Compatibility:** We can view and interact with HTML pages from decades ago; and the language structure hasn't much changed.

> First ever HTML page:
> https://info.cern.ch/hypertext/WWW/TheProject.html

And you can see the source of the page, thanks to another big feature of the Web and HTML: we can **inspect** the HTML of any web page. The exceptional **Developer Tools** built into any browser let us inspect and take inspiration from HTML written by anyone in the world.




## HTML Basics

HTML has been morphing over the years, but has been standard since the launch of the HTML we know now as HTML5. HTML5 is a term that now defines a whole set of technologies, which includes HTML but adds a lot of APIs and standards like WebGL, SVG and more. We have no such thing as "HTML Versions" now.

> Everything about HTML lives here:
> https://html.spec.whatwg.org/multipage/

HTML, as a language, is a **Markup Language**.
We use it to structure content that we consume on the Web.
It is basically like the skeleton of the web, whereas its compatriot CSS is the "makeup" of the web (beautifier).

Diving into it:
- By convention, an HTML file is saved with a **.html** or **.htm** extension. 
- Inside this file, we organize the content using **tags**. 
- Tags **wrap** the content, and each tag gives a special meaning to the text it wraps.

As an example:
This HTML snippet creates a paragraph using the p tag:

    <p>A paragraph of text</p>

This HTML snippet creates a list of items using the ul tag, which means unordered list, and the li tags, which mean list item:

    <ul> 
	    <li>First item</li>
	    <li>Second item</li>
	    <li>Third item</li>
    </ul>

Most tags come in pairs with an **opening tag** and a **closing tag**. The closing tag is written the same as the opening tag, but with a / :

    <sometag>content goes here</sometag>

The combination of an opening and closing tag form what we call a HTML **Element**.

There are a few **self-closing tags**, which means they don’t need a separate closing tag as they don’t contain anything in them.

HTML is **case insensitive**. Tags can be written in all caps, or lowercase. In the early days, caps were the norm. Today **lowercase** is the norm. It is a convention.

Also, In HTML, even if you add multiple white spaces into a line, it’s collapsed by the browser’s CSS engine. (demonstrate).

Some of the few built in rules of HTML are these. (How the browser interprets which tags are which, and what they mean, and how the page should be structured).

Now, let’s make an example of a proper HTML page.

## HTML Page Structure

Things start with the Document Type Declaration (aka doctype), a way to tell the browser this is an HTML page. 

    <!DOCTYPE html>

Then we have a `html` tag, which has an opening and closing tag.

    <!DOCTYPE html>
	    <html>
	    ...
	    </html>

Inside the html element we have 2 elements: `head` and `body` :	

    <!DOCTYPE html>
    <html>
      <head>
	    ...
      </head>
      <body> 
        ...
      </body>
    </html>

Inside `head` we will have tags that are essential to creating a web page, like the title, the metadata, and internal or external CSS and JavaScript. (Other essential languages which complement HTML). Mostly things that do not directly appear on the page.

Inside `body` we will have the content of the page. The **visible** stuff.

As a form of convention/good practice: Nested tags should be indented with 2 or 4 characters, depending on your preference.

## Attributes

The starting tag of an element can have special snippets of information we can attach, called attributes. 

Attributes have the `key="value"` syntax:

    <p class="a-class">A paragraph of text</p>

You can also use single quotes, but using double quotes in HTML is a nice convention.

We can have many of them:

    <p class="a-class" id="an-id">A paragraph of text</p>

The class and id attributes are two of the most common you will find used. They have a special meaning, and they are useful both in CSS and JavaScript. 

The difference between the two is that an id is unique in the context of a web page; it cannot be duplicated. Classes, on the other hand, can appear multiple times on multiple elements. Plus, an id is just one value. class can hold multiple values, separated by a space:

    <p class="a-class another-class">A paragraph of text</p>

It’s common to use the dash - to separate words in a class value, but it’s just a convention.

Those are just two of the possible attributes you can have. (general). Some attributes are highly specialized and are only used for one tag.
