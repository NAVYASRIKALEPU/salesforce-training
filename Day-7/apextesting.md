# Unit Testing Basics and Salesforce Testing Requirements

## Unit Testing Basics

* Unit testing is the process of testing individual parts or units of code.
* It checks whether each function or method works correctly.
* Helps detect errors early in development.
* Unit tests are usually automated and repeatable.
* Improves code quality and maintainability.
* In Apex, unit tests are written using test classes and test methods.

Example:

```apex id="qumqqf"
@isTest
private class CalculatorTest {
    @isTest
    static void additionTest() {
        Integer sum = 5 + 5;
        System.assertEquals(10, sum);
    }
}
```

---

## Why Salesforce Requires Testing

* Salesforce requires testing to ensure application reliability and security.
* Apex code must have at least 75% code coverage before deployment to production.
* Testing helps prevent bugs from affecting live users.
* Ensures new updates do not break existing functionality.
* Validates business logic and automation processes.
* Supports stable and high-quality enterprise applications.
* Salesforce uses test execution to verify system performance during deployment.
