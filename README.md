**Creating a Year Calculator App with HTML, CSS, and JavaScript**


Introducing the AgeCraft App! Ever wondered about the precise duration of your existence? Dive into this tutorial where we'll guide you to craft a sleek web application that instantly calculates your age in years, months, days, hours, and minutes. Unleash your coding prowess and let's make time tangible! 🚀 #AgeCraft #WebDevMagic

## **HTML Structure**

We start by setting up the basic structure of our app using HTML. Save the following code in an `index.html` file:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <!-- Meta tags, title, and CSS link -->
</head>

<body>
  <main class="container" role="main">
    <div class="content">
      <!-- Input fields for day, month, and year -->
      <!-- Calculate button -->
      <!-- Display results -->
    </div>
  </main>
  <footer class="attribution" role="contentinfo">
    <!-- Attribution text -->
  </footer>
  <script src="./assets/js/main.js"></script>
</body>

</html>
```

Customized Styling with CSS

Let's add a touch of uniqueness to our app by applying some creative CSS styles. Open the style.css file and replace the placeholder with the following code:

/* style.css */

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f5f5f5;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  padding: 20px;
  text-align: center;
}

h1 {
  color: #333;
}

input {
  padding: 10px;
  margin: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  padding: 10px 20px;
  background-color: #4caf50;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #45a049;
}

Enhanced Functionality with JavaScript

Let's bring more life to our app by refining the JavaScript functionality. Open the main.js file and replace the placeholder with the following code:

// main.js

function calculateAge() {
  var birthdate = new Date(document.getElementById('birthdate').value);
  var currentDate = new Date();

  var ageInMilliseconds = currentDate - birthdate;
  var ageInSeconds = ageInMilliseconds / 1000;

  var years = Math.floor(ageInSeconds / (365.25 * 24 * 60 * 60));
  var months = Math.floor((ageInSeconds % (365.25 * 24 * 60 * 60)) / (30.44 * 24 * 60 * 60));
  var days = Math.floor((ageInSeconds % (30.44 * 24 * 60 * 60)) / (24 * 60 * 60));
  var hours = Math.floor((ageInSeconds % (24 * 60 * 60)) / (60 * 60));
  var minutes = Math.floor((ageInSeconds % (60 * 60)) / 60);

  document.getElementById('result').innerHTML = `
    <p>Years: ${years}</p>
    <p>Months: ${months}</p>
    <p>Days: ${days}</p>
    <p>Hours: ${hours}</p>
    <p>Minutes: ${minutes}</p>
  `;
}

Complete App Integration

Replace the placeholders in your HTML file with the actual code snippets. Your users will now experience an interactive and uniquely styled Year Calculator App.

Feel free to explore further customization options, add animations, or incorporate additional features to make the app even more engaging. The world of web development is vast, and this project is just the beginning of what you can create. 
Enjoy coding! ☕️