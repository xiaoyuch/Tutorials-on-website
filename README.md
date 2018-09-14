# How to build a website
## Agenda
1. Introduction to HTML
2. Introduction to CSS
3. Introduction to JavaScript
4. Introduction to Server and Client, and Express in Node.js
5. On building a simple website

## Requirements
- A web browser
- A text editor (notepad is okay, VScode is suggested)
- Node.js

## 1. Introduction to HTML
>- HTML stands for Hyper Text Markup Language
>- HTML describes the structure of Web pages using markup
>- HTML elements are the building blocks of HTML pages
>- HTML elements are represented by tags
>- HTML tags label pieces of content such as "heading", "paragraph", "table", and so on
- Browsers do not display the HTML tags, but use them to render the content of the page
- An simple example of HTML file:
```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
    </head>
    <body>
        <h1>My First Heading</h1>
        <p>My first paragraph.</p>
    </body>
</html>
```
To use the above HTML file:
- Create a file named `[name].html`
- Copy and paste the above html code to the file, save it
- Double click on the html file and run it on your browser
- You only need to know the following tags if you 

Tags | Functionality
---|---
`<h1> - <h6>`|Heading
`<p>`	|Paragraph
`<i>`	|Italic
`<b>`	|Bold
`<a>`	|Anchor
`<ul>` & `<li>`	|Unordered List & List Item
`<blockquote>`	|Blockquote
`<hr>`	|Horizontal Rule
`<img>`	|Image
`<div>`	|Division

- Each tag has a few attributes, for example:

```
<a href="http://172.29.120.237:3000/Shirley">This is a link to literature review</a>
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">

```
- HTML Comment Tags
```
<!-- Write your comments here -->
```
---
## 2. Introduction to CSS
> - CSS stands for Cascading Style Sheets
> - CSS describes how HTML elements are to be displayed on screen, paper, or in other media
>- CSS saves a lot of work. It can control the layout of multiple web pages all at once
>- External stylesheets are stored in CSS files
![image](https://www.w3schools.com/css/selector.gif)
- Motivating example (from W3School)
```
<!DOCTYPE html>
<html lang="en">
<head>
<title>CSS Template</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, Helvetica, sans-serif;
}

/* Style the header */
header {
    background-color: #666;
    padding: 30px;
    text-align: center;
    font-size: 35px;
    color: white;
}

/* Create two columns/boxes that floats next to each other */
nav {
    float: left;
    width: 30%;
    height: 300px; /* only for demonstration, should be removed */
    background: #ccc;
    padding: 20px;
}

/* Style the list inside the menu */
nav ul {
    list-style-type: none;
    padding: 0;
}

article {
    float: left;
    padding: 20px;
    width: 70%;
    background-color: #f1f1f1;
    height: 300px; /* only for demonstration, should be removed */
}

/* Clear floats after the columns */
section:after {
    content: "";
    display: table;
    clear: both;
}

/* Style the footer */
footer {
    background-color: #777;
    padding: 10px;
    text-align: center;
    color: white;
}

/* Responsive layout - makes the two columns/boxes stack on top of each other instead of next to each other, on small screens */
@media (max-width: 600px) {
    nav, article {
        width: 100%;
        height: auto;
    }
}
</style>
</head>
<body>

<h2>CSS Layout Float</h2>
<p>In this example, we have created a header, two columns/boxes and a footer. On smaller screens, the columns will stack on top of each other.</p>
<p>Resize the browser window to see the responsive effect (you will learn more about this in our next chapter - HTML Responsive.)</p>

<header>
  <h2>Cities</h2>
</header>

<section>
  <nav>
    <ul>
      <li><a href="#">London</a></li>
      <li><a href="#">Paris</a></li>
      <li><a href="#">Tokyo</a></li>
    </ul>
  </nav>
  
  <article>
    <h1>London</h1>
    <p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
    <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
  </article>
</section>

<footer>
  <p>Footer</p>
</footer>

</body>
</html>

```
- An interesting toy example to show the power of CSS (from w3school)

```
<!DOCTYPE html>
<html>
<head>
<style> 
div {
    width: 100px;
    height: 100px;
    background-color: red;
    position: relative;
    -webkit-animation-name: example; /* Safari 4.0 - 8.0 */
    -webkit-animation-duration: 4s; /* Safari 4.0 - 8.0 */
    animation-name: example;
    animation-duration: 4s;
}

/* Safari 4.0 - 8.0 */
@-webkit-keyframes example {
    0%   {background-color:red; left:0px; top:0px;}
    25%  {background-color:yellow; left:200px; top:0px;}
    50%  {background-color:blue; left:200px; top:200px;}
    75%  {background-color:green; left:0px; top:200px;}
    100% {background-color:red; left:0px; top:0px;}
}

/* Standard syntax */
@keyframes example {
    0%   {background-color:red; left:0px; top:0px;}
    25%  {background-color:yellow; left:200px; top:0px;}
    50%  {background-color:blue; left:200px; top:200px;}
    75%  {background-color:green; left:0px; top:200px;}
    100% {background-color:red; left:0px; top:0px;}
}
</style>
</head>
<body>

<p><b>Note:</b> This example does not work in Internet Explorer 9 and earlier versions.</p>

<div></div>

</body>
</html>

```
---
## 3. Introduction to JavaScript
- Difference between Java and JavaScript
    - ==Difference between Togerson and Togerson Hall==
>- JavaScript is the programming language of HTML and the Web.
>- JavaScript is easy to learn.
- Four ways to use JavaScript
    - As an attribute:
    ``` 
    <button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
    ```
    - Within a `<script>` and `</script>` tag:
    ``` 
    <script>
        document.getElementById('demo').innerHTML = Date()
    </script>
    ```
    - As commands:
    ```
    graph LR
    F12-->BrowserConsole
    BrowserConsole-->InputCommands
    InputCommands-->Output
    ```
    - As independent file:
    ``` 
    <script src="main.js"></script>
    ```
- Fundamentals
    - Refer to [this link](https://www.w3schools.com/js/default.asp):

- An interesting example (from w3school):
    ```
    <!DOCTYPE html>
    <html>
    <style>
    #container {
      width: 400px;
      height: 400px;
      position: relative;
      background: yellow;
    }
    #animate {
      width: 50px;
      height: 50px;
      position: absolute;
      background-color: red;
    }
    </style>
    <body>
    
    <p>
    <button onclick="myMove()">Click Me</button>
    </p> 
    
    <div id ="container">
    <div id ="animate"></div>
    </div>
    
    <script>
    function myMove() {
      var elem = document.getElementById("animate");   
      var pos = 0;
      var id = setInterval(frame, 5);
      function frame() {
        if (pos == 350) {
          clearInterval(id);
        } else {
          pos++; 
          elem.style.top = pos + 'px'; 
          elem.style.left = pos + 'px'; 
        }
      }
    }
    </script>
    
    </body>
    </html>
    ```
---
## 4. Introduction to Server and Client, and Express in Node.js
### Server and Client models
![image](https://qph.fs.quoracdn.net/main-qimg-66c398359e7857d60d712d30ef63ad29)
- Client:
    - Always ==initiates requests to servers==.
    - Waits for replies.
    - Receives replies.
    - Usually connects to a small number of servers at one time.
    - Usually interacts directly with end-users using any user interface such as graphical user interface.
- Server:
    - Always ==wait for a request== from one of the clients.
    - Serve clients requests then replies with requested data to the clients.
    - A server may communicate with other servers in order to serve a client request.
    - If additional information is required to process a request (or security is implemented), a server may request additional data (passwords) from a client before processing a request.
    - ==End users typically do not interact directly with a server, but use a client==. Which means you cannot hack the server! :)
### Node.js and express
- Download Node.js [here](https://nodejs.org/en/download/). Remember to allow the administrative permission request!
- After having Node.js installed:
    - Open `cmd` on windows or `terminal` on Linux/macOS
    - Create a folder and enter the folder by executing 
    ```
      npm install express -g
      npm install express-generator -g
    ```
    - Execute 
    ```
      express [app_name]
    ```
    - Now if you check the files in the folder "myapp", you will see a `package.json` file, which is used to download the necessary packages when building a server for website
    ```json
    {
      "name": "app",
      "version": "0.0.0",
      "private": true,
      "scripts": {
        "start": "node ./bin/www"
      },
      "dependencies": {
        "cookie-parser": "~1.4.3",
        "debug": "~2.6.9",
        "express": "~4.16.0",
        "http-errors": "~1.6.2",
        "jade": "~1.11.0",
        "morgan": "~1.9.0"
      }
    }

    ```
    - Now install Express in the myapp directory and save it in the dependencies list. For example: 
    ```
        cd [app_name]
        npm install
    ```
    - The dependancies will be installed. Then you can start a web server by executing:
    ```
        npm start
    ```
    And now you can click on the following link to log on your website: [link](localhost:3000)
    
    Folder | Functionality
    ---|---
    `/bin`| for starting server (including the port on listening)
    `/public`| store the static resources you want to send to the clients
    `/routes`| store the functions which determine how will the server respond to requests
    `/views`| store the template `.jade` files
    `app.js`| entry script of starting server

---
## 5. On building a simple website
- We will build a simple website which has two webpages:
    - `/animation`: a webpage which plays a simple animation we created before
    - '/map': a visualization webpage which presents the interactable map of the United States based on an open source library `echarts`
