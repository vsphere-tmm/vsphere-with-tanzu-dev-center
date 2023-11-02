# Network Service - UI Support

⚠️ Work In Progress - Page under construction ⚠️

The UI can be used in addition to the kubectl and API support available in CCI.

The UI allows users to execute all necessary workflows:
- Services
    - List all Services
        - See summary of the service
        - See details for the service, including recent events
    - Action
        - View the YAML for a service
- List all Load Balancers
    - List all Load Balancers
        - See summary of the Load Balancer
        - See details for the Load Balancer
    - Action menu bar
        - Create a new Load Balancer
    - Grid action menu
        - View the YAML for a Load Balancer
        - Delete a Load Balancer
        - Edit a Load Balancer

## List all Services

List of available Network Services. You can deploy and manage services in a self-service way using Kubernetes APIs.

Users can view all the Network Services created in the namespace. The user will see the following information in the grid's default view:
- Name
- Type
- Cluster IP
- External IP
- Ports
- Age

There are additional columns that can be toggled through the Manage Columns button located at the bottom of the grid:

- Labels - any labels assigned to the service
- Created On - specific time the service was created

![NetworkServices List](source/network-services-list.png "Network Services List")

### Summary of Network Services

Click on the double chevrons to see key information for the resources.

![NetworkService Summary](source/netwrok-service-summary.png "Network Service Summary")

### Details of Network Services

Click on the Service name to see all the details for the resource, including recent events.

![NetworkService Details](source/netwrok-service-details.png "Network Service Details")

### Action Menubar
#### View YAML

To view the resource YAML in the YAML Explorer panel at bottom.

![NetworkService View_YAML](source/network-services-view-yaml.png "Network Services View YAML")

## List all Load Balancers

List of available Load Balancers. You can deploy and manage load balancers in a self-service way using Kubernetes APIs.

Users can view all the Network Services created in the namespace. The user will see the following information in the grid's default view:
- Name
- Selector
- Age

There are additional column that can be toggled through the Manage Columns button located at the bottom of the grid:
- Created On - specific time the service was created

![VM_Load_Balancers_List](source/vm-lb-list.png "Load Balancer List")

### Summary of Network Services

Click on the double chevrons to see key information for the resources.

![VM_Load_Balancer Summary](source/vm-lb-summary.png "Load Balancer Summary")

### Details of Network Services

Click on the Service name to see all the details for the resource, including recent events.

![VM_Load_Balancer Details](source/vm-lb-details.png "Load Balancer Details")

### Action Menubar
#### Create

Create Load Balancer workflow.

When you click the Create button, the Load balancer modal will open with a pre-populated name.
The name can be updated. When updating the name, the 'Selector' value will get updated accordingly.

![Create_Load_Balancer](source/vm-lb-create.png "Create Load Balancer")

##### Create new port

To add new port to a port group, the user must enter the following fields and click Add button,
- Name
- Port
- Protocol
- Target

![Create_Add_Port](source/vm-lb-add-port.png "Create VM Add Port")

![Create_Load_Balancer_Valid](source/vm-lb-create-vaild.png "Create Load Balancer Valid")

### Grid action menu

There are several actions available from the grid menu.
1. Viewing the YAML for the resource
2. Deleting the Load Balancer
3. Edit the Load Balancer

Click on the 3 vertical dots to open the menu.

![Load_Balancers_Action_Menu](source/vm-lb-action-menu.png "Load Balancers Action Menu")

#### View YAML

To view the resource YAML in the YAML Explorer panel at bottom / right.

![Load_Balancer View_YAML](source/vm-lb-view-yaml.png "Load Balancer View YAML")

#### Delete

Show Delete confirmation popup

![Load_Balancers_Delete_Confirmation](source/vm-b-delete-confirmation.png "Load Balancers Delete Confirmation")

#### Edit

Show edit VM LB popup to add / remove port

![Load_Balancers_Edit](source/vm-lb-edit.png "Load Balancers Edit")
