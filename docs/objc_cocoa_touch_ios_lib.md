# Getting started

Simple calculator API hosted on APIMATIC

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Open the project workspace using the (APIMATICCalculator.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the APIMATICCalculator library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'APIMATICCalculator', :path => 'Vendor/APIMATICCalculator'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the APIMATICCalculator.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=APIMATIC%20Calculator-ObjC&workspaceName=APIMATICCalculator&projectName=APIMATICCalculator&rootNamespace=APIMATICCalculator)


## Initialization

### 

Configuration variables can be set as following.
```Objc

```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [SimpleCalculatorGroupController](#simple_calculator_group_controller)

## <a name="simple_calculator_group_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SimpleCalculatorGroupController") SimpleCalculatorGroupController

### Get singleton instance
```objc
SimpleCalculatorGroup* simpleCalculatorGroup = [[SimpleCalculatorGroup alloc]init] ;
```

### <a name="calculate_async_with_operation"></a>![Method: ](https://apidocs.io/img/method.png ".SimpleCalculatorGroupController.calculateAsyncWithOperation") calculateAsyncWithOperation

> Calculates the expression using the specified operation.


```objc
function calculateAsyncWithOperation:(enum OperationTypeEnum) operation
                x:(double) x
                y:(double) y
                completionBlock:(CompletedGetCalculate) onCompleted(operation x : x y : y)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| operation |  ``` Required ```  | The operator to apply on the variables |
| x |  ``` Required ```  | The LHS value |
| y |  ``` Required ```  | The RHS value |





#### Example Usage

```objc
    // Parameters for the API call
    OperationTypeEnum operation = SUM;
    double x = 75.4144631933488;
    double y = 75.4144631933488;

    [self.simpleCalculatorGroup calculateAsyncWithOperation: operation x : x y : y  completionBlock:^(BOOL success, HttpContext* context, NSNumber* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



