


# My First Blog Project

## Overview  
This is my first blog project, created using **HTML, CSS, and JavaScript**. It features a responsive design, a clean layout, and an easy-to-read format for blog posts.  

## Features  
- Responsive design for all devices  
- Structured blog layout  
- Interactive navigation  
- Deployed on **Netlify**  

## Live Demo 
[https://web-design-blog-project.netlify.app/]  

## Technologies Used
- **HTML** – For the structure  
- **CSS** – For styling and responsiveness  
- **JavaScript** – For interactive elements  

## How to Use 
1. Visit the **Live Demo** link above.  
2. Browse through different blog posts.  
3. Enjoy a clean and minimalistic reading experience!  

## Acknowledgments 
Special thanks to **Anisul Islam's tutorials** for guidance in CSS.  

---

Let me know if you want any modifications!


#### 1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?

- #### Answer: 
   **Difference:**

    1. **getElementById** allows to access the specific element by using JavaScript DOM MODEL. ID should be unique in    JavaScript. If multiple ID with same name **getElementById** will return first One Only. If no id found it will return null.
  
     2. **getElementsByClassName** allows to access all elements which have same className. **getElementsByClassName** give a  array like collection of elements. Html collection can be accessed by name, id or index. We can conduct **for loop** on those elements. If no className found it will return empty array of htlml collection. Html collection is live because it updates if any changes in DOM.
 
     3. **querySelectorAll** allows to access all  elements which match css selector. By **querySelector** we can access elements as like css. Which we can not do by **getElementById** and **getElementsByClassName**. It gives a  array like collection of nodes.Nodelist can be accessed only through by index number. Nodelist is Static it does not update even if the DOM changes.
 
     4. **querySelector** allows to access element by using css selector as like ** querySelectorAll**. But access only first element of given css selector.
 

#### 2. How do you **create and insert a new element into the DOM**?

- #### Answer: 
   I can create a new element by using DOM creation methods: **document.createElement**.
 
  I can insert a new element into the DOM by using **appendChild**.

  **Example:**
  
 ```javascript
  
   // Create Element
   const div = document.createElement('div');

   // Insert Element into a container
   callHistoryContainer.appendChild(div);

```

#### 3. What is **Event Bubbling** and how does it work?

- #### Answer: 
    When an event is triggered on child elements.First of All it propagates from root element to child elements. After this it propagates again go back upwards through DOM tree from child to parent. This upwards propagation is called ***event bubbling.*** During event bubbling it executes all event listner from child to upwards parents.
    
    Example:
    
    ```html
    
    <div id="container">
     <ul id="ul-lists">
      <li id="list-item"></li>
     </ul>
    </div>
    ```
    ```javascript
    document.getElementById('list-item').addEventListner('click', function() {
      
      console.log('list item clicked')
    } )
     
     document.getElementById('ul-lists').addEventListner('click', function() {
      
      console.log('Unordered clicked')
    } )

    document.getElementById('container').addEventListner('click', function() {
      
      console.log('container clicked')
    } )

```

  **Output:**
    -list item clicked
    -Unordered clicked
    -container clicked

   if I clicked on list-items. first it executes list items addEventListner then it go upwards by event bubbling and executes ul-list event listner and container event listner.
