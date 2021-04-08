# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) CODE IN ONE DAY: HTML & CSS BOOTCAMP

![](/images/html-css-js.png)

#### Goals:
- Basics of the internet and how webpages work
- Syntax of HTML and CSS
- Building common types of websites including landing pages and marketing sites
- Principles of front-end code organisation and project structure
- How to get your website live on the internet
- Build a basic web page from scratch
- Modify the code of existing websites
- Deploy a website to the internet

## Introduction
### Who am I?
**Kyle Liu**

### Who are you?
- Name
- Where are you from?
- What you do?
- Why are you taking this class?

## A little bit about the World Wide Web
Just about everyone has accessed a website. Its typical as a normal user that you type a web address and your page changes to the website you expect, but what is actually happening here? 
![](/images/client-server.png)
What is happening is a client/server request and response. The client will make a request usually using a web address and the request will travel to that company's server and respond with a HTML page. 

## What makes up a website
The 3 languages of a website are HTML, CSS, and Javascript. We will not be covering Javascript today but we will still be able to create a website with just HTML and CSS. Often referred to as a static site, a static website is one that has web pages stored on the server in the format that is sent to a client web browser. It is primarily coded in Hypertext Markup Language (HTML); Cascading Style Sheets (CSS) are used to control appearance beyond basic HTML. 

## HTML
### What is Hyper Text Markup Language(HTML)?
HTML is a markup language for creating webpages/documents. Its one of the building blocks for the web. It is **NOT** a programming language. A basic programming language will be able to decide between 2 things, ex if something do this, if not do that. HTML cannot do that, its strictly presentational. This does not mean HTML is not important, it is very important.

Every website returns some sort of HTML page. Nowadays there are all types of technologies that have advanced web programming with different programming languages but it all still boils down to HTML. Just to make things clear we will be working with HTML version 5 or HTML5.

[Feel free to read up on the history of HTML here](https://en.wikipedia.org/wiki/HTML)

### Lets Get Started
#### Web Browser
- Google Chrome (What were using in class)
- Mozilla Firefox
- Safari
- Microsoft Edge (newer versions)
- Internet Explorer (discouraged)

#### Text Editor
- Visual Studio Code (what were using in class)
- Sublime Text
- Atom

#### Creating a HTML file
Couple things to note:
- File must end with .html extension
- Runs in a web browser
- index.html is the root/home page of a website by default. For example:

    Accessing: www.example.com/
    > Loads the `index.html` file

    Accessing: www.example.com/sample.html
    > Loads the `sample.html` file

You can think of Google Chrome as a program that can open files with an `.html` extension. Like Microsoft Word is program that can open files with a `.docx` extension.

Lets open up our own file:
1. Create a folder on your computer, feel free to label it whatever you like
2. Open VS Code and go to the menu options to open the folder. `File > Open...` and select the folder you just created. It should be empty
3. Now click on the left hand side of the VS Code Window and select the document icon ![](/images/document-icon.png)
4. With the pane open you can either select the new file icon ![](/images/new-file.png) or right click and select `New File`
5. Go ahead and type in `index.html` and press enter. You have now created a HTML file

#### Writing HTML (elements)
HTML is made of elements. These elements are what structure a webpage. Below is a HTML Element:
```html
<h1>Hello Friend!</h1>
```

As you can see, the `h1` element is made up of:
- an opening `<h1>` tag
- the text content of `Hello Friend!`
- a closing `</h1>` tag

This `h1` tag is the largest of heading tags, its used to define the most important heading. You can select from `<h1>` down to `<h6>`. Feel free to try it out and notice the changing of size in your text.

Self closing tag:
```html
<br/>
```
- a special tag that does not need a closing tag
- does not contain any content between tags like normal tags would
- `/` goes at the end of the single tag before the `>`
- Remnant of XHTML, closing slashes are no longer needed in HTML5

There are many tags with the intention of organization and convention to display content in your HTML file. Here are some commonly used tags:
| Tag | Name |
| --- | --- |
| `<h1>` to `<h6>` | Heading |
| `<p>` | Paragraph |
| `<button>` | Button |
| `<br/>` | Line Break |
| `<a>` | Anchor |
| `<ul>` & `<li>` | Unordered List & List Item |
| `<body>` | Body |
| `<hr>` | Horizontal Rule |
| `<img>` | Image |
| `<div>` | Division |


### HTML Vocabulary

**HTML element (or simply, element)** — a unit of content in an HTML document formed by HTML tags and the text or media it contains.

**HTML Tag** — the element name, surrounded by an opening (<) and closing (>) angle bracket.

**Opening Tag** — the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.

**Content** — The information (text or other elements) contained between the opening and closing tags of an HTML element.

**Closing tag** — the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.

### HTML File Layout
![](/images/html-structure.png)

A typical HTML page will look something like this:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h1>Hello Friend</h1>
    </body>
</html>
```

Lets break this down:
- This represents the version of HTML we are working with which is HTML5
```html
<!DOCTYPE html>
```

- The head tag contains the document title, scripts, styles, meta information, and other resources that help the HTML look and behave as expected. The `title` tag will display on the website's tab description. More on [UTF-8](https://www.w3schools.com/tags/att_meta_charset.asp), [X-UA-Compatible](https://stackoverflow.com/questions/6771258/what-does-meta-http-equiv-x-ua-compatible-content-ie-edge-do), [viewport](https://www.w3schools.com/css/css_rwd_viewport.asp)
```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

- The body tag contains the content that shows up on the page (often will contain more but for this example is very minimal)
```html
<body>
    <h1>Hello Friend</h1>
</body>
```

Also take note everything is wrapped inside a `<html></html>` tag of course.

### HTML Hierarchy
Elements can be nested within other elements
```html
<div>
    <h1>Hello Friend</h1>
    <p>Hello Elliot</p>
</div>
```

### Attributes
Attributes are values placed inside your opening tags. The most common one you will probably encounter is `class`. We will not go over it just yet but it will help us with CSS later on. Lets look at some tags with attributes to help us display images and links.

#### Anchor
The anchor tag is written simply as `<a></a>` but it also has a larger purpose and that is to display and create links for an user to access. 
```html
<a href="https://www.google.com">Google</a>
```
In this example, the `<a>` tag has allowed us to create a link and access Google. The attribute here is: 

**`href="https://www.google.com"`**
- `href` is the name
- `"https://www.google.com"` is the value

#### Images
The image tag as it is named, is used to display an image. Note that due to no content going within the tags, the image tag is self closing.
```html
<img src="https://i.kym-cdn.com/entries/icons/facebook/000/021/807/ig9OoyenpxqdCQyABmOQBZDI0duHk2QZZmWg2Hxd4ro.jpg" alt="hackerman">
```
Again speaking about attributes, we have 2 attributes, `src` and `alt`
- `src` is used to tell your image tag where the image is located, so a file path or website link would work
- `alt` is used for screen readers and is used to describe the image

## CSS
### What is Cascading Style Sheet(CSS)?
As said before, CSS is used to style HTML elements. This will allow for different colors, layouts, designs, etc. for what you see on the HTML page. CSS is a bit more artistic so there are many different ways to do the same thing. Keep in mind we will be learning more about syntax rather than styling and design trends

### 3 Methods for Adding CSS
- Inline CSS: Directly in the HTML element. Highly discouraged
```html
<p style="color: blue;">This is a paragraph.</p>
```
- Internal CSS: Using `<style>` tags within a single document
```html
<html>
<head>
    <style>
        h1 {
            color:red;
        }
        p {
            color:blue;
        }
    </style>
</head>
<body>
    <h1>A heading</h1>
    <p>A paragraph.</p>
</body>
</html>
```
- External CSS: Linking an external .css file in the `<head>` tag
```html
<head>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
```
### Creating a CSS file
Couple things to note:
- File must end with .css extension
- If separated out from HTML, must be linked to the HTML file with a `<link>` tag

### Breaking Down CSS
![](/images/css-syntax.png)

Which is the same as writing it like this:
```css
h1 {
    color: yellow;
    font-size: 11px;
}
```
Keep in mind that you need semicolons after each property/value

### Writing CSS
Lets try the 3 different methods out. Experiment and see if you can get some different styles to apply with any of the 3 methods

#### Colors
You are able to write colors in the following was in CSS:
- Color Names (ex. yellow, green, blue)
- [HTML5 Color Names](https://www.w3schools.com/colors/colors_names.asp) (ex. coral, aqua)
- [Hexadecimal](https://www.w3schools.com/colors/colors_picker.asp) (ex. #F0F8FF)
- [RGB](https://www.w3schools.com/colors/colors_picker.asp) (ex. `rgb(0, 0, 255)`)

Examples:
```css
h1 {
    background-color: coral;
    color: rgb(0, 0, 255);
}
h2 {
    background-color: #F0F8FF;
}
```

#### Fonts
To change your font, you want to use the property `font-family`. You can list different fonts to ensure maximum compatibility browsers/operating systems. Start with the font you want, and end with a generic family (to let the browser pick a similar font in the generic family, if no other fonts are available). The font names should be separated with comma. More about [font-family](https://www.w3schools.com/css/css_font.asp) and [web safe fonts](https://www.w3schools.com/css/css_font_websafe.asp)

Example:
```css
h1 {
  font-family: "Times New Roman", Times, serif;
}
```
**Google Fonts**

Google fonts is a great resource to find different fonts you would like to use. They also provide the necessary `link` and even an example of how to write in CSS
![](/images/google-font.png)
HTML File:
```html
<head>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Train+One&display=swap" rel="stylesheet">
</head>
```
CSS File:
```css
h1 {
    font-family: 'Train One', cursive;
}
```

**Font Related Styling**
| Property | Values | Example |
| --- | --- | --- |
| text-align | left, center, right, justify | `text-align: center;` |
| text-transform | uppercase, lowercase, capitalize | `text-transform: uppercase;` |
| text-decoration | none, underline | `text-decoration: underline;` |
| letter-spacing | px, em, rem | `letter-spacing: 1px;` |
| font-weight | normal, bold | `font-weight: bold;` |
| font-style | regular, italic | `font-style: italic;` |
| font-size | px, em, rem | `font-size: 1em;` |


#### Pseudo Classes
Pseudo-classes are ways to target not just an element, but a specific state of an element

| Pseudo Class | State | Example |
| --- | --- | --- |
| `:hover` | When the mouse hovers an element | a:hover |
| `:focus` | When the mouse clicks inside an input field | input:focus |
| `:visited` | After a link has been previously visited | a:visited |
Example:
```css
a:hover {
    background-color: gray;
}
```

### Classes and Ids
**DRY** - Don't Repeat Yourself

Why should we practice writing "DRY" code?
- Performance: Having repeated code will lead to longer scripts. Longer scripts take up more memory and will take more time to load, which can make a website seem slow.

- Maintainability: Imagine that we have the same line of code repeated 10 times in our program. If we ever want to change that functionality, we would have to search for all 10 places where that code is repeated and make 10 individual changes

#### Classes
Classes are used to group elements together so a class can be applied multiple times in one HTML document. Multiple classes can be applied to one element.

Classes are easy to write, on your HTML file be sure to write an attribute called `class` with any name you would like for the class. On your CSS file, to target that element, the selector with start with a `.` and the name you gave your class.

Multiple classes can also be set on an element separated by a space.

HTML File:
```HTML
<span class="heading">Hello Elliot</span>
<p class="clothes anotherClass">Black Sweater</p>

<span class="heading">Hello Darlene</span>
<p class="clothes">Sunglasses</p>
```

CSS File:
```css
.heading {
    font-size: 20px;
    font-weight: 3px;
}
.clothes {
    font-style: italic;
}
.anotherClass {
    font-weight: bold;
}
```

#### Ids
Ids are used to target one specific element, so each element can only have one id, and each id can only be used once in an HTML document. 

Writing ids are very similar to classes. The attribute on the HTML side will be `id` and the CSS selector will start with a `#` instead.

HTML File:
```HTML
<span class="heading">Hello Elliot</span>
<p class="clothes">Black Sweater</p>
<p id="pet">QWERTY</p>

```

CSS File:
```css
#pet {
    color: blue;
}
```

### Other Ways to Target
Here are other common ways to target elements in CSS. They will also provide more specific control on where you want to apply your styling
| Selector | Example | Example description
| --- | --- | --- |
| .class1.class2 | `.name1.name2` | Selects all elements with both `name1` and `name2` set within its class attribute |
| .class1 .class2 | `.name1 .name2` | Selects all elements with `name2` that is a descendant of an element with `name1` |
| element,element | `div, p` | Selects all `<div>` elements and all `<p>` elements |
| element element | `div p` | Selects all `<p>` elements inside `<div>` elements |
| element>element | `div > p` | Selects all `<p>` elements where the parent is a `<div>` element |

[More CSS Selectors](https://www.w3schools.com/cssref/css_selectors.asp) 


#### Tips about HTML and CSS
- Use descriptive classes/ids
- Use camelCase or snake-case for classes/ids (names with spaces won't work)
- Be consistent in formatting and naming
- Don't repeat yourself (DRY)

### Box Model & Layouts
#### Block Elements
![](/images/box-model.png)
Every element is by default considered a box with four parts:
- Content: The content of the box where text and images appear
- Padding: Area between content and border
- Border: A border that goes around the padding
- Margin: Area between border and neighboring elements


#### Margin and Padding
Margin and padding can be used to position elements and create layout:

![](/images/margin.png)


Margin and padding can be added to all four sides at once:

![](/images/all-sides.png)


#### Display
The display property is used to change whether an element displays as `none`,`inline`, `inline-block`, or `block`
Example:
```css
li {
    display: inline-block;
}
```
**Block**

The `block` value can be applied to inline elments so that they stack and acquire properties like `width`, `height`, `padding`, and `margin`.

Elements displayed with `block` extend the length of the element to the end of the page.
![](/images/display-block.png)

**Inline**

Setting an element to `inline` would cause them to sit next to each other or have them on the same line. They would in turn lose properties such as `width`, `height`, `padding`, and `margin`.
![](/images/display-inline.png)

**Inline-Block**

Setting a block or inline element to `inline-block` causes the element to flow like an inline element, while being able to set a `width`, `height`, `padding`, and `margin`.

![](/images/display-inline-block.png)

#### Position
The `position` property specifies the type of positioning method used for an element. There are five different position values:

- `static`: not positioned in any special way, positioned according to the normal flow of the page 
- `relative`: is positioned relative to its normal position
- `fixed`: is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled
- `absolute`: is positioned relative to the nearest positioned ancestor (similar to fixed)
- `sticky`: is positioned based on the user's scroll position (used less comonly)


## Deploying a Project (GitHub Pages)
We will be using GitHub to deploy our project. This is not the only way to deploy a project but it is a free and very quick way to do so. Deploying just means assigning a URL/domain to your website and making it publicly accessible.

You could use sites like https://domains.google/ or https://www.godaddy.com/ to purchase your domain. You can even set up the purchased url to be hosted for free on GitHub pages.

### What is GitHub?
An online version control service for code. It uses a technology called git. Think of how Google Docs keeps track of everyone who’s made changes to a document, with the ability to go back to a previous version. GitHub is Google Docs for code.

GitHub is also like a social media for engineers, to share their projects with the world.

It also offers its users a free hosting service for static sites. It can host sites that are front-end only (no backend data). If all you need is HTML, CSS, JavaScript, we can use it!

### GitHub Deployment
1. Go to github.com and signup for an account
2. In the upper-righthand corner, there is a plus (+) symbol. Click on it and then click on New Repository from the dropdown.
3. In the field under Repository Name enter username.github.io. For example, if your GitHub username is janesmith, you’ll enter janesmith.github.io of the Repository name field. (You can find your username in the dropdown under Owner to the left of the Repository Name field).
4. Go ahead and check Initialize this repository with a README. This isn’t necessary, but it gives you a file that you can use to describe your project if you’d like.
5. Click Create Repository
6. Find the Upload Files button and click it.
7. Drag your website folder into the appropriate area. Make sure it contains all of your files (.html, .css, etc)
8. Once everything is uploaded, click Commit Changes
9. Open up a new browser and navigate to the website username.github.io

## Reference Pages
Mozilla Developer Network
W3Schools
CSS-Tricks

## Which Developer Role Is Right for Me?
![](/images/developers.png)

## Keep Learning!
[GA Dash](https://dash.generalassemb.ly/)
[codecademy](https://www.codecademy.com/learn)
[freecodecamp](https://www.freecodecamp.org/)

## Q&A
NEVER BE AFRAID TO ASK QUESTIONS

## My Contact Info
kyle116@yahoo.com