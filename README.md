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
<img src="https://www.sample.com/image.jpg" alt="family">
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


### Writing CSS


Lets try the 3 different methods out. Experiment and see if you can get some different styles to apply with any of the 3 methods





