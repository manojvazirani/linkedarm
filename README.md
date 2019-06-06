# Linked ARM template

A simple example of deployment of nested ARM template on Azure for reference.

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/?repository=https://github.com/manojvazirani/linkedarm)

<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fmanojvazirani%2Flinkedarm%2Fmaster%2Fazuredeploy.json" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>

### Files:
- [azuredeploy.json](./azuredeploy.json) (Master template which calls the other templates)
- [master-resources1](./master-resources1.json) (First round ofdeployment of resources)
- [master-resources2](./master-resources2.json) (Second round of deployment of resources, dependent on resources from first round)

### Deployments on Azure:
- master-resources1
    - Public IP address
    - VNET
    - subnet
    - NIC

- master-resources2
    - Availability set
    - VM (uses above NIC)

