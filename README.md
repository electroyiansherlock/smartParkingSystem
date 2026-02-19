# smartParkingSystem
The project file for the smart parking system project which is having the Spring MVC based backend written in Java and the frontend is written in React. The data is stored in a in-memory database named as H2 database and using the Axios calls the data is fetched by the frontend from backend.

# Promise

Meaning of a Promise in JavaScript
A Promise is a JavaScript object that links producing code and consuming code [1]. 
"Producing code" is code that does something and takes time (like fetching data from a server).
"Consuming code" is code that wants the result of the "producing code" once it's available. 
A promise can be in one of three states:
Pending: The initial state, neither fulfilled nor rejected.
Fulfilled: The operation completed successfully, and a value is available (e.g., the data from a server request).
Rejected: The operation failed, and an error reason is available. 
You can attach callbacks to a promise to handle the fulfilled value (.then()) or the rejection reason (.catch()) [1]. 

A Promise basically represents the eventual completion of an async operation, It represents that the
asynchronous call which you are making will be either completed successfully or will be failed, but
the response will definitely be there.

Like fetch() method returns a promise so .then() will be used when the 200 http status code is there
and if any error is there then .catch() will be used.

If we are not using the await in the async calls then the function will not be able to understand where it has to wait for the response, as the API calls to other services has some network latency to fetch the data from the different servers.
If we are not making the API calls as async calls then that will make the JS application UX very bad because JS is a single threaded application and if we are blocking the main thread in the API calls then all the user interactions, and other
features will be blocked till the response from the API is not there.

More Details about making the API calls as Async calls is mentioned below :

1. Prevents Blocking the Main Thread: JavaScript is single-threaded, meaning it has one "main thread" that handles all operations, including rendering the user interface, executing scripts, and handling user events (like clicks or keyboard input). 
If an API call were synchronous (blocking), the main thread would pause until the data is fetched, making the user interface unresponsive and seemingly "frozen".

2. Enhances User Experience: Asynchronous operations allow the application to continue running smoothly. The user can scroll, click buttons, and interact with other parts of the page while data is being fetched in the background. 
Once the API call is complete, a callback function or a Promise is used to process the data and update the UI.

3. Improves Performance: Asynchronous programming optimizes resource usage. Instead of the CPU waiting idly for network I/O (input/output) operations to complete, it can switch to other tasks
