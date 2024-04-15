# Node + Cypress

This example shows how to configure Node to work with Cypress


## What is it for

- End-to-end
- User Interface
- Api's
- Components
- Unity

## Technologies

- Node
- Javascript/Typescript
- Mocha
- Chai
- Asynchronous


## Commands

### Find elements on canvas

- get: Selects DOM elements using CSS selectors, enabling interaction and assertion with the matched elements.

- contains: Searches for elements that contain specific text, facilitating interaction or assertion based on the presence of the specified text.

- context: Establishes a scoped context for subsequent commands, allowing interaction and assertion within a specific section of the page without the need for repetitive element selection.



### Interact with elements


- type: This command is used to simulate keyboard input into input fields. 

- click: This command simulates a mouse click on the selected DOM element. 

- select: This command is specifically designed to interact with  elements, commonly known as dropdown menus. It allows you to choose an option from the dropdown by value, text, or index.

- check/uncheck: These commands are used to interact with checkboxes or radio buttons. 


### File handling

- writeFile: This command is used to write data to a file on the file system. It's typically used in Cypress tests to create or modify files, such as fixtures or temporary files, during test execution.

- readFile: The readFile command is used to read data from a file on the file system. It's often used in Cypress tests to retrieve data from files like fixtures or configuration files for use in test scenarios.

- fixture: Fixtures are static data files containing test data or expected outcomes. 

### Mocks and simulations

- server & route: Cypress allows you to control network requests and responses using a server and route mechanism. You can define custom routes to intercept HTTP requests made by your application during testing and respond with predefined data or behavior.

- intercept: This command intercepts and modifies HTTP requests made by your application. It allows you to stub responses or manipulate requests to simulate various network scenarios and test how your application handles them.

- wait: The wait command pauses test execution until a specific condition is met. It's useful for dealing with asynchronous behavior, such as waiting for elements to appear or for certain actions to complete before proceeding with the test.

- spy, stub: Cypress provides utilities for spying on and stubbing functions in your application. Spies allow you to observe function calls and their parameters, while stubs replace functions with custom behavior, enabling you to simulate different scenarios during testing.

- tick: This command advances the virtual clock in Cypress, allowing you to control time-related behavior in your tests. It's particularly useful for testing features that depend on timers, animations, or other time-sensitive functionality.

- clock: Cypress allows you to manipulate the system clock within your tests using the clock command. You can set the current time to a specific value, freeze time, or advance it by a certain amount to simulate different time scenarios and test how your application behaves under those conditions.
  

### Browser control

- clearCookie/clearCookies: Clears cookies in the browser. clearCookie clears a single cookie by name, while clearCookies clears all cookies.

- clearLocalStorage: Clears the local storage of the browser, removing any stored data associated with the current domain.

- onBeforeLoad: Specifies a function to run before the page loads, allowing you to modify the behavior of the page or stub network requests.

- onLoad: Specifies a function to run after the page loads, enabling actions or assertions that should occur after the page has fully rendered.

- window: Provides access to the browser's window object, allowing you to interact with or manipulate browser functionality directly.

- viewport: Sets the dimensions of the browser viewport for the test, allowing you to simulate different screen sizes and test responsive design.
  

### Assertions

- expect: Allows you to make assertions about the state of elements or variables. It's typically used with Chai assertion syntax to verify specific conditions or values, ensuring that the expected behavior of the application is met.

- should: Provides a fluent interface for making assertions about the state of DOM elements. It allows you to chain multiple assertions together, providing a clear and readable way to express expectations about the state or behavior of elements.

- assert: Performs assertions to verify expected outcomes in tests. It's often used in conjunction with expect or should to validate that certain conditions are true, helping to ensure the correctness of the application under test.



## Best Practicies

### Organization of tests, Background login and control of the application status

❌: Share page objects, use the interface to log in
<br>
✔️: Test specs in isolation
<br>
✔️: Generate token via api + set to storages
<br>


### Select elements on screen using data-selectors

❌: Use bad selectors: xpath, id's and dynamic classes, etc
<br>
⚠️: id
<br>
✔️: use dedicated selectors: data-cy, data-selector, test-id
<br>


### Subscribe or Assign return values

❌: sign values ​​directly e.g.: let text =
<br>
✔️: use aliases and escape the name e.g.: cy.get().text().as('aliasName')
<br>

### Visit external websites during testing

❌: visit different domains in the same test
<br>
⚠️: If you need, visit different tests (it's)
<br>
✔️: validate href / use mocks
<br>

### Create tests that depend on the execution of other tests

❌: create sequential tests (which depend on other)
<br>
✔️: create independent tests per execution
<br>
✔️: that can run alone / parallel / backwards
<br>
✔️: abstract common actions to hooks
<br>


### Create weak tests with just one assertion

❌: act as if they were unit tests, small asserts 
<br>
⚠️: evaluate whether it is worth creating another test
<br>
✔️: add as many assertions as necessary
<br>

### Use the after or afterEach hooks

❌: use hooks with things that can be done before
<br>
✔️: use preparation hooks - before / beforeEach
<br>

### Add unnecessary wait

❌: wait randomly for a period (10 seconds)
<br>
✔️: use routes/aliases/wait
<br>
✔️: + assertions - to check if you can follow
<br>
✔️: Cypress has some automatic waits.
<br>

### Web servers

❌: upload the server/api during testing
<br>
✔️: wait-on - task for
<br>
✔️: start-server-and-test
<br>

### Set a baseUrl globally

❌: always inform the entire url e.g.: http://example1.co/cars, http://example1.co/motocycles
<br>
✔️: set baseUrl e.g.: http://example1.co/
<br>
✔️: 
use routes e.g. cars, motorcycles
<br>


## Getting Started

Initialize a Node project

```bash
npm init –yes
```

Install Cypress

```bash
npm install -D cypress@12.5.0
```

Open Cypress

```bash
npx cypress open
```





