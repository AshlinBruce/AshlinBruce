<!DOCTYPE html>

<html>

<head>

<title>Circular Menu</title>

<style>

.circle-container {

position: relative;

width: 300px;

height: 300px;

margin: 40px auto;

border-radius: 50%;

background-color: #f0f0f0;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);

}

.circle {

position: absolute;

top: 50%;

left: 50%;

transform: translate(-50%, -50%);

width: 250px; /* Increased size */

height: 250px; /* Increased size */

border-radius: 50%;

background-color: #fff;

box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);

}

.menu-button {

position: absolute;

top: 50%;

left: 50%;

transform: translate(-50%, -50%);

width: 60px; /* Increased size */

height: 60px; /* Increased size */

border: none;

border-radius: 50%;

background-color: #4CAF50;

color: #fff;

cursor: pointer;

font-size: 18px; /* Increased font size */

transition: background-color 0.3s;

}

.menu-button:hover {

background-color: #3e8e41;
}

.menu-button:nth-child(n+2) {

transform: translate(-50%, -50%) rotate(calc(360deg / 10 * (var(--i)))) translate(120px)

rotate(calc(-360deg / 10 * (var(--i))));

}

.settings-button {

width: 80px; /* Increased size */

height: 80px; /* Increased size */

background-color: #f44336;

color: #fff;

font-size: 20px; /* Increased font size */

z-index: 2;

position: relative;

}

.settings-button:hover {

background-color: #d32f2f;

}

</style>

</head>

<body>

<div class="circle-container">

<div class="circle">

<!-- Home Button in the Center -->

<button class="menu-button settings-button" id="settings-btn">Home</button>

<!-- Circular Menu Buttons -->

<button class="menu-button" id="btn1" style="--i:0;">Delete</button>

<button class="menu-button" id="btn2" style="--i:1;">SMS</button>

<button class="menu-button" id="btn3" style="--i:2;">Music</button>

<button class="menu-button" id="btn4" style="--i:3;">Tools</button>
<button class="menu-button" id="btn5" style="--i:4;">Gmail</button>

<button class="menu-button" id="btn6" style="--i:5;">XAMPP</button>

<button class="menu-button" id="btn7" style="--i:6;">Cam</button>

<button class="menu-button" id="btn8" style="--i:7;">SOS</button>

<button class="menu-button" id="btn9" style="--i:8;">Clock</button>

<button class="menu-button" id="btn10" style="--i:9;">Wi-Fi</button>

</div>

</div>

<script>

const buttons = document.querySelectorAll('.menu-button');

buttons.forEach((button, index) => {

button.addEventListener('click', () => {

if (button.id === 'settings-btn') {

// Home button: Open a new tab with the welcome message

const welcomeHtml = `<html><body><h1>Welcome Ashlin

Bruce</h1></body></html>`;

const newWindow = window.open();

newWindow.document.write(welcomeHtml);

newWindow.document.close();

} else if (button.id === 'btn9') { // Clock button

const now = new Date();

const formattedDate = now.toLocaleDateString();

const formattedTime = now.toLocaleTimeString();

const dateTimeHtml = `<html><body><h1>Date and

Time</h1><p>${formattedDate}</p><p>${formattedTime}</p></body></html>`;

const newWindow = window.open();

newWindow.document.write(dateTimeHtml);

newWindow.document.close();

} else if (button.id === 'btn2') { // SMS button

const messageHtml = `<html><body><h1>Message</h1><p>Hi Sir, how are

you?</p><p>Have a great day!</p></body></html>`;

const newWindow = window.open();

newWindow.document.write(messageHtml);
newWindow.document.close();

} else {

alert(`${button.textContent} button clicked!`);

}

});

});

</script>

</body>

</html>
