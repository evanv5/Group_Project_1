# Group_Project_1
## Team Members:
1. Abigail, Kern
2. Amber, Um
3. Evan Voss
## Problem Description:
Our data model is designed to address common challenges faced by small used vehicle dealerships, such as keeping track of inventory, preventing errors in availability, and managing sales records. The system maintains detailed information about each vehicle, including identifying details, pricing, and availability status, ensuring the dealership always knows which cars are on the lot and which have been sold. Once a sale occurs, the model links the vehicle to the employee who completed the sale and updates its status. By also recording customer information, the system helps with follow-ups and future marketing opportunities. Overall, the model improves efficiency, increases accountability, and provides valuable insights into both sales performance and inventory management.

## Data Model:
Our database is built to store information needed to run a used car dealership. The main table (used_vehicles) stores all the vehicles the dealership has and has had. it records data such as VIN, year, color, mileage, price, number of previous owners, and whether the car has a clean title. This table also relates to the next table model. 

The model table stores informaton specific to that model so it would not need to be written exactly the same for each car of that model the dealership has meaning it has a one-to-many relationship. Similar to the model table the make table which is also a one-to-many relationship since each make can have multiple models, stores the information relevant to all the models a manufacturer sells. Since each car only has one make and one model these tables make it easier for the dealership to keep track of what kinds of vehicles they have.

Sales are managed through the Sales Transaction entity, a one-to-one relationship because each car is unique it can only be sold to one person. Each transaction stores customer information (name and phone number), the car that was sold (VIN), and the final sale price. Since each car can only be sold once, each transaction links to one used car the employee who sold the car.

The Employee entity stores staff details, including their name, contact information, and manager assignment. Employees can be linked to multiple cars, but each car is associated with only one employee at a time therefore it is a one-to-many relationship.

<img width="1178" height="799" alt="Screenshot 2025-09-21 222752" src="https://github.com/user-attachments/assets/2f63668f-3a87-40b9-8bc8-1241b21218d8" />


## Queries:
###1. Query 1 retrieves all information about cars that are from 2021 and newer. If a customer wants a newer car this is a helpful query to be able to quickly retrieve the information about what cars are less than 5 years old.
<img width="791" height="279" alt="image" src="https://github.com/user-attachments/assets/ef6164b2-f3d4-48e0-a4e4-82084bd4dadc" />


2. This query returns  the number of cars and their status, so that managers can easily see the number of vehicles they have sold, on hold, and available for purchase.
<img width="630" height="261" alt="image" src="https://github.com/user-attachments/assets/4d498cf4-939b-41fd-983f-fa30dc981946" />


3. Query 3 allows the manager to see which employees are top sellers by adding together the prices of the cars each employee has sold. This query allows managers to evaluate employee
performance, set goals, and identify if there needs to be additional training. ​
<img width="598" height="261" alt="image" src="https://github.com/user-attachments/assets/f6443534-f80f-4cb5-9cb0-99854b88d54b" />


4. Query 4 allows managers to see the average price of cars that are available, sold, or on hold. It helps with pricing decisions and sales strategies, including determining which
vehicles may need promotions or discounts. Additionally, the average price of available cars provides a snapshot of the current inventory value.​
<img width="574" height="214" alt="image" src="https://github.com/user-attachments/assets/e82c2e44-e5cd-4a02-a303-7976aa3644db" />



5. Query 5 shows models in inventory that have never been sold. This is useful for managers because it helps to identify models that are stagnant, and may need price adjustments, marketing, or even removal from the dealership. ​
<img width="387" height="391" alt="image" src="https://github.com/user-attachments/assets/9ddea430-798c-40d3-906e-11e31a19a9c4" />



6. Query 6 allows managers to see higher performing employees by  retrieving employees who have sold cars with more than 2 previous owners OR without a clean title. These qualifications
make it trickier for employees to sell those vehicles due to their less desirable qualities. Thus, employees who have sold those vehicles could have more potential for rewarding. ​
<img width="457" height="366" alt="image" src="https://github.com/user-attachments/assets/d58763b5-982f-4c3f-854a-1df0bb19d0dc" />




Name of the database: 

All queries are bookmarked through stored procedures and can be called using this format: CALL TP_Qx(); where 'x' is the query number.





