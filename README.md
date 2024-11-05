# Car-Dealership-Management-System
## Overview
The "Car Dealership System" is a Java-based application designed to manage a car dealership. It keeps track of available cars, employees, and sales transactions. Key features include adding new cars, selling cars, viewing car and employee lists, and updating records upon each sale.

## Features
- #### **Car Management**:
  - Add new cars to the dealership.
  - View a list of available cars.
  - Record the sale of a car, updating inventory and recording details in a sales file.
- #### **Employee Management**:
  - Add employees and track their sales performance.
  - View employee details, including sales count and calculated salary.
  - Generate and update employee salary based on the number of cars sold.

- #### **File Handling**:
  - Read data from and write updates to files, including sold cars (`Sold.txt`), dealership cars (`CarDealership.txt`), and employee records (`Employee.txt`).
 
## Class Details
### `Car`
- Attributes: `carNum`, `year`, `name`, `kilometers`, `price`
- Methods:
    - **Constructor**: Initializes a car with attributes such as serial number, year, kilometers driven, and price.
    - **Setters**: Validates values like year (must be between 2017 and 2023) and price (must be positive).
    - `downValue(double percents)`: Calculates price reduction based on percentage.
    - `carSell(Path p)`: Records car details in the specified path upon sale.
    - `toString()`: Returns car details as a formatted string​.
 
### `Employee`
- Attributes: `name`, `ID`, `numOfSales`
- Methods:
    - **Constructor**: Initializes employee with name, ID, and sales count.
    - **Setters**: Validates inputs like ID (must be a 9-digit integer) and sales count (non-negative).
    - `carSell(Car car, Path p)`: Logs the sale of a car and increments sales count.
    - `salary()`: Calculates the employee's salary based on a base amount plus sales commission.
    - `compareTo()`: Compares two employees based on sales countarDealership`
- **Main Class**: Handles system operations, such as loading and saving data, viewing car and employee records, selling cars, and adding new cars.
-  **Methods**:
    - `main()`: Runs a menu-based interface for users to interact with the system.
    - `compareID(int id, ArrayList<Employee> emp)`: Checks if an employee with the given ID exists.
    - `compareCarNum(String carNumber, ArrayList<Car> car)`: Checks if a car with the given serial number exists.
    - `sortArray()`: Sorts lists (e.g., employees by sales) .
