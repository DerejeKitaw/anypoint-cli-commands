## [Prerequisites](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli#prerequisites)
```
Download and install NodeJS and npm (node package manager) on your system
```

## [Install CLI](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli#installation)
```
npm install -g anypoint-cli@latest
```

## [Setup credentials](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli#credentials-file)
> Save the file in 
```
C:\Users\USERNAME\.anypoint\credentials
> For me
C:\Users\dereje\.anypoint\credentials
```
```json
{
 "default": {
  "username": "yourAnypointUserName",
  "password": "yourAnypointPassword",
  "organization": "",
  "environment": "", // default `Design`, can be set in cli using use environment Sandbox
  "host": ""
 },
 "otherProfile": {
  "username": "",
  "password": "",
  "organization": "",
  "environment": "",
  "host": ""
 },
 "connAppProfile": {
  "client_id": "",
  "client_secret": "",
  "organization": "",
  "environment": "",
  "host": ""
 }
}
```

## Run cli
```
> anypoint-cli
```

### [cli options](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli#cli-options)
```
If you pass only your username, the Anypoint CLI prompts for your password.

> anypoint-cli --username="user"
Password: ****
```

### [use environment](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#use-environment)
> This command is only available for interactive mode.
```
use environment [options] <name>
use environment Sandbox
```

## [runtime-mgr cloudhub-application start](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#runtime-mgr-cloudhub-application-start)
```
runtime-mgr cloudhub-application start [options] <name>
runtime-mgr cloudhub-application start "dtk-customer-proxy-api"
runtime-mgr cloudhub-application start system-customer-der-api
```

## [runtime-mgr cloudhub-application stop](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#runtime-mgr-cloudhub-application-stop)
```
runtime-mgr cloudhub-application stop  [options] <name>
runtime-mgr cloudhub-application stop  dtk-customer-proxy-api
runtime-mgr cloudhub-application stop system-customer-der-api
```

## [runtime-mgr cloudhub-application deploy](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#deploy-to-cloudhub)
```

runtime-mgr cloudhub-application deploy --runtime "4.4.0" --workers "1" --workerSize "0.1" --region "us-east-2" --property "env:Sandbox" mule-simple-api "C:\Users\derej\mule-simple-api.jar"
```

## [runtime-mgr cloudhub-application describe](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#runtime-mgr-cloudhub-application-describe)
```
runtime-mgr cloudhub-application describe [options] <name>
runtime-mgr cloudhub-application describe mule-simple-api

```
## [runtime-mgr cloudhub-application list](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#runtime-mgr-cloudhub-application-list)
```
runtime-mgr cloudhub-application list [options]
```
runtime-mgr cloudhub-application list
## [use environment](https://docs.mulesoft.com/runtime-manager/anypoint-platform-cli-commands#use-environment)
> This command is only available for interactive mode.
```
use environment [options] <name>
use environment Sandbox
```

## Exit cli
```
ctrl + c
```