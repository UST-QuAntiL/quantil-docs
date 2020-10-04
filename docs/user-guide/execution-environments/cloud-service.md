#
## Create Cloud Service

To create a cloud service the user has to navigate to the ``Cloud Services List View`` by using the navigation sidebar. 
This will be done by first clicking on the ``Execution Environments`` menu in the navigation sidebar, which makes the ``Cloud Services`` submenu visible.
In general, the ``Cloud Service List View`` displays a list of all available cloud services. Creating a new cloud service is done via the ``Plus Button`` which is located above the list.

![alt text](./../images/cloud_service/Create_Cloud-Service_-_Step_1.png "Create cloud service")

Clicking on the ``Plus Button`` will open the following dialog.
In the dialog it is possible to give the new cloud service a name.

!!! note 
    To create a new cloud service only a ``name`` is required.

![alt text](./../images/cloud_service/Create_Cloud-Service_-_Step_2.png "Create cloud service")

After all necessary fields have been filled in, the creation of the cloud service can be confirmed by clicking on the ``OK Button``. After a successfull creation, the user will be navigated to the detailed view of the new cloud service.


## Delete Cloud Service

!!! info 
    To perform the deletion of a cloud service, the user has to be in the ``Cloud Service List View``.
	
To remove a specific cloud service, the user has to simply click on the ``Delete Button`` in the ``Action Column`` of the data table.


![alt text](./../images/cloud_service/Delete_Cloud-Service_-_Step_1.png "Delete cloud service")


It is also possible to delete mulitple cloud services at once by selecting them one by one using the checkboxes within the table. When at least one cloud service is selected, a ``Master Delete Button`` will show up above the table. To delete the selected cloud services at once, this button must be pressed.

![alt text](./../images/cloud_service/Delete_Cloud-Service_-_Step_2.png "Delete cloud service")

Both ways of deleting cloud services will lead to a confirmation dialog. This dialog will list all the previously selected algorthims that will be deleted. To finally confirm the deletion, the ``OK Button`` at the bottom of the dialog has to be pressed. After a successfull deletion the deleted cloud services will disappear from the table.

![alt text](./../images/cloud_service/Delete_Publication_-_Step_3.png "Delete cloud service")

## Update Cloud Service Properties

!!! info 
    To update the properties of a software platform, the user has to be in the ``Cloud Service View`` which can be reached by clicking on a cloud service in the ``Cloud Service List View``.

The ``General`` tab of the view, allows to adjust all basic properties of the cloud service.

![alt text](./../images/cloud_service/Update_Cloud_Service_Properties_-_Step_1.png "Update cloud service properties")


!!! note 
    To save any changes to the properties of a cloud service there are two options:

    * Save the changes on a field by field basis. For that the user has to click on the ``Save Button`` located next to the field that was edited. Alternatively the user can confirm the changes by pressing ``Enter`` on the keyboard. 

    * Save all changes at once by clicking on the round  ``Save Button`` button which appears at the right side of the screen.

![alt text](./../images/cloud_service/Update_Cloud_Service_Properties_-_Step_2.png "Update cloud service properties")

## Reference Software Platform

!!! info
    To reference software platforms in an existing cloud service, the user has to be in the ``General View``

In the ``General View`` of the cloud service, the user as to switch to the tab ``Software Platforms``, which is dedicated to referencing software platforms.
To link software platform with the currently selected cloud service, the user has to click on the ``Plus Button`` at the top of the data table.

![alt text](./../images/cloud_service/Link_Software_Platform_-_Step_1.png "Link software platform")

This will open a dialog with a separate data table containing existing software platforms.
The table can be searched or sorted using the given input fields.
For referencing software platforms the user has to click on the ``Link Button`` of a selected software platform.

![alt text](./../images/cloud_service/Link_Software_Platform_-_Step_2.png  "Link software platform")

Alternatively, the users can use the check-boxes of the first column of the table to select all software platforms to reference. 
After at least one check-box is checked, a ``Master Link Button`` will appear at the top of the table which can be used to link all selected algorithms with the cloud service.

![alt text](./../images/cloud_service/Link_Software_Platform_-_Step_2.1.png  "Link software platform")

## Dereference Software Platform

!!! info 
    To dereference software platforms, the user has to be in the ``Software Platforms Tab`` of the ``Cloud Service View``, which can be reached by clicking on a cloud service in the ``Cloud Service List View``.
	
To remove a reference from a cloud service, the user has to simply click on the ``Delete Button`` in the ``Actions Column`` of the data table.

![alt text](./../images/cloud_service/Unlink_Software_Platform_-_Step_1.png "Dereference single software platform")

Alternatively use the check-boxes to select multiple software platforms and then click on the ``Master Delete button`` to unlink multiple software platforms .

!!! note 
    ``Master Delete button`` will only appear if at least one software platform has been selected.
	
![alt text](./../images/cloud_service/Unlink_Software_Platform_-_Step_2.png "Dereference multiple software platform")

## Reference Compute Resource

!!! info
    To reference compute resources in an existing cloud service, the user has to be in the ``General View``

In the ``General View`` of the cloud service, the user as to switch to the tab ``Compute Resource``, which is dedicated to referencing software platforms.
To link compute resource with the currently selected cloud service, the user has to click on the ``Plus Button`` at the top of the data table.

![alt text](./../images/cloud_service/Link_Compute_Rescource_-_Step_1.png "Link compute resource")

This will open a dialog with a separate data table containing existing software platforms.
The table can be searched or sorted using the given input fields.
For referencing compute resources the user has to click on the ``Link Button`` of a selected compute resource.

![alt text](./../images/cloud_service/Link_Compute_Rescource_-_Step_2.png  "Link compute resource")

Alternatively, the users can use the check-boxes of the first column of the table to select all compute resources to reference. 
After at least one check-box is checked, a ``Master Link Button`` will appear at the top of the table which can be used to link all selected compute resources with the cloud service.

![alt text](./../images/cloud_service/Link_Compute_Rescource_-_Step_2.1.png  "Link compute resource")

## Dereference Compute Resource

!!! info 
    To dereference compute resources, the user has to be in the ``Compute Resource Tab`` of the ``Cloud Service View``, which can be reached by clicking on a cloud service in the ``Cloud Service List View``.
	
To remove a reference from a cloud service, the user has to simply click on the ``Delete Button`` in the ``Actions Column`` of the data table.

![alt text](./../images/cloud_service/Unlink_Compute_Resource_-_Step_1.png "Dereference single compute resource")

Alternatively use the check-boxes to select multiple compute resources and then click on the ``Master Delete button`` to unlink multiple compute resources.

!!! note 
    ``Master Delete button`` will only appear if at least one compute resource has been selected.
	
![alt text](./../images/cloud_service/Unlink_Compute_Resource_-_Step_2.png "Dereference multiple compute resource")