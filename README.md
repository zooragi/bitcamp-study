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
     <img src="https://github.com/zooragi/bitcamp-study/blob/main/ref-image/3day/img1.PNG" width="200" height="100">
  3. 세번째 단계에는 프로젝트 크기가 커짐에 따라 설정파일, 특정 개발에 사용되는 파일, 단위 테스트 관련 소스 및 설정 파일 등이 필요하게 되었다.
     <img src="https://github.com/zooragi/bitcamp-study/blob/main/ref-image/3day/img2.PNG" width="100" height="150">
  4. 네번째 단계에는 세번째 단계에서는 프로젝트 하나만으로 구성되어있다면 네번째에서는 폴더 안에 여러 프로젝트들이 같이 있는 구조이다.

- javac, java 를 cmd 창에서 명령 하는 법을 알게되었다.
  - javac -d 실행파일위치 소스파일위치 --> 바이트코드로 변환
  - java -cp bin 폴더위치(패키지 명을 반드시 기입)
  - ex) java -cp bin/main com.eomcs.lang.ex01.EXam1
