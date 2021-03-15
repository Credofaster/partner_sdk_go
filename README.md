# Getting started

Buy Airtime on the most simplistic System. We abstract all the nitty-gritty leaving you with just the option to specify the account number to receive airtime and how much. 

We guarantee 95% uptime, 99% reliability.

Just Request and we will make sure you get, in realtime. If not, you will be notified immediately by events.

Now, what Credo is faster that Credofaster!

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=Credofaster%20Partner%20Api-GoLang&projectName=credofasterpartnerapi_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=credofasterpartnerapi_lib)

## How to Use

The following section explains how to use the CredofasterpartnerapiLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=credofasterpartnerapi_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=credofasterpartnerapi_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=credofasterpartnerapi_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=credofasterpartnerapi_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=credofasterpartnerapi_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=Credofaster%20Partner%20Api-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=credofasterpartnerapi_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=credofasterpartnerapi_lib)

## Initialization

### Authentication
In order to setup authentication of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| apiKey | Assigned APIKey |
| clientId | Assigned ClientId |


To configure these for your generated code, open the file "Configuration.go" and edit it's contents.


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [main_pkg](#main_pkg)
* [events_pkg](#events_pkg)

## <a name="main_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".main_pkg") main_pkg

### Get instance

Factory for the ``` MAIN ``` interface can be accessed from the package main_pkg.

```go
main := main_pkg.NewMAIN()
```

### <a name="airtime_request"></a>![Method: ](https://apidocs.io/img/method.png ".main_pkg.AirtimeRequest") AirtimeRequest

> Request Airtime Purchase


```go
func (me *MAIN_IMPL) AirtimeRequest(request *models_pkg.PartnerAirtimeRequest)([]*models_pkg.PartnerAirtimeResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| request |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var request *models_pkg.PartnerAirtimeRequest

var result []*models_pkg.PartnerAirtimeResponse
result,_ = main.AirtimeRequest(request)

```


### <a name="airtime_balance"></a>![Method: ](https://apidocs.io/img/method.png ".main_pkg.AirtimeBalance") AirtimeBalance

> Gets the current Working Balance. 
> Balance is SIGNED


```go
func (me *MAIN_IMPL) AirtimeBalance()(*models_pkg.PartnerAirtimeBalanceResponse,error)
```

#### Example Usage

```go

var result *models_pkg.PartnerAirtimeBalanceResponse
result,_ = main.AirtimeBalance()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="events_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".events_pkg") events_pkg

### Get instance

Factory for the ``` EVENTS ``` interface can be accessed from the package events_pkg.

```go
events := events_pkg.NewEVENTS()
```

### <a name="register_callback"></a>![Method: ](https://apidocs.io/img/method.png ".events_pkg.RegisterCallback") RegisterCallback

> A callback to receive the below Callbacks


```go
func (me *EVENTS_IMPL) RegisterCallback(request *models_pkg.RegisterCallbackRequest)(*models_pkg.RegisterCallbackResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| request |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var request *models_pkg.RegisterCallbackRequest

var result *models_pkg.RegisterCallbackResponse
result,_ = events.RegisterCallback(request)

```


### <a name="client_event_feedback"></a>![Method: ](https://apidocs.io/img/method.png ".events_pkg.ClientEventFeedback") ClientEventFeedback

> *Tags:*  ``` Skips Authentication ``` 

> You are required to provide a HTTP/HTTPS endpoint, to which we will publish various events. 
> 
> This Endpoint will be hosted on the CLIENT's Environment. If no endpoint is provided, we are not liable to any missing events. 
> 
> NOTE: A DETAILED PDF of all Events is shared on request. It contains application events, System Health Events and Alerts on the same.


```go
func (me *EVENTS_IMPL) ClientEventFeedback(payloadToReceive *models_pkg.EventCallbackPayload)(*models_pkg.EventCallbackFeedback,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| payloadToReceive |  ``` Required ```  | Sample Payload: {"EventId":"123456789","EventType":"QUEUED","RequestId":"A09797a11e2564061b859781b18bb34dd","EventData":{}} |


#### Example Usage

```go
payloadToReceiveValue := []byte("{\"EventId\":\"123456789\",\"EventType\":\"QUEUED\",\"RequestId\":\"A09797a11e2564061b859781b18bb34dd\",\"EventData\":{}}")
var payloadToReceive *models_pkg.EventCallbackPayload
json.Unmarshal(payloadToReceiveValue,&payloadToReceive)

var result *models_pkg.EventCallbackFeedback
result,_ = events.ClientEventFeedback(payloadToReceive)

```


[Back to List of Controllers](#list_of_controllers)



