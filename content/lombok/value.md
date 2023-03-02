+++
weight=17
+++

{{% section %}}

## Value

---

### Value

It's like `@Data` but it's its `immutable` version.

All the fields are made **private** and **final** as it includes:

```
@FieldDefaults(makeFinal = true, level = AccessLevel.PRIVATE)
```

It will also generate the same functionalities of:

- @ToString
- @EqualsAndHashCode
- @Getter
- @Setter
- @RequiredArgsConstructor

---

### Value

```java{|1-6}
@ToString
@EqualsAndHashCode
@Getter
@Setter
@RequiredArgsConstructor
@FieldDefaults(makeFinal = true, level = AccessLevel.PRIVATE) // experimental
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

---

### With Lombok

```java{|1}
@Value
public class Aircraft {
    String registration; // unique identifier
    String make;
    String model;
    int year;
}
```

{{% /section %}}