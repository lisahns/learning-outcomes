# fac learning-outcomes
 
## 1. Git
- Why do we use git?
git is a version control, helping us to track progress in a project and enabling us to return to previous version if something breaks
- What’s the difference between Git and GitHub?
git is the version control system and GitHub is a platform where code can be hosted
- What happens when you clone a repository?
it gets cloned either locally or remotely, with a connection to the repo
- What happens when we do git pull origin main?
changes are being pulled form the main branch
-  How do we create a new branch on our local machine?
git checkout -b name-of-branch (creates new branch and switches to it)
- How do we control which changes will be included in the next commit?
git add file-name -> will only commit changes in the files listed
- When might git add . be inappropriate?
does not track deletions, instead use git add -A
-  What does git push origin [branch-name] do?
pushes changes from specific branch
- Why should you review your teammates’ pull requests?
they might have added bugs without noticing, or maybe even code that could break the application. 

## 2. HTML
- Why is accessibility important?
it is important to make website and online applications accessible to as many people as possible. Some people might have trouble accessing certain services, due to mobile or sensory impairments.
- How can you quickly find simple accessibility problems?
Chrome Lighthouse, using tab to navigate a website, using a reader
- What is semantic HTML?
describes the meaning of elements to the browser. this makes some things more accessible or has default functionalities, such as form.
- Why is it important to use the “correct” semantic element?
accessibility, functionalities, avoiding weird behaviour in the browser
- What is the <form> element used for?
anything user-input related
 
 ## 3.CSS
 - How would you use CSS variables to make a reusable colour palette?
 declaring the variable in the root element:
 * {
 --primary: #f7d0db;
 }
 using it in elements:
 body {
 background-color: var(--primary);
 }
 - How would you use flexbox to make elements sit on a single line?
 display:flex;
 flex-direction:row;
 - How would you use grid to make a layout that automatically adds columns as the screen gets wider?
 display:grid;
 grid-template-columns: repeat( auto-fit, minmax(200px, 1fr) );
 - Why is it important to create a responsive design?
 there are so many different screen-sizes and devices and it is important to provide working services to all of them, which responsive design enables us to do.
 - How would you structure your CSS to make it “mobile-first”?
 start designing the website for a phone screen first and then work my way up to bigger designs. I would write media queries for a few important breakpoints.
 /* phones */
@media screen and (max-width: 480px) {
 /* css rules here */
}
 other breakpoints:
 /* large tablets & laptops */ (max-width: 1024px)
 /* desktop */ (min-width: 1025px)

 ## 4. JavaScript
 - Why should we avoid using var to define variables?
 var is an outdated keyword, it is better to use const or let. Something about the scope of var, but need research on that
 - How might you make a long, complex chunk of code easier to read?
 see if I can make any parts re-usable, so write functions that I then call instead of repeating code.
 Breaking the code down into smaller pieces and functions
 - What is a “callback”?
 a function that calls another function
 
 ## 5. Array methods
 - How would you use array.map() to create a new array with transformed values?
 .map() does not change the original array, therefore the result needs to be stored in a different array. create new array and push changes in
 - How would you use array.filter() to create a new array with certain values removed?
 same as above
 - How would you use array.find() to get a single value from an array?
 find returns the first truthy value
 
 ## 6. Promises & fetch
 - What is a promise?
 a pending object, that promises a result as soon as it as been received by an API
 - How do promises help manage asynchronous code?
 it helps to load js even if some of the code is not yet executable
 - What does a promise’s .then method return?
 an empty object
 - 
