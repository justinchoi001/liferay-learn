# Database Templates

Below are templates (example [portal properties](./portal-properties.md)) for configuring various databases as a built-in data source for Liferay DXP.

## MariaDB

```properties
jdbc.default.driverClassName=org.mariadb.jdbc.Driver
jdbc.default.url=jdbc:mariadb://localhost/lportal?useUnicode=true&characterEncoding=UTF-8&useFastDateParsing=false
jdbc.default.username=
jdbc.default.password=
```

## MySQL

```important::
   MySQL Connector/J 8.0 is highly recommended for use with MySQL Server 8.0 and 5.7.
```

```properties
jdbc.default.driverClassName=com.mysql.cj.jdbc.Driver
jdbc.default.url=jdbc:mysql://localhost/lportal?characterEncoding=UTF-8&dontTrackOpenResources=true&holdResultsOpenOverStatementClose=true&serverTimezone=GMT&useFastDateParsing=false&useUnicode=true
jdbc.default.username=
jdbc.default.password=
```

## PostgreSQL

```properties
jdbc.default.driverClassName=org.postgresql.Driver
jdbc.default.url=jdbc:postgresql://localhost:5432/lportal
jdbc.default.username=
jdbc.default.password=
```

See the [default portal properties](https://docs.liferay.com/dxp/portal/7.3-latest/propertiesdoc/portal.properties.html#JDBC) for more database templates.
