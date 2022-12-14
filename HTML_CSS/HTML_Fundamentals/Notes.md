# HTML Fundamentals

## HTML comments

Comments in HTML are created using `<!-- -->`.

## Text Elements

* Heading (h1 - h6) elements are used to establish hierarchy.
* It is best practice to only have one `h1` heading on your page.
* Use the `<strong> </strong>` element to bold text.
* "Semantic HTML" is html elements that hold meaning.
* Use the `<em> </em>` element to emphasize/italic text

## Lists

There are two types of lists in HTML.

1. Ordered lists which are created using the `<ol> </ol>` tag
2. Unordered lists which are created using the `<ul> </ul>` tag.

Lists are made up of items which are created using the `<li> </li>` "list item" tags.

## Images and Attributes

To insert an image we use the `<img>` tag which needs a `src="path to image"` and `alt = 'image description'`. Alt is
important because it allows search engines to describe the image to blind people/screen readers. Inside the `<img>`
tag we can also specify `width = "500"` and `height = "200`.

## Hyperlinks

In HTML, we have the possibility to link to both internal and external paths. For example, we can link to a different
page, or we can link to a different website.

Links in HTML are called "anchors" and are created using the `<a> </a>` tag. Between the tags goes the text we want to display for the link such as `<a> Click Here </a>`. The actual link to an external website goes inside `href = ""`.  
So an example would be `<a href = 'www.google.com' > Go to Google </a>`.

We can open a link in a new tab by using the `target = "_blank"` attribute inside the `<a>` tag.

To link to a new HTML page, first we must create it and then using the `<a>` tag, we specify the name of the HTML page
as the `href` attribute. For example, if we create a `blog.html` page, we can link to it from out `index.html`
page by using `<a href= "blog.html" > Blog </a>`.

Lastly, it's possible to have links that do not redirect anywhere. To achieve this we use `href="#"` which will take you
back to the top of the page.

## Page Structure

We can add structure to our page by including containers. We do this to group elements together in order to make css
styling easier to implement and de-bug. We also use page structure in order to follow sematic HTML design which is the
usage of html elements with meaning. For example, we can use `div` to define a `nav` bar but by using `nav` we introduce
meaning to this section of the page. Another major reason is search engine optimization which allows search engines to
better understand the structure of our content. This is why when writing out HTML we should not simply think about how
the elements look but rather focus on what the elements mean and stand for.

* `<nav> </nav>` is used to represent a section of a page whose purpose is to provide navigation links.
* `<header> </header>` defined introductory content, and it mostly found at the top part of webpages and/or other
  elements.
* `<article> </article>` is used to contain information that can be distributed independently of the rest of the page.
* `<footer> </footer>` typically contains author info, copyright, contact info etc.
  * To create the copyright symbol we use `$copy;`.
* `<div> </div>` is used to create a container that holds no meaning.
