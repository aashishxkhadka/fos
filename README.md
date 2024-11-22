# Food Ordering System (FOS) for McGee Restaurant  

Are you an **APU student** looking for a comprehensive **Food Ordering System project** using **Java RMI**? This repository is perfect for your academic and personal projects. Developed to streamline the ordering process at McGee Restaurant in Sri Petaling, Malaysia, this **FOS (Food Ordering System)** leverages distributed computing to create an efficient, modern solution for restaurants.  



## Project Overview  

**McGee Restaurant** previously relied on outdated, paper-based order management, leading to issues such as billing errors, data loss, and long wait times. This **Food Ordering System** replaces manual processes with a fully digital ordering solution, specifically designed to cater to:  

* **Dine-in and Take-away customers.**  
* **Order registration and billing accuracy.**  
* **Reduced waiting time during busy hours.**  

This project is ideal for **Asia Pacific University students** working on:  
- Distributed Computing coursework.  
- Java RMI projects.  
- Database management integration with **MySQL**. 


## Key Features  

1. **User Registration:**  
   - Simple and secure sign-up process.  
   - Username validation for unique accounts.  

2. **Secure Ordering Process:**  
   - View categorized menus for drinks and food.  
   - Place orders directly via the GUI.  

3. **Accurate Billing System:**  
   - Automatically calculates totals.  
   - Reduces manual calculation errors.  

4. **Distributed Technology with Java RMI:**  
   - Ensures seamless communication between server and client. 

## Why APU Students Will Love This Project  

- **Learn Core Concepts:** Distributed systems, database integration, and GUI-based interaction.  
- **Practical Application:** Implement real-world technologies like Java RMI and MySQL for professional-grade projects.  
- **Customizable:** Adapt the code to meet additional coursework requirements.  

## Technologies Used  

* **Java RMI**: For distributed computing and client-server interaction.  
* **Java JDBC**: For database connectivity.  
* **MySQL**: As the external database to manage data securely and efficiently.


# Installation Instructions

**Step 1 : Clone the Repository**

 1. Open your terminal or command prompt.
 2. Clone the repository from GitHub:
    
    ```
     git clone https://github.com/aashishxkhadka/fos.git
    ```
 3. Navigate to the project directory:
    
    ```
    cd fos
    ```
**Step 2 : Setting Up Java**

 1. **Install Java Development Kit (JDK) :**
    If you haven't installed JDK, download and install the latest version from Oracle's    
    official site.
 2. **Set Up JAVA_HOME Environment Variable :**
    * Open System Properties > Environment Variables.
    * Under "System variables," add a new variable JAVA_HOME with the path to your JDK    
      installation.
 3. **Verify Installation:**
    Run the following command to confirm Java is installed:
    
    ```
    java -version
    ```
**Step 3: Install MySQL**

Follow these detailed guides for installing MySQL on Windows:
  * MySQL Installation Guide for Windows 11 https://www.tutorialsfield.com/how-to-install-mysql-on-windows-10/

**Step 4: Set Up MySQL Database**

1. Open MySQL:
   * Once MySQL is installed, launch MySQL Workbench or connect via command line.
2. Create a Database:
   * Run the following SQL command to create a new database for the Food Ordering System :
     
     ```
     CREATE DATABASE dcoms_db;
     ```
3.Add Tables and Data
   * set up necessary tables by import the provided SQL script .
     
     ```
     use dcoms_db; create table users(id int(20) unsigned auto_increment primary key not null,      name varchar(255) not null, username varchar(255) not null, email varchar(255) null,     u_password varchar(255) not null, role int(255) null); insert into users (name, username, u_password, role) values ('admin', 'admin', 'admin', 0);
     ```
     
     ```
     create table food(id int(20) unsigned auto_increment primary key not null, fname   varchar(255) not null, price varchar(10) not null, category varchar(50) not null);
     ```

     ```
     create table orders(id int(20) unsigned auto_increment primary key not null, customer_id int(20), timestamp timestamp not null default current_timestamp on update current_timestamp, address varchar(500), status varchar(10) default 'pending');
     ```

     ```
     create table order_items(id int(20) unsigned auto_increment primary key not null,order_id int(20) not null, food_id int(20) not null, quantity int(20) default 1);
     ```
**Step 5: Connect Java to MySQL**
Use the following tutorial for step-by-step guidance on setting up MySQL with Java:

* Connecting MySQL Database in Java using Eclipse
  ```
  https://www.tutorialsfield.com/how-to-connect-mysql-database-in-java-using-eclipse/
  ```

1. Add MySQL Connector JAR:
   * Download the MySQL Connector JAR from the official MySQL Connector page.
     https://mvnrepository.com/artifact/com.mysql/mysql-connector-j/9.1.0
   * Add this JAR to your project’s build path.
2. Update Database Configuration:
   * In your project, locate the database configuration file or settings.
   * Replace placeholder values with your database name, username, and password :
      ```
      String url = "jdbc:mysql://localhost:3306/dcoms_db";
      String user = "yourUsername";
      String password = "yourPassword";
      ```
**Step 6 : Run the Application**
1. Compile and Run the Server:
 * Start the RMI server to listen for client requests.
   ![1](https://github.com/user-attachments/assets/a394bac5-4655-4aa2-ab8e-819fa145878e)

2. Run the Client:
 * Open a new terminal window, navigate to the project directory, and run the client to connect to the server.
   ![2](https://github.com/user-attachments/assets/e2539c7d-d8ec-42f3-9f9d-06a13c23fa0a)
   



![Main ](https://github.com/user-attachments/assets/c27fdc14-0283-49f5-bc9c-62a031d91ae8)
<img width="1107" alt="Screenshot 2024-11-22 at 12 02 10 PM" src="https://github.com/user-attachments/assets/86e8b35e-d89a-4abc-aadf-8eb1ccf19085">
<img width="1138" alt="Screenshot 2024-11-22 at 12 02 38 PM" src="https://github.com/user-attachments/assets/294bd696-2064-49a1-9dd6-9bd12a3eeedd">
<img width="1140" alt="Screenshot 2024-11-22 at 12 02 54 PM" src="https://github.com/user-attachments/assets/a3cad3bd-571b-471c-a543-9c616c6656ab">
<img width="992" alt="Screenshot 2024-11-22 at 12 03 04 PM" src="https://github.com/user-attachments/assets/308b8e4c-ad44-4230-b340-fa9ef0d354f4">
<img width="442" alt="Screenshot 2024-11-22 at 12 03 16 PM" src="https://github.com/user-attachments/assets/f5e2a29d-e03d-4426-9c5f-efa72f16252c">


