# Apache_server

## 1. MySql 깔기
---

## 2. Apache
1. Apachelounge.com 다운로드
2. Apach24 폴더 > conf 폴더 > httpd.conf 파일
   * 37라인 : Define SRVROOT "c:/APM/Apache24" (경로 수정)
   * 60라인 : Listen 80(확인 하기)
3. Apach24 폴더 > conf 폴더 > bin 폴더를 cmd를 관리자 권한으로 열기
   * httpd.exe -k install : ApacheHTTPServer를 Windows 시스템에 설치하기 위한 명령어
       - httpd.exe : ApacheHTTPServer의 실행 파일
       - -k install : Apache 서버를 Windows 서비스로
   * httpd.exe -k start : ApacheHTTPServer를 시작하는 명령어
     - -k start : Apache 서버를 시작하는 옵션.
   * -k는 Apache 서버의 명령을 제어하는 데 사용된다.
   * Web 브라우저 주소에 http://localhost를 치고 It works!가 잘 뜨는 지 확인

## 3. php
1.

