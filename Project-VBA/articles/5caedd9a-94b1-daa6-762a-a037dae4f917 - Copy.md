
# Application.ProjectBeforeAssignmentNew Event (Project)

Occurs before one or more assignments are created.


## Syntax

 _expression_. **ProjectBeforeAssignmentNew**( **_pj_**,  **_Cancel_**)

 _expression_A variable that represents an  **Application** object.


### Parameters



|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
|pj|Required| **Project**|The project in which an assignment or assignments are being created.|
|Cancel|Required| **Boolean**| **False** when the event occurs. If the event procedure sets this argument to **True**, the new assignment(s) are not created.|

### Return Value

nothing


## Remarks

The  **ProjectBeforeAssignmentNew** event also fires when a resource assignment is replaced. Additionally, the event will fire when the only resource assignment on a task is removed, because an "Unassigned Resource" assignment is created after the existing assignment is removed.

Project events do not occur when the project is embedded in another document or application. 

The  **ProjectBeforeAssignmentNew** event doesn't occur when an assignment is created as the result of a drag-and-drop operation in the ** Resource Usage** view, during resource pool operations, when inserting or removing a subproject, or when changes have been made using a custom form.

