# What is HTML?
HTML (Hypertext Markup Language) is not a programming language. It is a markup language that tells web browsers how to structure the web pages you visit. It can be as complicated or as simple as the web developer wants it to be. HTML consists of a series of elements, which can be applied to pieces of text to give them different meaning in a document (Is it a paragraph? Is it a bulleted list? Is it part of a table?), structure a document (Does it have a header? Three colums of content? A navigation menu?), and embed contenct such as images and video into a page.

## Anatomy of an HTML element:
Consider the following line of text:

My cat is very grumpy

If we wanted the text to stand by itself, we could specify that it is a paragraph by enclosing it in a paragraph <p> element:

<p>My cat is very grumpy<p>

The anatomy of our element is:

- The opening tag: This consists of the name of the element, p for paragraph, wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect. It precedes the start of the paragraph text.
- The content: This is the content of the element. In this example, it is the paragraph text.
- The closing tag: This is the same as the opening tag, except that it includes a forward slash before the element name. This marks where the element ends. Failing to include a closing tag is a common beginner error that can produce peculiar results.

The element is the opening tag, followed by content, followed by the closing tag.

## Nesting elements:

Elements can be placed within other elements. This is called nesting. If we wanted to state that our cat is very grumpy, we could wrap the word very in a <strong> element, which means that the word is to have strong(er) text formatting:

<p>My cat is <strong>very</strong> grumpy.

There is a right and wrong way to do nesting. In the example above, we opened the p element first, then opened the strong element. For proper nesting, we should close the strong element first, before closing the p

## Block versus inline elements:

Block-level elements form a visible block on a page. A block-level element appears on a new line following the content that precedes it. Any content that follows a block-level element also appears on a new line.
- Block-level elements are usually structural elements on the page. For example, a block-level element might represent headings, paragraphs, lists, navigation menus, or footers. A block-level element wouldn't be nested inside an inline element, but it might be nested inside another block-level element.
- Inline elements are contained within block-level elements, and surround only small parts of the document’s content (not entire paragraphs or groupings of content). An inline element will not cause a new line to appear in the document. It is typically used with text, for example an <a> element creates a hyperlink, and elements such as <em> or <strong> create emphasis.
<em>first</em><em>second</em><em>third</em>

<p>fourth</p><p>fifth</p><p>sixth</p>

<em> is an inline element. As you see below, the first three elements sit on the same line, with no space in between . On the other hand, <p> is a block-level element. Each p element appears on a new line, with space above and below.

*firstsecondthird*

fourth

fifth

sixth

## Empty elements:

Not all elements follow the pattern of an opening tag, content, and a closing tag. Some elements consist of a single tag, which is typically used to insert or embed something in the document. For example, the <img> element embeds an image file onto a page:

<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png">

## Attributes:

Elements can also have attributes. Attributes contain extra information about the element that won't appear in the content.

![Attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started/grumpy-cat-attribute-small.png)

An attribute should have:

A space between it and the element name. (For an element with more than one attribute, the attributes should be separated by spaces too.)
The attribute name, followed by an equal sign.
An attribute value, wrapped with opening and closing quote marks.
Adding attributes to an element:
Another example of an element is <a>. This stands for anchor. An anchor can make the text it encloses into a hyperlink. Anchors can take a number of attributes, but several are as follows:

- href: This attribute's value specifies the web address for the link (href="https://www.google.com/").
- Title: The title attribute specifies extra information about the link, such as a description of the page that is being linked to. For example, title="The Google Homepage". This appears as the tooltip when a cursor hovers over the element.
- Target: The target attribute specifies the browsing context used to display the link. For example: target="_blank" will display the link in a new tab. If you want to display the linked content in the current tab, just omit this attribute.

Editable code:

<p>A link to my <a href="https://www.google.com/" title="The Google Homepage" target=_blank">favorite website</a>.</p>

## Anatomy of an HTML document:

Individual HTML elements aren't very useful on their own. Next, let's examine how individual elements combine to form an entire HTML page:

<!DOCTYPE html>

<html>

<head>

<meta charset="utf-8">

<title>My test page</p>

</head>

<body>

<p>This is my page</p>

</body>

</html>

Here we have:

- The doctype: The doctype is a historical artifact that NEEDS to be included for everything else to work right. That is all you need to know!
The <html> element: This element wraps all the content on the page. It is sometimes known as the root element.
- The <head> element: This element acts as a container for everything you want to include on the HTML page, that isn't the content the page will show to viewers. This includes keywords and a page description that would appear in search results, CSS to style content, characer set declarations, and more.
- The <meta charset="utf-8">: This element specifies the character set for your document to UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.
- The <title>: This sets the title of the page, which is the title that appears in the browser tab the page is loaded in. The page title is also used to describe the page when it is bookmarked.
- The <body>: This contains all the content that displays on the page, including text, images, video, games, playable audio tracks, or whatever else.

## Entity references; Including special character in HTML:

in HTML, the characters <, >, ", and & are special characters. They are parts of the HTML syntax itself. So we need to use character references, special codes that represent characters, to be used in these exact circumstances. each character reference starts with an ampersand (&), and ends with a semicolon (;).

Example code: <p>In HTML, you define a paragraph using the &lt;p&gt; element.</p>

There are many other entity referenes to use in HTML.

## HTML comments:

HTML has a mechanism to write comments in the code. Browsers ignore comments, effectively making comments invisible to the user. The purpose of comments is to allow you to include notes in the code to explain your logic or coding. This is very useful if you return to a code base after being away for long enough that you don't completely remember it. Likewise, comments are invaluable as different people are making changes and updates. To write an HTML comment, wrap it in the special markers <!-- and -->.

Example:

<p>This is not inside a comment</p>

<!-- <p>But this is!</p> -->