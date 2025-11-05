CSS (Cascading Style Sheets) controls how HTML elements look — their colors, layout, fonts, and responsiveness.


 HTML = Structure


 CSS = Style


 JS = Functionality



 How to Add CSS
There are three ways to use CSS:
 Inline CSS
<p style="color: blue;">This is inline styled text.</p>

 Internal CSS
<style>
  p { color: red; font-size: 18px; }
</style>

 External CSS
<link rel="stylesheet" href="style.css">

 Best Practice: Always use external CSS for clean and reusable code.

 CSS Syntax
selector {
  property: value;
}

Example:
h1 {
  color: green;
  text-align: center;
}


 Colors, Fonts, and Text
body {
  background-color: #f0f0f0;
  color: #333;
  font-family: Arial, sans-serif;
}

h1 {
  color: royalblue;
  text-transform: uppercase;
}

p {
  font-size: 18px;
  line-height: 1.6;
  text-align: justify;
}


Box Model
Every HTML element is a box made of:
+-----------------------+
|      Margin           |
|  +-----------------+  |
|  |     Border      |  |
|  | +-------------+ |  |
|  | |  Padding    | |  |
|  | | +---------+ | |  |
|  | | | Content | | |  |
|  | | +---------+ | |  |
|  | +-------------+ |  |
|  +-----------------+  |
+-----------------------+

Example:
div {
  margin: 20px;
  padding: 15px;
  border: 2px solid black;
  background-color: lightyellow;
}


 CSS Selectors
SelectorExampleDescriptionElementp {}Selects all <p> tagsID#header {}Selects element with id="header"Class.btn {}Selects all elements with class="btn"Universal* {}Selects all elementsGrouph1, h2, h3 {}Selects multiple tags
Example:
#title { color: red; }
.text { font-style: italic; }


 Backgrounds
body {
  background-color: lightblue;
  background-image: url('bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}


 Borders and Shadows
div {
  border: 2px solid black;
  border-radius: 10px;
  box-shadow: 2px 2px 10px gray;
}


 Display & Position
div {
  display: inline-block;
  position: relative;
  top: 20px;
  left: 50px;
}

 Common values for display:


block


inline


inline-block


flex


grid


none



 Flexbox (Modern Layout)
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.box {
  background: tomato;
  color: white;
  padding: 20px;
  margin: 10px;
}

 Flexbox helps align and distribute space dynamically — great for responsive layouts!

 CSS Grid
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}

.item {
  background: skyblue;
  padding: 20px;
  text-align: center;
}


 Responsive Design (Media Queries)
@media (max-width: 600px) {
  body {
    background-color: lightcoral;
  }
  h1 {
    font-size: 20px;
  }
}

 Try resizing your browser — the background and font size will change below 600px.

 CSS Transitions
button {
  background-color: blue;
  color: white;
  padding: 10px;
  transition: background-color 0.3s;
}

button:hover {
  background-color: darkblue;
}


 CSS Animations
@keyframes move {
  from { transform: translateX(0); }
  to { transform: translateX(100px); }
}

div {
  width: 100px;
  height: 100px;
  background: red;
  animation: move 2s infinite alternate;
}


 Z-Index (Layering Elements)
.box1 { position: absolute; z-index: 1; }
.box2 { position: absolute; z-index: 2; }

 Higher z-index → appears above others.

 Opacity and Filters
img {
  opacity: 0.8;
  filter: grayscale(50%);
}


 Gradients
div {
  background: linear-gradient(to right, red, yellow);
}


 Useful CSS Properties
PropertyExampleDescriptioncolorcolor: blue;Text colorbackground-colorbackground-color: pink;Backgroundmarginmargin: 10px;Outer spacepaddingpadding: 10px;Inner spaceborderborder: 1px solid black;Element borderwidth / heightwidth: 200px;Sizefont-sizefont-size: 20px;Text sizetext-aligntext-align: center;Align text

 Mini Project — Profile Card
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profile Card</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f4f4f4;
    }

    .card {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
      width: 250px;
    }

    .card img {
      border-radius: 50%;
      width: 100px;
      height: 100px;
    }

    .card h2 {
      color: #333;
    }

    .card p {
      color: gray;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="card">
    <img src="https://via.placeholder.com/100" alt="Profile">
    <h2>Rao Muhammad Faizan</h2>
    <p>Web Developer | Designer</p>
  </div>
</body>
</html>





✨ Star this Repo if You Like This CSS Guide!

Would you like me to make the JavaScript course (next) in the same GitHub README style (with code + preview sections)?
