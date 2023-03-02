+++
weight=19
+++

{{% section %}}

## Builder

---

### Builder

Builder is a creational design pattern that helps you construct objects step by step.

---

### Builder

You may create different objects with different fields by using the same builder.

```java{}
Aircraft F35 = 
    Aircraft.builder()
        .make("Lockheed Martin")
        .model("F-35")
    .build();

Aircraft A320 = 
    Aircraft.builder()
        .make("Airbus")
        .model("A320")
        .year(2022)
    .build();
```


---

### Builder

But you will need to create a LOT of code

```java{}
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

    public static AircraftBuilder builder() {
        return new AircraftBuilder();
    }

    public static class AircraftBuilder {
        private String registration;
        private String make;
        private String model;
        private int year;

        AircraftBuilder() {
        }

        public AircraftBuilder registration(String registration) {
            this.registration = registration;
            return this;
        }

        public AircraftBuilder make(String make) {
            this.make = make;
            return this;
        }

        public AircraftBuilder model(String model) {
            this.model = model;
            return this;
        }

        public AircraftBuilder year(int year) {
            this.year = year;
            return this;
        }

        public Aircraft build() {
            return new Aircraft(registration, make, model, year);
        }

        public String toString() {
            return "Aircraft.AircraftBuilder(registration=" + this.registration + ", make=" + this.make + ", model=" + this.model + ", year=" + this.year + ")";
        }
    }
}
```

---

<img src="img/this-is-fine.webp" alt="Lombok Project">

---

### With Lombok

```java{|1}
@Builder
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

{{% /section %}}