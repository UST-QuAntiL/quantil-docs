## Algorithm 
### Create Algorithm

To create an algorithm the user has to navigate to the ``Algorithm List View`` by using the navigation sidebar.
This view displays all available algorithms in a table. Creating a new algorithm is done via the ``Plus Button`` which is located above the table.

![alt text](/user-guide/images/algorithm/Create_Algorithm_-_Step_1.png "Open creation dialog")

Clicking on the ``Plus Button`` will open the following ``Creation Dialog``, where the user has to type in all required information for creating a new algorithm.

!!! note 
    Depending on the selected ``Computational Model``, a third input field might show up, allowing the user to define the ``Quantum Computation Model``.

![alt text](/user-guide/images/algorithm/Create_Algorithm_-_Step_2.PNG "Structure of creation dialog")

After entering all required information, the user has to confirm the creation of the algorithm by clicking on the ``OK Button``.

![alt text](/user-guide/images/algorithm/Create_Algorithm_-_Step_3.png "Confirm creation")

If the creation of the algorithm was successful, the user will be redirected to the detailed ``Algorithm View`` of the new algorithm.

![alt text](/user-guide/images/algorithm/Create_Algorithm_-_Step_4.PNG "Algorithm view of created algorithm")

### Delete Algorithm

!!! info 
    To perform the deletion of an algorithm, the user has to be in the ``Algorithm List View``.

To remove a specific algorithm, the user has to simply click on the ``Delete Button`` in the ``Actions Column`` of the data table.

![alt text](/user-guide/images/algorithm/Delete_Algorithm_-_Step_1.1.png "Delete single algorithm")

The user can also remove multiple algorithms at once by selecting them using the check-boxes of the data table. After the user has made his selection he can press the ``Master Delete Button`` at the top of the data table.

!!! note 
    The delete button will only appear if at least one algorithm is selected.

![alt text](/user-guide/images/algorithm/Delete_Algorithm_-_Step_1.2.png "Delete multiple algorithms")

To confirm the deletion of the selected algorithm(s), the user has to click on the ``YES Button`` of the ``Confirmation Dialog``.

!!! note 
    **Names** of algorithms that will be deleted are displayed in the body of the dialog and should be checked before confirming the deletion.

![alt text](/user-guide/images/algorithm/Delete_Algorithm_-_Step_2.png "Confirm deletion")

### Update Algorithm Information

!!! info 
    To update the information of an algorithm, the user has to be in the ``Algorithm View`` which can be reached by clicking on a algorithm in the ``Algorithm List View``.
	
Updating basic information is done in the ``General Tab`` of the ``Algorithm View``. To do that, the user has to simply use the ``Input fields``, ``Check-Boxes`` or ``Selection Drop-Downs`` to add new values or adjust existing ones.

![alt text](/user-guide/images/algorithm/Update_Algorithm_Properties_-_Step_1.PNG "A small part of the 'General Tab' of the 'Algorithm View'")

If information is changed, a ``Save button`` will be displayed next that specific input field. Also, a ``Master Save button`` will appear at the right side of the screen. To save the changes of each input field individually, the user can click on the ``Save button`` next to any updated input field. Alternatively the user can save all changes by clicking the ``Master Save button``.

!!! note 
    The user can also hit ``Enter`` on the keyboard to save the changes of a single field in most cases. In some cases, it may be necessary to focus the ``Save button`` by hitting ``TAB`` on the keyboard and then confirming with ``Enter``.
	
![alt text](/user-guide/images/algorithm/Update_Algorithm_Properties_-_Step_2.PNG "Saving the changes")

!!! info 
	**Required Compute Resource Properties**, **Problem Types** and **Application Areas** are stored separately and therefor do not belong to the basic information of the algorithm. They are saved, deleted or updated instantly without the use of the mentioned ``Save buttons``.

### Load Algorithm Revision

!!! info 
    To load a revision of an algorithm, the user has to be in the ``Algorithm View`` which can be reached by clicking on an algorithm in the ``Algorithm List View``.
    Please see the [revision section](overview.md#revisions) for further details about revisions.
    

Loading a revision is done by clicking on the revision selection field in the ``Algorithm View``. 

![alt text](/user-guide/images/algorithm/Load_Algorithm_Revision_-_Step_1.PNG "Open Revision Selection")

This will open a dropdown menu with all available revisions sorted by their date with the latest revision at the top.
By selecting an element from the dropdown menu, the data of a revision is loaded in the ``Algorithm View`` and can be viewed and edited.

![alt text](/user-guide/images/algorithm/Load_Algorithm_Revision_-_Step_2.PNG "Revision Selection Menu")

### Create Compute Resource Properties

!!! info 
    To create a compute resource property for the algorithm, the user has to be in the ``Algorithm View`` which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Creating properties for a compute resource is done in the ``General Tab`` of the ``Algorithm View``. To do that, the user has to simply click on the ``Plus button`` of the dedicated ``Required Compute Resource Property Field``.

![alt text](/user-guide/images/algorithm/Add_Compute_Resource_-_Step_1.PNG "Open Property Dialog")

This will open a separate ``Creation Dialog`` where the user will have to enter all important information about the property he wants to create.

!!! note 
	The **Type Name** field supports auto-completion functionality. While typing a type name, the system will suggest existing types with that name in a drop-down. On click of an existing type, all necessary fields will be filled automatically.

![alt text](/user-guide/images/algorithm/Add_Compute_Resource_-_Step_2.PNG "Dialog structure")

After all fields have been filled, the user can finally add the property by confirming the creation via the existing ``OK Button``.

!!! note 
	The **Property Value** needs to match the selected **Data Type**.

![alt text](/user-guide/images/algorithm/Add_Compute_Resource_-_Step_3.PNG "Confirm creation")

After the property has been successfully created, it will appear in the the dedicated ``Required Compute Resource Property Field`` of the ``Algorithm View``.

![alt text](/user-guide/images/algorithm/Add_Compute_Resource_-_Step_4.PNG "Verify creation")

### Update Compute Resource Properties

!!! info 
    To update a compute resource property of the algorithm, the user has to be in the ``Algorithm View`` which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Updating properties of an algorithm is done in the ``General Tab`` of the ``Algorithm View``. To do that, the user has to simply hover over an existing property in the dedicated ``Required Compute Resource Property Field`` and then click on the ``Edit button``.	
	
![alt text](/user-guide/images/algorithm/Update_Compute_Resource_-_Step_1.PNG "Open update property dialog")

This will open a separate ``Update Dialog`` where the information of the property can be adjusted.

!!! note 
	The **Type Name** field supports auto-completion functionality. While typing a type name, the system will suggest existing types with that name in a drop-down. On click of an existing type, all necessary fields will be filled automatically.

![alt text](/user-guide/images/algorithm/Update_Compute_Resource_-_Step_2.PNG "Dialog structure")

After all fields have been adjusted, the user can finally update the property by confirming the update via the existing ``OK Button``.

!!! note 
	The **Property Value** needs to match the selected **Data Type**.

![alt text](/user-guide/images/algorithm/Update_Compute_Resource_-_Step_3.PNG "Confirm update")

### Delete Compute Resource Properties

!!! info 
    To delete a compute resource property of an algorithm, the user has to be in the ``Algorithm View`` which can be reached by clicking on a compute resource in the ``Algorithm List View``.
	
Deleting compute resource properties is done in the ``General Tab`` of the ``Algorithm View``. To do that, the user has to simply hover over an existing property in the dedicated ``Required Compute Resource Property Field`` and then click on the ``Delete button``.

![alt text](/user-guide/images/algorithm/Delete_Compute_Resource.PNG "Delete Compute Resource")

!!! info 
	A successfully deleted property should disappear from the dedicated ``Required Compute Resource Property Field``.

### Reference Application Areas

!!! info 
    To reference application areas in an algorithm, the user has to be in the ``General Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Referencing problem types is done via the dedicated ``Application Areas`` field.

![alt text](/user-guide/images/algorithm/Link_Application_Area_-_Step_1.PNG "Go to dedicated application area field in algorithm view")

To link a application area with the algorithm, the user has to use the input field to search for an application area by typing it's name. While typing, the system's auto-complete feature will display available application areas in a drop-down.
To finally link a application area, the user has to click on one of the available areas from the drop-down. 

!!! note
    Alternatively, the user can use the arrow keys of the keyboard to select an application area and confirm by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Link_Application_Area_-_Step_2.PNG "Search for application area by name")

After successfully referencing the application area, it will be displayed in the ``Application Areas`` field.

![alt text](/user-guide/images/algorithm/Link_Application_Area_-_Step_3.PNG "Verify reference")

### Dereference Application Areas

!!! info 
    To remove an existing reference to an application area, the user has to be in the ``General Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

To dereference an application area, the user has to scroll to the ``Application Areas`` field and simply click on the ``Delete button`` of the application area he wants to remove from the algorithm.

![alt text](/user-guide/images/algorithm/Unlink_Application_Area.PNG "Unlink Application Area")

### Reference Problem Types

!!! info 
    To reference problem types in an algorithm, the user has to be in the ``General Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Referencing problem types is done via the dedicated ``Problem Types`` field.

![alt text](/user-guide/images/algorithm/Link_Problem_Type_-_Step_1.PNG "Go to dedicated problem types field in algorithm view")

To link a problem type to the algorithm, the user has to use the input field to search for a problem type by typing it's name. While typing, the system's auto-complete feature will display available problem types in a drop-down.
To finally link a problem type, the user has to click on one of the problem types from the drop-down. 

!!! note
    Alternatively, the user can use the arrow buttons on the keyboard to select a problem type and confirm the link with the "Enter" button on the keyboard.

![alt text](/user-guide/images/algorithm/Link_Problem_Type_-_Step_2.PNG "Link Problem Type")

After the linking process has been successfully completed, the freshly linked problem type will be displayed beneath the input field.

![alt text](/user-guide/images/algorithm/Link_Problem_Type_-_Step_3.PNG "Link Problem Type")

### Dereference Problem Types

!!! info 
    To remove an existing reference to a problem type, the user has to be in the ``General Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

To dereference a problem type, the user has to scroll to the ``Problem Types`` field and simply click on the ``Delete button`` of the problem type he wants to remove from the algorithm.

![alt text](/user-guide/images/algorithm/Unlink_Problem_Type.PNG "Unlink Problem Type")

### Reference other Algorithms

!!! info 
    To reference other algorithms, the user has to be in the ``Related Algorithms Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.
	
To reference some other algorithm in the current one, the user has to click on the ``Plus button`` in the ``Related Algorithms Tab``.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_1.PNG "Click on '+' in 'Related Algorithms'-Tab")

A dialog will open that contains multiple fields that need to be filled by the user to create a relation to some algorithm.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_2.PNG "Structure of dialog")

In the first step, the user has to describe the relation by entering a description of the relation.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_3.PNG "Enter description of relation")

Then, the other algorithm that should be referenced needs to be selected. For that he can use the input field to find available algorithms by name. The auto-complete of the system will filter available algorithms and display them in a drop-down. The user can pick an algorithm by clicking on it.

!!! note
    Alternatively, the user can use the arrow buttons on the keyboard to select an algorithm and then confirm it by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_4.PNG "Choose algorithm to link")

At last, the type of the relation of the two algorithms needs to be selected. While typing in a relation type, the auto-complete of the system will filter existing relation types while giving the user to ability to create a new one. The user can select an existing relation type or create a new by just by clicking on it.

!!! note
    Alternatively, the user can use the arrow buttons on the keyboard to select a relation type and then confirm it by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_5.PNG "Select relation type")

After all input data has been filled, the user can confirm the creation of a reference between the two algorithms by clicking on the ``OK Button``.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_6.PNG "Confirm the reference to the selected algorithm")

After the other algorithm was successfully referenced, it will appear in the ``Related Algorithms`` tab of the ``Algorithm View``.

![alt text](/user-guide/images/algorithm/Link_Other_Algorithm_-_Step_7.PNG "Verify reference to other algorithm")

### Update Algorithm Relation

!!! info 
    To update an existing algorithm relation, the user has to be in the ``Related Algorithms Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Updating an algorithm relation is done by clicking on the "Edit" button of a related algorithm in the ``Related Algorithms`` tab.

![alt text](/user-guide/images/algorithm/Update_Link_Other_Algorithm_-_Step_1.PNG "Open update relation dialog")

This will open a dialog where the user can adjust the information of the relation. Here, the user can change the description and the type of the relation, before confirming the changes by clicking the ``OK Button``.

!!! note
    Same as with the ``Creation Dialog``, the ``Relation Type`` field has auto-complete functionality. The system will filter existing relation types while giving the user the ability to create a new one. The user can select an existing relation type or create a new by just by clicking on it or by using the arrow keys on the keyboard in combination with the ``Enter`` key.

![alt text](/user-guide/images/algorithm/Update_Link_Other_Algorithm_-_Step_2.PNG "Adjust algorithm relation in dialog and confirm")

### Dereference other Algorithms

!!! info 
    To delete existing references to other algorithms, the user has to be in the ``Related Algorithms Tab`` of the ``Algorithm View``, which can be reached by clicking on a compute resource in the ``Algorithm List View``.

To remove a reference, the user can to simply click on the ``Delete Button`` of a related algorithm in the ``Actions Column``.

![alt text](/user-guide/images/algorithm/Unlink_Other_Algorithm_-_Step_1.1.PNG "Dereference single algorithm")

Alternatively, use the check-boxes to select multiple algorithms and then click on the ``Master Delete button`` to unlink all of them at once.

![alt text](/user-guide/images/algorithm/Unlink_Other_Algorithm_-_Step_1.2.PNG "Dereference multiple algorithms")

!!! note 
    ``Master Delete button`` will only appear if at least one related algorithm is selected.

If a ``Delete`` button is pressed, a confirmation dialog will appear listing all related algorithms that will be unlinked. To confirm the deletion of the relations to all displayed algorithms, the user has to click on the ``YES Button``.

![alt text](/user-guide/images/algorithm/Unlink_Other_Algorithm_-_Step_2.PNG "Confirm deletion of the references")

### Reference Publications

!!! info 
    To reference publications in an algorithm, the user has to be in the ``Publications Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.
	
To initiate the linking of a publication, the user has to click on the ``Plus Button`` in the ``Publications Tab``.

![alt text](/user-guide/images/algorithm/Link_Publication_-_Step_1.PNG "Click on '+' in 'Publications'-Tab")

This will open a new dialog containing a page-able table of available publications. This table can be searched or sorted using the given input fields and buttons.

![alt text](/user-guide/images/algorithm/Link_Publication_-_Step_2.PNG "Link Publication")

To reference a publication simply click on the ``Link Button`` in the ``Actions Column``.

![alt text](/user-guide/images/algorithm/Link_Publication_-_Step_3.1.PNG "Link Publication")

Alternatively, use the check-boxes to select multiple publications and then click on the ``Master Link Button`` to link all of them at once.

!!! note 
    ``Master Link button`` will only appear if at least one publication is selected.
	
![alt text](/user-guide/images/algorithm/Link_Publication_-_Step_3.2.PNG "Link Publication")

!!! info 
    Successfully referenced publications(s) will now be visible in the ``Publications Tab`` of the ``Algorithm View``.

### Dereference Publications

!!! info 
    To dereference publications, the user has to be in the ``Publications Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.
	
To remove a reference from a publication, the user has to simply click on the ``Delete Button`` of a publication in the ``Actions Column``.

![alt text](/user-guide/images/algorithm/Unlink_Publication_-_Step_1.1.PNG "Dereference single publication")

Alternatively, use the check-boxes to select multiple publications and then click on the ``Master Delete Button`` to unlink all of them at once.

!!! note 
    ``Master Delete Button`` will only appear if at least one publication is selected.
	
![alt text](/user-guide/images/algorithm/Unlink_Publication_-_Step_1.2.PNG "Dereference multiple publications")

### Add Tags

!!! info 
    To add tags to an algorithm, the user has to be in the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

In the ``Header`` of the ``Algorithm View``, the user has to click on the ``Plus Button`` which is used to add tags.

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_1.PNG "Click '+' button in 'Algorithm View' header")

A ``Add Tag Dialog`` will open which contains fields for ``Tag Category`` and ``Tag Value`` that need to be defined for creating a new tag.

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_2.PNG "Structure of 'Add Tag Dialog'")

The ``Tag Value Field`` is equipped auto-complete functionalities. While typing, it will recommend existing values to the user. The user can then either pick one of the existing values by clicking on it. Alternatively, the user can ignore the recommendations and fill the input field with a new tag value.

!!! note
    Alternatively, the user can use the arrow buttons on the keyboard to select an existing tag value and then confirm it by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_3.PNG "Enter Tag Value")

The ``Tag Category Field`` is equipped auto-complete functionalities. While typing, it will recommend existing categories to the user. The user can then either pick one of the existing categories by clicking on it. Alternatively, the user can ignore the recommendations and fill the input field with a new tag category.

!!! note
    Alternatively, the user can use the arrow buttons on the keyboard to select an existing tag category and then confirm it by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_4.PNG "Enter Tag Category")

To finally add a new tag to the algorithm, the user has to confirm his selection by clicking on the ``OK Button``. 

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_5.PNG "Confirm addition of a new tag")

If the tag was added successfully, it will appear in the ``Header`` of the ``Algorithm View``.

![alt text](/user-guide/images/algorithm/Add_Tag_-_Step_6.PNG "Verify if tag was created")

### Remove Tags

!!! info 
    To remove tags from an algorithm, the user has to be in the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Removing tags is done by clicking on their ``Delete Buttons``, which are located in the ``Header`` of the ``Algorithm View``.

![alt text](/user-guide/images/algorithm/Remove_Tag.PNG "Remove Tag")

### Reference Patterns

!!! info 
    To reference patterns in an algorithm, the user has to be in the ``Related Patterns Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.
	
To initiate the linking of a pattern, the user has to click on the ``Plus Button`` in the ``Related Patterns Tab``.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_1.PNG "Click on '+' button")

This will open a new dialog containing multiple steps that need to be performed.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_2.PNG "Structure of dialog for referencing patterns")

In the first step, a pattern language needs to be selected by simply clicking on it. To filter specific pattern languages, the user can use the input field to filter them by their name.  

!!! info
    By clicking on the small button at the bottom of a specific pattern language, a new browser window will open and all patterns of the selected pattern language are presented in the Pattern Atlas.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_3.PNG "Select Pattern Language")

After a specific pattern language has been selected, the user can move the the next step by either clicking on the ``Next Button`` or by clicking on the second step.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_4.PNG "Move to second step")

In the second step, the user has to pick a pattern he wants to reference by clicking on it. Like in the first step, he can use the input field to filter the patterns by their names and he also can use the scrollbar to scroll through all patterns.

!!! info
    By clicking on the small button at the bottom of a specific pattern, a new browser window will open and the selected pattern with its properties is presented in the Pattern Atlas.


![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_5.PNG "Select Pattern")

After a specific pattern has been selected, the user can move to the next step by either clicking on the ``Next Button`` or by clicking on the third step.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_6.PNG "Move to third step")

In the third step, the user has to describe the relation between the selected pattern and the algorithm. To do that, he has to specify a ``Relation Type`` and add a ``Description``.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_7.PNG "Structure of dialog's third step")

The input field for the relation type has auto-complete functionality. It will filter all existing relation types while still providing the user the option to create a new one. To confirm a relation type, the user has to simply click on it. 

!!! note
    Alternatively, the arrow keys of the keyboard can be used to navigate through all the options. Selecting a relation type can be done by hitting ``Enter``. 
	
![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_8.PNG "Select Relation Type")

At last, the user has to add a description by using the existing input field. After that, the user can proceed to the last step by clicking on the ``Next Button`` or by clicking directly on the step itself.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_9.PNG "Add Description and move to last step")

The last step is used for verifying all the important selections from the previous steps. To finally reference the pattern in the algorithm, the user can press the ``Confirm Button``.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_10.PNG "Verify all inputs")

After the pattern was successfully referenced, it will appear in the ``Related Patterns Tab`` of the ``Algorithm View``.

![alt text](/user-guide/images/algorithm/Link_Pattern_-_Step_11.PNG "Verify if reference was successful")

### Update Pattern Relation

!!! info 
    To update the relation to a pattern, the user has to be in the ``Related Patterns Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Updating a pattern relation is done by clicking on it's ``Edit Button``.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_1.PNG "Click 'Edit' button")

This will open a dialog containing two steps that need to be performed to successfully update the relation.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_2.PNG "Structure of update dialog")

In the first step, the user can adjust the ``Relation Type`` and the ``Description``.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_3.PNG "Structure of first step")

To adjust the ``Relation Type``, the user simply has to use the existing input field to change the current type. The auto-complete functionality of the system will filter all existing relation types while still providing the user the option to create a new one. To confirm a relation type, the user has to simply click on it. 

!!! note
    Alternatively, the arrow keys of the keyboard can be used to navigate through all the options. Selecting a relation type can be done by hitting ``Enter``.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_4.PNG "Update Relation Type")

To adjust the ``Description``, the user can use the existing input field. After that, the user can proceed to the second step by clicking on the ``Next Button`` or by clicking directly on the step itself.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_5.PNG "Update Description and move to last step")

The second and last step is used for verifying all the important selections from the first step. To finally adjust the reference between the pattern and the algorithm, the user has to click on the ``Confirm Button``.

![alt text](/user-guide/images/algorithm/Update_Pattern_Link_-_Step_6.PNG "Confirm update of reference")

### Dereference Patterns

!!! info 
    To remove a reference to a pattern, the user has to be in the ``Related Patterns Tab`` of the ``Algorithm View``, which can be reached by clicking on an algorithm in the ``Algorithm List View``.

Dereferencing a pattern is done by clicking on it's ``Delete Button``.

![alt text](/user-guide/images/algorithm/Unlink_Pattern_-_Step_1.1.PNG "Dereference single pattern")

Alternatively, the user can use the check-boxes of the first column of the table to select all pattern relation he wants to remove before clicking on the ``Master Delete Button``. 

!!! note 
    ``Master Delete Button`` will only appear if at least one related pattern is selected.
	
![alt text](/user-guide/images/algorithm/Unlink_Pattern_-_Step_1.2.PNG "Dereference multiple patterns")

If a ``Delete Button`` is pressed, a confirmation dialog will appear listing all pattern references that will be removed. To confirm their deletion, the user has to click on the ``YES Button``.

![alt text](/user-guide/images/algorithm/Unlink_Pattern_-_Step_2.PNG "Confirm the removal of the references")
