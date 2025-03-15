# Java: Constructors & Singleton Pattern

## 🚀 Constructors
Constructors initialize objects in Java.

### ✅ Key Points:
- **Same name** as the class.
- **No return type** (not even `void`).
- **Automatically invoked** when an object is created.
- Types: **Default, Parameterized, Copy Constructor**.
- **Overloading allowed**, but **no overriding**.

### 📌 Example:
```java
class Car {
    String model;
    
    // Constructor
    Car(String model) {
        this.model = model;
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Tesla");
        System.out.println(myCar.model); // Output: Tesla
    }
}
```

---

## 🔥 Singleton Pattern
Ensures only **one instance** of a class exists globally.

### ✅ Key Points:
- **Private constructor** to prevent direct instantiation.
- **Static instance variable** stores the single instance.
- **Public static method** returns the instance.

### 📌 Example:
```java
class Singleton {
    private static Singleton instance;
    
    private Singleton() {} // Private constructor
    
    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}

public class Main {
    public static void main(String[] args) {
        Singleton obj1 = Singleton.getInstance();
        Singleton obj2 = Singleton.getInstance();
        
        System.out.println(obj1 == obj2); // Output: true (same instance)
    }
}
```

---

## 🎯 Why Use Singleton?
✅ **Efficient resource management** (e.g., Database connections, Logging).  
✅ **Ensures global state consistency**.  
✅ **Prevents redundant object creation**, saving memory.  

---


