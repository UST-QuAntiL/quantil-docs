# 
## Create Implementation

!!! info 
    To create an implementation, the user has to be in the ``General View`` of a specific algorithm.

In the ``General View`` the user has to click on the ``Implementation`` tab, which opens the ``Implementation List View``.
This view contains all implementations of the algorithm. Within this view, a new implementation will be created via the ``Plus Button`` which is located above the list.

![alt text](./../images/implementation/Create_Implementation_-_Step_1.png "Create implementation")

Clicking on the ``Plus Button`` will open the following dialog.
In the dialog it is possible to give the new implementation a name.

!!! note 
    To create a new implementation only a ``name`` is required.

![alt text](./../images/implementation/Create_Implementation_-_Step_2.png "Create implementation")

After all necessary fields have been filled in, the creation of the implementation can be confirmed by clicking on the ``OK Button``. After a successfull creation, the user will be navigated to the detailed view of the new implementation.

## Delete Implementation

!!! info 
    To create an implementation, the user has to be in the ``Implementation List View`` of a specific algorithm.

To remove a specific implementation, the user has to simply click on the ``Delete Button`` in the ``Action Column`` of the data table.

![alt text](./../images/implementation/Delete_Implementation_-_Step_1.png "Delete implementation")

It is also possible to delete mulitple implementations at once by selecting them one by one using the checkboxes within the table. When at least one implementation is selected, a ``Master Delete Button`` will show up above the table. To delete the selected implementations at once, this button must be pressed.

![alt text](./../images/implementation/Delete_Implementation_-_Step_2.png "Delete implementation")

Both ways of deleting cloud services will lead to a confirmation dialog. This dialog will list all the previously selected algorthims that will be deleted. To finally confirm the deletion, the ``OK Button`` at the bottom of the dialog has to be pressed. After a successfull deletion the deleted cloud services will disappear from the table.

![alt text](./../images/implementation/Delete_Implementation_-_Step_3.png "Delete implementation")

## Update Implementation Properties

!!! info 
    To update the properties of an implementation, the user has to be in the ``Implementation View`` which can be reached by clicking on an implementation in the ``Implementation List View``.

The ``General`` tab of the view, allows to adjust all basic properties of the implementation.

![alt text](./../images/implementation/Update_Implementation_Properties_-_Step_1.png "Delete implementation")


!!! note 
    To save any changes to the properties of an implementation there are two options:

    * Save the changes on a field by field basis. For that the user has to click on the ``Save Button`` located next to the field that was edited. Alternatively the user can confirm the changes by pressing ``Enter`` on the keyboard. 

    * Save all changes at once by clicking on the round  ``Save Button`` button which appears at the right side of the screen.

![alt text](./../images/implementation/Update_Implementation_Properties_-_Step_2.png  "Delete implementation")

## Manage Compute Resource Properties

!!! info 
    To manage computing resource properties of an existing implementation, the user has to be in the ``General`` tab within the``General View`` of the implementation, which can be reached by clicking on an implementation in the ``Implementation List View``.

In the general view of the implementation, the user can also manage the compute resource of the selected implementation. For that the user has to go to the ``Required Compute Resource Properties`` field and click on the ``Plus Button``, which will open up a new dialog for the creation of a new compute resource property.

![alt text](./../images/implementation/Open_Implementation_View.png "Add Compute Resource")

In the creation dialog, the user has to fill in all necessary data for the new property. Here it is important that the "Property Value" matches the given "Data Type". After all data has been provided by the user, the new property can finally be created using the "OK".

![alt text](./../images/implementation/Add_Compute_Resource_-_Step_1.png "Add Compute Resource")


In case of a successful creation, the created compute resource property will be directly visible in the general view of the selected implementation. 

!!! note 
    Compared to the basic properties of the algorithm, the management of the compute resource properties will be performed directly and does not have to be confirmed by clicking on a save button.
