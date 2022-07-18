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
 - How could you chain promises together to avoid “callback hell”?
 using promises (.then()) helps us to avoid "callback hell"
 - How would you handle a fetch request that failed to get a response from the server?
 .error() can help us to show throw an error in case it failed
 - How would you handle a fetch request that received a 404 response from the server?
 check internet connection. And if connection is stable check the link, because it seems it might not be available
 
 ## 7. HTTP
 - What is an HTTP request?
 An HTTP request is made by a client, to a named host, which is located on a server.
 - What kind of request is sent when you click a link in your browser?
GET
 - What kind of request is sent when you submit a form in your browser?
 POST
 - What is an HTTP response?
 data exchange
 -  What does the status code of an HTTP response tell us?
dicate whether a specific HTTP request has been successfully completed. 
    Informational responses (100–199)
    Successful responses (200–299)
    Redirection messages (300–399)
    Client error responses (400–499)
    Server error responses (500–599)
- What are HTTP methods for?
 to indicate the desired action to be performed for a given resource
 - What kind of request should have a GET method?
 eturns a representational view of a resource's contents and data. GET should be used in read-only mode, which keeps the data safe and the resource idempotent. 
 - What kind of request should have a POST method?
 When creating a subordinate resource in a collection, applying POST to the parent resource prompts it to create a new resource, associate it with the proper hierarchy and return a dedicated URL for later reference. However, keep in mind that POST is not idempotent; you can't use this method more than once and expect a consistent outcome or result.
 - What kind of request should have a DELETE method?
 When a DELETE method targets a single resource, that resource is removed entirely.
 - What is the “body” of an HTTP request for?
 
 -What is the “body” of an HTTP response for?
 
 
 ## 8. DOM
 -  How would you get a reference to a DOM element in your JS?
 .querySelector("html tag")
 - How would you get references to multiple DOM elements at once in your JS?
 .querySelector(".classname")
 - How would you update properties of a DOM element?
 .getAttribute() 
 .setAttribute().
 - What’s the difference between a “property” and an “attribute”?
 Attribute is a quality or object that we attribute to someone or something. Property is a quality that exists without any attribution.
 - What are some different ways to add content inside a DOM element?
 .createElement() creates element in HTML
 .appendChild() adds an item to a parent element.
 - When might the <template> element be useful?
 tells HTML that multiple js elements will be added with the same structure
 - What are the different ways to add event handlers to elements?
 .addEventListener(), "click", "keypress", "mouseenter", "keyup", "keydown", etc.
 - Why is addEventListener the safest way to add an event handler?
 makes it easier to control how the event reacts to bubbling
 - How can you access submitted form values in your JS?
 store them in a variable with .value
 
 ## 9. Testing
 - Why are tests useful?
 if we have big chunks of code it can become a bit confused as to where errors are coming from and why some things broke. Testing helps to check which pieces of code are actually working
 - What is the difference between unit and integration tests?
 unit tests test small pieces of code, for example a function, whereas integration tests can test a whole feature, for example if submitting data and then using if for something else works
 - What kind of code is easier to test?
 code that has only one functionality
 - Why should your tests be isolated from each other?
if one test is reliant on another test, it might show false results
- What is Test Driven Development (TDD)?
 writing tests before the actual code
 - When might TDD be a useful process to follow?
 when building very complex structures?
 
 ## 10. Debugging
 - What process would you take to find out why your code isn’t working?
 looking at the error code, and which line of code it indicates. console logging pieces that are involved in that line
 - What tools do JS/dev tools have to help debug your code?
 console
 -  At what point should you ask for someone else’s help?
 First I look at the error codes and then I'll try to google what I'm trying to do. If I'm unsuccessful for about 20-30 minutes I should ask for someone's help.
