

# Simple HTML Page with Dialogflow Integration

This project is a basic HTML web page that displays a "Hello World!" heading, the current time, and integrates a **Dialogflow chatbot** using Google's `df-messenger` component.

---

## Project Structure

```
project-root/
│
├── index.html         # Main HTML file (provided)
├── script.js          # JavaScript to display current time
├── styles.css         # Optional CSS for styling
└── README.md          # Project documentation
```

---

## Features

###  HTML Features

* Displays a simple "Hello World!" heading.
* Shows current time dynamically using JavaScript.
* Uses a separate CSS file (`styles.css`) for custom styling.

### Chatbot Integration

* Integrates **Dialogflow Messenger** for real-time chatbot interactions.
* Uses the `df-messenger` web component provided by Google.
* Auto-loads with the **WELCOME** intent.

---

## How It Works

### 1. **Time Display**

* JavaScript (`script.js`) updates the `<p>` element with ID `currentTime` to show the current local time.

### 2. **Dialogflow Chatbot**

* Loads the Dialogflow Messenger widget via Google’s `bootstrap.js`.
* Connects to a Dialogflow agent with this ID:
  `8e0a0596-c9b9-41e8-bda9-84be99e901a5`
* Automatically triggers the **WELCOME** intent on page load.

---

## How to Run

1. Clone/download the repository or copy the files to your local system.
2. Open `index.html` in any modern web browser (Chrome, Edge, Firefox).
3. Make sure you’re connected to the internet to load the Dialogflow widget.

---

## File Details

### `index.html`

```html
<h1 class="title">Hello World!</h1>
<p id="currentTime"></p>
<script src="script.js"></script>
```

### `script.js`

> This script dynamically updates the time shown on the page.

```js
document.addEventListener("DOMContentLoaded", () => {
  const timeElement = document.getElementById("currentTime");
  const updateTime = () => {
    const now = new Date();
    timeElement.textContent = `Current Time: ${now.toLocaleTimeString()}`;
  };
  updateTime();
  setInterval(updateTime, 1000);
});
```

### `styles.css` (Optional Example)

```css
.title {
  color: navy;
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}
```

---

##  Requirements

* Internet connection (for Dialogflow widget to load)
* A browser that supports Web Components (Chrome, Firefox, Edge, Safari)

---

##  Notes

* To use your own Dialogflow agent, replace the `agent-id` in the `<df-messenger>` tag with your Dialogflow agent's ID.
* Ensure the agent is deployed and accessible publicly via the Dialogflow Console.

---

## 📤 Author & Usage

This is a beginner-friendly template for integrating Dialogflow into any HTML page. You can extend it with advanced styling, custom intents, or more complex logic as needed.



