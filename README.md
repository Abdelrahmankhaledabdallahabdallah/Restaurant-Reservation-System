# Restaurant-Reservation-System

**Description:**

Restaurant Reservation System is a program that completely simulates a real life in a restaurant. The users of the system are divided into: Customers and 
Employees. Customers can reserve a table, make orders and finally checkout (get the price of their orders). On the other hand, Employees consists of three 
different types: Cooks, Waiters and Managers. First, Cooks are able to see the table number reserved by the customer with its ordered dishes to be ready. 
Second, Waiters can see the customers’ names and table numbers in order to be able to serve them. Finally, Managers can view all staff and customers 
details, and also see the total profit of the day.



**Features and Tasks implementation Details:**

The project required the implementation of the following features and tasks:
Implement three types of dishes: appetizers, main courses, and desserts.
Implement three types of employees: managers, waiters, and cooks.
Implement one or more types of customers.
Implement two or more types of tables, such as smoking and non-smoking areas.
Implement file handling to store and load data, including employee information, customer lists, dishes, and tables.
Develop a GUI that supports two modes of operation for customers and employees.
Draw a class diagram for the project.
Handle errors and display error messages to the user.
Apply object-oriented concepts like encapsulation, inheritance, and polymorphism.

**Scenarios Details:**

*  	Program starts with the Login screen, where all the data in the file, which contains all users, tables and dishes, is read. The login screen checks 
    entered username and password from the users data in the file and then navigate the user according to his role.

*  	In the login screen, there is a register button which navigate the user to another window where he can sign up if he is a new customer, otherwise he 
    should be a manager so that he can add new staff members or new tables or even new dishes. After registration, the user will be navigated back to the 
    login screen.

*  	If the username and password belongs to a Customer, then he will be navigated to the Customer Dashboard, where he can reserve a table from the 
    available ones and see the menu to be able to order the desired dishes with any quantity, where he can order the same dish more than once. Finally, he 
    is able to get his receipt with the order number, in addition to all ordered dishes, taxes and total price. **If the customer has already reserved a 
    table but his order wasn’t delivered yet, and he wanted to make another order, he will be considered as a new customer with the same table number but 
    different dishes (order)**. Finally, he will press the logout button and will be navigated to the login screen. To keep the state of the restaurant, we
    made an attribute called **“mode”**, which in this case the mode is **“preparing”** indicating that the order has been made and the dishes are being
    prepared.

*  	If the username and password belongs to a Cook, then he will be navigated to the Cook Dashboard, where he will be able to see the orders including : 
    order number, table number and dishes . He should choose which order to cook. Finally, he will press the logout button and will be navigated to the 
    login screen. Now, the mode of the customer becomes **“ready”** indicating that his order is ready.

*  	If the username and password belongs to Waiter, then he will be navigated to the Waiter Dashboard, where he will be able to see the orders including :
    order number, table number and customer name. He should choose which order to deliver to the customer. After all the orders for the same customer are 
    delivered to him, the table will be available to another customer to reserve. Finally, the waiter will press the logout button and will be navigated 
    to the login screen. Now, the mode of the customer becomes **“delivered”** indicating that he has received his order. **When the state is “delivered”, 
    the table becomes available again to other customers if and only if the same customer hasn’t ordered anything else on the same table as assumed before 
    (in Customer Dashboard)**.

*  	If the username and password belongs to a Manager, then he will be navigated to the Manager Dashboard, where he will be able to view all restaurant’s 
    staff and all customers details. He can see the total profit for each day. Finally, he will press the logout button and will be navigated to the login 
    screen.

*  	Each time anyone of the pre-mentioned users presses on the Logout button and navigated back to the login screen, the new data will saved and will be
    appended in the file “todayData”, which contains all users’ data, tables, dishes and all reservations of the day.

*  	**At the end of each day (at 12:00 AM)**, the xml file “todayData” that contains today reservations will **remove all reservations upon any
  	modification made to the system (registering or ordering)** and **append** them to another xml file “historyData” which will contain past reservations 
  	containing the date of the day with all customers’ details.
    
*  	To run the executable jar, images and files must be in the same folder of the jar in order to be able to run.

*  	**It is not allowed to exit any screen except the login screen**.

