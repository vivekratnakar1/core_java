# Java Object Cloning POC

A simple Proof of Concept (POC) demonstrating the difference between **Shallow Cloning** and **Deep Cloning** in Java using the `Cloneable` interface.

## 🚀 Overview

Object cloning in Java refers to the creation of an exact copy of an object. This project illustrates:
- **Shallow Cloning:** The default behavior where nested object references are shared between the original and cloned objects.
- **Deep Cloning:** A custom implementation where nested objects are cloned independently, ensuring full isolation.

## 📋 Prerequisites

To run this project, you need:
- **Java Development Kit (JDK 8)** or higher.
- A terminal or an IDE (like IntelliJ IDEA, Eclipse, or VS Code).

## 🛠️ How to Run

Follow these steps to compile and execute the POC:

1. **Save the file:** Save the code as `CloningDemo.java`.
2. **Compile the code:** Open your terminal and run:
   ```bash
   javac CloningDemo.java
   ```
3. **Run the application:** Execute the compiled bytecode:
   ```bash
   java CloningDemo
   ```

## 📊 Expected Output

When you execute the program, you will see how modifying a shallow copy alters the original object, while the deep copy remains protected:

```text
--- After modifying Shallow Clone's City to 'Delhi' ---
Original Emp City: Delhi
Shallow Cloned Emp City: Delhi
Deep Cloned Emp City: Mumbai
```

## 📝 Key Code Components

- **`Cloneable` Interface:** Marker interface implemented by `Employee` and `Address` to authorize cloning.
- **`super.clone()`:** Invokes the native method to copy field values layer-by-layer.
