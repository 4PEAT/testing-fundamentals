### Task: Using AssertJ in Java

#### Objective
The goal of this task is to introduce the AssertJ library for fluent assertions in Java. You will write a simple class with basic methods and then write tests for these methods using AssertJ.

#### Prerequisites
- Java Development Kit (JDK) installed
- Maven or Gradle for project management
- Basic knowledge of Java and unit testing

#### Task Steps

1. **Set Up the Project:**
    - Create a new Maven or Gradle project.

    **For Maven:**
    Add the following dependency to your `pom.xml`:
    ```xml
    <dependency>
        <groupId>org.assertj</groupId>
        <artifactId>assertj-core</artifactId>
        <version>3.20.2</version>
        <scope>test</scope>
    </dependency>
    ```

    **For Gradle:**
    Add the following dependency to your `build.gradle`:
    ```groovy
    testImplementation 'org.assertj:assertj-core:3.20.2'
    ```

2. **Create a Simple Class:**
    - Create a class `MathUtils` with the following methods:
        ```java
        public class MathUtils {
            public int square(int number) {
                return number * number;
            }

            public int cube(int number) {
                return number * number * number;
            }

            public boolean isEven(int number) {
                return number % 2 == 0;
            }

            public boolean isOdd(int number) {
                return number % 2 != 0;
            }
        }
        ```

3. **Write Tests Using AssertJ:**
    - Create a test class `MathUtilsTest` in the `src/test/java` directory.
    - Write tests for each method in `MathUtils` using AssertJ for assertions.

4. **Specific Tests to Write:**

    - **Test the `square` method:**
        - Verify that the square of a positive number is calculated correctly.
        - Verify that the square of zero is zero.
        - Verify that the square of a negative number is positive.
        
    - **Test the `cube` method:**
        - Verify that the cube of a positive number is calculated correctly.
        - Verify that the cube of zero is zero.
        - Verify that the cube of a negative number is negative.

    - **Test the `isEven` method:**
        - Verify that an even number returns `true`.
        - Verify that an odd number returns `false`.
        - Verify that zero returns `true`.

    - **Test the `isOdd` method:**
        - Verify that an odd number returns `true`.
        - Verify that an even number returns `false`.
        - Verify that zero returns `false`.

5. **Run Your Tests:**
    - Use your IDE or build tool (Maven or Gradle) to run the tests and ensure they pass.

#### Deliverables
- A Maven or Gradle project with the following structure:
    ```
    project-root
    ├── src
    │   ├── main
    │   │   └── java
    │   │       └── MathUtils.java
    │   └── test
    │       └── java
    │           └── MathUtilsTest.java
    ├── pom.xml (if using Maven)
    └── build.gradle (if using Gradle)
    ```
- Ensure all tests pass successfully using AssertJ for assertions.

#### Tips
- Ensure that the `MathUtils` class and the test class are placed in the correct directories.
- Focus on using AssertJ’s fluent API to make assertions, which provides a more readable and expressive way to write tests.

```
