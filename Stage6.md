# Stage 6

Form tags and Hibernate Validator:
---

Add the following at the top of *todo.jsp*:

```xml
<%@taglib uri="http://www.springframework.org/tags/form" prefix="form"%>
```

Add Hibernate Validator to *pom.xml*:

```xml
		<dependency>
    			<groupId>org.hibernate</groupId>
    			<artifactId>hibernate-validator</artifactId>
    			<version>5.0.2.Final</version>
 		</dependency>
```

Format Tag Library
---

Add the following to *list-todos.jsp*:

```xml
<%@ taglib uri="http://java.sun.com/jsp/jstl/fmt" prefix="fmt"%>
```

Navigation bar and JSP fragments
---

Add the following to the start of the `<body>` tag in *list-todos.jsp*:

```xml
	<nav role="navigation" class="navbar navbar-default">
		<a href="http://www.ranyalbegwein.com" class="navbar-brand">My Todos</a>
	
		<div>
			<ul class="nav navbar-nav">
				<li class="active"><a href="/login">Home</a></li>
				<li><a href="/list-todos">Todos</a></li>
			</ul>
		</div>
	</nav>
```
