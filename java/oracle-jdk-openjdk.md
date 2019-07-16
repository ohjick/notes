# Oracle JDK와 OpenJDK

* Java 애플리케이션을 실행하기 위해서는 JVM이 필여하고 컴파일하기 위해서는 JDK가 필요하다. 일반적으로 JDK를 설치하면 JVM\(Hotspot이라고도 표현, Java 기술의 핵심\)도 함께 설치 된다.
* JDK는 2개의 버전으로 나뉜다. 하나는 폐쇄적인 상업 코드 기반의 Oracle JDK이고 하나는 오픈 소스 기반의 Open JDK이다. 
* 둘 간의 큰 차이라면 Oracle JDK는 OpenJDK에는 없는 재산권이 걸린 플러그인을 제공한다. 해당 플러그인은 Oracle이 재산권을 보유하고 있다. \(보다 정확히 설명하면 Oracle이 인수하여 없어진 Sun Microsystems 시절의 유산이다.\) 
* Oracle JKD에 존재하고 OpenJDK에 없는 대표적인 기능으로 글꼴 라이브러리와 Java Web Start가 있다. 사용자의 웹브라우저에서 자바 애플릿을 실행하려면 필요한 기능이다. 서버 애플리케이션 개발에는 쓰이지 않는 기능들이다.
* 제공되는 기능적 차이 외에 Java6 시대에는 분명히 OpenJDK가 Oracle JDK보다 성능이나 안정성이 크게 떨어졌다. 하지만 오늘날에는 Oracle JDK만이 제공하는 일부 라이브러리를 제외하고는 차이가 없다.

OpenJDK는 운영 환경에 부적합한가?

* 결론부터 이야기하면 TCK 인증을 받은 OpenJDK기반의 빌드 버전을 사용하면 운영 환경에 아무런 문제가 없다.
* Java SE 7 부터 모든 JDK는 OpenJDK 레퍼런스 소스 코드를 기반으로 제작된다. \(Java SE 6 버전의 OpenJDK는 백포트 방식으로 구현되어 성능 저하 이슈가 존재한다.\) OpenJDK는 자바 스펙을 명시한 JSR336, JSR337을 빠짐없이 완전히 구현한 구현체이다.
* OpenJDK의 운영 주체는 오라클이다. 오라클 또한 OpenJDK를 기반으로 자사의 부가적인 기능을 추가한 Oracle JDK를 제작하여 배포한다. 
* 오라클이 아닌 서드파티 업체가 OpenJDK를 기반으로 공인된 JDK를 제작하여 배포하려면 오라클의 유료 라이센스인 OCTLA에 가입해야 한다. 현재 전세게에 19개 업체가 가입되어 있다. 이 업체들이 OpenJDK 기반의 자체 빌드를 배포하려면 오라클의 엄격한 TCK 인증을 통과해야 한다. 수만가지의 테스트를 단 하나라도 통과하지 못하면 인증되지 않는다.
* OpenJDK를 멀티 플래폼 바이너리로 빌드하여 배포하는 대표적인 업체로는 Azul Systems가 있다. 개발 환경과 운영 환경 모두 Oracle JDK의 대안으로 좋은 평가를 받고 있다. 
