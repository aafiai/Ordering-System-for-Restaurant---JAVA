# Ordering-System-for-Restaurant---JAVA
Developed a Java-based ordering system using Eclipse IDE with a graphical user interface (GUI) for seamless customer interaction. Integrated MySQL for database storage to manage orders and customer information. Established a direct connection between customers and the kitchen, and implemented a billing system to automatically generate final invoices, enhancing the efficiency and convenience of the food ordering process.



The provided code is for a Restaurant Management System written in Java using AWT (Abstract Window Toolkit) for the GUI, and MySQL for the backend database. Here's an overview of its functionality:

# Key Functionalities:
Main Menu:

The program starts with a MainMenu class, which displays a welcome frame with a button labeled "Order."
Clicking the "Order" button transitions the user to the SaladPage class.

Salad and Pasta Ordering:

SaladPage: Allows the user to select from a variety of salads, displaying their names and prices. A "Submit" button adds selected salads to the order.
PastaPage: Similar to SaladPage, but for pasta items. The user can select pasta dishes with their respective prices and add them to the order.
Both pages utilize the Order class to store the selected items and their prices.

Order Management:

The Order class handles the storage of selected items (salads and pasta) and their prices using ArrayLists. It includes getter methods for retrieving the size and individual items/prices.

Billing:

After making selections, the Billing class displays a receipt with a list of items (salads and pasta) and their prices. It calculates the total and provides an option to submit the order.
Upon submission, the order details are inserted into a MySQL database table (Kitchen) for further processing.

Feedback:

After submitting the order, the user is directed to a Feedback form where they can rate various aspects of the restaurant (e.g., food, service, ambiance) using radio buttons.
The feedback data, along with the user's name, is stored in a MySQL database (Feedback table).
# Key Technical Features:
GUI Components:

Uses AWT components like Frame, Label, Button, Checkbox, and Panel.
Positions components manually with setBounds for precise layout control.

Database Integration:

Connects to a MySQL database using the com.mysql.cj.jdbc.Driver.
Executes SQL INSERT queries to store order and feedback data in the Kitchen and Feedback tables.

Navigation:

Uses dispose() to close the current window and transition to the next step in the workflow.

Object-Oriented Structure:

Classes like Order, SaladPage, PastaPage, and Billing modularize functionality, maintaining clear separation of concerns.

# Workflow:
User starts at the MainMenu.
Navigates to SaladPage to select salads.
Proceeds to PastaPage to add pasta to the order.
Reviews the order in the Billing class, which displays a receipt and calculates the total.
Submits the order, saving it to the Kitchen table in the database.
Completes feedback in the Feedback form, storing ratings in the database.
