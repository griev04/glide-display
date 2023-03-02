+++
weight=16
+++

{{% section %}}

## Data

---

### Data

@Data is a shortcut annotation that combines:
- @ToString
- @EqualsAndHashCode
- @Getter
- @Setter
- @RequiredArgsConstructor

---

### With Lombok

```java{|1-5}
@ToString
@EqualsAndHashCode
@Getter
@Setter
@RequiredArgsConstructor
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

---

### With Data

```java{|1}
@Data
public class Aircraft {
    private final String registration; // unique identifier
    private final String make;
    private final String model;
    private int year;
}
```

{{% /section %}}