+++
weight=20
+++

{{% section %}}

## Log

---

### Log

```java{}
public class ApiClientConfiguration {

    private static Logger LOG = LoggerFactory.getLogger(ApiClientConfiguration.class);

    // LOG.debug(), LOG.info(), ...

}
```

---

### With Lombok

```java{|1,4-6}
@Slf4j
public class ApiClientConfiguration {

    log.debug("All is good")

    log.info("Action triggered")

}
```

{{% /section %}}