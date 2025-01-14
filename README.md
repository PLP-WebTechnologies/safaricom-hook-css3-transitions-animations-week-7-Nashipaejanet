### **Assignment: Building an Interactive and Dynamic Web Page**  

#### **Objective**  
Create a visually engaging and interactive webpage that utilizes **CSS3 transitions and animations**, **advanced JavaScript functions** (including scope, parameters, and return values), and combines **CSS animations with JavaScript** to create dynamic user interactions.  

---

### **Part 1: CSS3 Transitions and Animations**  
1. **Task**:  
   - Use **CSS transitions** to create smooth effects on hover or focus (e.g., buttons that change color or grow).  
   - Use **CSS animations** with `@keyframes` to create dynamic effects like fading, sliding, or rotating.  

2. **Requirements**:  
   - At least **two elements** must include hover or focus transitions.  
   - At least **two animations** must be created using `@keyframes` (e.g., an animated banner or an animated loading spinner).  

---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Webpage with CSS3 Transitions and Animations</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #f7f7f7;
    }
    
    /* Button with Hover Transition */
    .button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .button:hover {
      background-color: #45a049;
      transform: scale(1.1); /* Button grows when hovered */
    }

    /* Input field with Focus Transition */
    .input-field {
      padding: 10px;
      font-size: 16px;
      border: 2px solid #ddd;
      border-radius: 5px;
      margin: 20px 0;
      transition: border-color 0.3s ease;
    }

    .input-field:focus {
      border-color: #4CAF50; /* Border color changes on focus */
    }

    /* Keyframe Animation - Fade In */
    .fade-in {
      animation: fadeIn 2s ease-in-out forwards;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }

    /* Keyframe Animation - Rotate Spinner */
    .spinner {
      margin: 50px auto;
      border: 5px solid #f3f3f3;
      border-top: 5px solid #4CAF50;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      animation: spin 2s linear infinite;
    }

    @keyframes spin {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    /* Animated Banner */
    .banner {
      padding: 20px;
      background-color: #4CAF50;
      color: white;
      font-size: 24px;
      animation: slideIn 3s ease-out forwards;
    }

    @keyframes slideIn {
      0% {
        transform: translateY(-100%);
      }
      100% {
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <!-- Animated Banner -->
  <div class="banner">
    Welcome to the Interactive Webpage!
  </div>

  <!-- Button with Hover Effect -->
  <button class="button">Hover Me</button>

  <!-- Input Field with Focus Effect -->
  <input type="text" class="input-field" placeholder="Click or type here">

  <!-- Animated Spinner -->
  <div class="spinner"></div>

  <!-- Fade In Element -->
  <div class="fade-in">
    This element fades in after loading.
  </div>

</body>
</html>


### **Part 2: JavaScript Functions**  
1. **Task**:  
   - Write JavaScript functions to handle interactivity on the webpage.  
   - Utilize **parameters**, **return values**, and demonstrate an understanding of **scope**.  

2. **Requirements**:  
   - Write at least **three functions**:  
     - A function with parameters and return values (e.g., calculate a value like the area of a rectangle based on user input).  
     - A function that demonstrates the concept of scope (local vs. global variables).  
     - A function to toggle a CSS class that applies an animation (e.g., toggling a "hidden" class for a modal).  

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Webpage with JavaScript Functions</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #f7f7f7;
    }

    .button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .button:hover {
      background-color: #45a049;
      transform: scale(1.1);
    }

    .input-field {
      padding: 10px;
      font-size: 16px;
      border: 2px solid #ddd;
      border-radius: 5px;
      margin: 20px 0;
      transition: border-color 0.3s ease;
    }

    .input-field:focus {
      border-color: #4CAF50;
    }

    .fade-in {
      animation: fadeIn 2s ease-in-out forwards;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }

    .spinner {
      margin: 50px auto;
      border: 5px solid #f3f3f3;
      border-top: 5px solid #4CAF50;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      animation: spin 2s linear infinite;
    }

    @keyframes spin {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    .banner {
      padding: 20px;
      background-color: #4CAF50;
      color: white;
      font-size: 24px;
      animation: slideIn 3s ease-out forwards;
    }

    @keyframes slideIn {
      0% {
        transform: translateY(-100%);
      }
      100% {
        transform: translateY(0);
      }
    }

    /* Modal Hidden Class */
    .hidden {
      display: none;
    }

  </style>
</head>
<body>

  <div class="banner">
    Welcome to the Interactive Webpage with JavaScript Functions!
  </div>

  <button class="button" onclick="toggleModal()">Toggle Modal</button>

  <div id="modal" class="hidden">
    <div class="modal-content">
      <span onclick="toggleModal()">Close</span>
      <p>This is a modal.</p>
    </div>
  </div>

  <input type="text" class="input-field" placeholder="Click or type here" oninput="calculateArea()">

  <div class="spinner"></div>

  <div class="fade-in">
    This element fades in after loading.
  </div>

  <script>
    // Part 1: Function with parameters and return values
    function calculateRectangleArea(length, width) {
      return length * width; // Calculates the area of a rectangle
    }

    function calculateArea() {
      const length = 5; // Assume some fixed length value
      const width = parseFloat(document.querySelector('.input-field').value) || 0; // Get width from input
      const area = calculateRectangleArea(length, width);
      console.log('Rectangle Area:', area);
    }

    // Part 2: Function demonstrating the concept of scope (local vs. global variables)
    let globalVariable = 'I am a global variable';

    function demonstrateScope() {
      let localVariable = 'I am a local variable';
      console.log(globalVariable); // Can access global variable
      console.log(localVariable); // Can access local variable
    }

    demonstrateScope();
    console.log(globalVariable); // Can access global variable
    // console.log(localVariable); // Error: localVariable is not defined outside the function

    // Part 3: Function to toggle a CSS class for animations (e.g., toggle modal visibility)
    function toggleModal() {
      const modal = document.getElementById('modal');
      modal.classList.toggle('hidden');
    }
  </script>

</body>
</html>


### **Part 3: Combining CSS Animations with JavaScript**  
1. **Task**:  
   - Use JavaScript to trigger or control CSS animations dynamically.  

2. **Requirements**:  
   - Create an interactive element (e.g., a button, card, or slider) that triggers an animation when clicked.  
   - Dynamically add or remove CSS classes to control the animation.  
   - Ensure that the animation resets properly when triggered multiple times.  

---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Animations with JavaScript</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #f7f7f7;
    }

    /* Button to trigger animation */
    .button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .button:hover {
      background-color: #45a049;
    }

    /* Card style */
    .card {
      width: 200px;
      height: 300px;
      background-color: #fff;
      border: 1px solid #ddd;
      border-radius: 10px;
      margin: 20px auto;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    /* Animation: Shake */
    @keyframes shake {
      0% {
        transform: translateX(0);
      }
      25% {
        transform: translateX(-10px);
      }
      50% {
        transform: translateX(10px);
      }
      75% {
        transform: translateX(-10px);
      }
      100% {
        transform: translateX(0);
      }
    }

    /* Apply the shake animation */
    .shake-animation {
      animation: shake 0.5s ease-in-out;
    }
  </style>
</head>
<body>

  <button class="button" onclick="triggerAnimation()">Shake the Card!</button>

  <div class="card" id="card">
    <p>Card Content</p>
  </div>

  <script>
    function triggerAnimation() {
      const card = document.getElementById('card');

      // Remove the animation class if it exists (reset the animation)
      card.classList.remove('shake-animation');

      // Force a reflow to restart the animation
      void card.offsetWidth;

      // Add the animation class to trigger the animation
      card.classList.add('shake-animation');
    }
  </script>

</body>
</html>

