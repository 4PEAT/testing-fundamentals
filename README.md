# IMPORTANT
##### Please don't forget to add the dependencies in your pom.xml file from the project.
To use these dependencies in a Maven project, you should place it within the <dependencies> section of your project's pom.xml file.
-
```xml
<!-- https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api -->
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.7.0-M1</version>
    <scope>test</scope>
</dependency>
```
-
```xml 
<!-- https://mvnrepository.com/artifact/org.assertj/assertj-core -->
<dependency>
    <groupId>org.assertj</groupId>
    <artifactId>assertj-core</artifactId>
    <version>3.16.1</version>
    <scope>test</scope>
</dependency>
```
-
```xml 
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-params</artifactId>
    <version>5.6.1</version><!-- the current version may change -->
    <scope>test</scope>
</dependency>
```



# Example 1
  **Used classes:**
  ```java
 test.java.exercise.ex01.CalculatorTest
 main.java.exercise.ex01.Calculator
```

 >The Java code consists of two classes: Calculator, which implements basic arithmetic operations like addition, subtraction, multiplication, and division, and CalculatorTest, which tests these operations using JUnit. 
      The CalculatorTest class includes methods to test each arithmetic operation in the Calculator, ensuring they work correctly. It also tests for exceptional cases, such as division by zero, to validate that the Calculator handles errors appropriately.    

# Example 2
**Used classes:**

   ```java
   test.java.exercise.ex02.CalculatorTest
   main.java.exercise.ex01.Calculator
   ```
   
> The CalculatorTest class uses AssertJ for its assertions. AssertJ is a Java library providing fluent assertion syntax. In the provided code, methods like assertThat, isEqualTo, and assertThatThrownBy are part of the AssertJ library, used for making assertions in a more readable and fluent way. 

# Example 3
**Used classes:**
```java
test.java.exercise.TODO.AccountTest
main.java.exercise.TODO.Account
```
>The AccountTest class in Java is a unit test for the Account class, using JUnit for testing. 
It includes setup and teardown methods for initializing and cleaning up before and after tests. 
The class tests key functionalities of the Account class like depositing money and checking the balance.
It also contains a placeholder for testing withdrawals beyond the account balance, which is currently disabled.
The Account class itself represents a simple bank account with basic operations like deposit, withdrawal, and balance checking.


# Example 4
**Used classes:**
```java
test.java.testing.exception.ExceptionTest
```
>The ExceptionTest class in Java contains a test method shouldThrowException() to verify that an IllegalArgumentException is thrown under certain conditions. The test deliberately triggers this exception by checking an empty string, and then asserts that the exception's message is as expected. If the exception is not thrown, the test fails, ensuring the exception handling works correctly.


# Example 5
**Used classes:**
```java
main.java.testing.exception.Divide
test.java.testing.exception.DivideExceptionTest
```
>The DivideExceptionTest class tests exception handling in the Divide class, specifically verifying that dividing by zero throws an IllegalArgumentException. It uses different JUnit and AssertJ methods to check if the exception is thrown with the correct message ("dividend can't be 0") when attempting to divide by zero. Each test method in DivideExceptionTest is a different way of performing this check, demonstrating various approaches to exception testing in Java. The Divide class itself contains a divide method which throws an 
IllegalArgumentException if the divisor is zero.

# Example 6
**Used classes:**
```java
main.java.testing.parametrized.Numbers01Helper01Test
```

>The Numbers01Helper01Test class in Java uses JUnit 5's parameterized testing feature to test if the Numbers01Helper.isOdd(number)  method correctly identifies odd numbers. The test method shouldReturnTrueForOddNumbers is supplied with a set of integers
(1, 3, 5, -3, 15, Integer.MAX_VALUE) via the @ValueSource annotation. Each of these values is tested in turn to check if the isOdd method returns true for these odd numbers, using the assertTrue assertion.


# Example 7
**Used classes:**
```java
main.java.testing.parametrized.Temperature02Converter
test.java.testing.parametrized.Temperature02ConverterTest
```
>The Temperature02Converter class is a Java enum providing temperature conversion functionalities using lambda expressions. 
It defines converters between Celsius, Kelvin, and Fahrenheit. The convertTemp method applies the appropriate conversion based on the enum instance.
The Temperature02ConverterTest class tests these conversions using JUnit 5's parameterized tests with the @EnumSource annotation.
It includes tests to ensure:

- The conversion result is greater than Integer.MIN_VALUE.
- The conversion is within a valid range (above -273.15 and below Float.MAX_VALUE).
- Specific conversions (Celsius to Fahrenheit and Celsius to Kelvin) result in values less than Integer.MAX_VALUE.
- Conversions, excluding Kelvin to Celsius, produce positive values.
  
These tests verify the correctness and range of the temperature conversions provided by the enum.

# Example 8

**Used classes:**
```java
main.java.testing.parametrized.Strings03
test.java.testing.parametrized.Strings03Test
```
>The Strings03 class contains two methods: toUpperCase (converts a string to uppercase after trimming spaces) and isBlank (checks if a trimmed string is empty).
The Strings03Test class tests these methods using JUnit 5's parameterized tests:
Test with CSV Source: Checks toUpperCase with various string inputs and expected uppercase results, using @CsvSource.
Test with CSV File: Verifies toUpperCase against data from a CSV file, using @CsvFileSource.
Test for Blank Strings: Tests isBlank with empty inputs using @EmptySource, to confirm it returns true for empty or null strings.


# Example 9
**Used classes:**
```java
test.java.testing.parametrized.MethodSource04Test
main.java.testing.parametrized.NumberWithParityArgumentsProvider
```
> The MethodSource04Test class in Java uses JUnit 5's parameterized testing feature with various methods for providing test arguments:
Odd Number Test: Uses @MethodSource("provideNumbers") to test if numbers are odd, using a stream of integers (1, 13, 101, 11, 121).
Number Parity Test with Detailed Arguments:
Uses @MethodSource("provideNumbersWithInfoAboutParity") to test number parity (odd or even), with detailed arguments (number and expected result) provided by Arguments.of().
Combined Sources Test: Demonstrates combining @CsvSource and @MethodSource in a single test to check number parity.
Parity Test with Custom Argument Provider:
Uses @ArgumentsSource(NumberWithParityArgumentsProvider.class) to test number parity, where NumberWithParityArgumentsProvider is a custom argument provider implementing ArgumentsProvider.
These tests efficiently handle multiple input scenarios for testing number properties (like being odd or even) using different sources of arguments.
