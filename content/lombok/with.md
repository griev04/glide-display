+++
weight=18
+++

{{% section %}}

## With

---

### With

When working with immutable objects, you don't have access to setter methods but you may need to create a new object by modifying an existing one.

---

### With Lombok

You may define some `with` methods that will create a new object by modifying only the supplied field value.

```java{|8-22}
@AllArgsConstructor
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;

    Aircraft withRegistration(String registration) {
        return new Aircraft(registration, make, model, year);
    }

    Aircraft withMake(String make) {
        return new Aircraft(registration, make, model, year);
    }

    Aircraft withModel(String model) {
        return new Aircraft(registration, make, model, year);
    }

    Aircraft withYear(int year) {
        return new Aircraft(registration, make, model, year);
    }
}
```

---

### With Value

```java{|3,5,7,9,15}
@Value
public class Aircraft {
    String registration; // unique identifier
    String make;
    String model;
    int year;
}
```

{{% /section %}}