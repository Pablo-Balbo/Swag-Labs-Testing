#Getting started

>This is an Automation Testing practice of a specific website (https://www.saucedemo.com/), created with the only objective of learning how to use the automated testing tool (WebDriverIO). I have written code for all its components as well as its functions separately, and for end to end testing too.

###The work is organized as follows:
>In one hand, we find the WebdriverIO configuration file "wdio.config.js", as well as a "package.json" file and a "package-lock.json". Inside the file "wdio.config.js" is the organization of the test suite, organized like this:

    suites: {
        standardUser: [
            './test/specs/standardUser/loginTest.js',
            './test/specs/standardUser/inventoryTest.js',
            './test/specs/standardUser/headerTest.js',
            './test/specs/standardUser/footerTest.js',
            './test/specs/standardUser/cartTest.js',
            './test/specs/standardUser/checkoutStepOneTest.js',
            './test/specs/standardUser/checkoutStepTwoTest.js',
            './test/specs/standardUser/checkoutCompleteTest.js'
        ],
        e2eTests: [
            './test/specs/e2eTests/e2eTest.standardUser.js',
            './test/specs/e2eTests/e2eTest.problemUser.js',
            './test/specs/e2eTests/e2eTest.lockedUser.js',
            './test/specs/e2eTests/e2eTest.performanceGlitchUser.js'
        ],
    },

>There is also a folder called "pageObjects", where all the files corresponding to each test are found, and within them, the selectors corresponding to each part of the page to be tested (for example, "login.page.js" , "inventory.page.js", etc.).

>Finally, there is the ".gitignore" file, through which we avoid uploading the "node_modules" folder.

##Start testing

>Important! 
>Before you start, remember to run "npm install" in your console in order to install the necessary dependencies to run this test suite.

>In the file "package.json" is declared "test", which we will use to run the tests in the console through the command "npm run test". 
- In case you want to carry out only one test suite, it can be done by modifying the "package.json" file, in the "test" command by: "npx wdio run ./wdio.conf.js --suite e2eTests", for example , in case you want to run only the End to End tests; 
- In case you want to run only the Standard User's Tests, just change that command by: "npx wdio run ./wdio.conf.js --suite standardUser".

#
#

####Author: Pablo A. Balbo
