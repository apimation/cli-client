# apimation/cli-client

### Binaries:
[Download](https://github.com/apimation/cli-client/releases/latest)

### Install with brew:
```
# register apimation brew tap
brew tap apimation/brew-taps git@github.com:apimation/brew-taps.git

# update brew to update apimation brew tap
brew update

# install latest apimation version
brew install apimation
```

### First usage of apimation-cli-client with existing apimation account:
##
0. It is recommended to create an alias for cli client, like in this example:
```
alias apimation="/Users/dlocmelis/Apimation/apimation-cli-client"
!NB The path to cli client will be different
```
1. Go to a directory reserved for the tests
2. Run command 
```
apimation restore --project "<NameOfExistingProject>"
# no need to use '--project' flag if you have only one project associated with your username
```
3. Input account credentials when prompted
4. Use generate command to create new test assets:
`apimation generate -h`
5. Start test engine worker
```
# To start the worker you'll need worker access token, contact dev@apimation.com
  # Start the worker when worker access token is acquired
  apimation worker start
```
6. Synchronize test assets with apimation cloud to be able to run latest tests
```
  apimation deploy
```
7. Execute test sets and load scenarios based on run command:
```
  apimation run -h
```

### Account creation and first project setup:
##
0. It is recommended to create an alias for cli client, like in this example:
```
alias apimation="/Users/dlocmelis/Apimation/apimation-cli-client"
!NB The path to cli client will be different
```
1. Go to a directory reserved for the tests and execute:
```
  apimation user create --email test@testuser.com --project TestProject
  cd TestProject
```
2. Create new YAML test assets using generate command
`apimation generate -h`
3. Start test engine worker
```
# To start the worker you'll need worker access token, contact dev@apimation.com
  # Start the worker when worker access token is acquired
  apimation worker start
```
4. Synchronize test assets with apimation cloud to be able to run latest tests
```
  apimation deploy
```
5. Execute test sets and load scenarios based on run command:
```
  apimation run -h
```

##### General help:
##
```
  apimation -h
```
