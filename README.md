# reTHINK Hackathon

This Repo is dedicated to help TADHack participants using reTHINK framework for web application development. First, it helps with reTHINK configuration and give some guidelines on how to use it in web applications. Then, a programming challenge is proposed, with several tasks that each participant should accomplish. At the end, is provided a form, which must be filled out by each participant.
 
## 1st Challenge

Each team should develop a web application that uses the X hyperty that can deployed from the `hysmart.rethink.ptinovacao.pt` catalogue. This hyperty generates a code according to the name of your team that should be passed as input. The resulting code should be shown in the developed application.   

##### IMAGE

To overcome this first challenge, each team should accomplish all the tasks bellow. 
Your feedback is extremely important for us in order to improve reTHINK framework in the future. As such, after complete all the tasks, each team must fill out the page 2 of this [FORM](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform). 

##### Note: If you do not fill out this form, your participation wont be considered! 

### Task 1 (`estimation: 45 minutes`)

#### Task 1.1:

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

#### Task 1.2:

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

#### Task 1.2:

`Load an Hyperty` - An Hyperty can be loaded using `requireHyperty()` method. For this challenge should be loaded the `X` Hyperty, which is ready to be used in `hybroker.rethink.ptinovacao.pt` catalogue. To deploy it in a successful manner, authentication is mandatory.

```shell
#Example
RUNTIME.requireHyperty(hypertyURI(hyperty_domain, 'GroupChatManager')).then((hyperty) => {
  ...
});
```

### Task 2 (`estimation: 45 minutes`)

`Generate a code` - The generated code depends of the name of each team that should be passed as input.

```shell
#Example
XHyperty.generateCode(name).then((code) => {
  ...
});
```

##### Note: Don't forget to display the generated code on your developed application (html page).


## 2nd Challenge


