# ToDoList
perform list of toDo missions

Explanation of the project:

Client-side :

On the client side there are 2 components:
to-do-list - which shows the main content of all the tasks.
The second component:
edit-list which is responsible for all issues of editing the tasks.
In addition, I created a service:
edit-list where all the api calls to the server are made.
In addition, I also performed data validation, 
as the user enters a value in any field, then the same value must be validated, 
otherwise he receives an error message.

Server-side:
I choose to work for the Sql-server as my DB.
In the server we have "Models" folder There is defined the template of the list with all the properties.
 We have the control folder where all the CRUD operations and saving and updating of the DB are managed.
The operations on the DB are done through the use of migration.
In addition, we have the Logger library which actually  returns the value received from the Header to the Logger class
In the "appsettings" file there are the connection settings (connection string) to the DB

Excute project :

In order to run the program, first we will run the Server project.
After downloading the project, open the project and open the "toDoListAPI.sln" file.
Then we will run the project.
Preparations for working with the DB:

In order to create the tables in the DB we have to enter the "Packae manager console" (PMO)
and run the following commands:
1. dotnet ef migrations add InitialCreate
2. dotnet ef database update

After running the commands, we will make sure that the DB named "Todo" has been created  and in it the table: "Todos"

Now we will run the client's project:
Open the project (I developed in Visual Studio Code) and access the folder: "environments" and open the file: "environments.ts"
Now in the file we will change the value of the variable: "apiUrl" to the address of the server.
You can copy the URL from Swagger.
And now we will run the project by opening the terminal and typing the command:
ng serve -o
Now we can start using the app

