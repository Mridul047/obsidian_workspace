
## Why use Spring Boot ?
	* Dep. resolution
	* Avoid additional config. req. in spring framework
	* Provides embedded Servlet container (Tomcat/Netty/Jetty)
	* Provides Auto config. 
	* Provides prod. ready features like metrics, health checks

## Popular Modules in Spring Boot : 
	* Spring boot starter Web
	* Spring boot starter Data JPA / Cassandra
	* Spring boot starter Security
	* Spring boot starter for Spring Cloud

## Annotations in Spring Boot :
	* @SpringBootApplication = 
	    @EnableAutoConfiguration + @ComponentScan + @SpringBootConfiguration
	* This annotation can be replaced with following combination
	    @EnableAutoConfiguration , @ComponentScan & 
	    @Import used for importing @Configuation class
	* @ConditionalOnClass: If supplied class present in classpath then load the config.

## CommandLineRunner :
	Functional Interface provided to run BL after application context is up & running.

## @PostConstruct vs CommandLineRunner :
	Both can be used to run BL after application cxt is up & running.
	Order of Execution of code: PostConstruct then CommandLineRunner

## Stereotype Annotations in Spring :
	Used to define the role of a class in the application
	* Parent for all annotations @Compoent
	* Base annotation @Service
	* Base annotation @RestController = @Controller + @ResponseBody
	* Base annotation @Repository

## Properties file vs YAML file :
	Both can be used for configuring app. properties.
	Order of precedence: application.properties then application.yml
	Check <I>PropertiesSourceLoader

## Load external properties file :
	We can use spring.config.import=file:/FILE_PATH in properties file to load external config.


## Map Class to properties from .properties or .yml :
	We can use Class with following annotations on class: 
	@ConfigurationProperties(prefix = "property.prefix") 
	@ConfigurationPropertiesScan

## BeanPostProcessor in Spring :