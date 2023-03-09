
# Virtual Machine Image Supervisor Service

⚠️ Work In Progress - Page under construction ⚠️

This is the overview page for the virtual machine service. This is where the summary would go  

[VM Service API Documentation](http://developers.eng.vmware.com/apis/iaas/)

## Support
* Only support v1 API
* Something else


## Tutorials
[This would be one example tutorial](#this-would-be-one-example-tutorial) - [***(Video Tutorial)***](#demo-video-for-this-example)

[Another example tutorial](#another-example-tutorial)


## This would be one example tutorial

This would be a summary of what this tutorial covers, example deploy a vm.....


#### Demo Video for this example

[![Example Thumbnail](source/images/example_thumbnail.PNG "This is an example")](https://www.youtube.com/)

## Another example tutorial
1. Configure something
2. Deploy secret
3. Deploy config-map
4. deploy VM object

# Virtual Machine Service - UI Support

[#Create VM]

The UI can be used in addition to the kubectl and API support available in CCI.

The UI allows users to execute all necessary workflows:
- Create VM
- View all VMs
- Day 2 operations
- Delete VMs

## Create VM

The create VM workflow supports two distinct paths.

For both paths the user must select a VM Image and VM Class for the VM.

![VM Create](source/images/vm-service-create-image-class.png "VM Create")

The user is then presented with "REVIEW AND CONFIRM" and "GO TO ADVANCED SETTINGS" buttons.

### Standard

If the user clicks on "REVIEW AND CONFIRM", then they are taken immediately to the last step of the wizard to review the settings before dpeloying the VM.

After reviewing the two options they selected, they can proceed with the VM creation by clicking the DEPLOY VM button.

### Advanced Settings

If the user has opted for the advanced settings flow, they have the abililty to:
- Add additional volumes to the VM
- Specify a ssh keypair to use to access the VM
- Add additional LoadBalancer configuration (service resources)
- Add Cloud-config data, configuration, or scripts

Once the additional settings have been selected, the user clicks on the NEXT button to review and deploy the VM. The user can click the DEPLOY VM button to initiate the creation of the VM.

![VM Create PVC](source/images/vm-service-pvc.png "VM Create PVC")
![VM Create SSH Keypair](source/images/vm-service-public-key.png "VM Create SSH Keypair")
![VM Create LB](source/images/vm-service-lb.png "VM Create LB")
![VM Create Cloud-config](source/images/vm-service-cloud-config.png "VM Create Cloud-config")


## View all VMs

Users can view all the VMs created in the namespace. The user will see the following information in the grid's default view:
- Name
- Status (Ready, Error, etc.)
- Power State (On/Off)
- Managed by : indicates whether the VM is part of a Tanzu Kubernetes Cluster
- Address : IP address
- Age : How long the VM has existed

![VM List](source/images/vm-service-list.png "VM List")


## Day 2 operations

The user has the ability to toggle the Power State and manage the volumes associated with the VM. Volumes can be added, detached, or have their capacity increased through the UI.

![VM Edit](source/images/vm-service-day-2.png "VM Edit")

## Delete VM

VMs can be deleted by clicking on the three vertical dots for a VM in the datagrid and selecting Delete and providing confirmation.

![VM Delete](source/images/vm-service-delete.png "VM Delete")
