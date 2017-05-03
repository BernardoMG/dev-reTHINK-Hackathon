# 1st Challenge

Each team should develop a web application that uses the `Code Generator` hyperty that can be deployed from the `hysmart.rethink.ptinovacao.pt` catalogue. This hyperty generates a code according to the name of each team, which should be passed as input. The resulting code should be shown in the developed application.   

![1st Challenge](https://github.com/BernardoMG/dev-reTHINK-challenge/blob/master/Figures/1-Challenge.jpg)

To overcome this first challenge, each team should accomplish all the tasks bellow. 
Your feedback is extremely important for us, in order to improve the reTHINK framework in the future. As such, after completing all the tasks, each team must fill out page 2 of this [Survey](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform). 

### Note: If you do not fill out this Survey, your participation won't be considered! 

## Task 1 (`estimate: 45 minutes`)

### Task 1.1:

`reTHINK distribution files` - To deploy the reTHINK runtime in your web application, it is necessary to execute `rethink.js`. This script can be found in the `dev-runtime-browser` repository. 

* Clone the repository using the following command and copy the `bin` folder into the root of your application 

```shell
# Clone the runtime-browser repository:
$ git clone --branch=develop https://github.com/reTHINK-project/dev-runtime-browser.git
```

### Task 1.2:

`Script Execution` - To be able to install reTHINK in your application, should be executed the `rethink.js` script. There are several options to do that. Your team can try the following method that uses the `javascript` and `html` capabilities:

```shell
#Example
let head = document.getElementsByTagName('head')[0];
let script = document.createElement('script');
script.type = 'text/javascript';
script.onload = function() {
... (Task 1.3)
}
script.src = 'http://localhost:PORT/bin/rethink.js';
head.appendChild(script);
```


### Task 1.3:

`Load Runtime` - the reTHINK runtime can be obtained after the instalation of the reTHINK in your application.

```shell
#Example
rethink.default.install({ 
  domain: 'localhost',
  development: true,
  runtimeURL: 'hyperty-catalogue://catalogue.localhost/.well-known/runtime/Runtime'
  }).then((runtime) => {
    ... 
});
```

#### Note: The `domain` and `runtimeURL` fields depends on where the application is deployed. For this case, should be in some local machine.


### Task 1.4:

`Load an Hyperty` - An Hyperty can be loaded using `requireHyperty()` method. For this challenge, the `Code Generator` hyperty, which is ready to be used in `hysmart.rethink.ptinovacao.pt` catalogue, should be loaded. To deploy it in a successful manner, authentication is mandatory.

```shell
#Example
const hypertyURI = (hyperty_domain, hyperty) => `hyperty-catalogue://catalogue.${hyperty_domain}/.well-known/hyperty/${hyperty}`;

runtime.requireHyperty(hypertyURI('localhost', 'CodeGenerator')).then((hyperty) => {
  ...
});
```

## Task 2 (`estimate: 30 minutes`)

`Generate a code` - The generated code depends on the name of each team, which should be passed as input.

```shell
#Example
CodeGenerator.generateCode(name).then((code) => {
  ...
});
```

#### Note: Don't forget to display the generated code on your developed application (HTML page).

##

### [Survey Page 2!!!](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform) 
