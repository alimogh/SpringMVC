# Stage 5

1 JSTL
---

Add the following dependency to *pom.xml*

```xml
       <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>jstl</artifactId>
            <version>1.2</version>
        </dependency>
```

Tab library:

```xml
<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%>
```

2 Bootstrap
---
Add the following dependencies to *pom.xml*

```xml
		<dependency>
			<groupId>org.webjars</groupId>
			<artifactId>bootstrap</artifactId>
			<version>3.3.6</version>
		</dependency>
		
		<dependency>
			<groupId>org.webjars</groupId>
			<artifactId>jquery</artifactId>
			<version>1.9.1</version>
		</dependency>
```

Add the following to the `<head>` tag in *list-todos.jsp*:

```xml
<link href="webjars/bootstrap/3.3.6/css/bootstrap.min.css"
	rel="stylesheet">
```

To use Bootstrap we need two more JS files. Add the following to *list-todos.jsp* just before the closing `</body>` tag:

```xml
	<script src="webjars/jquery/1.9.1/jquery.min.js"></script>
	<script src="webjars/bootstrap/3.3.6/js/bootstrap.min.js"></script>
```

For Spring to locate resources of webjars, add the following to *todo-servlet.xml*, just before the tag `<mvc:annotation-driven />`:

```xml
<mvc:resources mapping="/webjars/**" location="/webjars/" />
```

