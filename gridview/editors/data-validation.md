---
title: Data validation
page_title: Data validation | UI for WinForms Documentation
description: Data validation
slug: winforms/gridview/editors/data-validation
tags: data,validation
published: True
position: 3
---

# Data validation



## 

__RadGridView__ provides a convenient way to perform validation before data is committed to the underlying data source. You can validate data by handling __CellValidating__ event which is raised by __RadGridView__ when the current cell changes or when the cell loses input focus (when pressing Enter key). Canceling this event prevents the user from exiting the cell until a valid editor value is entered or the edit process is canceled. The __RowValidating__ event can be used the same way to prevent the user from exiting the current row.

Here is a list of all validation events:

__CellValidating__ – Fires when a cell loses input focus, enabling content validation.

__CellValidated__ – Fires after the cell has finished validating.

__RowValidating__ – Fires when a row is validating.

__RowValidated__ – Fires after a row has finished validating.

The __GridViewDataRowInfo.ErrorText__ property can be used to indicate validation errors. It will show an error indicator at the row header when you set this property to a non empty string.

The code snippet below demonstrates simple data validation scenario. It is enabled in a textbox column to enter only non-empty strings. When the string is empty, the validation fails and the error indicator at the row header is shown:#_[C#] Cell validation_

	



{{source=..\SamplesCS\GridView\Editors\DataValidation1.cs region=dataValidation}} 
{{source=..\SamplesVB\GridView\Editors\DataValidation1.vb region=dataValidation}} 

````C#
        void radGridView1_CellValidating(object sender, Telerik.WinControls.UI.CellValidatingEventArgs e)
        {
            GridViewDataColumn column = e.Column as GridViewDataColumn;
            if (e.Row is GridViewDataRowInfo && column != null && column.Name == "CategoryName")
            {
                if (string.IsNullOrEmpty((string)e.Value) || ((string)e.Value).Trim() == string.Empty)
                {
                    e.Cancel = true;
                    ((GridViewDataRowInfo)e.Row).ErrorText = "Validation error!";
                }
                else
                {
                    ((GridViewDataRowInfo)e.Row).ErrorText = string.Empty;
                }
            }
        }
````
````VB.NET
    Private Sub RadGridView1_CellValidating(ByVal sender As Object, ByVal e As Telerik.WinControls.UI.CellValidatingEventArgs) Handles RadGridView1.CellValidating
        Dim column As GridViewDataColumn = TryCast(e.Column, GridViewDataColumn)
        If TypeOf e.Row Is GridViewDataRowInfo AndAlso column IsNot Nothing AndAlso column.Name = "CategoryName" Then
            If String.IsNullOrEmpty(DirectCast(e.Value, String)) OrElse DirectCast(e.Value, String).Trim() = String.Empty Then
                e.Cancel = True
                DirectCast(e.Row, GridViewDataRowInfo).ErrorText = "Validation error!"
            Else
                DirectCast(e.Row, GridViewDataRowInfo).ErrorText = String.Empty
            End If
        End If
    End Sub
    '
````

{{endregion}} 




>note You can watch the movie[Validation with RadGridView for WinForms](http://tv.telerik.com/winforms/radgridview/validation-with-radgridview-winforms)regarding the usage of RadGridView built-in validation.
>
