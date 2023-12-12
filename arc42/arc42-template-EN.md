
# RideShare: EcoRide

# Introduction and Goals

<!-- (Describes the relevant requirements and the driving forces that software architects and development team must consider. These include)-->

EcoRide aims to provide its customers with a convenient, safe, and environmentally friendly mode of transportation for seamless, efficient, and eco-conscious travel from point A to point B.

The subsequent paragraphs delve into our architecture and elaborate on the various aspects and solutions contributing to these goals

### Essential features of the System
    - Easy and intuitive booking of a ride from A to B via the web, app, or mobile
    - Real-time driver tracking
    - Registration and  verification of drivers and passengers
    - Create and edit profiles
    - User feedback, support and rating system
    - Integrated payment system
    - Reporting and analytics features


### Business Goals
- Our Business Goals include
    - Ensuring seamless and accessible ride bookings, to offer a consistently dependable user experience
    - Emphasis on sustainability and adopting eco-friendly practices to reduce emissions, promote electric shared mobility solutions, and actively contribute to a greener and more sustainable future
    - Strong focus on data security
    - Advanced Safety measures to safeguard the well-being of our riders and drivers, ensuring their trust in our platform 

### Essential functional requirements
- These outlined functional requirements serve as a foundation for the development of our EcoRide app. They aim to provide a fast and secure mode of transportation while ensuring a user-friendly and efficient experience for our users.

    - User Registration and Profile Management
        - Allow users to register for the service, providing necessary personal information
        - Enable users to create and edit their profiles, including name, contact details, and profile picture
    - Ride Booking
        - A System that enables users to book rides from point A to point B
        - The booking process has to be accessible through the web, mobile and app
    - User Verification
        - Verification system for both drivers and passengers to enhance platform safety and trust
        - Verification may include identity checks, driver's license verification, and other relevant measures
    - Real-time Driver Tracking
        - Provide real-time driver tracking features, allowing passengers to track the driver's location and receive estimated arrival times (ETA)
    - Profile Creation and Editing
        - Allow users to create and edit their profiles, including personal details and profile pictures, to personalize their accounts
    - Feedback, Support, and Rating System
        - A System that enables users to provide feedback, seek support, and ask questions
        - Includes a user-friendly rating system for passengers to rate drivers and vice versa
    - Integrated Payment System
        - A secure payment system for handling transactions between drivers and passengers
        - Support various payment methods to ensure convenience for users
    - Reporting and Analytics Features
        - Reporting and analytics functions to monitor the platform's performance and user activities
        - Gather data related to rides, earnings, user engagement, and other relevant information

[comment]: <> (Quality Goals for the architecture)
### Quality Goals

In EcoRide, we are committed to achieving three core quality goals:

    - Reliability
    - User-friendliness
    - Data Security

These pillars serve as the cornerstones of our mission to provide an exceptional and secure user experience

### Stakeholders
Our Stakeholders and their expectations are:
- Investors
     - As an investor, I want to support an innovative ride-sharing app that revolutionizes the existing model and provides users with a convenient, efficient, and sustainable way to get around
- Drivers
    - As a driver, I want to be able to use an efficient and user-friendly ride-sharing app to offer my services and generate additional income 
- Customers
    - As a customer, I want to be able to use a user-friendly ride-sharing app to travel conveniently, safely, quickly, and environmentally friendly from A to B
- Government & Authorities
    - As a government authority, I want to promote an environmentally friendly ride-sharing app to support sustainable mobility and reduce CO2 emissions in my region
 - Payment Providers
    - As a payment provider, I want the ride-sharing app to seamlessly integrate payment processing to provide its users with a smooth transaction experience

<div style="page-break-after: always;"></div>

## Requirements Overview
This overview outlines the essential criteria for innovative, efficient, and environmentally responsible solutions.

| Requirements                |  Explanation |
|-----------------------------|---|
| Search for Rides            |  Allows passengers to search for available rides based on location, destination, and desired travel time |
| Book a Ride                 | Allows passengers to select and book a ride from the list of available rides  |
| Accept/Decline Ride Request | Allows drivers to view and accept or decline ride requests from passengers |
| Track Ride                  | Allows passengers and drivers to track the progress of the ride and monitor estimated arrival time |
| Complete Ride               | Allows passengers and drivers to confirm that the ride has been completed and process payment through the app |
| View Ride History           | Allows users to view their ride history, including details such as ride date, time, location, and payment information  |

## Quality Goals
Our goals set the standard for excellence in sustainable transportation, focusing on unparalleled innovation, reliability, and environmental integrity.

| Priority   | Contact        | Expectations       |
|-------------|----------------|--------------------|
| *1* | *Reliability* | *Reliability is crucial for our car-sharing company, as it enhances customer trust in punctual and well-maintained vehicles, thus promoting a positive user experience and long-term customer loyalty.* |
| *2* | *User-friendliness* | *User-friendliness is a central quality goal for our car-sharing company, as it ensures that customers can effortlessly and intuitively use our services, leading to a positive user experience and increasing the attractiveness of our service* |
| *3* | *Data security* | *Data security is a primary quality objective for our car-sharing company, as it protects the confidentiality and integrity of sensitive user information, strengthens the trust of our customers, and simultaneously minimizes legal and financial risks.* |

## Stakeholders
This section is dedicated to understanding and aligning with their interests and expectations, fostering a collaborative and sustainable future.

| Role/Name   | Contact        | Expectations       |
|-------------|----------------|--------------------|
| *Investors* | *Maryam Patel* | *As an investor, I want to support an innovative ride-sharing app that revolutionizes the existing model and provides users with a convenient, efficient, and sustainable way to get around* |
| *Drivers* | *Amirah Rahman* | *As a driver, I want to be able to use an efficient and user-friendly ride-sharing app to offer my services and generate additional income* |
| *Customers* | *Megan Chen* | *As a customer, I want to be able to use a user-friendly ride-sharing app to travel conveniently, safely, quickly, and environmentally friendly from A to B* |
| *Government & Authorities* | *Raj Gupta, Javier Gomez* | *As a government authority, I want to promote an environmentally friendly ride-sharing app to support sustainable mobility and reduce CO2 emissions in my region*
| *Payment Providers* | *PayPal, Klarna* | *As a payment provider, I want the ride-sharing app to seamlessly integrate payment processing to provide its users with a smooth transaction experience* |


<div style="page-break-after: always;"></div>

# Architecture Constraints

These constraints encompass various elements, from infrastructure choices to database selection and real-time data processing, all of which impact the way our software meets the needs of our users and stakeholders.

<!-- See [Architecture Constraints](https://docs.arc42.org/section-2/) in the arc42 documentation.-->

| Context | Decision | Consequences |
|---|---|---|
|The imperative for operational flexibility, cost-effectiveness, and heightened security guides the decision to adopt an infrastructure that aligns with the specific needs of our system | We will use a Cloud Based Infrastructure to max out efficiency, reduce costs, increase agility, improve accessibility and enhance security | On demand scalability and flexibility, no upfront capital costs for buying hardware, improved Data Security. Service availability in cloud infrastructure varies by provider and design, requiring a commitment to ensure consistent uptime. Furthermore Third-party dependencies, data transfer costs and security concerns, limited control over physical hardware |
| The need for flexibility in handling dynamic data, coupled with challenges related to potential data inconsistency and the nuanced trade-offs of the CAP theorem, as well as the demands for high data volume and scalability, influence the decision to employ a database solution suited to our specific data characteristics | We will use a NoSQL Database to address scalability, flexibility, performance and cost efficiency concerns | Flexibility to handle unstructured or semi-structured data, achieve horizontal scalability, and attain high read and write throughput contributes to improved application performance and responsiveness. However, this flexibility may lead to data inconsistency. The use of NoSQL may require careful planning to scale effectively, and trade-offs outlined by the CAP theorem can impact performance and/or strong consistency |
| Concerns, in managing a dynamic system, arise from the balance required between swift decision-making, consistency, and reliability, all of which are crucial for ensuring user satisfaction and safety | We will use Real Time Data Processing, to enable immediate analysis and response to incoming data | Immediate updates and responses to users, enables real time decision making, competitive advantage. Implementing real-time data processing features adds complexity, requires additional computational resources |


## Architecture Decisions
These Architecture Decisions reflect our commitment to sustainable innovation, detailing the strategic choices that shape our transportation solutions. The following three are the ones with the highest priority:
<div class="formalpara-title">


</div>

| Problem   | Considered Alternatives | Decision       |
|-------------|----------------|--------------------|
| *Which type of database?* | *SQL, Maria DB, Oracle* | *NoSQL: Cost-Effective, Scalability, High Availability, Compatibility with most Cloud Solution Services, Migration* |
| *What type of Infrastructure?* | *Cloud Based, On Premise Infrastructure, Edge Computing* | *Cloud Based: On demand scalability and flexibility, Cost-Effective, no upfront capital costs, pay-as-you-go model, Data Security, Availability* |
| *Which Data Process model?* | *Batch Processing, Stream Processing Model, Lambda Architecture* | *Real Time Data Processing: immediate updates and responses to users, enables real time decision making, competitive advantage.* |




## Risks and Technical Debt
EcoRide is committed to identifying and addressing potential risks and technical debts in our operations, with a focus on implementing robust strategies to overcome challenges. In the following, we detail specific areas of concern, such as NoSQL database management, cloud-based infrastructure, and reliance on third-party services, along with our targeted strategies for each. 
<div class="formalpara-title">

</div>

| Risk/Technical Debt   | Description |
|-------------|----------------|
| *NoSQL Database & Real Time Data Processing* | *NoSQL databases, introduces challenges related to data consistency, complex queries, and developer learning curves.*  | 
| *Using Cloud Based Infrastructure* | *The shift to cloud-based infrastructure introduces risks such as service outages, cost unpredictability, and vendor dependencies. | *Cloud Based: On demand scalability and flexibility, Cost-Effective, no upfront capital costs, pay-as-you-go model, Data Security, Availability* |
| *Dependency on Third-Party Services* | *Excessive dependence on external services, such as payment gateways and mapping APIs, may result in service interruptions and higher expenses.* | 

<div style="page-break-after: always;"></div>

# System Scope and Context

<div class="formalpara-title">

This overview encapsulates EcoRide's engagement with its operational and technical spheres, detailing user interactions and system infrastructure.

## Business Context

The following diagram provides a comprehensive view of the system's communication partners, their specific interactions, and the data exchanged with the system's environment:

<p align="center">
<img src="images/Business_Context_Diagram.png" alt="Business Context Diagram">
</p>

**User Interaction**: At the top left, the 'User' represents the customers who will be using the Ride Sharing service. They interact directly with 'Drivers' who provide the transportation service. Users also interact with the system for payments through a 'Payment Gateway' and for navigation or locating rides through a 'Map Service.'

**Eco Ride Central System**: In the center of the diagram, 'Eco Ride' represents the central system that orchestrates the service. It connects all components of the service, facilitating communication between them.

**Driver Services**: 'Eco Ride' provides services to 'Drivers,' including ride assignments, navigation assistance, and other support needed to complete the rides.

**Payment Processing**: The 'Payment Gateway' handles the financial transactions, such as processing user payments and disbursing earnings to drivers.

**Mapping Services**: 'Eco Ride' provides mapping capabilities, including route optimization and real-time traffic updates, which are essential for a transportation service through Google Maps.

**Backend Operations**: At the bottom of the diagram, we see the backend components that 'Eco Ride' uses to manage its operations:

**Admin Panel**: This is where the management and monitoring of the service happen. It provides control over the various aspects of the service, from ride prices to driver management.

**Database**: 'Eco Ride' stores its data in a 'Database,' which includes user profiles, ride history, payment transactions, and more. This is critical for maintaining records, analytics, and personalizing the user experience.

## Technical Context

Understanding EcoRide's technological landscape involves delving into the fundamental elements that shape our RideSharing platform. This includes the intricate interplay of technologies, infrastructure, and environments that collectively define the technical context of the App, shown in the following diagram:

<img src="images/TechnicalContext.png">

<div class="formalpara-title">

<div style="page-break-after: always;"></div>

### Development Environment: 

#### This is where the application is initially developed. It includes:

**Application Servers**: Where the actual development of the EcoRide application takes place. <p>
**Development Repository**: A version control system where the application code is stored and managed. <p>
**Issue Tracking and Document System**: Tools to track bugs and manage project documentation. <p>
**Containerization and Orchestration**: Technologies used to package the application in containers, making it easy to deploy across different environments. <p>
**Developer Tools**: Software and applications that developers use to write, test, and debug code. <p>
**Frameworks**: These are used to provide structured testing of the application's functionalities. <p>
**Test Environment**: After the application is developed, it moves to the test environment for quality assurance. <p>

**Test Management System**: Here, the application undergoes various tests to ensure it meets quality standards. <p>


### Production Environment: 

#### This is where the live application is hosted.

**Database Servers**: These servers manage the databases that store the EcoRide application data. <p>
**Load Balancers**: These help to distribute the incoming network traffic across multiple servers to ensure no single server becomes overwhelmed, which increases reliability and performance. <p>
**Application Servers**: The servers that host the live EcoRide application, serving users' requests.<p>
**Backup System**: It ensures data integrity and availability, safeguarding against data loss. <p>
**EcoRide Application**: The actual application that users interact with. <p>
**External Services**: These include third-party services that the application relies on, such as payment processors or map services. <p>
**Security Services**: Systems in place to protect the application from security threats and ensure user data is safely handled.

<div style="page-break-after: always;"></div>

# Solution Strategy

Our Solution Strategy combines a Service-Oriented Architecture (SOA) with cloud-based infrastructure, ensuring scalability, reliability, and rapid development cycles

### Technology Decisions:

We are utilizing a Service-Oriented Architecture (SOA) with loosely coupled services, which enables efficient scaling of specific features in response to increased user traffic

A cloud-based infrastructure ensures system reliability, availability, and accelerated development and deployment cycles through fault isolation and redundancy

### Top-Level Decomposition:

The chosen microservices architectural pattern effectively decomposes the system into manageable, loosely coupled services, allowing for specialized functionalities and easy scaling.

### Achieving Key Quality Goals:

Scalability is achieved through SOA, enabling seamless resource allocation to handle escalating user traffic while minimizing performance impact.

The combination of SOA and a cloud-based infrastructure provides flexibility, reliability, and availability, supporting rapid development and deployment cycles, aligning with the goal of continuous integration and delivery.

<div class="formalpara-title">

</div>

<!--See [Solution Strategy](https://docs.arc42.org/section-4/) in the arc42
documentation.-->

<div style="page-break-after: always;"></div>

# Building Block View

The Building Block View offers a structured snapshot of our system's architecture, breaking down key components and their interconnections to provide a comprehensive understanding of how EcoRide's functionalities are organized and interact

## Whitebox Overall System

This level serves as an overview of the entire system. It showcases the core components, such as FileSystemStorage, Cars, Rides, Profile and more. This level explains the interactions between these components, revealing how users access the system, how data flows between different servers or services, and how external systems communicate with the system.

![Level 1 of the Building Blocks Hierachy](images/level1-Page-1.jpg)

### Contained Building Blocks

**EcoRide API**: This is the central interface for the application, the set of application programming interfaces (APIs) through which the application's services are accessed and interacted with.

**Cars**: Represents the component that manages information related to vehicles in the service, such as registration details, availability, and other car-specific data.

**Rides**: This component manages the ride details, such as scheduling, ride status, and ride history.

**Profile**: Handles user profile information, which include personal details, preferences, and usage history.

**User**: Represents the end-user component that interacts with the application, including user authentication and session management.

**PaymentProcessor**: The system that handles payment transactions, connected to an external payment API for processing payments.

**FileSystemStorage**: The storage system where data such as ride details, car information, and user profiles are stored.

**Statistics**: This component is responsible for collecting and analyzing data for reporting and analytics purposes.

**Locations**: Manages geographic data, related to rides, user locations, and available cars.

**Mapping**: Interacts with an external mapping API to provide mapping and navigation services within the application.

**User-Interface**: The front-end component that users interact with in this context that would be the mobile app.

**Booking**: Handles the booking process for rides, including ride requests and assignment of cars to users.

**Communications**: Manages in-app communication, such as notifications, alerts, and in-app messaging between users and drivers.

The dashed lines with labels such as "cars api," "rides api," "charts," "locations api," "real-time location updates," "mapping api," "booking api," and "communications api" are external APIs, third-party services or other services that the respective components within the EcoRide ecosystem interact with. <p> 

For example, "cars api" and "rides api" are interfaces for external services that provide additional information or capabilities related to cars and rides, such as a third-party vehicle tracking service. <p>
**"Charts"** is a tool for visualizing the statistical data. The "locations api" and "mapping api" indicate the use of external mapping and location services, essential for a ride-sharing service's operations.

<div style="page-break-after: always;"></div>

## Level 2

The Level 2 view delves into the "Cars" component, which comprises the following components: ChartsService, CarsController, CarsRepository, and CarsInsuranceRepository. Notably, the ChartsService component is linked to the charts API and the CarsController component is linked to the cars API.

![Level 2 of the Building Blocks Hierachy](images/level2-Page-2.jpg)

**ChartsService**: This service is responsible for generating charts. It handles visual data representations related to cars, such as usage statistics, maintenance schedules, or availability. It interacts with a 'charts api', which is a specialized service for creating various types of charts.

**CarsController**: Acts as the intermediary between the 'CarsRepository', 'ChartsService'. It receives requests, processes them ( using data from 'CarsRepository' and 'ChartsService'), and sends back the appropriate responses.

**CarsRepository**: This repository is where data related to the cars is stored and retrieved from. It functions as the data access layer, interacting directly with the database where car information is stored.

**CarsInsuranceRepo**: A specialized repository that handles car insurance-related data. This component is responsible for storing, updating, and retrieving insurance information for each vehicle.

The 'cars api' connects to the 'CarsController', and is the entry point for external requests related to car data within the application.

<div style="page-break-after: always;"></div>

## Level 3

This level dives even deeper into the system. It gets more detailed about the CarsController mentioned in Level 2. This level shows exactly how the CarsController is set up and its communication with external APIs.

![Level 3 of the Building Blocks Hierachy](images/level3-Page-3.jpg)

**getAllCars()**: Returns a list of all cars in the system. The List < Car > shows that it returns a collection of Car objects.

**getCarById(carId)**: Retrieves a single car's details based on a unique identifier provided as carId.

**addCar(newCar Car)**: Adds a new car to the system. The parameter newCar is of type Car, meaning it expects an object that represents a car.

**updateCar(carID, car)**: Updates the details of an existing car. It requires the car's identifier and the new Car object that contains updated information.

**deleteCar(carID)**: Removes a car from the system using the car's identifier.

**getStats(carID)**: Fetches statistics related to a specific car, meaning performance or usage statistics.

**getInsurance(carID)**: Retrieves insurance information for a particular car.

At the bottom of the CarsController class, there is a reference to another component:

**carsService CarsService**: This indicates that the CarsController relies on a service named CarsService, which contains the business logic needed to carry out the operations listed above.

On the right side of the diagram, there are two dashed lines labeled "RideManagementComponent", "Database", and "Charts", describing that CarsController interacts with these components or services:

**RideManagementComponent**: This acts as part of the application responsible for managing ride details. The CarsController is interfacing with it to get or set information related to rides for specific cars.

**Database**: This represents the persistence layer, where CarsController will store and retrieve data.

**Charts**: This shows that the controller uses a charting service or component to visualize data, possibly for reporting or analytics purposes.



<div style="page-break-after: always;"></div>

# Runtime View

The Runtime View provides a dynamic perspective on our system's operation, detailing the seamless interactions during the ride-booking process and real-time driver tracking. These visualizations showcase the responsive and communicative nature of EcoRide:

## Runtime Scenario: Ride Booking

![Alt text](images/UML-image-1.png)

The Runtime View of the ride-booking process visually outlines interactions among three entities: the User's Device with the App, the Server, and the Driver's Device. Users initiate the process by entering their destination (Step 1), leading to the server displaying ride options (Step 2). After confirming ride details (Step 3), the server sends a request to a driver (Step 4), followed by driver acceptance (Step 5). The server communicates confirmation and estimated arrival time to the user (Step 6). Successful ride booking (Step 7) and accurate arrival time (Step 8) conclude the process, emphasizing system responsiveness and seamless communication

## Runtime Scenario: Real-Time Driver Tracking

![Alt text](images/UML-image-2.png)

The Runtime View of the Real-Time Driver Tracking captures the interaction dynamics involving a Passenger, the Ride-Sharing App, a Driver, and the GPS Service. It initiates with the Passenger activating real-time tracking in the app, triggering a sequence where the app requests real-time tracking from the Driver. Subsequently, the Driver seeks location data from the GPS Service, which is then relayed back to the Passenger through the app. Continuously updating the Estimated Time of Arrival (ETA), the EcoRide App ensures the Passenger remains informed about the Driver's location until the completion of the journey. The iterative process, marked by the condition 'until Driver Reaches Destination Location,' underscores the repetitive nature of these actions throughout the ride

<div style="page-break-after: always;"></div>

# Deployment View

The following diagrams are dedicated to illustrating and explaining how our system is structured and deployed across different environments. The focus here is to provide a comprehensive overview of the physical distribution of our software components, their interaction with hardware, and the network infrastructure that supports them.

## Infrastructure Level 1

Having a well-structured technical infrastructure is important to ensuring efficient workflow and product stability. The infrastructure is divided into different environments, each serving a unique purpose, and is designed to work cohesively to support the lifecycle of a software application from development to deployment.

<img src="images/DeploymentView-Level1.drawio.png" alt="Deployment View Diagram">


At the top of the diagram, we have the Development Environment, which is the playground where new software is created and refined. It includes Application Servers for running the software, a Development Repository where code is stored and versioned, and Continuous Integration Servers that help in integrating code changes smoothly. There is also an Issue Tracking and Document System, which is essential for keeping track of bugs and documentation.

Parallel to this is the Test Environment, equipped with Test Servers and a Test Management System, where the software undergoes rigorous testing to ensure quality and performance. This environment mimics the production setting to catch any potential issues before the software goes live.

These environments are supported by Developer Tools and Frameworks, which provide the necessary utilities and libraries for developers to write and test their code efficiently.

Once the software has passed the testing phase, it moves to the Production Environment. This is where the software is available for end-users. It consists of Database Servers to store user data, which are backed up regularly for data safety. Load Balancers are used to distribute incoming traffic to ensure the application remains stable and responsive under different load conditions.

The central element here is the EcoRide Application, which is available as an iOS App and an Android App. This setup shows the application's flexibility across different mobile platforms. External Services are integrated to provide additional functionality to the application.

The Application Servers in the production environment also contain a Web Server to handle web traffic and a Cache Server to improve performance by temporarily storing frequently accessed data. Security Services including Encryption Services and a Firewall safeguard the system from unauthorized access and potential security threats.

## Infrastructure Level 2

Here we can see the Infrastructure Level from a deeper viewpoint. We see each layer depicted more thorougly and with more detail. Below is a quick explanation what purpose all these blocks serve.

<img src="images/DeploymentView.png" alt="Deployment View Diagram">

### <u>Development Environment: </u>

#### Application Servers: Host the development version of the application. <p>
Continuous Integration Server: Automatically tests code changes to ensure they don't break the application <p>
Development Database Server: The database used during development, containing test data. <p> <p>

#### Containerization and Orchestration: 

Both Tools Docker and Kubernetes help in creating consistent development environments and managing them at scale.<p>


#### Development Repository: 

Where the code is stored, managed with a version control system called GitHub. <p>

#### Issue Tracking and Document System: 

Tools for managing project tasks and documentation, in this case Jira for task management, and Confluence for documentation.

#### Test Environment:
##### Test Servers: Where the application is deployed for testing.
##### Test Management System: Includes tools for continuous integration/deployment (CI/CD), API testing, and automated testing, in this case Jenkins, Postman, and JUnit.

#### Developer Tools:

IDE (Integrated Development Environment): The software application used for writing code, in this case Visual Studio Code (VSC). <p>
Git (Version Control System): Used for tracking changes in the source code during development.


#### Frameworks:
Frontend: React and Angular for user interfaces.
Backend: Spring Boot for server-side logic, APIs, and routing.
Mobile: Retrofit for Android network requests and Alamofire for iOS.
### <u>Production Environment: </u>
#### Database Servers: 
Production databases, in this case MySQL. <p>

#### Load Balancers: 
Distributes traffic across servers and resources, using the tool Google Cloud Balancing. <p>

#### EcoRide Application: 

The actual application available to end-users, with versions for iOS (Swift) and Android (Kotlin). <p>

#### Backup System: 
Ensures data integrity and availability,  using a cloud solution called Google Cloud.

#### External Services:
Third-party services used by the application, such as real-time location tracking and Google Maps.

#### Application Servers:
Web Server: Apache Tomcat for serving web content. <p>
Cache Server: Caches frequently accessed data, in this case Apache mod_cache is used to improve performance. <p>

#### Security Services:
Encryption Services: Protects data through end-to-end encryption. <p>
Firewall: Protects the web application from unauthorized access or cyber-attacks.


<div style="page-break-after: always;"></div>

# Cross-cutting Concepts

<div class="formalpara-title">

These cross-cutting concepts play a pivotal role in establishing and maintaining conceptual integrity, contributing to the consistency and homogeneity of our architecture and underpinning the inner qualities of our system

### *User Experience (UX)*

User Experience focuses on creating a positive and seamless interaction between users and a digital product or service.

It encompasses various aspects, including the consistency of design and functionality, the representation of branding elements and logos, app navigation that ensures easy and intuitive user journeys, user authentication processes, push notifications for timely updates, geolocation and maps for location-based services, the flow for booking rides, payment processing, offline functionality to maintain usability without an internet connection, and a 5-star rating system with optional comments to gather user feedback. 

Additionally, it includes the recognition of driver achievements through medals, enhancing the overall user experience.

### Architecture and Design Patterns

The architecture and design of a digital application involve key decisions regarding the underlying technology and structure. 

This includes the use of a NoSQL database for flexible data storage, a Google Cloud-based infrastructure to ensure scalability and reliability, integration with Google Maps for location-related features. 

In addition payment gateways like PayPal and Klarna for secure and convenient transactions, the implementation of reusable components such as buttons, cards, and navigation bars for a consistent look and feel, and adherence to design guidelines like Material Design for Android and Human Interface Guidelines for iOS to provide a user-friendly and familiar interface.

### Safety and Security Concepts

Ensuring the safety and security of users' data and the application itself is paramount. 

This involves implementing data encryption techniques to protect sensitive information, establishing a robust data backup and recovery system to prevent data loss, complying with data privacy regulations such as the General Data Protection Regulation (DSVGO), creating an incident response plan to address security breaches and other emergencies effectively, and employing secure user authentication methods to prevent unauthorized access and maintain user privacy.

<div style="page-break-after: always;"></div>

# Architecture Decisions

This table offers an in-depth examination of key architecture decisions, shedding light on both high-priority choices previously mentioned and two additional significant decisions, Payment System Integration and User Authentication and Authorization, contributing to the overall development trajectory of our innovative ride-sharing platform.

<div class="formalpara-title">

| Title | Context | Decision | Status | Consequences |
|---|---|---|---|---|
| **Database Selection** | Evaluating SQL, Maria DB, Oracle, and NoSQL options for the system's database | NoSQL | Proposed | **Positives**: <br> Cost-effective solution - Scalability to handle increasing data volume - High availability for robust performance - Compatibility with diverse cloud services - Smooth migration process <br> **Negatives**: <br> Learning curve for NoSQL may impact initial development speed, Potential data consistency challenges due to flexibility, Requires careful planning for effective scaling |
| **Infrastructure Model** | Choosing between Cloud-Based, On-Premise Infrastructure, and Edge Computing | Cloud-Based | Proposed | **Positive**: On-demand scalability and flexibility, Cost-effectiveness with no upfront capital costs, Pay-as-you-go model for financial management, Enhanced data security measures, High availability <br> **Negative**: Dependency on third-party cloud services, Potential service outages affecting system availability, Data transfer costs and security concerns, Limited physical control over infrastructure |
| **Data Processing Model** | Selecting the appropriate data processing model among Batch Processing, Stream Processing, and Lambda Architecture | Real-Time Data Processing | Proposed | **Positive**: Immediate updates and responses for enhanced user experience, Real-time decision-making capabilities, Competitive advantage in responsiveness and decision speed <br> **Negative**: Increased system complexity, Additional computational resources required for real-time processing, Potential challenges in implementing and maintaining real-time features |
| **Payment System Integration** | Determining the approach for integrating a payment system within the EcoRide app, choosing between an in-house payment system development or third-party payment gateway integration | Third-party payment gateway integration | Proposed | **Positive**: Seamless and secure transaction processing, Enhanced user trust through established payment gateways <br> **Negative**: Dependency on external payment service providers, Transaction fees may impact overall operating costs |
| **User Authentication and Authorization** | Selecting the strategy for user authentication and authorization within the EcoRide system, among traditional username/password authentication, social media login integration and/or multi-factor authentication | Multi-factor authentication with social media login integration | Proposed | **Positive**: Improved security with multi-factor authentication, Enhanced user convenience through social media login options <br> **Negative**: Potential user resistance to additional authentication steps, Dependency on external social media platforms for login |


<div style="page-break-after: always;"></div>

# Quality Requirements

<div class="formalpara-title">

This section elaborates on the established quality goals of **Reliability**, 
**User-Friendliness**, and **Data Security**. <br>
The Quality Tree provides a detailed quality tree along with associated scenarios, encompassing both high-priority requirements essential for core objectives and additional quality measures with lower priority.

Each requirement is carefully tailored to address the specific and quantifiable expectations of stakeholders, providing a robust foundation for informed development and rigorous evaluation of our ride-sharing solution.

| Quality Requirements |  |  |
|---|---|---|
| Reliability |  |  |
| User-Friendliness |  |  |
| Data Security |  |  |


## Quality Tree

Our Quality Tree consists of the values reliability, user-friendliness, and data security. The leaves are: Real-time Transaction Latency, Accurate ETA and Tracking, Intuitive App Interface, Efficient Customer Support, Secure Payment Processor, and Privacy Protection. 

![QualityTree](images/QualityTree.png)


## Quality Scenarios
EcoRide rigorously tests against a range of realistic, challenging situations to ensure our transportation solutions consistently meet the highest standards of efficiency, sustainability, and user satisfaction.

**Reliability**

Real-time Transaction Latency: <br>
A user initiates a ride booking transaction. Under normal operations the system maintains an average latency of two seconds or better for processing all ride booking transactions, consistently falling within the acceptable range of 1.5 to 2.5 seconds

Accurate ETA and Tracking: <br>
A user wants an accurate and reliable estimated time of arrival (ETA) and real-time tracking of drivers at runtime. 
The system consistently provides this information and checks the provided information with ride completion times, passenger feedback and tracking data, to confirm that the displayed ETAs align with actual arrival times

**User-friendliness**

Intuitive App Interface: <br>
A user wants to switch seamlessly between devices, sign in or register quickly and wants to request rides without manually entering their location.
The system provides a uniform, intuitive interface with a hamburger icon for additional settings. It requires only email and password for login and registration and auto-tracks the user's location for ride requests in a few seconds.

Efficient Customer Support: <br>
A user encounters an application error during the live-phase and seeks assistance. 
The system provides swift and efficient customer support which takes a maximum of 10 minutes, additionally the system includes a FAQ and live chat support, and automatically opens a new ticket for each issue.

**Data Security**

Privacy Compliance: <br>
The developer wants to adapt the system after data protection regulations have been breached or new laws have been passed. The system is updated to solve security measurements and undergoes weekly reviews to implement preventive measures. 


Secure Payment Processing: <br>
A user who conducts a payment transaction wants secure handling of the payment data. 
The system confirms secure processing of user payment data through robust encryption, weekly security audits and penetration testing 


<div style="page-break-after: always;"></div>

# Risks and Technical Debts

This section delves deeper into the potential risks and technical debts, addressing the challenges and uncertainties that may impact the seamless development and operation in more detail.

| Risk/Technical Debt Category | Risk/Technical Debt Description | Suggested Measures |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NoSQL Database & Real Time Data Processing           | NoSQL databases introduce challenges related to data consistency, complex queries, and developer learning curves.                                                    | - Use ACID Transactions to maintain data consistency.<br>- Implement a microservices-based architectural approach for horizontal scalability and to handle growing data volumes and demand spikes efficiently.                               |
| Using Cloud Based Infrastructure                     | The shift to cloud-based infrastructure introduces risks such as service outages, cost unpredictability, and vendor dependencies.                                   | - Conduct Traffic Testing to ensure the system can handle variable traffic loads.<br>- Engage in Workload Planning to optimize costs by accurately provisioning resources.<br>- Develop an Incident Response Plan for swift action during service outages or security incidents.<br>- Perform Security Audits to regularly assess IaaS security. |
| Dependency on Third-Party Services                   | Excessive dependence on external services, such as payment gateways and mapping APIs, may result in service interruptions and higher expenses.                     | - Optimize Service Usage and Contracts by actively monitoring service usage to identify cost-saving opportunities and negotiate cost-effective contracts.<br>- Prepare for Service Outages with contingency plans to ensure business continuity, including strategies for graceful degradation and backup solutions.                     |
|    Payment System Integration                | Dependence on third-party payment service providers may introduce risks such as lack of control over the payment processing, potential for service downtime, and transaction fees affecting profitability.                     | - Establish Service Level Agreements (SLAs) with the payment gateway provider to ensure uptime and reliability standards.<br>- Integrate multiple payment gateways to reduce the risk of service interruptions.<br>- Regularly review and renegotiate transaction fees to manage operating costs.<br>- Ensure compliance with Payment Card Industry Data Security Standard (PCI DSS) and regularly update security measures to protect sensitive customer data.                     |
|    User Authentication and Authorization                | Integrating multi-factor authentication alongside social media logins could complicate the sign-in process, possibly deter users with extra security layers, and create dependence on social media services, which may change their API policies or face downtime.         |  - Inform users about multi-factor authentication advantages to lessen resistance.<br>- Make the multi-factor authentication process smooth and intuitive<br> - Continuously refine and test authentication methods for social media policy changes.<br> - Implement alternative authentication options for social media outages.<br> - Track social media platforms' performance and proactively report issues.

<div style="page-break-after: always;"></div>

# Glossary

<div class="formalpara-title">
</div>


| Term        | Definition        |
|-------------|-------------------|
| MySQL | is a popular open-source relational database management system (RDBMS), known for its reliability, performance, and ease of use in web-based applications.
| API |An Application Programming Interface is a program component provided by a software system to allow other programs to connect and interface with the system.
| REST | or Representational State Transfer, is an architectural style for designing networked applications, relying on stateless, client-server communication, primarily used for building web services. |
|         Github Repository    |is a centralized online location for storing, managing, version-controlling, and collaborating on code or project files, integrated with Git and offering features like issue tracking and pull requests.|
|       Jira      |is a project management tool designed for agile teams, featuring issue tracking, task management, sprint planning, and workflow customization.|
|      Confluence       |is a collaboration platform for team documentation, knowledge sharing, project collaboration, and integration with Jira for enhanced team coordination.|
|     IDE        |or Integrated Development Environment, is a software suite that combines code editing, compiling, debugging, and development tools into a single user interface.|
|       Docker      |is a platform for developing, shipping, and running applications in isolated containers, enabling software to work uniformly across different environments.|
|      Kubernetes       |is a container orchestration system for automating application deployment, scaling, and management, supporting cluster management and load balancing.|
|     Jenkins        |is an open-source automation server used for continuous integration and continuous delivery (CI/CD), supporting various build, test, and deployment tasks.|
|       Postman      |is a popular API (Application Programming Interface) development tool used for building, testing, and documenting APIs, with support for various HTTP methods and API protocols.|
|      JUnit       |is a framework for Java programming, designed for the purpose of writing and running repeatable automated tests to ensure code quality.|
|     React        |is a JavaScript library for building dynamic user interfaces, emphasizing declarative components, virtual DOM, and efficient data handling for web and mobile apps.|
|       Angular      |is a TypeScript-based framework for creating scalable web applications, featuring robust tools for two-way data binding, MVC architecture, and rich interactive components.|
|      Spring Boot       |is a Java-based framework that simplifies the development of stand-alone, production-grade applications with minimal configuration, emphasizing convention over configuration, embedded server support, and a wide range of extensions.|
|     Retrofit        |is a type-safe HTTP client for Android and Java, designed for consuming RESTful web services with ease, supporting JSON/XML converters, custom requests, and synchronous/asynchronous calls.|
|     Alamofire        |is a Swift-based HTTP networking library for iOS and macOS, providing an easy-to-use interface for making network requests, handling JSON data, file uploads, and network response validation.|
|     Swift        |is a powerful, Apple-developed programming language for iOS, macOS, watchOS, and tvOS, emphasizing safety, performance, and modern syntax for building responsive and user-friendly applications.|
|     Kotlin        |is a statically typed programming language for modern multiplatform applications, known for its concise syntax, interoperability with Java, and support for Android development, functional programming, and coroutines.|
|     Apache        |often referring to the Apache HTTP Server, is a widely-used web server software, known for its role in the LAMP stack, flexibility, security features, and support for various modules and scripting languages.|
|     Firewall        |is a network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules, providing a barrier between a trusted and an untrusted network.|


