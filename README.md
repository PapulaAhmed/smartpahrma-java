# SmartPharma
SmartPharma is a comprehensive web application designed to help users search and find detailed information about various drugs and medicines. Built using Java with Maven and Spring Boot, SmartPharma also enables users to purchase over-the-counter (OTC) medicines directly from the application.

## Key Features
- **Drug Search:** Users can search for drugs and medicines, with search suggestions provided as they type in the search field.
  
- **Detailed Information:** Each drug has a dedicated page displaying its description, usage, side effects, and other relevant details.
  
- **OTC Medicine Purchase:** Users can buy OTC medicines online, with options to select the desired quantity and add items to their cart.
  
- **User Roles:** The application supports multiple user roles, including Admin, and Pharmacist.
  
- **Checkout Process:** A streamlined checkout process allows users to enter their personal information, place orders, and receive a thank you message upon completion.
  
- **Order Management:** Admins can access detailed order information through their panel.


## Technologies Used
- Java
- Maven
- Spring MVC
- JSP
- MySQL

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Java JDK 11 or higher installed
- IntelliJ IDEA (Community or Ultimate Edition)
- MySQL Server (or any compatible SQL database)
- Maven (usually bundled with IntelliJ IDEA)
- Tomcat Server 10.1.25

## Application Configuration

### Clone the Repository
Start by cloning the SmartPharma repository from GitHub to your local machine.

```git clone https://github.com/PapulaAhmed/smartpharma-java.git```

### Extract the Project
If the repository is downloaded as a zip file, extract it to a suitable location on your computer.

### Open the Project in IntelliJ IDEA
- Launch IntelliJ IDEA.
- Select 'Open' and navigate to the directory where you have extracted the project.
- Select the project folder and click 'OK' to open the project in IntelliJ.

### Configure Tomcat Server
- Download Tomcat 10.1.25 if you haven't already done so and extract it to a known location.
- In IntelliJ, go to 'Run' -> 'Edit Configurations'.
- Click the '+' button and select 'Tomcat Server' -> 'Local'.
- Name the configuration (e.g., "SmartPharma").
- In the 'Server' tab, click 'Configure...' and set the Tomcat home (the location where you extracted Tomcat).
- Under the 'Deployment' tab, click the '+' button, choose 'Artifact...', and select 'smartpharma exploded' from the list.
- Apply the changes and close the dialog.

### Configure the Database with XAMPP
- Ensure XAMPP is installed on your machine.
- Start the XAMPP Control Panel and start both 'Apache' and 'MySQL' services.
- Open a browser and go to http://localhost/phpmyadmin to access the PHPMyAdmin interface.
- Create a new database for the project as specified in your dispatcher-servlet.xml.

### Update Database Configuration
- Navigate to WEB-INF in your project directory in IntelliJ and open dispatcher-servlet.xml.
- Update the datasource bean with the correct database credentials, including the URL, username, and password that match your MySQL setup in XAMPP.

  ```
  <bean id="dataSource" class="org.springframework.jdbc.datasource.DriverManagerDataSource">
        <property name="driverClassName" value="com.mysql.cj.jdbc.Driver"/>
        <property name="url" value="jdbc:mysql://localhost:3306/smartpharmadb?useSSL=false"/>
        <property name="username" value="root"/>
        <property name="password" value=""/>
    </bean>
  ```

### Run the Project
- Back in IntelliJ, select the run configuration you created for Tomcat and click the run button (green play button).
- This will build the project, deploy it to Tomcat, and start the server.
- Once the server starts, open a web browser and go to http://localhost:8080 to access the SmartPharma application.


