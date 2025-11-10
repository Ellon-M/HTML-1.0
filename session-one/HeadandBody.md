# Head, Body ...

We'll see how to build our HTML document - starting with the head of it. Then the main content of it in the body.

## Document Heading

So what goes into the `<head>` tag?

It’s always written before the `body` tag, right after the opening html tag:

We never use attributes on this tag. And we don’t write content in it. 
It’s just a container for other tags. 

Inside it we can have a wide variety of tags, depending on what you need to do:

    - title
    - script 
    - noscript 
    - link 
    - style 
    - base 
    - meta

The `title` tag determines the page title. The title is displayed in the browser, and it’s especially important as it’s one of the key factors for Search Engine Optimization (SEO).

The `script` tag is used to add JavaScript into the page. You can include it inline, using an opening tag, the JavaScript code and then the closing tag. You can also load an external JavaScript file by using the `src` attribute. (We'll learn more about script tags and JavaScript later).

The `noscript` tag is used to detect when scripts are disabled in the browser. (Users can choose to disable JavaScript scripts in the browser settings, or some old browsers might not support them by default). It is used differently depending on whether it’s put in the document head or in the document body. In the head, it can only contain other head tags. If used in the body, it will contain body content, like paragraphs and other tags, which are rendered in the UI.

The `link` tag is used to set relationships between a document and other resources. It’s mainly used to link an external CSS file to be loaded. This element has no closing tag. It can also be used to link other things as well. (RSS Feeds, Favicons, etc). Attributes used: `href` points to the source/path/name of the file being linked. (CSS or other) `rel` shows what is being linked. There is also an optional `type` attribute which points to the type of file being linked.

The `style` tag can be used to add styles into the document, rather than loading an external stylesheet.


The `base` tag is used to set a base URL for all relative URLs contained in the page.

Meta tags (`meta`) perform a variety of tasks and they are very, very important. Especially for SEO. They are self closing. These tags are used by Google when web crawlers crawl a website. They interact with Search Engine bots.
Some examples: 

> `<meta name="description" content="A nice page" />` 
> - This might be used by Google to generate the page description in its result pages, if it finds it better describes the page than the on-page content.
> 
>  `<meta charset="utf-8" />`
> - The charset meta tag is used to set the page character encoding. utf-8 in most cases.
>
> `<meta name="robots" content="noindex" />`
>  - The robots meta tag instructs the Search Engine bots whether to index a page or not.
>
> `<meta name="robots" content="nofollow" />` 
> - Or if the bots should follow links or not. (This is how you set it globally. You can also set it for each individual `link` tag. You can also combine this with `noindex`. By default, the meta robots tag is set to `index, follow` if not explicitly set.
>  - There are also other robots content settings such as `nosnippet , noarchive , noimageindex` which all specify options to be disabled during SEO.
>
>`<meta name="googlebot" content="noindex, nofollow" />`
> - You can also target Google's search engine specifically. For example, we can tell Google to disable some features. This prevents the translate functionality in the search engine results
> `<meta name="google" content="notranslate" />`
>
> `<meta name="viewport" content="width=device-width, initial-scale=1" />`
> - The viewport meta tag is used to tell the browser to set the page width based on the device width. This is very important and should almost always be present when building a web page. The above example is the most common setting is the following, which sets the viewport to match the device's width and displays content at 100% zoom.
>
>`<meta http-equiv="refresh" content="3;url=http://jw.org/another-page"/>` 
> - Another rather popular meta tag is the `http-equiv="refresh"` one. This line tells the browser to wait 3 seconds, then redirect to that other page. Using 0 instead of 3 will redirect as soon as possible.

There are other meta tags that are less used. For a full reference: MDN Mozilla documentation or the HTML Living Standard Page. 


## Document Body


Just like the head and html tags, we can only have one `body` tag in one page. 
Inside the body tag we have all the tags that define the content of the page.
 
Visual elements, the ones defined in the page body, can be generally classified in 2 categories:
- Block elements (`div`, `p`, `li` ...)
- Inline elements (`a`, `img`, `span` ...)

What is the difference? 

Block elements, when positioned in the page, do not allow other elements next to them. To the left, or to the right. Inline elements instead can sit next to other inline elements. 
The difference also lies in the visual properties we can edit using CSS. We can alter the width/height, margin, padding and border of block elements. We can’t do that for inline elements.
Another difference is that inline elements can be contained in block elements. The reverse is not true.

> Note that using CSS we can change the default for each element, setting a p tag to be inline, for example, or a span to be a block element

Let's look at some examples of tags we can use:

### The `p` tag

 This tag defines a paragraph of text.

    <p>Some text</p>

It’s a block element, and inside it, we can add any inline element we like, like `span` or `a` . We cannot add block elements. We cannot nest a `p` element into another one.


### The `span` tag

This is an inline tag that can be used to create a section in a paragraph.

    <p>A part of the text<span>and here is another part</span></p>


### The `br` tag

This tag represents a line break. It’s an inline element, and does not need a closing tag.

    <p> Some text here <br/>Another line </p>

### The heading tags

HTML provides us 6 heading tags. From most important to least important, we have `h1 , h2 , h3 , h4 , h5 , h6` . 

Typically a page will have one h1 element, which is the page title. Then you might have one or more h2 elements depending on the page content.

The browser by default will render the h1 tag bigger, and will make the elements size smaller as the number near h increases.

They cannot contain other elements, just text.


### Other, important text related tags

`strong` tag - it’s not a visual hint, but a semantic hint. By default the browsers make this text **bold**.
`em` tag - also not a visual hint, but a semantic hint. It is used to mark the text inside it as *emphasized*. By default browsers make this text italicized. 
`blockquote` and `q` tags - are useful to insert citations in the text.
`hr` tag - adds a horizontal line in the page, and is useful for separating sections in the page. 
`code` tag - is especially useful to show code, because browsers give it a monospaced font.

For presentational purposes:

 - the `mark` tag  
 - the `ins` tag  
 - the `del` tag  
 - the `sup` tag  
 - the `sub` tag  
 - the `small` tag  
 - the `i` tag  
 - the `b` tag

### Lists

There are 3 types of lists:
- Unordered lists (most common)
- Ordered lists
- Definition lists (rarely used)

Unordered lists are created using the `ul` tag. Each item in the list is created with the `li` tag.

Ordered lists are similar, just made with the `ol` tag.

The difference between the two is that ordered lists have a number before each item.

Definition lists are a bit different. You have a term, and its definition.

    <dl>
      <dt>Dee</dt>
      <dd>Your Nickname</dd>
      <dt>Ellon</dt>
      <dd>Your Name</dd>
      <dt>Mordecai</dt>
      <dd>Middle name</dd>
    </dl>


### Links

Links are defined using the `a` tag. The link destination is set via its `href` attribute.

    <a href="https://ellon.netlify.app">click here</a>

Between the starting and closing tag we have the link text.

Link (`a`) tags can also include other things inside them, not just text.


### Images

Images can be displayed using the `img` tag. This tag accepts a `src` attribute, which we use to set the image source:

    <img src="image.png" />

We can use a wide set of images. The most common ones are PNG, JPEG, GIF, SVG and more recently WebP.

The HTML standard requires an `alt` attribute to be present, to describe the image. This is used by screen readers and also by search engine bots. This also greatly influences SEO.

    <img src="dog.png" alt="A picture of a dog" />

You can set the `width` and `height` attributes to set the space that the element will take, so that the browser can account for it and it does not change the layout when it’s fully loaded. It takes a numeric value, expressed in pixels.

    <img src="dog.png" alt="A picture of a dog" width="300" height="200" />


The `figure` tag - often used along with the `img` tag.

    <figure>
      <img src="dog.png" alt="A nice dog" />
      <figcaption>A nice dog</figcaption>
    </figure>

`figure` is a semantic tag often used when you want to display an image with a caption.

*Tiny detour on semantic HTML.*

Responsive images using `srcset`
The `srcset` attribute allows you to set responsive images that the browser can use depending on the pixel density or window width, according to your preferences.

This way, it can only download the resources it needs to render the page, without downloading a bigger image if it doesn't need to.

    <img 
	  src="dog.png" 
	  alt="A picture of a dog" 
	  srcset="dog-500.png 500w, 
				 dog-800.png 800w, 
				 dog-1000.png 1000w, 
				 dog-1400.png 1400w " 
	/>

In the `srcset` we use the `w` measure to indicate the window width. Since we do so, we also need to use the `sizes` attribute:

    <img 
      src="dog.png" 
      alt="A picture of a dog" 
      sizes="(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px" 
      srcset=" dog-500.png 500w, dog-800.png 800w, dog-1000.png 1000w, dog-1400.png 1400w " 
    />

In this example the `(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px` string in the sizes attribute describes the size of the image in relation to the viewport, with multiple conditions separated by a comma.

The media condition max-width: 500px sets the size of the image in correlation to the viewport width. 

In short, if the window size is < 500px, it renders the image at 100% of the window size. If the window size is bigger but < 900px , it renders the image at 50% of the window size. And if even bigger, it renders the image at 800px.

The `vw` unit of measure can be new to you, and in short we can say that 1 vw is 1% of the window width, so `100vw` is 100% of the window width.


The `picture` tag - used when instead of just serving a smaller version of a file, you completely want to change it. Or serve a different image format. (maybe if a certain image might be unavailable/not supported by a browser)
In the picture tag you specify a list of images, and they will be used in order. 

    <picture>
      <source type="image/webp" srcset="image.webp"/>
      <img src="image.jpg" alt="An image"/>
    </picture>

> The source tag defines one (or more) formats for the images. The `img` tag is the fallback in case the browser is very old and does not support the `picture` tag.

The picture tag is recent but is now supported by all the major browsers except Opera Mini and IE (all versions).


### Container tags and page structure HTML

HTML provides a set of container tags. 
Those tags can contain an unspecified set of other tags.

The `div` is the generic container element. Stuff goes inside it.

    <div>...</div>

The `article` tag identifies a thing that can be independent from other things in a page. For example a list of blog posts in the homepage. Or a list of links.

    <div>
      <article>
        <h2>A blog post</h2>
        <a>Read more..</a>
     </article>
      <article>
          <h2>Another Blog Post</h2>
          <a>Read more..</a>
     </article>
    </div>

It doesn't necessarily have to be a list of articles. An article can also be the main element of a page. 

a `section` tag represents a section of a document. Each section has a heading tag ( h1 - h6 ), then the section body.

When you have a long container (div/article) it is useful to break it up into sections.