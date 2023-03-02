+++
weight=20
+++

{{% section %}}

## Log

---

### Log

```java{|1-5|7-12|14-18|20-21}
public class ApiClientConfiguration {

    private static Logger LOG = LoggerFactory.getLogger(ApiClientConfiguration.class);

    // LOG.debug(), LOG.info(), ...

}
```

---

### With Lombok

```java{|1}
@Slf4j
public class ApiClientConfiguration {

    // log.debug(), log.info(), ...

}
```

{{% /section %}}