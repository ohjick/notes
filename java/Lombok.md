#Lombok

### Lombok 이란?
롬복은 자바에서 Model(DTO, VO, Domain) Object를 만들 때, 멤버필드(Property)에 대한 Getter/Setter, ToString과 멤버필드에 주입하는 생성자를 만드는 코드 등 불필요하게 반복적으로 만드는 코드를 어노테이션을 통해 줄여주는 라이브러리, 프로젝트이다.
	
### License: MIT License
MIT 라이선스는 미국 매사추세츠 공과대학에서 해당 대학의 소프트웨어 공학도들을 돕기 위해 개발한 라이선스다. MIT 라이선스를 따르는 소프트웨어를 개조한 제품을 반드시 오픈 소스로 배포해야 한다는 규정이 없으며 GNU 일반 공중 라이선스의 엄격함을 피하려는 사용자들에게 인기가 있다. 이 라이선스를 따르는 대표적인 소프트웨어로 X 윈도 시스템이 있다.
	
### 다운로드 링크
http://projectlombok.org/download.html
	
### Maven 설정
```
<dependency>
    <groupid>org.projectlombok</gorupid>
    <artifactid>lombok</artifactid>
    <version>1.16.20</version>
 </dependency>
```

### Lombok 설치 & 사용하기
1. 콘솔창에서 'java-jar lombok.jar' 실행
2. 이클립스 재기동
---

3. 애노테이션 
@Data : All
@ToString, @EqualsAndHashCode, @Getter, @Setter
@NoArgsConstructor: 인자 없는 생성자
@RequiredArgsConstructor: 필수 인자만 있는 생성자
@AllArgsConstructor: 모든 인자를 가진 생성자
@Builder: 생성자 대신 빌더를 사용할 경우 빌더를 생성
**@Singular: 컬렉션 필드에 원소를 하나씩 추가**
@NotNull : 필드에 null 체크하고, null 일 경우 예외 발생
@Cleanup : IO 리소스 관리, close() 자동 호출
@Value : 불변 클래스 생성
@SneakyThrows : Exception 발생시 체크된 Throwable 로 랩핑 후 전달
@Synchronized : 메소드에서 동기화  Lock 설정
@Getter(lazy=true) : 동기화를 이용하여 최초 1회만 getter가 호출
@Log : 다중 Logging 라이브러리 사용 (@Log, @Slf4j, @CommonLog)
---


