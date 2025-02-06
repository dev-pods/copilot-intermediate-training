# Demo Guide: Copilot Chat Coding Practices

This guide provides a detailed walkthrough of how to utilize GitHub Copilot Chat to implement and validate a utility function within the PowerBI JavaScript repository. The focus is on efficiency, maintainability, and best practices.

---

## Prerequisites

1. **Repository Setup**:
   - Clone the [PowerBI JavaScript Repository](https://github.com/microsoft/PowerBI-JavaScript).
   - Install [Visual Studio Code](https://code.visualstudio.com/) with GitHub Copilot and Copilot Chat extensions.

2. **Development Environment**:
   - Ensure Node.js and npm are installed.
   - Confirm Jest is configured for testing.

---

## Task 1: Implement `calculatePercentage` Utility Function

### Objective
Create a reusable utility function that calculates percentages, handling edge cases such as division by zero.

### Steps

1. **Identify the Utilities File**:
   - Use `@workspace` to locate the correct file for utility functions:
     ```
     @workspace, where should I place a new utility function for percentage calculations?
     ```

2. **Create the Function**:
   - Ask Copilot Chat to generate the function:
     ```
     Can you write a utility function named calculatePercentage in JavaScript that takes two arguments, part and total, and calculates the percentage? Ensure the function handles cases where total is zero by returning 0.
     ```

3. **Handle Edge Cases**:
   - Query Copilot Chat for additional edge cases:
     ```
     What are some additional test cases I should include for this utility function?
     ```

4. **Document the Function**:
   - Add a description of the function and its parameters:
     ```
     Refactor the following file to include a brief description of the function’s purpose and parameters.
     ```

---

## Task 2: Generate Unit Tests

### Objective
Write and execute unit tests using Jest to validate the functionality of `calculatePercentage`.

### Steps

1. **Set Up the Test Environment**:
   - Run:
     ```
     npm test
     ```
   - If Jest is not installed, use:
     ```
     npm install jest
     ```

2. **Create a Test File**:
   - Locate the tests directory with `@workspace`:
     ```
     @workspace, where is the current test directory?
     ```
   - Create `calculatePercentage.test.js` in the directory.

3. **Write Unit Tests**:
   - Ask Copilot Chat to generate test cases:
     ```
     Create unit tests for the calculatePercentage function that we have created.
     ```

4. **Run the Tests**:
   - Execute:
     ```
     npm test calculatePercentage.test.js
     ```

5. **Debug and Iterate**:
   - Use Copilot Chat to troubleshoot any failing tests:
     ```
     Why is this test failing, and how can I fix it?
     ```

---

## Task 3: Refactor and Add Comments

### Objective
Enhance code readability by adding robust comments and adhering to naming conventions.

### Steps

1. **Locate Modified Files**:
   - Use `@workspace` to find changed files:
     ```
     @workspace, what files have I changed so far for this task?
     ```

2. **Add Comments**:
   - Request Copilot Chat to add explanatory comments:
     ```
     Add robust comments for the following file that explains what each piece of code is doing.
     ```

3. **Refactor for Naming Conventions**:
   - Update to camelCase or other conventions if needed.

---

## Task 4: Deployment and Consumption

### Objective
Demonstrate the functionality of `calculatePercentage` in a standalone JavaScript file.

### Steps

1. **Create a Consumer File**:
   - Navigate to the root of the repository.
   - Create `consumeCalculatePercentage.js`.

2. **Import the Function**:
   ```javascript
   const { calculatePercentage } = require('./path/to/utilities');
   ```

3. **Write Example Use Cases**:
   ```javascript
   console.log('Example 1:', calculatePercentage(50, 100)); // Expected Output: 50
   console.log('Example 2:', calculatePercentage(23, 0));  // Expected Output: 0
   console.log('Example 3:', calculatePercentage(7, 20));  // Expected Output: 35
   ```

4. **Run the File**:
   ```
   node consumeCalculatePercentage.js
   ```

5. **Document the File**:
   - Add a comment block explaining its purpose:
     ```javascript
     /**
      * This is a simple demo file to consume the calculatePercentage utility function.
      * It demonstrates the functionality of the function with basic use cases.
      */
     ```

6. **Enhance the Demo**:
   - Use Copilot Chat for suggestions and refactoring.
   - Optionally, add error handling:
     ```javascript
     try {
       console.log('Example 4:', calculatePercentage('invalid', 20));
     } catch (error) {
       console.error('Error:', error.message);
     }
     ```

---

## Summary

This demo showcased the power of GitHub Copilot Chat in implementing, testing, and documenting a reusable utility function. By following these steps, you’ll:
- Develop clean, maintainable code.
- Leverage AI to streamline development processes.
- Ensure robust functionality through comprehensive testing and documentation.

### Resources
- [PowerBI JavaScript Repository](https://github.com/microsoft/PowerBI-JavaScript)
- [Jest Documentation](https://jestjs.io/docs/getting-started)
