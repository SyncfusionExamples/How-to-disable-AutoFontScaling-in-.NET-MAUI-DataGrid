# How to disable AutoFontScaling in .NET MAUI DataGrid (SfDataGrid)?
In this article, we will show you how to disable AutoFontScaling in [.Net Maui DataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid).

## xaml
The below code illustrates how to disable AutoFontScaling even if the user has accessibility options or screen size settings enabled on the device.
```
<ContentPage.Resources>
    <ResourceDictionary>
        <Style TargetType="syncfusion:SfDataGridLabel">
            <Setter Property="FontAutoScalingEnabled" Value="False" />
        </Style>
        <Style TargetType="syncfusion:SfDataGridHeaderLabel">
            <Setter Property="FontAutoScalingEnabled"
                    Value="False" />
        </Style>
        <Style TargetType="syncfusion:DataGridHeaderCell">

            <Setter Property="FontAttributes"
                    Value="Bold" />
            <Setter Property="FontSize"
                    Value="12" />
            <Setter Property="Padding"
                    Value="1" />
        </Style>

        <Style TargetType="syncfusion:DataGridCell"
               x:Key="ComponentCellStyle">
            <Setter Property="FontSize"
                    Value="12" />
            <Setter Property="TextAlignment"
                    Value="Start" />
            <Setter Property="Padding"
                    Value="5,5,5,5" />
            <Setter Property="FontAttributes"
                    Value="Bold" />
        </Style>

        <Style TargetType="syncfusion:DataGridCell">
            <Setter Property="FontSize"
                    Value="12" />
            <Setter Property="Margin"
                    Value="0,0,0,0" />
            <Setter Property="Padding"
                    Value="0,0,0,0" />
        </Style>
    </ResourceDictionary>
</ContentPage.Resources>

<ContentPage.BindingContext>
    <local:EmployeeViewModel x:Name="viewModel"/>
</ContentPage.BindingContext>

<syncfusion:SfDataGrid x:Name="sfGrid"
                       Margin="0,0,0,0"
                       Padding="0"
                       GridLinesVisibility="Both"
                       HeaderGridLinesVisibility="Both"
                       ColumnWidthMode="Fill"
                       HeaderRowHeight="30"
                       RowHeight="40"
                       HorizontalScrollBarVisibility="Never"
                       VerticalScrollBarVisibility="Never"
                       AutoGenerateColumnsMode="None"
                       AllowResizingColumns="False"
                       ItemsSource="{Binding Employees}">

    <syncfusion:SfDataGrid.DefaultStyle>
        <syncfusion:DataGridStyle HeaderRowBackground="#e0e0e0"
                                   HeaderRowTextColor="Black"
                                   RowBackground="White"
                                   RowTextColor="Black"
                                   SelectionBackground="#AFD5FB"
                                   CurrentCellBorderColor="#AFD5FB"
                                   GridLineStrokeThickness="2"
                                   GridLineColor="#e0e0e0" />
    </syncfusion:SfDataGrid.DefaultStyle>

    <syncfusion:SfDataGrid.Columns>

        <syncfusion:DataGridNumericColumn MappingName="EmployeeID"
                                          HeaderTextAlignment="Center"
                                          CellTextAlignment="Center"
                                          Format="#" HeaderText="Employee ID" />
        <syncfusion:DataGridTextColumn MappingName="Name" 
                                       HeaderText="Employee Name"
                                       HeaderTextAlignment="Center"
                                       CellTextAlignment="Center" />
        <syncfusion:DataGridTextColumn MappingName="Title"
                                       HeaderText="Designation"
                                       HeaderTextAlignment="Center"
                                       CellTextAlignment="Center" />
        <syncfusion:DataGridDateColumn MappingName="HireDate"
                                       HeaderText="Hire Date"
                                       Width="130"
                                       HeaderTextAlignment="Center"
                                      />

    </syncfusion:SfDataGrid.Columns>

</syncfusion:SfDataGrid>
```

![AutoFontScalling.png](https://support.syncfusion.com/kb/agent/attachment/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjMyODAzIiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.c8_BGUrUs_hUM6F2n_hGDzxD2kU_Iracyb4OzzgjqV4)
 
[View sample in GitHub](https://github.com/SyncfusionExamples/How-to-disable-AutoFontScaling-in-.NET-MAUI-DataGrid)

Take a moment to explore this [documentation](https://help.syncfusion.com/maui/datagrid/overview), where you can find more information about Syncfusion .NET MAUI DataGrid (SfDataGrid) with code examples. Please refer to this [link](https://www.syncfusion.com/maui-controls/maui-datagrid) to learn about the essential features of Syncfusion .NET MAUI DataGrid (SfDataGrid).
 
##### Conclusion
 
I hope you enjoyed learning about how to disable AutoFontScaling in .NET MAUI DataGrid (SfDataGrid).
 
You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to learn about its other groundbreaking feature representations. You can also explore our [.NET MAUI DataGrid Documentation](https://help.syncfusion.com/maui/datagrid/getting-started) to understand how to present and manipulate data. 
For current customers, you can check out our .NET MAUI components on the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to explore our .NET MAUI DataGrid and other .NET MAUI components.
 
If you have any queries or require clarifications, please let us know in the comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid), or the feedback portal. We are always happy to assist you!