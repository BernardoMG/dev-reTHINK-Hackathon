# reTHINK Challenge

This Repo is dedicated to help TADHack participants using reTHINK framework for web application development. First, helps with reTHINK configuration and give some guidelines on how to use it in web applications. At the end, is presented a challenge that participants needs to do.
 

## NVM, Node and NPM Installation

```shell
# NVM Installation
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
# Restart your terminal so NVM can be used

# Node Installation
$ nvm install 6.6.0

# To verify that node and npm was correctly install run:
$ node -v
$ npm -v
```


## reTHINK environment configuration 

```shell
# clone the toolkit repository:
$ git clone --branch=develop https://github.com/reTHINK-project/dev-hyperty-toolkit.git

# clone the dev-hyperty repository:
$ git clone --branch=develop https://github.com/reTHINK-project/dev-hyperty.git

# Note: Ensure that both repositories are cloned inside the same directory 
```

```shell
# Inside the toolkit repository run:
$ npm install -g karma-cli gulp-cli browserify
$ npm install

# Note: It may take a while to install all modules. Hang tight. 
```

```shell
# run the toolkit for browser
$ npm run start:browser

# Note: If you are using MAC OS you may need to run the above command with sudo privileges; 
#       Otherwise with Linux, you can solve this problem with following command. 
#       As result, you do not need sudo privileges.

$ sudo setcap 'cap_net_bind_service=+ep' `which node`

```


Open https://catalogue.localhost/ and accept certificate

Open https://localhost/ and select an Hyperty to run.


## reTHINK distribution files 

To deploy reTHINK runtime in web applications is necessary to execute `rethink.js`. This script can be found in `dev-runtime-browser` repository. There are two ways to use this script:

* Add the following dependency into your `package.json` file, or

* Clone the repository using the following command and copy the `bin`paste into the web application directory

```shell
# Clone the runtime-browser repository:
$ git clone --branch=develop https://github.com/reTHINK-project/dev-runtime-browser.git
```


## Usefull documentation

* [Complete espefication](https://github.com/reTHINK-project/specs)

* [GroupChatManager](https://github.com/reTHINK-project/dev-hyperty/tree/develop/docs/group-chat-manager)

* [APP Example](https://github.com/reTHINK-project/dev-app/tree/develop)

## Challenge

The main goal of this challenge is to develop a Chat web application using the GroupChatManager hyperty. In this application, users can create chat rooms to exchange messages with other users. Each chat room must be identified by a certain name. The ideia is that users can invite others to some specific chat room by indicating their email address. In addition, users can also join some chat room using its identifier. Once inside a chat room, users can exchange messages between them. 
Each user should be authenticated using their preferred Identity Provider (e.g. Google, Microsoft). reTHINK provides an authentication mecanism, so the developer does not have to handle with this.

### Task 1 (`estimation 45 minutes`)

`Load Runtime` - reTHINK runtime is obtained after the `rethink.js` execution.

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

`Load an Hyperty` - An Hyperty can be loaded using `requireHyperty()` method. For this challenge should be loaded the `GroupChatManager` Hyperty, already present in the `hybroker.rethink.ptinovacao.pt` catalogue. To deploy it in a successfull manner, authentication is mandatory.

```shell
#Example
RUNTIME.requireHyperty(hypertyURI(hyperty_domain, 'GroupChatManager')).then((hyperty) => {
  ...
});
```

### Task 2 (`estimation 1 hour and 30 minutes`)

`Creation of chat rooms` - Chat rooms must be identified by a certain name. When a chat room is created, the user could also provide a list of emails to invite to the chat room. Opcionally, if some user is in a different domain must be provided in order to receive the invitation.

```shell
#Example
GroupChatManager.create(identifier, emails, domains).then(function(chatController) => {
  ...
});
```

### Task 3 (`estimation 45 minutes`)

`Join chat room` - Once created the chat room, is generated a URL (`DataObject Reporter URL`) that other users should use if they want to join the chat room.

```shell
#Example
GroupChatManager.join(url).then(function(chatController) => {
  ...
});
```

### Task 4 (`estimation 45 minutes`)

`Exchange of messages` - Inside the chat room, users can easly exchange messages between them.

```shell
#Example
chatController.send(message).then(function(result) => {
  ...
});
```

### How to succeed and win the prize 


## Feedback

[form](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform)
