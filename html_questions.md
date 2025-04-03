### 1) API in HTML
### 2) Picture Tag  (srcset)
### 3) Explain Flex Box
### 4) Pseudo Element (placeholder, after, before) 
### 5) CSS Box Modal
### 6) Void Element (that do not need closing tag like input, br, img)
### 7) HTML entities (Symbol like &nbsp, &copy, @quot)
 
<details>
 <summary> <h3> 08) What is White Space in HTML?</h3> </summary> 

**White space** in HTML refers to **spaces, tabs, and new lines** that help structure the code but are usually ignored by the browser when displaying content.

---

### **🛠 Real-Life Example**  
Imagine typing a sentence with multiple spaces like this:
```
Hello       World!
```
The browser will display it as:
```
Hello World!
```
HTML **automatically removes extra spaces** unless we use special methods.

---

### **🔹 How to Preserve White Space?**  

#### **1️⃣ Using `&nbsp;` (Non-Breaking Space)**  
```html
<p>Hello &nbsp;&nbsp;&nbsp; World!</p>
```
✅ Keeps extra spaces between words.

#### **2️⃣ Using `<pre>` Tag**  
```html
<pre>
    This   text  keeps   spaces  and   line breaks.
</pre>
```
✅ Displays text exactly as written.

#### **3️⃣ Using CSS `white-space` Property**  
```css
p {
    white-space: pre;
}
```
✅ Makes spaces and line breaks visible.

---

### **🔹 Where is White Space Handling Used?**  
✔ **Formatting Code Blocks** → Shows code with indentation.  
✔ **Designing Layouts** → Adjusting space between elements.  
✔ **Preventing Text Wrapping** → Keeps words together in a single line.  

---

✅ **Conclusion:** White space helps structure HTML code but is usually ignored unless special techniques are used! 🚀

</details>



### 9) Map in HTML (Using Coords and area tag)
### 10) Absolute URL (https://google.com) and relative URL (/img/user.jpg)
### 11) Use of tile tag - (for worked like tooltip while hovering)
### 12) Form Input Fields in HTML (checkbox, button, radio, range, reset, password, email, color, date etc.)
### 13) Action attribute - use for targeting specific script or page after submitting data. 
### 14) Method attribute in HTML forms specifies the HTTP method (GET or POST) used to send form data to the server.
### 15) Way to Display Element in HTML  - (Display: inline, inline-block, block, none, table, grid, flex)
### 16) Figure Tag
### 17) datalist vs select 
### 18) DOCTYPE - Define HTML Version
### 19) HTML5 Semantic Elements (header, nav, main, section, article, aside, footer)
### 20) Novalidate attribute (use for disabled validation in form)?

<details>
 <summary> <h3> 21) What are Web Workers in JavaScript? </h3> </summary>

**Web Workers** allow JavaScript to run in the **background**, so your webpage doesn’t freeze when doing heavy tasks.

### **🛠 Real-Life Example**
Imagine you are ordering food online. While your order is being prepared (**background process**), you can still browse the menu (**main UI remains responsive**). Web Workers work the same way!

---

### **✅ Why Use Web Workers?**
✔ Prevents the webpage from **freezing**.  
✔ Runs **heavy calculations** in the background.  
✔ Makes web apps **faster & smoother**.  

---

### **🛠 Example: Using Web Workers**  

#### **1️⃣ Create a Web Worker File (`worker.js`)**
```js
// worker.js
self.onmessage = function (event) {
    let result = event.data * 2; // Perform some task
    postMessage(result); // Send result back
};
```

#### **2️⃣ Use the Web Worker in Main Script (`main.js`)**
```js
// main.js
let worker = new Worker("worker.js"); // Create worker

worker.postMessage(5); // Send data to worker

worker.onmessage = function (event) {
    console.log("Result from worker:", event.data); // Output: 10
};
```

---

### **🔹 Real-Life Uses of Web Workers**
✔ **Online Games** → Keeps the game smooth while processing moves in the background.  
✔ **Chat Apps** → Runs notifications & message updates without freezing the app.  
✔ **Data Processing** → Handles large calculations (e.g., encryption, image processing) without slowing the page.  

---

### **❌ Limitations of Web Workers**
- 🚫 **Cannot directly access the DOM** (HTML elements).  
- 🚫 **Not needed for small tasks**, use `setTimeout()` instead.

---

✅ **Conclusion:** Use Web Workers to keep web applications **fast & smooth** when handling **heavy tasks!** 🚀

</details>


<details>
 <summary> <h3>22) Server-Sent Events (SSE) in HTML5 </h3></summary>
 
**Server-Sent Events (SSE)** allow a server to **send updates to the browser automatically** without the browser repeatedly requesting them.

---

### **🛠 Real-Life Example**  
Imagine **live cricket scores** updating on a website without refreshing the page. SSE makes this possible!

---

### **✅ How SSE Works?**  
1️⃣ **Server Sends Data** → The server pushes updates to the browser.  
2️⃣ **Browser Receives Data** → The browser listens and updates the webpage.  

---

### **🛠 Simple Example**  

#### **1️⃣ Create a Server (`server.php`)**  
```php
<?php
header('Content-Type: text/event-stream');
header('Cache-Control: no-cache');

echo "data: " . date('h:i:s A') . "\n\n"; // Send current time
flush();
?>
```

#### **2️⃣ Connect SSE in HTML (`index.html`)**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Live Time Update</title>
</head>
<body>
    <h2>Current Time:</h2>
    <p id="time"></p>

    <script>
        let eventSource = new EventSource("server.php");

        eventSource.onmessage = function(event) {
            document.getElementById("time").innerText = event.data;
        };
    </script>
</body>
</html>
```

---

### **🔹 Where is SSE Used?**  
✔ **Live Sports Scores**  
✔ **Real-time Notifications**  
✔ **Stock Market Updates**  
✔ **Live Chat (One-Way Messaging)**  

---

✅ **Conclusion:** SSE is best for real-time updates **without refreshing the page!** 🚀

</details>

<details>
 <summary><h3> 23)  What is MathML in HTML5? </h3></summary>

**MathML (Mathematical Markup Language)** is used to display **mathematical equations** on web pages.

---

### **🛠 Real-Life Example**  
Imagine you are on a **study website** that shows a **math formula** like:  
✅ **Quadratic Formula:**  
\[
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\]
This can be written in **MathML** inside an HTML page!  

---

### **🔹 Simple Example: Writing a Math Formula**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>MathML Example</title>
</head>
<body>
    <h2>Quadratic Formula</h2>
    <math>
        <mi>x</mi>
        <mo>=</mo>
        <mfrac>
            <mrow>
                <mo>-</mo>
                <mi>b</mi>
                <mo>&#xB1;</mo>
                <msqrt>
                    <msup><mi>b</mi><mn>2</mn></msup>
                    <mo>-</mo>
                    <mn>4</mn><mi>a</mi><mi>c</mi>
                </msqrt>
            </mrow>
            <mrow>
                <mn>2</mn><mi>a</mi>
            </mrow>
        </mfrac>
    </math>
</body>
</html>
```

---

### **🔹 Where is MathML Used?**  
✔ **Online Education Websites** → To show math formulas easily.  
✔ **Scientific Articles** → Used in research papers.  
✔ **Engineering & Finance Websites** → For complex calculations.  

---

✅ **Conclusion:** MathML helps display **math formulas in web pages** just like text! 🚀
</details>

### 24) HTML Graphics (Using canvas)
### 25) Output represents the result of a calculation. Could you explain its attributes?
### 26) Microdata in HTML5  (use for SEO with itemscope  itemprop and itemtype attribute)
### 27) Web Storage in HTML5 (storage api - localstorage, sessionStorage)
### 28) Svg vs canvas?
### 29) What is the difference between <code> section </code> and <code>div </code> in HTML
### 30) Thematic block (example- section, article, header, footer, nav, aside)
### 31) What is the difference between <code> em </code> and <code> strong </code> tags in HTML?
### 32) What is the difference between <code> i </code> and <code> em </code> tags in HTML?
### 33) What is the difference between <code> localStorage </code> and <code>sessionStorage </code> in HTML?
### 34) What is the difference between <code>async </code> and <code> defer </code> in HTML?

<details>
 <summary> <h3> 35)  What is `aria-label` in HTML and Why is it Used? </h3> </summary>

`aria-label` is an **ARIA (Accessible Rich Internet Applications) attribute** that provides a text description for screen readers when an element does not have visible text. It improves accessibility by making web content more readable for visually impaired users.

### **📌 When to Use `aria-label`?**
- **Icons Without Text**: Buttons or links with only icons.
- **Buttons Without Text**: If a button lacks a visible label.
- **Hidden Labels**: Input fields or elements without a visible `<label>`.

### **🔹 Example 1: Icon Button Without Text**
```html
<button aria-label="Close">
  <img src="close-icon.png" alt="">
</button>
```
✅ Helps screen readers understand the purpose of the button.

### **🔹 Example 2: Search Icon Without Text**
```html
<button aria-label="Search">
  <i class="fa fa-search"></i>
</button>
```
✅ Allows screen readers to identify the button as a **Search** button.

### **🔹 Example 3: Input Field Without a Label**
```html
<input type="text" aria-label="Enter your email" placeholder="Email">
```
✅ Provides an accessible label for screen reader users.

### **✅ Benefits of `aria-label`**
- Enhances **accessibility** for visually impaired users.
- Provides **clear meaning** when a visible label is missing.
- Helps with **SEO and usability**.

**🔹 Best Practice:** Use a visible `<label>` whenever possible. Use `aria-label` only when a visible label is not feasible.
</details>



<details>
 <summary> <h3> 36) What is the difference between  <code>  div  </code> and <code>  span  </code> ? </h3> </summary>
  <small>
  <strong>  div (block level element) </strong>  - example -  p, h, div, section, article, footer, header, 

  <strong>  span (inline  element) </strong> - example - span, a, table, img, ul, form, 
  </small> 
</details>


<details>
 <summary> <h3> 37)   What is the difference between id and class attributes in HTML? </h3> </summary>
  <small>
  <strong>  id (Identifier): </strong>  A unique identifier for a single HTML element. It must be unique within the page.
  <strong>  class   (Class Name):  </strong> Used to apply styles to multiple elements that share the same class.
  </small> 
</details>



<details>
 <summary> <h3>38) Standard Mode vs Quirks Mode in HTML? </h3></summary>
**🔹 Standard Mode** → The browser follows **modern HTML & CSS rules** correctly.  
**🔹 Quirks Mode** → The browser behaves like **older versions** (before HTML5), causing inconsistencies.  

---

### **🛠 Real-Life Example**  
Imagine you are designing a webpage:  

✅ **Standard Mode:** The page looks the **same** in all modern browsers.  
❌ **Quirks Mode:** The page looks **different** because the browser tries to mimic old behavior.  

---

### **✅ How to Enable Standard Mode?**  
Use the **correct DOCTYPE** at the top of your HTML file:  
```html
<!DOCTYPE html>
<html>
<head>
    <title>Standard Mode Example</title>
</head>
<body>
    <p>This page runs in Standard Mode!</p>
</body>
</html>
```
✅ **With `<!DOCTYPE html>`, the browser uses Standard Mode.**  

---

### **❌ What Triggers Quirks Mode?**  
If **DOCTYPE is missing or incorrect**, the browser may switch to **Quirks Mode** and cause:  
- **Incorrect layouts** (CSS issues).  
- **Inconsistent box models** (padding/margins behave unpredictably).  
- **Font & image size issues** (older rendering methods).  

---

### **🔹 How to Check Mode in a Browser?**  
1️⃣ Open **DevTools (F12)** → **Console** → Type:  
```js
console.log(document.compatMode);
```
✔ If it shows `"CSS1Compat"`, it's **Standard Mode**.  
✔ If it shows `"BackCompat"`, it's **Quirks Mode**.  

---

### **✅ Conclusion**  
🔹 Always use `<!DOCTYPE html>` to ensure **modern, predictable** webpage rendering! 🚀
</details>



<details>
 <summary> <h3>39)  Which elements are used to represent output in HTML? Explain their use. </h3></summary>
 <small> ✅ Answer:
In HTML, there are 4 main output elements:
**` <output> `** – Used to display the result of a calculation.
**` <progress> `** – Shows task completion percentage.
**` <meter> `**  – Represents a value within a range (e.g., battery level).
**` <input type="range"> `** – Allows users to select a value using a slider.
</small>
</details> 
 


<details>
 <summary> <h3> 40) What is the difference between **`<output>`** and **`<meter>`**? </h3></summary>
  <small>
 ✅ Answer:
  
**`<output>`** – Yeh kisi calculation ka final result show karta hai, jaise ki sum ya average.
**`<meter>`** – Yeh ek value ko predefined range ke according graphically represent karta hai, jaise battery level ya CPU usage.
Example:
  
 ```
<label>Sum:</label>
<output>50</output>

<label>Battery Level:</label>
<meter value="0.8" min="0" max="1"></meter>
```
Yahan <output> ek static result show kar raha hai.
<meter> ek visual indicator provide kar raha hai jo value ke range ko dikhata hai.

</small>
</details> 


<details>
 <summary> <h3> 41)  How does **` <progress> `** work in HTML? Give an example. </h3> </summary>
  <small>
   <progress> element kisi task ka completion status show karta hai. Yeh mainly loading bars ya file upload progress dikhane ke liye use hota hai.

```
<label>File Upload Progress:</label>
<progress value="60" max="100"></progress>
```
 
Yeh 60% completed task show karega. Jaise jaise value update hoti hai, progress bar change hota hai.
  </small>
</details>



 <details>
<summary> <h3> 42) How can we use **`<input type="range">`** with <output>? </h3> </summary>
<small>
✅ Answer:
  
**`<input type="range">`** ek slider provide karta hai jo numeric values ko select karne ke liye use hota hai. Isko <output> ke saath link karke real-time value display kar sakte hain.
  
  ```
 <label>Volume:</label>
<input type="range" min="0" max="100" value="50" oninput="result.value=this.value">
<output id="result">50</output>
```
</small>
 </details>
 

 <details>
  <summary> <h3> 43) What’s new in HTML5? </h3></summary>
  <small>
   HTML5 introduced several new features to enhance web development. Some of the key improvements are:

#### **1. New Semantic Elements**
- `<header>` – Defines the header section of a page.
- `<footer>` – Represents the footer section.
- `<article>` – Contains independent, self-contained content.
- `<section>` – Groups related content together.
- `<aside>` – Used for side content like ads or sidebars.
- `<nav>` – Defines navigation links.
- `<figure>` & `<figcaption>` – Used for images with captions.

#### **2. Improved Forms & Input Types**
- **New Input Types:** `email`, `url`, `date`, `time`, `number`, `range`, `search`, `tel`, `color`.
- **New Attributes:** `placeholder`, `autofocus`, `required`, `pattern`, `autocomplete`, `formnovalidate`.
- **Datalist Support:** `<datalist>` provides input suggestions.
- **Output Element:** `<output>` is used for displaying calculation results.

#### **3. Enhanced Multimedia Support**
- `<audio>` – Embeds audio files directly.
- `<video>` – Allows video playback without Flash.
- `<track>` – Adds subtitles or captions.
- `<source>` – Supports multiple media formats for compatibility.

#### **4. Advanced Graphics & Animations**
- `<canvas>` – Used for drawing graphics and animations using JavaScript.
- **SVG (Scalable Vector Graphics)** – Defines vector-based graphics that scale without losing quality.
- **WebGL** – Enables 3D graphics rendering.

#### **5. New JavaScript APIs**
- **Geolocation API** – Retrieves the user's location.
- **Web Storage API (LocalStorage & SessionStorage)** – Stores data in the browser without cookies.
- **Drag & Drop API** – Enables drag-and-drop functionality.
- **WebSockets** – Allows real-time communication between client and server.
- **Web Workers** – Runs background scripts without blocking the main thread.
- **Fetch API** – Provides a modern way to make HTTP requests (replacing AJAX).

#### **6. Mobile-Friendly Features**
- **Viewport Meta Tag** – Helps create responsive designs for different screen sizes.
- **Touch Event API** – Detects touch gestures for mobile interaction.
- **Responsive Image Support** – Uses `<picture>` and `srcset` to load different images based on screen size. 
  </small>
 </details>



 <details>
  <summary> <h3> 44) ** What are the Limitations of HTML?** </h3> </summary>

HTML ek **markup language** hai jo **webpages ka structure** define karti hai, **lekin isme kuch limitations** hain. Chalo inhe samajhte hain:

---

### **🔹 1. No Dynamic Functionality**  
❌ HTML **sirf static** hota hai, iska matlab yeh **user interaction** (like button click pe action) nahi handle kar sakta.  
✅ **Solution:** JavaScript use karo taaki webpage interactive ho sake.  

---

### **🔹 2. No Database Connectivity**  
❌ HTML **database se direct connect nahi** ho sakta, yani yeh **data store ya fetch** nahi kar sakta.  
✅ **Solution:** PHP, Node.js jese **backend languages** ka use karo.  

---

### **🔹 3. Limited Styling Options**  
❌ HTML sirf **page ka structure** banata hai, **design aur styling** ke liye zyada options nahi deta.  
✅ **Solution:** CSS ka use karo taaki page **achha dikh sake**.  

---

### **🔹 4. Not Secure**  
❌ HTML code **sabko easily visible** hota hai aur koi **security features** nahi provide karta.  
✅ **Solution:** HTTPS, authentication aur secure backend coding ka use karo.  

---

### **🔹 5. No Logic or Conditions**  
❌ HTML me **if-else conditions, loops ya calculations** nahi likh sakte.  
✅ **Solution:** JavaScript ya backend programming languages ka use karo.  

---

### **🔹 6. Responsive Design Issues**  
❌ Basic HTML me **automatically screen sizes adjust nahi hoti**.  
✅ **Solution:** CSS media queries aur Bootstrap jese frameworks use karo.  

---

### **✅ Conclusion**  
**HTML akela ek complete website nahi bana sakta!** Iske saath **CSS, JavaScript aur backend** languages ki zaroorat hoti hai taaki ek **fully functional website** ban sake. 🚀

 </details>
 
