# Network Service - UI Support

⚠️ Work In Progress - Page under construction ⚠️

The UI can be used in addition to the kubectl and API support available in CCI.

The UI allows users to execute all necessary workflows:
- Services
    - List all Services
        - See summary of the service
        - See details for the service
    - Action
        - View the YAML for a service
- List all VM Load Balancers
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

## List all VM Load Balancers

List of available Network Services. You can deploy and manage service in a self-service way using Kubernetes APIs.

Users can view all the Network Services created in the namespace. The user will see the following information in the grid's default view:
- Name
- Selector

![VM_Load_Balancers_List](source/vm-lb-list.png "VM Load Balancer List")

### Summary of Network Services

Click on the double chevrons to see key information for the resources.

![VM_Load_Balancer Summary](source/vm-lb-summary.png "VM Load Balancer Summary")

### Details of Network Services

Click on the Service name to see all the details for the resource, including recent events.

![VM_Load_Balancer Details](source/vm-lb-details.png "VM Load Balancer Details")

### Action Menubar
#### Create

Create VM Load Balancer workflow.

On Create button click VM Load Balancer model open with pre-populated name. 
We are able to edit the name, depend on the name 'Selector' value get populated.

![Create_VM_Load_Balancer](source/vm-lb-create.png "Create VM Load Balancer")

##### Create new port

To add new port to port group. THe user will enter following required fields and click Add button.
- Name
- Port
- Protocol
- Target

![Create_VM_Add_Port](source/vm-lb-add-port.png "Create VM Add Port")

![Create_VM_Load_Balancer_Valid](source/vm-lb-create-vaild.png "Create VM Load Balancer Valid")

### Action Menubar

![VM_Load_Balancers_Action_Menu](source/vm-lb-action-menu.png "VM Load Balancers Action Menu")

#### View YAML

To view the resource YAML in the YAML Explorer panel at bottom.

![VM_Load_Balancer View_YAML](source/vm-lb-view-yaml.png "VM Load Balancer View YAML")

#### Delete

Show Delete confirmation popup

![VM_Load_Balancers_Delete_Confirmation](source/vm-b-delete-confirmation.png "VM Load Balancers Delete Confirmation")

#### Edit

Show edit VM LB popup to add / remove port

![VM_Load_Balancers_Edit](source/vm-lb-edit.png "VM Load Balancers Edit")
