# Selecting Elements in the DOM

## Problem Statement

The Document Object Model, or DOM, allows us to access page elements via
JavaScript and perform a variety of actions with them. But before we can do
anything, we have to understand more about the DOM's structure and how
JavaScript interacts with it.

## Objectives

1. Review the Document Object Model
2. Identify the DOM hierarchy
3. Explore how to access the DOM with JavaScript

## Review the Document Object Model

The DOM is an intermediate representation that is built from a page's HTML and
CSS when the page is loaded. The DOM provides a way of manipulating the HTML it
represents. The "way of manipulating" things is an Application Programming
Interface, or API. The JavaScript API for DOM manipulation is a vast topic and
so we're going to introduce it piece by piece.

First, the DOM has a hierarchical structure. It represents the HTML as parent
nodes that have children. A `<div>` parent that contains several `<p>`s is said
to be a parent with multiple children or child-nodes. Let's see this hierarchy
in action.

## Identify the DOM Hierarchy

![Dom Structure Tree](https://s3.amazonaws.com/learn-verified/dom-tree.gif)

### **Window**

  + The highest level of the DOM tree is the `window` object. Think of the window as the browser window. The `window` contains the entire DOM document. All components of your HTML file will be accessible from within the window.
  + The `window` object has a large number of properties that return information about the object. Below are a few examples.

```js
window.document;
//returns the entire HTML document

window.innerWidth;
// returns the inner width of the browser window. Open a console in the browser and enter this. Then shrink the browser window and run it again. You should get a different value.

window.innerHeight;
// returns the inner height of the browser window.
```

### **Document**

  + The `document` object represents any web page loaded in the browser. The `document` contains all the nodes that represent the HTML elements of the page. We use the `document` object to traverse through the HTML and manipulate elements.
  + There are many `document` properties that allow us to obtain information about the `document` programmatically.

```js
document.all;
// returns all the nodes inside the document object

document.contentType;
// returns the type of content contained. Most web pages should return "text/html"

document.URL;
// returns the URL of the document object
```

Below the document are all the nodes representing the HTML on
the page.

## Explore How To Access the DOM with JavaScript

We can alter the DOM several different ways:

1. Add/remove HTML elements in the page.
  + You can add elements with functions like `appendChild`.
  + You can remove elements with the similarly named `removeChild`.
  + Both of these functions can be called on any node in the DOM tree.
2. Add/remove/change HTML attributes.
  + If you have a DOM node called `element`, `element.attributes` gives you access to its attributes.
  + You can remove attributes with `removeAttribute`.
3. Add/remove/change CSS styles.
  + You can modify any DOM node's `style` property.

We can select HTML elements in the document with JavaScript and jQuery:

```js
document.getElementsByTagName("p");
//returns all p tags on a page

// alternatively, we could do
document.querySelectorAll('p');

// the results of these two functions
// are the same in this example, but as
// we'll see later, getElementsByTagName
// and querySelectorAll have different uses
```

The DOM will become increasingly important as we use JavaScript to
manipulate our sites.

## Resources

+ [MDN DOM Introduction](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
+ [MDN Document Properties](https://developer.mozilla.org/en-US/docs/Web/API/Document)
+ [MDN EventTarget.addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

## Conclusion

We covered the basics of the Document Object Model and outlined its tree
structure. We then dived into the different ways we can use JavaScript to modify
page elements, including adding/removing/changing HTML elements, HTML attributes
and CSS styles, and listening for or creating events. This fundamental
understanding of the DOM will be useful as we work more with JavaScript.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-jquery-dom-reading'>The DOM</a> on Learn.co and start learning to code for free.</p>
