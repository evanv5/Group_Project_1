# Group_Project_1
## Team Members:
1. Abby, Kern
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
