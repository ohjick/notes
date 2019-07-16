SpringBoot로 웹 애플리케이션을 만들고 이를 WAR로 배포할 때에는 (Aphache Tomcat 같은 Servlet Container에) SpringBootServletInitializer를 상속 하도록 가이드 하고 있다.

사라진 web.xml
5년 전 쯤으로 기억한다. 필자는 Apache Tomcat을 기반으로 Spring3 웹 애플리케이션을 개발 했었다.
당시 web.xml에 Spring 웹 애플리케이션 컨텍스트(WebApplicationContext) 구성하는 작업을 했다. 그중에 대표적인 것이 서블릿 애플리케이션 컨텍스트(DispatcherServlet)를 web.xml에 등록하는 것이었다.
결국 이러한 작업은 Spring을 Apache Tomcat 같은 Servlet Container에서 동작하도록 하기 위한 것이었다.
다시 현재로 돌아와서 필자는 Spring Boot 애플리케이션을 만들 때 Bootstrap 도구인 Spring Initializer를 즐겨 사용하는데 Spring Initializer에서 자동으로 생성해준 코드는 web.xml을 찾을 수 없었다. 

Servlet 3.0
Servlet 3.0 스펙에 새로운 기능 중 하나는 web.xml 없이 배포가 가능해진 것이다. 
그리고 Apache Tomcat의 경우 Servlet 3.0 스펙을 7.0 버전 부터 지원한다. 

Spring Framework와 Servlet 3.0
Spring Framework는 Servlet3.0 이상 환경에서 web.xml 대신하여 ServletContext를 프로그래밍적으로 다룰 수 있게 WebApplicationInitializer  인터페이스를 제공한다. 
아래 처럼 web.xml 역할을 WebApplicationInitializer 인터페이스를 구현하여 프로그래밍적으로 ServletContext에 Spring Ioc 컨테이너를 생성하여 추가할 수 있다.

SpringBootServletInitializer는 WebApplicationInitializer 인터페이스의 구현체 
SpringBootServletInitializer는 웹 애플리케이션 컨텍스트를 생성하여 ServletContext에 추가한다. 이 과정에서 웹 애플리케이션 컨텍스트로는 AnnotationConfigEmbeddedWebApplicationContext를 사용한다.

결론
SpringBootServletInitializer를 상속한다는 결국 Tomcat 같은 Servlet Container 환경에서 Spring Boot 애플리케이션 동작 가능하도록 웹 애플케이션 컨텍스트를 구성한다는 의미 이다.
