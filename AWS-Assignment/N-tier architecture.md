What is N-Tier Architecture?

N-tier architecture is also called multi-tier architecture because the software is engineered to have the processing, data management, and presentation functions physically and logically separated.  That means that these different functions are hosted on several machines or clusters, ensuring that services are provided without resources being shared and, as such, these services are delivered at top capacity.  The “N” in the name n-tier architecture refers to any number from 1.

Not only does your software gain from being able to get services at the best possible rate, but it’s also easier to manage.  This is because when you work on one section, the changes you make will not affect the other functions.  And if there is a problem, you can easily pinpoint where it originates.

A More In-Depth Look at N-Tier Architecture
N-tier architecture would involve dividing an application into [three different tiers](https://msdn.microsoft.com/en-us/library/bb384398.aspx).  These would be the

1- logic tier,
2- the presentation tier, and
3- the data tier.

![Image](https://github.com/users/agileguru/projects/24/assets/130822600/9597f9a3-eed0-466c-b40e-fc4ea353480d)

## Presentation Tier:

The presentation tier is the tier in which users interact with an application. It often contains additional application logic also. Typical presentation tier components include the following:

Data binding components, such as the [BindingSource](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.bindingsource) and [BindingNavigator](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.bindingnavigator).

Object representations of data, such as [LINQ to SQL](https://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655) entity classes for use in the presentation tier.

The presentation tier typically accesses the middle tier by using a service reference (for example, a [Windows Communication Foundation Services and WCF Data Services in Visual Studio](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2015/data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio?view=vs-2015) application). The presentation tier does not directly access the data tier. The presentation tier communicates with the data tier by way of the data access component in the middle tier.

## Middle Tier:

The middle tier is the layer that the presentation tier and the data tier use to communicate with each other. Typical middle tier components include the following:

Business logic, such as business rules and data validation.

Data access components and logic, such as the following:

[TableAdapters](https://msdn.microsoft.com/library/09416de9-134c-4dc7-8262-6c8d81e3f364) and [DataAdapters and DataReaders](https://msdn.microsoft.com/library/cc952ca2-ec19-46ab-9189-15174b52cb74).

Object representations of data, such as [LINQ to SQL](https://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655) entity classes.

Common application services, such as authentication, authorization, and personalization.

The following illustration shows features and technologies that are available in Visual Studio and where they might fit in to the middle tier of an n-tier application.

## Data Tier: 

The data tier is basically the server that stores an application's data (for example, a server running SQL Server).

The following illustration shows features and technologies that are available in Visual Studio and where they might fit in to the data tier of an n-tier application.



