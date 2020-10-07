#
## Create Compute Resource

To create a compute resource the user has to navigate to the ``Execution Environment List View`` by using the navigation sidebar.

![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_1.PNG "Navigate to execution environments list view")

While in the ``Execution Environment List View``, the navigation sidebar will display sub menus for different kinds of execution environments. To create a compute resource, the user has to navigate to the ``Compute Resource List View``.

![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_2.PNG "Navigate to compute resource list view")

Inside the ``Compute Resource List View``, the user can click on the ``Plus Button`` to initiate the creation of a new compute resource inside a separate ``Creation Dialog``.

![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_3.PNG "Open creation dialog")

Within the ``Creation Dialog``, the user will have to enter all important information of the compute resource he wants to create.

!!! note 
    Currently the only required information is the **name** of the compute resource.
	
![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_4.PNG "Structure of creation dialog")

After entering the name of the compute resource, the user has to confirm the creation by clicking on the ``OK Button``.

![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_5.PNG "Confirm creation")

In case the creation was successful, the user will be redirected to the ``Compute Resource View`` of the newly created compute resource.

![alt text](./../images/compute_resource/Create_Compute_Resource_-_Step_6.PNG "General View")

## Delete Compute Resource

!!! info 
    To perform the deletion of a compute resource, the user has to be in the ``Compute Resource List View``.
	
To remove a specific compute resource, the user has to simply click on the ``Delete Button`` in the ``Actions Column`` of the data table.

![alt text](./../images/compute_resource/Delete_Compute_Resource_-_Step_1.1.PNG "Delete single resource")

The user can also remove multiple compute resources at once by selecting them using the check-boxes of the data table. After the user has made his selection he can press the ``Master Delete Button`` at the top of the data table.

!!! note 
    The delete button will only appear after at least one compute resource has been selected by the user.

![alt text](./../images/compute_resource/Delete_Compute_Resource_-_Step_1.2.PNG "Delete multiple resources")

To confirm the deletion of the selected compute resource(s), the user has to click on the ``YES Button`` of the ``Confirmation Dialog``.

!!! note 
    **Names** of the compute resources that will be deleted are displayed in the body of the dialog and should be checked before confirming the deletion.

![alt text](./../images/compute_resource/Delete_Compute_Resource_-_Step_2.PNG "Confirm deletion of selected compute resource(s)")

## Update Compute Resource Information

!!! info 
    To update the information of a compute resource, the user has to be in the ``Compute Resource View`` which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
Updating basic information is done in the ``General Tab`` of the ``Compute Resource View``. To do that, the user has to simply use the ``Input fields``, ``Check-Boxes`` or ``Selection drop-downs`` to add new values or adjust existing ones.

![alt text](./../images/compute_resource/Update_Compute_Resource_-_Step_1.PNG "General Tab of Compute Resource View")

If information is changed, a ``Save button`` will be displayed next that specific input field. Also, a ``Master Save button`` will appear at the right side of the screen. To save the changes of each input field individually, the user can click on the ``Save button`` next to any updated input field. Alternatively the user can save all changes by clicking the ``Master Save button``.

!!! note 
    The user can also hit ``Enter`` on the keyboard to save the changes of a single field in most cases. In some cases, it may be necessary to focus the ``Save button`` by hitting ``TAB`` on the keyboard and then confirming with ``Enter``.
	
![alt text](./../images/compute_resource/Update_Compute_Resource_-_Step_2.PNG "Saving the changes")

!!! info 
	**Compute Resource Properties** of are stored separately and therefor do not belong to the basic information of a resource. They are saved, deleted or updated instantly without the use of the mentioned ``Save buttons``.
	
## Create Compute Resource Property

!!! info 
    To create a property for a compute resource,  the user has to be in the ``Compute Resource View`` which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
Creating properties for a compute resource is done in the ``General Tab`` of the ``Compute Resource View``. To do that, the user has to simply click on the ``Plus button`` of the dedicated ``Compute Resource Property Field``.

![alt text](./../images/compute_resource/Add_Compute_Resource_Property_-_Step_1.PNG "Open Property Dialog")

This will open a separate ``Creation Dialog`` where the user will have to enter all important information of about the property he wants to create.

!!! note 
	The **Type Name** field supports auto-completion functionality. While typing a type name, the system will suggest existing types with that name in a drop-down. On click of an existing type, all necessary fields will be filled automatically.

![alt text](./../images/compute_resource/Add_Compute_Resource_Property_-_Step_2.PNG "Dialog structure")

After all fields have been filled, the user can finally add the property by confirming the creation via the existing ``OK button``.

!!! note 
	The **Property Value** needs to match the selected **Data Type**.
	
![alt text](./../images/compute_resource/Add_Compute_Resource_Property_-_Step_3.PNG "Confirm creation")

After the property has been successfully created, it will appear in the the dedicated ``Compute Resource Property Field`` of the ``Compute Resource View``.

![alt text](./../images/compute_resource/Add_Compute_Resource_Property_-_Step_4.PNG "Verify creation")

## Update Compute Resource Property

!!! info 
    To update a property for a compute resource,  the user has to be in the ``Compute Resource View`` which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
Updating properties for a compute resource is done in the ``General Tab`` of the ``Compute Resource View``. To do that, the user has to simply hover over a existing property in the dedicated ``Compute Resource Property Field`` and then click on the ``Edit button``.

![alt text](./../images/compute_resource/Update_Compute_Resource_Property_-_Step_1.PNG "Open Property Dialog")

This will open a separate ``Update Dialog`` where the information of the property can be adjusted.

!!! note 
	The **Type Name** field supports auto-completion functionality. While typing a type name, the system will suggest existing types with that name in a drop-down. On click of an existing type, all necessary fields will be filled automatically.

![alt text](./../images/compute_resource/Update_Compute_Resource_Property_-_Step_2.PNG "Dialog structure")

After all fields have been adjusted, the user can finally update the property by confirming the update via the existing ``OK button``.

!!! note 
	The **Property Value** needs to match the selected **Data Type**.
	
![alt text](./../images/compute_resource/Update_Compute_Resource_Property_-_Step_3.PNG "Confirm update")

## Delete Compute Resource Property

!!! info 
    To delete a property for a compute resource,  the user has to be in the ``Compute Resource View`` which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
Deleting properties for a compute resource is done in the ``General Tab`` of the ``Compute Resource View``. To do that, the user has to simply hover over a existing property in the dedicated ``Compute Resource Property Field`` and then click on the ``Delete button``.

![alt text](./../images/compute_resource/Delete_Compute_Resource_Property_-_Step_1.PNG "Delete property")

!!! info 
	A successfully deleted property should disappear from the dedicated ``Compute Resource Property Field`` after deletion.
	
## Reference Software Platforms

!!! info 
    To reference software platforms in a compute resource, the user has to be in the ``Software Platforms Tab`` of the ``Compute Resource View``, which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
To initiate the linking of a software platform, the user has to click on the ``Plus button`` in the ``Software Platforms Tab``.

![alt text](./../images/compute_resource/Reference_Software_Platform_-_Step_1.PNG "Click on '+' in 'Software Platforms'-Tab")

This will open a new dialog containing a page-able table of available software platforms. This table can be searched or sorted using the given input fields and buttons.

![alt text](./../images/compute_resource/Reference_Software_Platform_-_Step_2.PNG "Filter existing software platforms using table controls")

To reference a software platform simply click on the ``Link button`` in the ``Action-Column``.

![alt text](./../images/compute_resource/Reference_Software_Platform_-_Step_3.1.PNG "Reference single software platform")

Alternatively, use the check-boxes to select multiple software platforms and then click on the ``Master Link button`` to link all of them at once.

!!! note 
    ``Master Link button`` will only appear if at least one software platform has been selected.
	
![alt text](./../images/compute_resource/Reference_Software_Platform_-_Step_3.2.PNG "Reference multiple software platforms")

!!! info 
    Successfully referenced software platforms(s) will now be visible in the ``Software Platforms Tab`` of the ``Compute Resource View``.
	
## Dereference Compute Resources

!!! info 
    To dereference software platforms, the user has to be in the ``Software Platforms Tab`` of the ``Compute Resource View``, which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
To remove a reference from a software platform, the user has to simply click on the ``Delete Button`` of a software platform in the ``Actions Column``.

![alt text](./../images/compute_resource/Dereference_Software_Platform_-_Step_1.1.PNG "Dereference single software platform")

Alternatively, use the check-boxes to select multiple software platforms and then click on the ``Master Delete button`` to unlink all of them at once.

!!! note 
    ``Master Delete button`` will only appear if at least one software platform has been selected.
	
![alt text](./../images/compute_resource/Dereference_Software_Platform_-_Step_1.2.PNG "Dereference multiple software platforms")

## Reference Cloud Services

!!! info 
    To reference cloud services in a compute resource, the user has to be in the ``Cloud Services Tab`` of the ``Compute Resource View``, which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
To initiate the linking of a cloud service, the user has to click on the ``Plus button`` in the ``Cloud Services Tab``.

![alt text](./../images/compute_resource/Reference_Cloud_Service_-_Step_1.PNG "Click on '+' in 'Cloud Services'-Tab")

This will open a new dialog containing a page-able table of available cloud services. This table can be searched or sorted using the given input fields and buttons.

![alt text](./../images/compute_resource/Reference_Cloud_Service_-_Step_2.PNG "Filter existing cloud services using table controls")

To reference a cloud service simply click on the ``Link button`` in the ``Action-Column``.

![alt text](./../images/compute_resource/Reference_Cloud_Service_-_Step_3.1.PNG "Reference single cloud service")

Alternatively, use the check-boxes to select multiple cloud services and then click on the ``Master Link button`` to link all of them at once.

!!! note 
    ``Master Link button`` will only appear if at least one cloud service has been selected.
	
![alt text](./../images/compute_resource/Reference_Cloud_Service_-_Step_3.2.PNG "Reference multiple cloud services")

!!! info 
    Successfully referenced cloud service(s) will now be visible in the ``Cloud Services Tab`` of the ``Compute Resource View``.
	
## Dereference Cloud Services

!!! info 
    To dereference cloud services, the user has to be in the ``Cloud Services Tab`` of the ``Compute Resource View``, which can be reached by clicking on a compute resource in the ``Compute Resource List View``.
	
To remove a reference from a cloud service, the user has to simply click on the ``Delete Button`` of a cloud service in the ``Actions Column``.

![alt text](./../images/compute_resource/Dereference_Cloud_Service_-_Step_1.1.PNG "Dereference single cloud service")

Alternatively, use the check-boxes to select multiple cloud services and then click on the ``Master Delete button`` to unlink all of them at once.

!!! note 
    ``Master Delete button`` will only appear if at least one cloud service has been selected.
	
![alt text](./../images/compute_resource/Dereference_Cloud_Service_-_Step_1.2.PNG "Dereference multiple cloud services")