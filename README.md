[mustache.js](http://mustache.github.com/mustache.5.html) view for [spring3](http://static.springsource.org/spring/docs/3.0.x/spring-framework-reference/html/mvc.html)
---------------------------

note: currently building against a non-released version of jmustache: https://github.com/sps/jmustache

maven dependency
-----------------

    <dependency>
        <groupId>com.github.sps.mustache</groupId>
        <artifactId>mustache-spring-view</artifactId>
        <version>1.0-SNAPSHOT</version>
    </dependency>


spring config
-------------

    <bean id="viewResolver" class="org.springframework.web.servlet.view.mustache.MustacheViewResolver">
        <property name="cache" value="${TEMPLATE_CACHE_ENABLED}" />
        <property name="prefix" value="" />
        <property name="suffix" value=".html" />
        <property name="templateLoader">
            <bean class="org.springframework.web.servlet.view.mustache.TemplateLoader" />
        </property>
    </bean>
