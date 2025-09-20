## Maven Multi Module Project:
Well this is very basic Project for those who need to understand how to build Maven multiple sub projects in Parent Project.
## Project Structure

ParentModule_ArithmeticOperations
│── pom.xml (Parent POM)
│
├── ChildModule1_ADD
│ ├── pom.xml (Module for Addition)
│ └── src/main/java/org/example/ChildModuleClass1_ADD.java
│
├── ChildModul2_SUB
│ ├── pom.xml (Module for Subtraction)
│ └── src/main/java/org/example/ChildModuleClass2_SUB.java

yaml
Copy code

- **Parent Module**: Contains the common configuration for all child modules.  
- **ChildModule1_ADD**: Performs addition operations.  
- **ChildModul2_SUB**: Performs subtraction operations.  

---

## Prerequisites

- Java 8 or higher  
- Maven 3.x  
- Git (if cloning from GitHub)  

---

## Build and Run

### 1. Clone the repository
bash
git clone https://github.com/Vaishnavi280/MavenMultiModuleProject.git
cd MavenMultiModuleProject

### 2. Build the project
From the parent module folder:

bash
Copy code
mvn clean install

### 3. Run a specific child module
Navigate to the child module folder:

bash
Copy code
cd ChildModule1_ADD
Run the main class (example for addition module):

bash
Copy code
mvn exec:java -Dexec.mainClass="org.example.ChildModuleClass1_ADD"
Or using Java directly:

bash
Copy code
java -cp target/classes org.example.ChildModuleClass1_ADD
Repeat the same steps for the subtraction module (ChildModul2_SUB).

### Notes
Ensure that each child module has a main method to execute.

#### This project uses Maven’s multi-module structure to separate concerns for different operations.

Dependencies and build settings are inherited from the parent POM.

Author
##### Vaishnavi

GitHub: https://github.com/Vaishnavi280 
