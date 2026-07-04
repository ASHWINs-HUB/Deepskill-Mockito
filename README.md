# Mockito Exercises

This repository contains practical examples of mocking, stubbing and verification using Mockito.

## Technologies Used

- Java 21
- Maven
- JUnit 5
- Mockito 5
- IntelliJ IDEA

## Project Structure

```
src
├── main
│   └── java
└── test
    └── java
```

## Exercises

### Exercise 1 – Mocking and Stubbing

Created mock objects and returned predefined values.

```java
when(mockApi.getData()).thenReturn("Mock Data");
```

---

### Exercise 2 – Verifying Interactions

Verified method invocation.

```java
verify(mockApi).getData();
```

---

### Exercise 3 – Argument Matching

Used Mockito argument matchers.

```java
verify(mockApi).sendData(anyString());
```

---

### Exercise 4 – Handling Void Methods

Stubbed void methods.

```java
doNothing().when(mockApi).sendData(anyString());
```

---

### Exercise 5 – Multiple Return Values

```java
when(mockApi.getData())
.thenReturn("First")
.thenReturn("Second")
.thenReturn("Third");
```

---

### Exercise 6 – Verify Interaction Order

```java
InOrder order = inOrder(mockApi);

order.verify(mockApi).getData();
order.verify(mockApi).sendData("ABC");
```

---

### Exercise 7 – Void Method Exceptions

```java
doThrow(new RuntimeException())
.when(mockApi)
.deleteData();
```

## Run Tests

```bash
mvn test
```

## Learning Outcomes

- Mock dependencies
- Stub methods
- Verify interactions
- Match arguments
- Handle void methods
- Verify invocation order
- Test exceptions
