# User Interface Specification
## 1. Introduction

This document specifies the usage and technical features of the user interface which is provided in the following figure.

![UI](/uispec/assets/image001.jpg "User Interface")
<br>
This user interface is designed to sign new users up to the system and to display the current users in the system.

There is a database connected to that application which stores the information of users. The columns of the related table of the database are like the following.
<br>
| ID          | Username    |  DisplayName      | Phone       | Email      | UserRole       | Enabled       |
| ----------- | ----------- |  -------          | ----------- | -------          | ----------- | -------       |
| NULL   | NULL        |  NULL           | NULL | NULL      | NULL       | NULL       |
<br>

The tuples of that table(users) is created with the filled inputs in the sign up form in the user interface. Display part of the user interface queries the database in order to display particular columns and their values such as *ID*, *User Name* , *Email* and *Enabled*.
<br>

## 2. Design Details
<br>
The user interface can be divided into three sections as it is provided in the following figure.<br>

![UI](/uispec/assets/son.png "User Interface")
<br>

### **Section 1**
This section is located on the top of the user interface. It contains two buttons and a checkbox. 

#### *New User Button*
This button creates an empty sign up form on the right side of the user interface.

#### *Save User Button*
This button let the system create a new tuple with the given values in the form inputs and insert the tuple to the database table.

#### *Hide Disable User Checkbox*
This checkbox hides the users whose *Enabled* value is false queried with `"Enabled" = false` in the table. So, it alters the display part regarding to that.
<br>

### **Section 2**
This section is located on the left side of the user interface. It displays the particular columns of the table which contains information about the signed up users. This part is updated as a new user signed up and inserted into database with the *Save User Button*.

Displayed columns can be sorted with the sort buttons near the column names.
<br>

### **Section 3**
This section is located on the right side of the user interface. This part contains a sign up form with input fields related to the information about user.

#### *Username*
This input field takes a text input in order to assign its value to the *Username* of the user.

#### *Display Name*
This input field takes a text input in order to assign its value to the *DisplayName* of the user.

#### *Phone*
This input field takes a text input in order to assign its value to the *Phone* of the user.

#### *Email*
This input field takes a text input in order to assign its value to the *Email* of the user.

#### *User Roles*
This input field takes a dropdown input in order to assign its value to the *UserRoles* of the user. The choice of the dropdown input can be *Guest*, *Admin* and *SuperAdmin*.

#### *Enabled*
This input field takes a checkbox input in order to assign its value to the *Enabled* of the user. The assigned value will be a boolean value and will assigned `true` if checkbox is checked, will assigned `false` vice versa.

After filling out the form, the user can be saved to the database and displayed via *Save User Button*.








  