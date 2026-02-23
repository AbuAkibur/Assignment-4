1. Difference between getElementById, getElementsByClassName, querySelector / querySelectorAll?
   Answer: They are all element selectors from HTML, and CSS.
   Differences between them are:
   a. getElementById selects one elements from HTML.
   b. getElementsByClassName selects many from class in HTML.
   c. querySelector selects CSS first match, selects first one element.
   d. querySelectorAll selects ALL matches in CSS.

2. How do you create and insert a new element into the DOM?
   Answer: I will create and element, add content to it and insert into page.

Example:
const p = document.createElement("p");
p.textContent = "Hello Mama";
document.body.appendChild(p);

Now a paragraph will show up on page.

3. What is Event Bubbling?
   Answer: When a event happens like click on elements, it hits on elements, eventually go to element's parent then document automatically. And event goes upward
   Example: When you click a button
   button> div > body All receive the events in this sequence.

4. What is Event Delegation? Why useful?
   Answer: Event Delegation means put event on parent. Instead of adding listener separately on to many elements like buttons, add one on parent.
   Usefulness:
   a. Faster.
   b. Less code. Instead of adding listener separately on to many buttons, adding one on parent needs less code.
   c. Works for new elements. You can add this to new elements.

5. Difference between preventDefault() and stopPropagation() ?
   Answer: They do different things.
   preventDefault() stops browser default actions.
   Example: HTML: <a href="https://google.com" id="myLink">Go to Google</a>
   JS: document.getElementById("myLink").addEventListener("click", function(e) {
   e.preventDefault(); // stops link opening
   console.log("Link click prevented");
   });

Stops a link from opening or a form from refreshing the page.

stopPropagation() Event bubble won't take place.
Example: HTML: <div id="parent" style="padding:20px; background:lightblue;">
Parent
<button id="child">Click Me</button>

</div>
CSS: document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});

document.getElementById("child").addEventListener("click", () => {
console.log("Button clicked");
});

Stops the click from reaching the parent elements.
