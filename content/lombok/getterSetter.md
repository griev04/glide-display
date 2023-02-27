+++
weight=11
+++

{{% section %}}

## Getters and Setters

---

### Getters and Setters


```java{|7-37|11-13}
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;

    public String getRegistration() {
        return registration;
    }

    protected void setRegistration(String registration) {
        this.registration = registration;
    }

    public String getMake() {
        return make;
    }

    public void setMake(String make) {
        this.make = make;
    }

    public String getModel() {
        return model;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public int getYear() {
        return year;
    }

    public void setYear(int year) {
        this.year = year;
    }
}
```

---

### With Lombok

```java{}
@Getter
@Setter
public class Aircraft {
    @Setter(AccessLevel.PROTECTED)
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;
}
```

When a field (i.e. `model`) is annotated with both @Getter or @Setter, Lombok will define a getModel() or a setModel() method respectively.

---

### With Lombok

```java{1-2|4-5}
@Getter
@Setter
public class Aircraft {
    @Setter(AccessLevel.PROTECTED)
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;
}
```

Entire classes can be annotated as well and the logic will be applied to each field.

The generated methods will be **public** unless a particular AccessLevel is specified (PUBLIC, PROTECTED, PACKAGE, and PRIVATE).

{{% /section %}}