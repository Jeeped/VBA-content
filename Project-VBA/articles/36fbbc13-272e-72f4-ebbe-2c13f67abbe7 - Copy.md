
# Resource.GetField Method (Project)

Returns the value of the specified resource custom field.


## Syntax

 _expression_. **GetField**( **_FieldID_**)

 _expression_A variable that represents a  **Resource** object.


### Parameters



|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
|FieldID|Required| **Long**|For a local custom field, can be one of the  ** [PjField](f0df0929-921c-1f33-ab42-192efdaeb64d.md)** constants for resource custom fields. For an enterprise custom field, use the ** [FieldNameToFieldConstant](0830db06-22a7-3ca5-c9ca-f9efbc360767.md)** method to get the FieldID.|

### Return Value

 **String**


## Example

The following example displays the value of a local resource custom field specified by the user.


```
Sub DisplayField() 
    Dim Temp As String 
 
    Temp = InputBox$("Enter the name of the field you want to see:") 
    Temp = LCase(Temp) 
 
    Select Case Temp 
        Case "name" 
            MsgBox (ActiveCell.Resource.GetField(FieldID:=pjResourceName)) 
        Case "initials" 
            MsgBox (ActiveCell.Resource.GetField(FieldID:=pjResourceInitials)) 
        Case "standard rate" 
            MsgBox (ActiveCell.Resource.GetField(FieldID:=pjResourceStandardRate)) 
        Case "" 
            End 
        Case Else 
            MsgBox "You entered an invalid field. Please try again." 
            End 
    End Select 
End Sub
```

For an example that uses an enterprise resource custom field, see the  ** [SetField](9ac1e770-8716-2954-4459-7f5ff090e2ed.md)** method.

