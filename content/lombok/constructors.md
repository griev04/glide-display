+++
weight=10
+++

{{% section %}}

## Constructors

---

### Constructors

```java{|1-5|7-12|14-18|20-21}
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;

    public Aircraft(String registration, String make, String model, int year) {
        this.registration = registration;
        this.make = make;
        this.model = model;
        this.year = year;
    }

    public Aircraft(String registration, String make, String model) {
        this.registration = registration;
        this.make = make;
        this.model = model;
    }

    public Aircraft() {
    }
}
```

---

### With Lombok

```java{|1-3}
@NoArgsConstructor
@AllArgsConstructor
@RequiredArgsConstructor // final and non null fields
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

{{% /section %}}