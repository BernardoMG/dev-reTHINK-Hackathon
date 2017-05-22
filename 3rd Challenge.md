# 3rd Challenge

Each team should continue working on the previous developed application that uses the `Code Generator Reporter` and `Group Chat Manager` hyperties. The goal with this third challenge is to change the `Code Generator Reporter` hyperty. Now, whenever a code is generated, it should also generate a timestamp that will return with the generated code to the application.   


![3rd Challenge](https://github.com/BernardoMG/dev-reTHINK-Hackathon/blob/master/Figures/3-Challenge.jpg)


To overcome this third challenge, each team should accomplish all the tasks bellow. 
Your feedback is extremely important for us in order to improve reTHINK framework in the future. As such, after complete all the tasks, each team must fill out the page 4 of this [Survey](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform). 

### Note: If you do not fill out this form, your participation wont be considered! 


## Task 1 (`estimation: 35 minutes`)

`Hyperty Development Toolkit` - Currently the toolkit can be used to develop hyperties to be executed in the Browser or in the NodeJS. It is essential to use the toolkit in order to change the `Code Generator Reporter` hyperty and complete this challenge. In order to configurate properly the Toolkit follow the available documentation [here](https://github.com/reTHINK-project/dev-hyperty-toolkit/blob/develop/README.md).

<!-- 
### Task 1.1: 

`NVM, Node and NPM Installation`

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


### Task 1.2: 

`reTHINK environment configuration` 

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
-->

## Task 2 (`estimation: 40 minutes`)

### Task 2.1:

`Change Code Generator Reporter hyperty` - Inside `dev-hyperty` folder is the source code of each hyperty (`src` folder). The toolkit encodes everything in this folder. Each team should change the `generateCode(name)` method present in the `CodeGeneratorReporter.hy.js` file. This method should generate a code, that will depend on the input, and a timestamp. Both should be returned.

##### Note: Use `betatester` branch of dev-hyperty repository.

<!--
### Task 2.2:

`Restart toolkit` - Run again the `npm run start:browser` command to restart the toolkit and check if everything is correctly encoded. It should not return any error in the terminal.
-->

### Task 2.2:

`Generate a code and broadcast to all the participants` - Restart your app and try to generate a new code and broadcast it to all the participants of some chat room.

#### Note: Don't forget that the hyperty domain changed. For this challenge, you want to obtain the hyperty from the toolkit, not from the `hysmart.rethink.ptinovacao.pt` catalogue.

##

### [Survey Page 4!!!](https://docs.google.com/forms/d/e/1FAIpQLSeFt56Ura0zkTqg_VX9od_jBZtE3-2mt_urTFvxsoRuQ3uJRw/viewform) 
