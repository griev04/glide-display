+++
weight=20
+++

{{% section %}}

## To String

---

### To String

```java{|7-15}
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;

    @Override
    public String toString() {
        return "Aircraft{" +
                "registration='" + registration + '\'' +
                ", make='" + make + '\'' +
                ", model='" + model + '\'' +
                ", year=" + year +
                '}';
    }
}
```

---

### With Lombok

```java{|1}
@ToString(includeFieldNames=true)
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

toString() will return a String containing the class name and all its non-static field values.

---


The method can be tweaked in a few ways:

{{% fragment %}}`@ToString(includeFieldNames=false)` to omit the field names.{{% /fragment %}}

{{% fragment %}}Annotate a field with @ToString.Exclude to make Lombok ignore it.{{% /fragment %}}

{{% fragment %}}@ToString(onlyExplicitlyIncluded = true) on the class and mark each field you want to include with @ToString.Include.{{% /fragment %}}

{{% /section %}}