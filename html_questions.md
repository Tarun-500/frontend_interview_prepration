### 1) API in HTML
### 2) Picture Tag  (srcset)
### 3) Explain Flex Box
### 4) Pseudo Element (placeholder, after, before) 
### 5) CSS Box Modal
### 6) Void Element (that do not need closing tag like input, br, img)
### 7) HTML entities (Symbol like &nbsp, &copy, @quot)
### 8) White Space in HTML 
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
### 20) Novalidate attribute (use for disabled validation in form)
### 21) Web Workers?
### 22) server-sent events in HTML5?
### 23) MathML element in HTML5?
### 24) HTML Graphics (Using canvas)
### 25) Output represents the result of a calculation? Could you explain its attributes?
### 26) Microdata in HTML5  (use for seo with itemscope  itemprop and itemtype attribute)
### 27) Web Storage in HTML5 (storage api - localstorage, sessionStorage)
### 28) Svg vs canvas
### 29) Which elements are used to represent output in HTML? Explain their use.
<small> ✅ Answer:
In HTML, there are 4 main output elements:
**` <output> `** – Used to display the result of a calculation.
**` <progress> `** – Shows task completion percentage.
**` <meter> `**  – Represents a value within a range (e.g., battery level).
**` <input type="range"> `** – Allows users to select a value using a slider.
</small>

### 30) What is the difference between **`<output>`** and **`<meter>`**?
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

### 31) How does **` <progress> `** work in HTML? Give an example.
✅ Answer:
<progress> element kisi task ka completion status show karta hai. Yeh mainly loading bars ya file upload progress dikhane ke liye use hota hai.

```
<label>File Upload Progress:</label>
<progress value="60" max="100"></progress>
```
 
Yeh 60% completed task show karega. Jaise jaise value update hoti hai, progress bar change hota hai.

### 32) How can we use **`<input type="range">`** with <output>?
<small>
✅ Answer:
  
**`<input type="range">`** ek slider provide karta hai jo numeric values ko select karne ke liye use hota hai. Isko <output> ke saath link karke real-time value display kar sakte hain.
  
  ```
 <label>Volume:</label>
<input type="range" min="0" max="100" value="50" oninput="result.value=this.value">
<output id="result">50</output>
```
</small>


### 33) HTML5 Important Questions & Answers

#### 1️⃣ What’s new in HTML5?
**Answer:**
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

---

