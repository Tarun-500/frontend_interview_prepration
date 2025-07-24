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
 




<details>
  <summary> <h3> 45)  Inline, Inline-Block, and Block Elements in HTML </h3></summary>
 
HTML has **three main display types**:
1. **Inline** → Stays in the same line, does not start a new line.
2. **Inline-Block** → Stays in the same line but allows width & height adjustments.
3. **Block** → Takes up the full width and starts on a new line.

---

  🔹 **2. Inline Elements**
  
  ✅ Takes only as much space as needed.
  ✅ Does **not** start a new line.
  ❌ Cannot change height & width.
  
  #### **✅ Example:**  
  ```html
  <p>This is <span style="background-color: yellow;">inline</span> text.</p>
  ```
  ✔ `span` is an **inline element**, so the next text stays on the same line.
  
  #### **✅ Common Inline Elements:**  
  `<a>, <span>, <strong>, <em>, <label>, <img>`  

  🔹 **2. Inline-Block Elements**
  
  ✅ Stays in the same line like inline elements.
  ✅ Allows setting **width & height**.
  
  #### **✅ Example:**  
  ```html
  <span style="display: inline-block; width: 100px; height: 50px; background-color: lightblue;">Inline-Block</span>
  ```
  ✔ Now, `span` is **inline-block**, so width & height will work.
  
  #### **✅ Common Inline-Block Elements:**  
  `<input>, <button>` (by default), or any element with `display: inline-block;`
 
  🔹 **3. Block Elements** 
  
  ✅ Always starts **on a new line**.
  ✅ Takes up **full width**.
  ✅ Allows height & width changes.
  
  #### **✅ Example:**  
  ```html
  <div style="background-color: lightgreen; width: 200px; height: 50px;">Block Element</div>
  ```
  ✔ `div` is a **block element**, so it takes the full width and moves the next element to a new line.
  
  #### **✅ Common Block Elements:**  
  `<div>, <p>, <h1> - <h6>, <section>, <article>, <form>`  


  ### **✅ Conclusion**
✔ **Inline** → Only takes necessary space, stays in the same line.
✔ **Inline-Block** → Stays in the same line but allows width & height adjustments.
✔ **Block** → Takes full width and starts on a new line.

**Use the right element type for better webpage design! 🚀**

</details>

 

<details>
 <summary> <h3> 46)  How Does HTML Work? </h3></summary>
  ❌ **No, HTML Does Not Need a Compiler!**
  
  HTML is a **markup language**, **not** a programming language. It does **not** need a compiler like C, Java, or Python. Instead, **browsers directly read and render** HTML.
 🔹 **How Does HTML Work?** 
  
  1️⃣ **You write HTML code** in a `.html` file.  
  2️⃣ **A web browser (like Chrome, Firefox)** reads the file.  
  3️⃣ **The browser interprets** the HTML and displays the web page.  

  #### ✅ **Example:**
  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>My Web Page</title>
  </head>
  <body>
      <h1>Hello, World!</h1>
  </body>
  </html>
  ```
  ✔ You just **open this file in a browser**, and it works—**no compilation needed!**
 
  <summary>🔹 **Why No Compiler?**</summary>
  
  ✔ **HTML is interpreted** by browsers, not compiled.  
  ✔ **It is not a programming language**, so it doesn't create executable files.  
  ✔ **Changes are instantly visible**—just refresh the page!  

  
### **✅ Conclusion**
🚀 **HTML does not require a compiler** because browsers **directly interpret** and display it. Just write, save, and open in a browser! 🎉
</details>





<details>
 <summary> <h3> 47)  Difference Between `window` and `document` in JavaScript </h3></summary>
  🔹 **What is `window`?**
  
  ✅ `window` is the **global object** that represents the browser window.  
  ✅ It includes **everything** related to the browser (like history, location, and alerts).  
  
  #### ✅ **Example:**
  ```javascript
  console.log(window.innerWidth); // Gets the browser window width
  window.alert("Hello!"); // Shows an alert pop-up
  ```
  ✔ `window.innerWidth` gives the width of the browser window.  
  ✔ `window.alert()` shows an alert box.

  
 🔹 **What is `document`?** 
  
  ✅ `document` represents the **web page content (HTML & CSS)** inside the browser.  
  ✅ It allows access to **HTML elements** like `<div>`, `<p>`, etc.  
  
  #### ✅ **Example:**
  ```javascript
  console.log(document.title); // Gets the title of the page
  document.body.style.backgroundColor = "lightblue"; // Changes background color
  ```
  ✔ `document.title` gets the webpage title.  
  ✔ `document.body.style.backgroundColor` changes the background color.
  
 🔹 **Key Differences** 
  
  | Feature      | `window` | `document` |
  |-------------|---------|------------|
  | Represents  | Browser window | Web page (HTML) |
  | Includes    | Browser properties like history, location, alert | HTML elements (DOM) |
  | Example    | `window.innerWidth` (window size) | `document.getElementById()` (selects an element) |
  | Usage      | Works with the whole browser | Works with webpage content |

  ### **✅ Conclusion**
✔ `window` → Represents the **browser window** (history, alert, location).  
✔ `document` → Represents the **web page content** (HTML elements).  

🚀 **Use `window` for browser-related tasks and `document` for webpage manipulation!**
</details>





 <details>
  <summary> <h3> 48) What is Web Accessibility? </h3> </summary>
  <small>
**Web Accessibility means making websites usable for everyone, including people with disabilities.** The goal is to ensure that everyone can **access web content** without difficulties.
  🔹 **Why is Web Accessibility Important?** 
  
  ✅ **Helps disabled users** (like blind, deaf, or people with motor disabilities) access websites.  
  ✅ **Improves SEO** since accessible sites are easier for search engines to understand.  
  ✅ **Legal compliance** – Many countries have laws requiring web accessibility (like ADA in the USA).  
  ✅ **Enhances User Experience (UX)** for everyone.  

  
 🔹 **How to Improve Web Accessibility?** 
  
  **1️⃣ Alt Text for Images:**  
   - Adding `alt="image description"` helps **screen readers** describe images for blind users.  
   - **Example:**  
     ```html
     <img src="photo.jpg" alt="A beautiful sunset over the ocean">
     ```

  **2️⃣ Keyboard Navigation:**  
   - Every functionality should work **without a mouse**, using only the keyboard (Tab, Enter).  
   - **Example:**  
     ```html
     <button tabindex="0">Click Me</button>
     ```

  **3️⃣ ARIA (Accessible Rich Internet Applications):**  
   - Provides extra information for **screen readers** to improve accessibility.  
   - **Example:**  
     ```html
     <button aria-label="Close Popup">X</button>
     ```

  **4️⃣ High Contrast Mode:**  
   - Ensures **better visibility** for users with color blindness or weak eyesight.  
   - **Example:**  
     ```css
     body { color: black; background-color: white; }
     ```

  **5️⃣ Captions & Transcripts for Videos:**  
   - Provides text alternatives for **deaf users** who cannot hear the audio.  
   - **Example:**  
     ```html
     <video controls>
       <source src="video.mp4" type="video/mp4">
       <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
     </video>
     ```
   
     ### **✅ Conclusion**
      ✔ **Web accessibility is important for everyone** – disabled users, SEO, and better UX.  
      ✔ **Using alt text, keyboard support, ARIA, high contrast, and captions can improve accessibility.**  
      ✔ **An accessible website provides a better experience for all! 🚀**
     
     </small>
</details> 




<details>
 <summary> <h3> 49) Difference Between <code><iframe></code> and  <code>< embed > </code> in HTML  </h3> </summary>
 <small>

### 🔹 `<iframe>` (Inline Frame)
- **Purpose**: Used to embed another **HTML page or external website** into the current page.
- **Full document embedding**.
- Can show content like web pages, maps, YouTube, etc.

#### ✅ Example:
```html
<iframe src="https://www.example.com" width="600" height="400"></iframe>
```
#### 🧠 Features:
- Can be styled using CSS.
- Can include scrollbars.
- You can interact with the embedded content (via JavaScript, `postMessage`, etc.).

---

### 🔹 `<embed>`
- **Purpose**: Used to embed **external content** like **PDFs, videos, or flash files** (non-HTML content).
- More suitable for **media files or plugins**.

#### ✅ Example:
```html
<embed src="file.pdf" width="600" height="400" type="application/pdf">
```

#### 🧠 Features:
- Minimal customization.
- Lightweight for static content.
- Doesn't support complex interactions like `<iframe>`.

---

### ✅ Summary Table
| Feature        | `<iframe>`                     | `<embed>`                          |
|----------------|--------------------------------|------------------------------------|
| Content Type   | Entire webpage or HTML content| Media files (PDF, videos, etc.)    |
| Interaction    | High (JS, messages, etc.)     | Low                                |
| Use Case       | Embed web apps/sites           | Show documents, media              |
| Customization  | CSS styling, scroll, JS access| Limited                            |

---

### ✅ Conclusion
Use `<iframe>` when you need to embed **interactive webpages**.  
Use `<embed>` when showing **non-interactive media files** like **PDFs or videos**. 🚀
 </small>
</details>






<details>
 <summary> <h3> 50) noscript tag use in html  </h3> </summary>

 

### Use of `<noscript>` Tag in HTML

The `<noscript>` tag in HTML is used to define content that will be displayed **only if the user’s browser does not support JavaScript or if JavaScript is disabled**.

---

#### Key points about `<noscript>` tag:

- **Purpose:** Show alternative content or messages when JavaScript is not available.
- **Usage:** Inside `<body>`, anywhere you want fallback content.
- **Typical uses:**  
  - Inform users to enable JavaScript for better experience.  
  - Provide alternative navigation or content that works without JavaScript.

---

#### Example:

```html
<noscript>
  <p>Please enable JavaScript to use this website properly.</p>
</noscript>
```
</details>




<details>
 <summary> <h3> 56) 🌍 Hreflang Tag in SEO </h3> </summary>
<small>
 ### 📝 Summary

| Feature      | Hreflang Tag                           |
|--------------|--------------------------------------|
| Used For     | Language & region targeting           |
| Placed In   | `<head>` tag or HTTP header           |
| SEO Impact   | Avoids duplicate content, improves targeting |
| Works With   | Google, Yandex (not supported by Bing, Yahoo) |

---

### ❓ What is the Hreflang Tag?

The `hreflang` tag is an HTML attribute used to tell search engines **what language and geographical target** your webpage is intended for. It's useful when you have **multiple versions of a page** for different languages or regions.

---

### ✅ Why is it Important?

- Helps **Google serve the correct version** of a page to users based on their location/language.
- Avoids **duplicate content issues** across translated/localized versions of the same page.
- Improves **user experience** by showing content in the user's preferred language.

---

### 🧩 Syntax

```html
<link rel="alternate" hreflang="x" href="url" />

<link rel="alternate" hreflang="en" href="https://example.com/en/" />
<link rel="alternate" hreflang="fr" href="https://example.com/fr/" />
<link rel="alternate" hreflang="es" href="https://example.com/es/" />

```
</small>
</details>




<details>
 <summary> <h3> 50)  HTML <code> template </code>   Tag - Easy Definition & Use </h3> </summary>
 <small>
## **Definition**
The `<template>` tag in HTML is a special container that holds HTML content but does not render it until JavaScript is used to insert it into the DOM.

#### **Why Use `<template>`?**
- Improves performance by reducing unnecessary re-renders.
- Allows reusable HTML structures.
- Content inside `<template>` is ignored by the browser until needed.

#### **Example Usage**

``` 
<template id="myTemplate">
    <p>This is a hidden template!</p>
</template>

<button onclick="showTemplate()">Show Template</button>
<div id="container"></div>

<script>
    function showTemplate() {
        let template = document.getElementById("myTemplate");
        let clone = template.content.cloneNode(true);
        document.getElementById("container").appendChild(clone);
    }
</script>
```

#### **Key Features**
- **Not Rendered Initially:** Content inside `<template>` is not displayed until JavaScript activates it.
- **Reusable:** One template can be used multiple times without repeating the HTML code.
- **Efficient DOM Manipulation:** Helps optimize performance by reducing direct modifications to the DOM.

#### **Use Cases**
- Dynamically adding elements (e.g., Todo lists, Shopping cart items).
- Creating reusable components in vanilla JavaScript.
- Loading HTML content only when needed for better performance.

 </small>   
</details>




### 51) Explain and use inert attribute. When will you use it?

### 52) Create a semantic and accessible collapsible FAQ section using HTML only.

### 53) How do you prevent screen reader from reading decorative images?

 

### 54) What is a Canonical Tag in HTML and why is it important for SEO?
 
A **canonical tag** (`<link rel="canonical">`) is an HTML element placed in the `<head>` section of a webpage. It is used to tell search engines which version of a page is the **preferred ("canonical") version** when there are **multiple pages with similar or duplicate content**.

It helps to:
- Avoid **duplicate content issues**
- **Consolidate SEO ranking signals** to a single URL
- Improve **crawl efficiency** for search engines

---

## 🛠️ Syntax

```html
<link rel="canonical" href="https://example.com/main-page/" />
```

### 55) ✅ Open Graph (OG) Tags

### 🔹 What are OG Tags?

Open Graph (OG) tags are HTML `<meta>` tags that control how your webpage appears when shared on social media platforms like Facebook, LinkedIn, etc.

They allow you to define:
- Title
- Description
- Image
- URL
- Content type

---

### 🧩 Basic Syntax

```html
<meta property="og:title" content="Your Page Title" />
<meta property="og:description" content="Short summary of your page" />
<meta property="og:image" content="https://example.com/image.jpg" />
<meta property="og:url" content="https://example.com/page" />
<meta property="og:type" content="website" />
<meta property="og:site_name" content="Your Website Name" />

## 🔀 Canonical vs Open Graph Tags

| Feature         | Canonical Tag                                      | Open Graph Tag                                         |
|-----------------|----------------------------------------------------|--------------------------------------------------------|
| **Purpose**     | Avoid duplicate content (SEO)                      | Improve link previews on social platforms              |
| **Format**      | `<link rel="canonical" href="...">`               | `<meta property="og:*" content="...">`                |
| **Target**      | Search engines (Google, Bing, etc.)                | Social media platforms (Facebook, LinkedIn, etc.)      |
| **Key Use**     | Point to the main/original version of the content  | Customize how your content appears when shared         |
| **Location**    | Inside `<head>`                                    | Inside `<head>`                                        |
| **Affects**     | SEO indexing, duplicate content handling           | Visual representation, engagement on shares            |
| **Example Tool**| Google Search Console                              | Facebook Sharing Debugger, LinkedIn Post Inspector     |

---

### ✅ Summary:

- **Canonical Tags** are used to tell search engines the **preferred version** of a page to avoid SEO penalties from duplicate content.
- **Open Graph Tags** are used to control how your web page **looks when shared** on social media, like the image, title, and description shown in the preview.
```

