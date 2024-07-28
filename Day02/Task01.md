## Task Requirements

### 1. Implementation

#### Class Creation:
- Create a class named `NumberProcessor`.

#### Method Addition:
- Add a method `computeSquareRoot` to the `NumberProcessor` class that:
  - Accepts an integer `number` as its parameter.
  - Throws an `IllegalArgumentException` with the message "Cannot compute square root of a negative number." if `number` is negative.
  - Returns the integer part of the square root of `number` if it is non-negative.

### 2. Testing

#### Test Class Creation:
- Create a test class named `NumberProcessorTest`.

#### Test Method Addition:
- Write a test method `testComputeSquareRoot_NegativeInput_ThrowsIllegalArgumentException` that:
  - Uses `assertThrows` to verify that an `IllegalArgumentException` is thrown when `computeSquareRoot` is called with a negative number
