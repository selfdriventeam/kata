# [UI Component](../../../README.md)

UI Component will provide different views for the following users 
+ [Chef](doc/personas/alice_(chef).md)
+ [Kiosk Worker](doc/personas/barbara_(kiosk_worker).md) 
+ [Analyst](doc/personas/claire_(analyst).md) 
+ [Delivery Driver](doc/personas/edward_(delivery_driver).md) 
+ [Subscription Customer](doc/personas/jennifer_(subscriber).md) 
+ [Nutritionist](doc/personas/mark_(nutritionist).md) 
+ [Occasional Customer](doc/personas/scott_(eater).md)

All users would be required to go through [authentication](doc/arc/adrs/adr_007.md), we decided to use [external identify provided](doc/arc/adrs/adr_007.md) because user can leverage existing accounts to login into the web application directly. 

We decided to use [responsive web application instead of native app](doc/arc/adrs/adr_012.md) s the form of front end, because it is fast to develop and available for all users. The responsiveness design will automatically adapt browser space for different platforms with different resolution, but the look and feel of the app will be consistent across all platforms.

There are many UI architecture patterns can be used to construct the GUI, and we will use MVC pattern to get started, because it is fast and easy to develop, and suitable for simple user interface. If GUI logical gets more complicated in the future, we can use MVVM pattern because it provides better separation and better test-ability. 


