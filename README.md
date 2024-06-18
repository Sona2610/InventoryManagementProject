
## Inventory Management System

This Java-based Inventory Management System is designed to handle inventory records, manage stock maintenance, and generate inventory reports. It uses MySQL as the backend database to store and retrieve inventory details.

### Features
- **Admin Functions**:
  - Login authentication
  - Add new products to the inventory
  - View inventory details
  - Logout
- **Agent Functions**:
  - Login authentication
  - Buy or sell products
  - Logout

### Prerequisites
- Java Development Kit (JDK) 8 or above
- MySQL Database
- MySQL Connector/J (JDBC Driver)

### Setup Instructions

1. **Clone the repository**:
   ```sh
   git clone https://github.com/yourusername/InventoryManagementSystem.git
   cd InventoryManagementSystem
   ```

2. **Database Setup**:
   - Create a MySQL database named `inventorymanagement`.
   - Create a table named `login` to store admin and agent credentials:
     ```sql
     CREATE TABLE login (
       id INT AUTO_INCREMENT PRIMARY KEY,
       username VARCHAR(50) NOT NULL,
       password VARCHAR(50) NOT NULL
     );
     ```
   - Create a table named `product` to store product details:
     ```sql
     CREATE TABLE product (
       productId VARCHAR(50) PRIMARY KEY,
       productName VARCHAR(50) NOT NULL,
       minSellingQuantity VARCHAR(50) NOT NULL,
       price INT NOT NULL,
       quantity INT NOT NULL
     );
     ```

3. **Add Database Credentials**:
   - Open the `Main.java` file located in the `InventoryManagement/src/InventoryMangement` directory.
   - Update the `DriverManager.getConnection` method with your MySQL username and password:
     ```java
     con = DriverManager.getConnection("jdbc:mysql://localhost:3306/inventorymanagement", "root", "yourpassword");
     ```

4. **Compile and Run**:
   - Compile the Java program:
     ```sh
     javac -d bin src/InventoryMangement/Main.java
     ```
   - Run the program:
     ```sh
     java -cp "bin:mysql-connector-java-8.0.25.jar" InventoryMangement.Main
     ```

### Usage

1. **Admin Login**:
   - Select option `1` for Admin.
   - Enter valid admin credentials.
   - Choose from the options to add a product, view products, or logout.

2. **Agent Login**:
   - Select option `2` for Agent.
   - Enter valid agent credentials.
   - Choose from the options to buy/sell products or logout.

3. **Exit**:
   - Select option `3` to exit the application.

### Contributing

1. Fork the repository.
2. Create a new feature branch:
   ```sh
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```sh
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```sh
   git push origin feature-branch
   ```
5. Create a new Pull Request.

### Contact

For any questions or issues, please contact mssonasp@gmail.com.

