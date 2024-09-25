### Task: Implement and Test a Temperature Converter using JUnit with Given-When-Then

#### Objective
The goal of this task is to implement a simple temperature conversion utility and write unit tests using the Given-When-Then structure with JUnit.

#### Task Steps

1. **Create a Temperature Converter Class:**
    - Implement a class `TemperatureConverter` with the following methods:
        ```java
        public class TemperatureConverter {
            
            // Convert Celsius to Fahrenheit
          celsiusToFahrenheit()

            // Convert Fahrenheit to Celsius
           fahrenheitToCelsius()
            
        }
        ```

2. **Write Unit Tests Using Given-When-Then:**
    - Create a test class `TemperatureConverterTest` in the `src/test/java` directory.
    - Write unit tests using the Given-When-Then structure to verify the functionality of each method.

3. **Specific Tests to Write:**

    - **Test the `celsiusToFahrenheit` Method:**
        - **Given:** A temperature in Celsius.
        - **When:** The temperature is converted to Fahrenheit.
        - **Then:** The result should be the correct Fahrenheit equivalent.
        - **Examples to Test:**
            - Given: 0°C, When converted, Then: 32°F.
            - Given: 100°C, When converted, Then: 212°F.
            - Given: -40°C, When converted, Then: -40°F.

    - **Test the `fahrenheitToCelsius` Method:**
        - **Given:** A temperature in Fahrenheit.
        - **When:** The temperature is converted to Celsius.
        - **Then:** The result should be the correct Celsius equivalent.
        - **Examples to Test:**
            - Given: 32°F, When converted, Then: 0°C.
            - Given: 212°F, When converted, Then: 100°C.
            - Given: -40°F, When converted, Then: -40°C.

4. **Run Your Tests:**
    - Use your IDE or build tool (Maven or Gradle) to run the tests and ensure they pass.

#### Deliverables
- A project with the following structure:
    ```
    project-root
    ├── src
    │   ├── main
    │   │   └── java
    │   │       └── TemperatureConverter.java
    │   └── test
    │       └── java
    │           └── TemperatureConverterTest.java
    ├── pom.xml (if using Maven)
    └── build.gradle (if using Gradle)
    ```
- Ensure all tests pass successfully using the Given-When-Then structure for assertions.

#### Tips
- Use JUnit’s `assertEquals` for checking expected vs. actual results.
- Use meaningful method and test names to clearly indicate what is being tested.
