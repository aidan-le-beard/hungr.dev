# hungr.dev
This is a cross-platform Android/iOS Dynamic Grocery List app created in Flutter/Dart, with full backend API/database support. The app allows creation of shopping lists that are shareable amongst groups such as family members, where all members can add and delete items from the shared dynamic grocery list. The API/database can be found at https://github.com/aidan-le-beard/api.hungr.dev

## Backend 


### Data Storage: JSON File, SQLite

Json File: 

While it is possible to use a file based system for the requirements of the application, lots of things will have to be considered. 
File access while many agents are using it will be a problem, having a lock file in place would eliminate the cause of many users having many different states. 
At the same time the cost of this would be the UX of the application. 
Not being able to edit the contents of grocery list in a reasonable amount of time would annoy most users. 

SQLite: 

Satisfies all the data requirements.
There are plenty of node modules for interacting with an sqlite database.
The database can live on the same machine as the http server, 
reducing the overhead of calling to another machine like we would with Postgres. 
Would also be the most accessible between the two databases because postgres can be a bear to handle. 

Auth: 

Google's Firebase auth comes with secure authentication that is easily implemented into Flutter apps.

Users: 
Standard email and password sign up using Firebase, with ability to reset password.

## Frontend

The clients of the application will feed directly to the servers with only taking a local state of the saved grocery list. 
The clients will be able to send push notifications to the users about the state of the server. 


### iOS Application: 
##### Stack: 
Swift: General Multi-Paradigm Programming Language
SwiftUI: Declarative User Interface Builder, Stateful updates
Async/Await: Asynchronous method of scheduling work to be done, useful for networking and other tasks that cannot be done synchronously. 

### Android Application: 
##### Stack: 

Dart

Python

SQL


## Website
A statically generated site to track the progress and show off the application. 

##### Stack: 
Hugo
HTML
CSS

## Sample App Use Images:

#### Home Screen:
<img src="https://user-images.githubusercontent.com/33675444/206810671-1e74b9ec-d457-4bb2-a487-cfc3f5a6178c.png" width="415" height="922" />

#### Temporary Deletion: Swiping to the Right on an Item
<img src="https://user-images.githubusercontent.com/33675444/206810024-09846ad9-7c19-4839-80d9-b90078848f92.png" width="415" height="922" />

#### Permanent Deletion: Long Press on an Item
<img src="https://user-images.githubusercontent.com/33675444/206810001-836d3ffa-c4b6-4055-beba-861f4e3f9082.png" width="415" height="922" />

#### Adding an Item to the Grocery List using Floating Action Button Marked "+"
<img src="https://user-images.githubusercontent.com/33675444/206810091-cdcac381-3ce9-435b-96c9-458b6958a85f.png" width="415" height="922" />

#### Options in 3 Dot Menu:
<img src="https://user-images.githubusercontent.com/33675444/206810076-8c5b5c6d-436c-4857-b360-234a468cb6f2.png" width="415" height="922" />

#### Hiding Floating Action Buttons on Scrolling Down:
<img src="https://user-images.githubusercontent.com/33675444/206810054-ba4dfd57-27aa-413c-84d9-2d9774b4195a.png" width="415" height="922" />

#### Result of Pressing "Join a Group" Button:
<img src="https://user-images.githubusercontent.com/33675444/206810829-8606ed9f-8151-4cb6-9ff2-13df8380b7a1.png" width="415" height="922" />

#### Result of Pressing "Make an Account"
<img src="https://user-images.githubusercontent.com/33675444/206810878-c9dae5b3-f1ae-4b49-a420-59aa2cd55582.png" width="415" height="922" />

#### Result of Pressing "Login"
<img src="https://user-images.githubusercontent.com/33675444/206810897-8c0ad046-da52-4f73-9aa5-b8a2682fe2c8.png" width="415" height="922" />

#### Result of Pressing "Join a Group" Button After Logging In/Making an Account:
<img src="https://user-images.githubusercontent.com/33675444/206810971-fc0c3623-76f8-4116-9c03-9a41a474ae50.png" width="415" height="922" />

#### Shared List Screen After Pressing "Add to Shared List"
##### Shows items added by self with blue highlighting, and added by others as white. Blue highlighted items can be dismissed by swiping to the right.
<img src="https://user-images.githubusercontent.com/33675444/206811023-a9a017a4-35d9-414b-8370-870a486296d7.png" width="415" height="922" />

#### Result of Pressing "Generate Shopping List" 
<img src="https://user-images.githubusercontent.com/33675444/206811076-285cc0e3-a609-440c-8758-fc38810987bd.png" width="415" height="922" />

#### Result of Pressing "Submit"
<img src="https://user-images.githubusercontent.com/33675444/206811091-8c6a0938-d41b-4dce-a83d-591c41930de9.png" width="415" height="922" />
