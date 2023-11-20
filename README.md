**FINAL PROJECT REPORT**

**on the** Software Design Patterns discipline

  

**Beisenov Zhangeldy**

Group: SE-2208

Teacher: Kalnazar Sayat

**Introduction**

Project Overview

The ZhandySound project encompasses a robust audio content management system, integrating diverse design patterns to attain a versatile and scalable architecture. The primary goal of the project is to provide users with the ability to listen to songs and audiobooks based on their access levels, with additional features such as upgrading access levels and adding new content for singers and writers.

  

Purpose and Objectives

  

**·**      Importance of Design Patterns

Design patterns play a crucial role in software development by offering reusable and proven solutions to common problems. In the ZhandySound project, design patterns are employed to enhance modularity, maintainability, and scalability. They allow for better code organization and promote the separation of concerns, making the system more robust and adaptable to changes.

**·**      Project Objectives

The main objectives of the ZhandySound project are as follows:

1.    Audio Content Management: Manage a variety of audio content, including songs and audiobooks.

2.    User Access Levels: Implement a user access level system, allowing users to access different types of content based on their subscription type.

3.    Design Patterns Implementation: Demonstrate the use of design patterns to address specific challenges in the project.

4.    Database Integration: Integrate a PostgreSQL database to store user information, content details, and payment-related data.

**Main Body**

Features and Design Patterns

  

1\. Factory Pattern

  

The Factory pattern is employed in the ZhandySound project to create instances of different audio content types, such as songs and audiobooks, without specifying their concrete classes in the client code. The Factory abstract class defines a method, createContent, which is implemented by subclasses (SongFactory and AudioBookFactory). This enables the creation of diverse content objects while adhering to a common interface. This approach enhances code maintainability and allows for easy extension when introducing new content types.

  

_Screenshot 1 Concrete Factory_

  

  

_Screenshot 2 Concrete product_

2\. Strategy Pattern

  

The Strategy pattern is used to encapsulate the behavior of different user roles in the ZhandySound project. The IStrategy interface defines a common method, action, implemented by concrete strategies like Listener, Singer, and Writer. This pattern enables the client (Client class) to switch between different strategies dynamically, promoting flexibility in managing user actions. The Strategy pattern enhances the scalability of the project by isolating the behavior of each user type.

  

  

_Screenshot 3 Concrete strategy_

  

_Screenshot 4 Context_

3\. Decorator Pattern

  

The Decorator pattern is employed for user access level management in the ZhandySound project. Access levels are dynamically decorated using IAccessLevelDecorator implementations such as BasicAccessDecorator, PremiumAccessDecorator, and UltraAccessDecorator. These decorators modify the user's access level behavior, allowing for incremental upgrades without modifying the core Client class. This pattern adheres to the Open/Closed Principle, facilitating easy extension of access level functionality.

  

_Screenshot 5 Concrete Decorator_

  

4\. Adapter Pattern

  

The Adapter pattern is utilized to adapt payment processing for different currencies in the ZhandySound project. The DollarToTengeAdapter adapts the DollarPayment class to the TengePayment class, allowing seamless integration with the existing payment system. This pattern ensures that the PaymentMachine can accept payments in both USD and KZT without modifying existing payment-related classes. The Adapter pattern promotes compatibility and flexibility in handling diverse payment scenarios.

  

  

_Screenshot 6 Adapter_

  

  

_Screenshot 7 Adaptee_

5\. Observer Pattern

  

The Observer pattern is implemented to notify users about payment statuses in the ZhandySound project. The PaymentMachine acts as the subject, and classes implementing IPaymentStatusObserver are observers interested in payment updates. This pattern decouples the payment processing logic from the notification system, promoting extensibility and maintainability. Observers can be added or removed dynamically, allowing for easy customization of the notification mechanism.

  

_Screenshot 8 Subject_

  

  

_Screenshot 9 Subscriber_

6\. Singleton Pattern

  

The Singleton pattern is applied to the Database class in the ZhandySound project. This pattern ensures that only one instance of the database connection exists throughout the application's lifecycle. The Database class is responsible for handling database connectivity, and the Singleton pattern guarantees a global point of access to this instance. This enhances efficiency and avoids the overhead of creating multiple database connections.

  

  

_Screenshot 10 Singleton_

  

ERD- Diagram:

  

  

  
![sql](https://github.com/whateveer/test2/assets/66480258/60821eb9-732b-4152-afdb-c7f84247fadf)

_Diagram 1 PostgreSQL Database_

  

UML-Diagram:

  

  

_Diagram 2 UML including dependencies_

**Conclusion**

Summary

  

In summary, the ZhandySound project epitomizes the seamless integration of theoretical concepts and practical insights gleaned from software design and Database Management Systems (DBMS) courses. By incorporating design patterns this audio content management system manifests a sophisticated and adaptable architecture. Successfully addressing challenges in user access levels and payment processing, the project exemplifies the pragmatic application of SOLID principles. The experience of applying DBMS knowledge in crafting an efficient and well-structured database underlines the project's commitment to both theory and hands-on proficiency.

  

Challenges Faced

  

During the development process, challenges were encountered in combining the decorator and the strategy patterns so that the decorator can change the value of the access level of the client.

  

Future Improvements

  

For future improvements, the project could benefit from additional content types, such as podcasts or lectures. Enhancements to the user interface by adding GUI and the improvement of security system through encoding all sensitive data, and SQL injection prevention. Also in the future, new functionality can be added: adding collaborations with other artists, albums and creating playlists for songs and podcasts, adding a system of likes and dislikes.

  

In essence, ZhandySound encapsulates not just a project's completion, but a journey of growth, informed decision-making, and the practical application of acquired knowledge — a testament to the transformative power of a comprehensive education in software engineering.

  

**References**

Refactoring Guru (n.d.). Retrieved November 21, 2023, from https://refactoring.guru/design-patterns

Okhravi, C. (n.d.). Christopher Okhravi. YouTube. Retrieved November 21, 2023, from https://www.youtube.com/@ChristopherOkhravi

Stack Overflow. (n.d.). Retrieved November 21, 2023, from https://stackoverflow.com/
