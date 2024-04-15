
# Getting Start

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




## What is it for

End-to-end
User Interface
Api's
Components
Unity

## Technologies

Node
Javascript/Typescript
Mocha
Chai
Asynchronous


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
⚠️: id
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






## Commands

Find elements on canvas
Interact with elements
File handling
Mocks and simulations
Browser control
Assertions


