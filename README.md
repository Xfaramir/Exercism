# Applitools Hackathon Automation Framework

This is Automated test which was build to test Applitools Hackathon App Functionality using Cypress.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Installing

A step by step series of examples that tell you how to get a development env running

```
git clone https://github.com/Xfaramir/visualApplitoolsHackathon
```

Navigate to the folder where your project is located.

#### Run this command in Terminal to install Npm packages.

```
npm install
```

### How to run tests:

```
npm run cypress:open
```

This command will execute **cypress** GUI-Chrome and you can select tests to run:

**TraditionalTest.e2e.specs.ts**

**VisualAITest.e2e.specs.ts**

```
npm run cypress:run
```

This command will execute the test **headless** using Chromium (Electron):

## Page Object

In order to avoid code duplication I set up Page Object structure for this challenge.

**Path to page object** :

```
visualApplitoolsHackathon/cypress/pages/basepage.ts
```

There you can modify which version of the APP you want to test by changing the URL
from 
**this.url = 'https://demo.applitools.com/hackathon.html';**
to 
**this.url = 'https://demo.applitools.com/hackathonV2.html';**

## Reporting

Im using Cypress- mocha built-in reporter, also generated videos for both runs of the app that can be found in cypress/videos

## Data Driven

Here I'm using a json for users that can be found in cypress/fixtures

## P.S.

**Running version of Cypress: 3.6.1 -- Electron 73 (headless) **

**Cypress** is new tool and during my work i experienced multiple issues which i want to note:

1.  There's no much support for typescript and lacking some TS typings for Applitools Eyes

2.  Sometimes when testing the canvas with cypress it didnt load so i had to restart the Cypress GUI in order to make it work -- Happens rarely but it can be noted **here**: https://eyes.applitools.com/app/test-results/00000251828938236936/00000251828938214746/steps/1?accountId=Quz2xHHZtkOFiIHxI6EMlw~~&display=gallery&mode=step-editor

So for that reason I used

```
cy.wait(150);
```


to make my test more stable.

## Authors

- **David Barrera - Colombia**

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
```
