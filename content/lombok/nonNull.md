+++
weight=13
+++

{{% section %}}

## Non Null

---

### Non Null

```java{|13-21}
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;

    public Aircraft(
            String registration,
            String make,
            String model,
            int year
    ) {
        if (registration == null) {
            throw new NullPointerException("registration must not be null");
        }
        if (make == null) {
            throw new NullPointerException("make must not be null");
        }
        if (model == null) {
            throw new NullPointerException("model must not be null");
        }
        this.registration = registration;
        this.make = make;
        this.model = model;
        this.year = year;
    }
}
```

---

### Fancier non Null
```java{|13-16}
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;

    public Aircraft(
            String registration,
            String make,
            String model,
            int year
    ) {
        this.registration = Objects.requireNonNull(registration, "model must not be null");
        this.make = Objects.requireNonNull(make, "make must not be null");
        this.model = Objects.requireNonNull(model, "model must not be null");
        this.year = year;
    }
}
```

---

### With Lombok

```java{|8-10|7-17}
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;

    public Aircraft(
            @NonNull String registration,
            @NonNull String make,
            @NonNull String model,
            int year
    ) {
        this.registration = registration;
        this.make = make;
        this.model = model;
        this.year = year;
    }
}
```

---
What about setters?

We can include non null check also on them by applying directly the `@NonNull` annotation on the corresponding fields

```java{|2-7}
public class Aircraft {
    @NonNull
    private String registration; // unique identifier
    @NonNull
    private String make;
    @NonNull
    private String model;
    private int year;
}
```