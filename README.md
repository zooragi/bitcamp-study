# bitcamp-study

## 1일차

- 아직 막힘 없이 이해가 잘 된다.

## 2일차

- 아직까지도 막힘없다

## 3일차

- 새로 알게 된 내용

  - 프로젝트 전체적인 파일 구조에 대해 알게 되었다( 자바 어플리케이션을 프로젝트로 관리)

  1. 첫번째 단계에는 git repo 가 project 관리 폴더 이다.
  2. 두번째 단계에는 소스파일과 bytecode가 들어있는 .class파일을 분리한다.
     <img src="https://github.com/zooragi/bitcamp-study/blob/main/ref-image/3day/img1.PNG" width="300" height="100">
  3. 세번째 단계에는 프로젝트 크기가 커짐에 따라 설정파일, 특정 개발에 사용되는 파일, 단위 테스트 관련 소스 및 설정 파일 등이 필요하게 되었다.  
     <img src="https://github.com/zooragi/bitcamp-study/blob/main/ref-image/3day/img2.PNG" width="200" height="250">
  4. 네번째 단계에는 세번째 단계에서는 프로젝트 하나만으로 구성되어있다면 네번째에서는 폴더 안에 여러 프로젝트들이 같이 있는 구조이다.

- javac, java 를 cmd 창에서 명령 하는 법을 알게되었다.
  - javac -d 실행파일위치 소스파일위치 --> 바이트코드로 변환
  - java -cp bin 폴더위치(패키지 명을 반드시 기입)
  - ex) java -cp bin/main com.eomcs.lang.ex01.EXam1

## 4일차

- Gradle 이란?
  - Maven을 대체 빌드 도구임
- Gradle 설치
  - 인터넷 ㄱㄱ
- Gradle 파일 구조
  - .gradle폴더 : Gradle이 사용하는 폴더 건드릴 일 없음
  - gradle 폴더 : Gradle 환경을 정리한 폴더
  - src 폴더 : 프로젝트 소스 폴더
    - main : 메인 폴더
    - test : 테스트 폴더
    - Maven이랑 구조는 비슷
  - build.gradle : Gradle 기본 설정 파일
  - gradlew, gradlew.bat : bat은 window용, 나머지는 macOS,Linux 용
  - setting.gradle : 프로젝트에 대한 설정 정보
- Gradle 사용법
  - `gradle init` --> 초기화시킴
  - `gradle wrapper` --> Gradle 설치 및 실행 파일 생성
- 'java' gradle 플러그인
  - compileJava
    - src/main/java 폴더에 있는 소스 파일을 모두 컴파일
    - build/classes/java/main 폴더에 .class 파일을 둔다.
  - compileTestJava
    - src/test/java 폴더에 있는 소스 파일을 모두 컴파일
    - build/classes/java/test 폴더에 .class 파일을 둔다.
  - processResources
    - src/main/resources 폴더에 있는 파일을 build/resources/main 폴더에 복사한다.
  - processTestResources
    - src/test/resources 폴더에 있는 파일을 build/resources/test 폴더에 복사한다.
  - clean
    - build 폴더를 삭제한다.
  - classes
    - compileJava와 processResources를 모두 수행
  - testClasses
    - classes + compileTestJava + processTestResources 수행
  - check
    - test + 단위 테스트 수행
  - javadoc
    - 소스 파일에서 javadoc 주석을 추출하여 HTML된 API 문서를 생성한다.
  - build
    - check + assemble(배포 파일 생성 작업) 수행
  - 'application' gradle 플러그인
    - run
      - 'java' 플러그인의 classes 작업을 먼저 실행한다.
      - 그런 후 application 설정에 지정한 클래스를 실행한다.
    - build
      - 이 플러그인을 장착한 상태에서 build 작업을 수행하면 고객에게 배포할 수 있는 파일을 build/distributions 폴더에 생성한다.
      - 자바 프로그램을 실행시킬 수 있는 스크립트 파일도 자동 생성된다.
  - 정리
    - 1. init 작업을 통해 프로젝트 폴더를 준비한다.
    - 2. build.script에 빌드 작업이 들어 있는 플러그인을 설정한다.
    - 3. 각 플러그인의 작업을 실행할 때 필요한 정보를 등록한다.
    - 4. 프로젝트에서 사용할 외부 라이브러리 파일을 등록한다.
    - 5. 필요한 작업을 실행하여 애플리케이션을 빌드한다.
