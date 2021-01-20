---
title: MinIO Operator cleanup Tutorial
description: This tutorial explains how to cleanup Operator
---


### Cleaning Up Operator



***Delete the operator's Custom Resource Definitions by kubectl delete commands :***

Example:
 
 ```copycommand
 kubectl delete -f KnativeServingInstance.yaml -n operators
 ```
 
 Similarly delete the operator's Custom Resource Definitions of Knative Eventing using below command:
 
 
 ```copycommand
 kubectl delete -f KnativeEventingInstance.yaml -n operators
 ```

Similarly,delete all the CRs.
 

***Delete the operator by kubectl delete command:***
 
 
 Example:
 
 ```copycommand
 kubectl delete -f https://operatorhub.io/install/knative-operator.yaml
 ```
 

 
***Delete all the yaml files:***
 
 Example:
 
  ```copycommand
  rm -rf KnativeServingInstance.yaml
  ```
  
  ```copycommand
  rm -rf KnativeEventingInstance.yaml
  ```
  
  Similarly, you can delete rest of yaml files.
