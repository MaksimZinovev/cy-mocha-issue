## Repro steps

Repro steps for [Couldn't determine Mocha version · Issue #9439 · cypress-io/cypress](https://github.com/cypress-io/cypress/issues/9439)

```
git clone https://github.com/MaksimZinovev/cy-mocha-issue.git
cd cy-mocha-issue
npm init -y
npm install cypress
npx cypress run --spec cypress/e2e/1-getting-started   

```

Observ in console `Couldn't determine Mocha version`


```js
// cypress.config.js
const { defineConfig } = require("cypress");

module.exports = defineConfig({
  reporter: 'junit',
  e2e: {
    setupNodeEvents(on, config) {
      // implement node event listeners here
    },
  },
});
```