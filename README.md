# reTHINK Challenge

This Repo is dedicated to help TADHack participants in the use of reTHINK framework for web application development. First, helps with reTHINK configuration and then give some guidelines on how to use it in web applications. At the end of this Repo, it describes a challenge that participants needs to do.
 

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
# run the toolkit for browse
npm run start:browser

# Note: If you are using MAC OS you may need to run the above command with sudo privileges; 
Otherwise with Linux, you can solve this problem with following command. 
As result, you do not need sudo privileges.

$ sudo setcap 'cap_net_bind_service=+ep' `which node`

```

Open https://catalogue.localhost/ and accept certificate

Open https://localhost/ and select an Hyperty to run.

## reTHINK distribution files 


## Usefull documentation


## Challenge

The main goal of this challenge is to develop a Chat web application, where users can create chat rooms to exchange messages with other users. Each chat room must be identified by a certain name. The ideia is that users can invite others to some specific chat room by indicating their email address. In addition, users can also join some chat room using its identifier. Once inside a chat room, users can exchange messages between them. 
Each user should be authenticated using their preferred Identity Provider (e.g. Google, Microsoft). reTHINK provides an authentication mecanism, so the developer does not have to handle with this.

### Task 1 (`estimation 30 minutes`)

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

`Load a Hyperty` - A Hyperty can be loaded using `requireHyperty()` method. For this challenge should be loaded the GroupChatManager Hyperty, already present in the `hybroker.rethink.ptinovacao.pt` catalogue.

```shell
#Example
RUNTIME.requireHyperty(hypertyURI(hyperty_domain, 'GroupChatManager')).then((hyperty) => {
  ...
});
```

### Task 2

### Task 3

### Task 4

### Task 5

### Task 6



### How to succeed and win the prize 


## Feedback
