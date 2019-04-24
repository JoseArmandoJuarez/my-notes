## Design the application architecture
---

* Every application must have an architecture, but plenty of applications have been created with architectures that were not well considered. As a developer, you should design your solutions architecture to fulfill application requirements an create a robust and high performing application.

---

## Application layers
* An application is simply a set of functionality: a screen or set of screens that displays information, a way to persist data across uses, and a way to make business decisions.
* A layer is a logical grouping of code that works together as a common concern. Layers work together to produce the completed application.

---

## Data Access
* Web-based business needs is how it connects users data.
* As you plan an application, you should evaluate your data requirements early in the process. 
* Will your application access a set of data you already have, or will your data data design be managed along with you application design? 
* For example, suppose you want to add a just-in-time supplier view to your inventory process so your suppliers can better your application will provide access to other data, or maybe you have to design and implement an entirely new database schema.
	
---

## Data access options
* After you determined your data requirements - existing data, new data or a combination - considere how you need to access the data. 
* Using an object relational mapper (O/RM)
    * An O/RM is an application or system that aids in the conversion of data within a relational database management system (RDBMS) and the object model that is necessary for use within object-oriented programming.

---

## Separation of Concern (SoC)
* Separation of concern (SoC) is a software development concept that separates a computer program into different sections, or concerns, in which each concern has a different purpose. By separating these sections, each can encapsulate information that can be developed and updated independently. N-tier development (multilayer architecture) is an example of SoC in which the user interface (UI) is separated from both the business layer and the data access layer.
* A term closely associated with SoC is loose coupling. Loose coupling is an architectural approach in which the designer seeks to limit the amount of interdependencies between various parts of a system. By reducing interdependencies, changes to one area of an application are less likely to affect another area. Also, by eliminating interdependencies, you ensure that your application is more maintainable, tesable, and flexible, which tends to result in a more stable system.

---

## Designing for scalability
* Scalability is the capability of a system to handle a growing amount of work. Although usage is minimal during site development, usage can increase greatly after implementation to a production environment. To ensure a positive user experience , you need to consider scalability early in the application planning phase because your scalability decisions affect your architectural design considerations. There are two primary ways that you can scale: horizontally or vertically.
* With horizontal scaling, you scale by adding additional nodes to the system. This is a web farm scenario, in which a number of commodity-level systems can be added or removed as demand fluctuates. They are served using a load balancer or other piece of network equipment that determines which server should be called.
* If your application will scale horizontally, you must make various decisions. Depending on the network hardware that will be deployed and how it handles sessions, your session state information will be affected. You also need to determine how multiple servers will affect server caching of information, such as whether to cache rendered HTML that was sent to the client or cache data from a database.
* Also, if your application will provide file management, considere where those files will be stored to ensure access to across multiple servers. Scaling horizontally adds some architectural considerations, but it is low-cost and effective way to scale, especially because the cost for commodity servers continues to drop. Keep in mind that commodity servers are not necessarily physical servers, but can be virtual machines. It is far less expensive to roll in unused capacity using virtualization from another system than it is to add capacity to a system.
* With vertical scaling, you scale by adding resources to a single system. This typically involves adding central processing units (CPUs) or memory. It can also refer to accessing more of the existing resources on the system. Vertical scaling has its own architecture considerations as well. An application that scales on a single system might pay more attention to threading, input/output (I/O), garbage collection, and other design decisions that would help the application take better advantage of the additional memory or CPUs. By definition, however, a vertical scaling solution is limited. Theoretically, you can keep adding systems when scaling horizontally; however, you might run out of physical capability in a vertical solution if usage continues to grow. Also, reliability is negatively affected in a vertical scaling solution because there remains a single point of failure. If the systems motherboard goes down, so does your application.

---

## Distributed application
* A distributed application is defined as software that runs on two or more computers. The capability to run on multiple computers is critical for systems that are concerned with performance, availability, scalability, and reliability.

---

## Hybrid Application
* A hybrid application is an application hosted  in multiple places. On part is hosted within the company's network and another part is hosted in windows azure.
