+++
weight=22
+++

{{% section %}}

## Val and var

---

### Val and var

Hassle-free local variables.

{{%fragment%}}`You can use `val` as the type of a local variable declaration instead of actually writing the type.{{%/fragment%}}

{{%fragment%}}`var` is the same but the local variable is not marked as final.{{%/fragment%}}

---

### Val and var

```java{|2}
public HashMap<Integer, String> getMap() {
    HashMap<Integer, String> map = new HashMap();
    map.put(0, "zero");
    map.put(5, "five");
    return map;
}
```

---

### With Lombok - val

```java{|2}
public HashMap<Integer, String> getMap() {
    val map = new HashMap<Integer, String>();
    map.put(0, "zero");
    map.put(5, "five");
    return map;
}
```
---

### With Lombok - var

```java{|2}
public String getTitle() {
    var title = "Some title";
    title = "Some better title";
    return title;
}
```

{{% /section %}}