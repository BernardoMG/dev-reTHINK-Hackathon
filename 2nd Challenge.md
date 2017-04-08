# 2nd Challenge

Each team should develop a Chat application that uses the `XHyperty` and `GroupChatManager` hyperties that can deployed from the `hysmart.rethink.ptinovacao.pt` catalogue. The `XHyperty` generates a code according to the name of your team that should be passed an input. The `GroupChatManager` hyperty main functionality is to handle text conversations among groups, including:

 * Creation of a new Group Chat with possibility to invite users to join it
 
 * Notification about invitation to join a Group Chat with options to accept or reject

 * Send message to group

 * Receive message from group with identity from sender
   

![2nd Challenge](https://github.com/BernardoMG/dev-reTHINK-challenge/blob/master/Figures/2-Challenge.jpg)

To overcome this second challenge, each team should accomplish all the tasks bellow. 
Your feedback is extremely important for us in order to improve reTHINK framework in the future. As such, after complete all the tasks, each team must fill out the page 3 of this [FORM](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform). 

#### Note: If you do not fill out this form, your participation wont be considered! 

## Task 1 (`estimation: 45 minutes`)

### Task 1.1:

`reTHINK distribution files` - To deploy reTHINK runtime in your web application is necessary to execute `rethink.js`. This script can be found in `dev-runtime-browser` repository. There are two ways to obtain this script:

* Add the following dependency into your `package.json` file

```shell
# Add dependency to your package.json file:
  "dependencies": {
    "runtime-browser": "reTHINK-project/dev-runtime-browser#develop"
  },
```

* Clone the repository using the following command and copy the `bin` folder into the root of your application 

```shell
# Clone the runtime-browser repository:
$ git clone --branch=develop https://github.com/reTHINK-project/dev-runtime-browser.git
```

### Task 1.2:

`Load Runtime` - reTHINK runtime can be obtained after the `rethink.js` execution by your application.

```shell
#Example
rethink.default.install({ 
  domain: runtime_domain,
  development: true,
  runtimeURL: runtimeURL
  }).then((runtime) => {
    ... 
});
```

### Task 1.3:

`Load an Hyperty` - An Hyperty can be loaded using `requireHyperty()` method. For this challenge should be loaded the `XHyperty` and the `GroupChatManaher` hyperties, which are ready to be used in `hybroker.rethink.ptinovacao.pt` catalogue. To deploy it in a successful manner, authentication is mandatory.

```shell
#Example
RUNTIME.requireHyperty(hypertyURI(hyperty_domain, 'XHyperty')).then((hyperty) => {
  ...
});
```

## Task 3 (`estimation: 45 minutes`)

`Generate a code` - The generated code depends of the name of each team that should be passed as input.

```shell
#Example
XHyperty.generateCode(name).then((code) => {
  ...
});
```



