+++
weight=14
+++

{{% section %}}

## Equals and hash code

---

### Equals and hash code

```java{|7-19|21-28}
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;

        Aircraft aircraft = (Aircraft) o;

        if (year != aircraft.year) return false;
        if (registration != null ? !registration.equals(aircraft.registration) : aircraft.registration != null)
            return false;
        if (make != null ? !make.equals(aircraft.make) : aircraft.make != null) return false;
        return model != null ? model.equals(aircraft.model) : aircraft.model == null;
    }

    @Override
    public int hashCode() {
        int result = registration != null ? registration.hashCode() : 0;
        result = 31 * result + (make != null ? make.hashCode() : 0);
        result = 31 * result + (model != null ? model.hashCode() : 0);
        result = 31 * result + year;
        return result;
    }
}
```

---

### With Lombok

```java{|1}
@EqualsAndHashCode
public class Aircraft {
    private String registration; // unique identifier
    private String make;
    private String model;
    private int year;
}
```

By default, all non-static, non-transient fields will be taken into account. 

---

You can modify which fields are used by annotating them with @EqualsAndHashCode.Include or @EqualsAndHashCode.Exclude.

{{% fragment %}}You may also annotate the class with @EqualsAndHashCode(onlyExplicitlyIncluded = true) and then specify exactly what fields and methods are to be used by marking them with @EqualsAndHashCode.Include.{{% /fragment %}}
