## Styling HTML with CSS

CSS (Cascading Style Sheets) is a language for specifying how documents are presented to users (how they are styled, laid out, etc.). You can control exactly how HTML elements look in the browser, presenting your markup using whatever design you like. CSS can be used for very basic document text styling. For example… 1. Changing the color and size of headings and links. It can be used to create layout. 2. Turning a single column of text into a layout with a main content area and a sidebar for related information. It can even be used for effects such as animation.


## CSS syntax:

CSS is a rule-based language. You define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. For example, you want the main heading of your page to be shown as large red text…

h1 {

color: red;

font-size: 5em

}

The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings `<h1>`. We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property. Before the colon, we have the property, and after the colon, the value. CSS properties have different allowable values, depending on which property is being specified. In our example, we have the color property, which can take various color values. We also have the font-size property. This property can take various size units as a value.

## CSS modules:

There is so much styling with CSS, that it is broken down into modules. For example, you could take a look at the Backgrounds and Borders module to find out what its purpose is, and what different properties and other features it contains. At this stage you don't need to worry too much about how CSS is structured, however it can make it easier to find information if you are aware that a certain property is likely to be found among other similar things and are therefore probably in the same specification.

## Styling HTML elements:

By making our heading red, we have already demonstrated that we can target and style an HTML element. We do this y targeting an element selector. This is a selector that directly matches an HTML element name. You can target multiple selectors at once, by separating the selectors with a comma.

Example: p, li {

color: green;

}

## Adding a class:

So far, we have styled elements based on their HTML element names. This works as long as you want all of the elements of that type in your document to look the same. Most of the time that isn't the case and so you wil lneed to find a weay to select a subset of the elements withought changing the others. The most common way to do this, is to add a class to your HTML element and target that class. In your HTML document, add a class attribute to the second list item. Your list will now look like this:

`<ul>`

`<li>`Item one<`/li>`

`<li class="special">Item two</li>`

`<li>`Item`<em>`three`</em><li>`

`</ul>`

In your CSS you can target the class of "special" by creating a selector that starts with a full stop character. Add the following to your CSS file:

.special {

color: orange;

font-weight: bold;

}

You can apply the class of "special" to any element on your page that you want to have the same look as this list item. For example, you might want the `<span>` in the paragraph to also be orange and bold.

## Styling things based on their location in a document:

There are times when you will want something to look different based on where it is in the document. There are a number of selectors that can help you here, but for now we will look at just a couple. In a document with two `<em>` elements, one inside a paragraph and the other inside a list item. To select only an `<em>` that is nested inside an `<li>` element Iyou can use a selector called the descendant combinator, which takes the form of a space between two other selectors.

li em {

color: rebeccapurple;

}

This selector will select any `<em>` element that is inside an `<li>`. So in your example, you should find that the `<em>` in the third list item is now purple, but the one inside the paragraph is unchanged.

## Styling things based on state:

An example of this is when styling links. When we style a link, we need to target the `<a>` element. This has different states depending on whether it is unvisited, visited, being hovered over, focused via keyboard, or in the process of being clicked (activated). You can use CSS to target these different states.

a:link {

color: pink;

}

a:visited {

color: green;

}

You can change the way the link looks when the user hovers over it, for example, removing the underline, which is achieved by:

a:hover {

text-decoration: none;

)

## Combining selectors and combinators:

It is worth noting that you can combine multiple selectors and combinators together. You can combine multiple types together too.

body h1 + p .special {

color:yellow;

background-color: black;

padding: 5px;

}

This will style any element with a class of "special", which is inside a <p>, which comes just after an `<h1>`, which is inside a `<body>`. Whew!

## Inline styles:
Inline styles are CSS declarations that affect a single HTML element, contained withing a style attribute. The implementation of an inline style in an HTML document looks like:

`<body>`

`<h1 style="color:blue;background-color: yetllow;border: 1px solid black;">Hello World!</h1>`

`</body>`

Avoid using CSS in this way when possible. It is not best practice.

## Selectors:

A selector targets HTML to apply styles to content. If CSS is not applying to content as expected, your selector may not match the way you think it should match. Each CSS rule starts with a selector or list of selectors, in order to tell the browser which element(s) the rules should apply to.

## Properties and values:

At its most basic level, CSS consists of two components:
- Properties: Thesse are human-readable identifiers that indicate which stylistic features you want to modify, such as font-size, width, background-color
- Values: Each property is assigned a value. This value indicates how to style the property.

The property name below is color and the value is blue.

![Properties & Values](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured/declaration.png)

Declaration block:

![Declaration Block](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured/declaration-block.png)

CSS rules, highlighting the h1 rule.

![CSS Rules, Highlighting the h1 rule](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured/rules.png)

## Comments:

As with any coding, it is best practice to write comments along with CSS. This helps you to remember how the code works as you come back later for fixes or enhancement. It also helps others understand the code. CSS comments begin with /* and end with */.