Apache_server

## 1. MySql 깔기

## 2. Apache
1. Apachelounge.com 다운로드
2. Apach24 폴더 > conf 폴더 > httpd.conf 파일
   * 37라인 : Define SRVROOT "c:/APM/Apache24" (경로 수정)
     
   ![image](https://github.com/kdahun/Apache_server/assets/101082485/39304f09-9307-4855-9a5a-1d333583f1e2)

   * 60라인 : Listen 80(확인 하기)
3. Apach24 폴더 > conf 폴더 > bin 폴더를 cmd를 관리자 권한으로 열기
   * httpd.exe -k install : ApacheHTTPServer를 Windows 시스템에 설치하기 위한 명령어
       - httpd.exe : ApacheHTTPServer의 실행 파일
       - -k install : Apache 서버를 Windows 서비스로
   * httpd.exe -k start : ApacheHTTPServer를 시작하는 명령어
     - -k start : Apache 서버를 시작하는 옵션.
       
   ![image](https://github.com/kdahun/Apache_server/assets/101082485/9f1cbc24-f02c-4007-ab02-a3e30ac1ef65)

   * -k는 Apache 서버의 명령을 제어하는 데 사용된다.
   * Web 브라우저 주소에 http://localhost를 치고 It works!가 잘 뜨는 지 확인


## 3. php
1. php.ini-production을 php.ini으로 변경
   * 768라인 : 주석을 없애주고 php폴더 안에 있는 ext경로를 써준다.
   * 929라인 : curl ,ftp, mysqli, gettext, mbstring, openssl, pdo_sqlite의 주석을 해제
   * 979라인 : date.timezone = Asia/Seoul로 변경
2. Apache의 Httpd.conf파일 수정
   * 285 라인 쯤에 DirectoryIndex index.html > DirectoryIndex index.php index.html(index.php 추가)
     
     ![image](https://github.com/kdahun/Apache_server/assets/101082485/62f4fe79-a4b6-4778-bfdd-ba00eb652ab9)

     
   * 맨 마지막 라인에 다음을 추가
       - PHPIniDir "c:/APM/php8" (자신의 php8폴더의 경로를 넣어주면 된다.)
       - LoadModule php_module "c:/php8/php8apache2_4.dll"
       - AddType application/x-httpd-php .html .php
       - AddHandler application/x-httpd-php .php

     ![image](https://github.com/kdahun/Apache_server/assets/101082485/99f5ac97-7d76-45d7-9364-a396fc5f7661)

    
만약 VC_redist가 안깔려 있으면 안되니 깔자!

## 4. PHP 확인
Htdocs 폴더에 phpinfo.php파일 생성 > <?php phpinfo() ?> 코드 추가 > http://localhost/phpinfo.php해서 mysqli가 있는지 확인

![image](https://github.com/kdahun/Apache_server/assets/101082485/5ca8e9a6-f857-4189-ac66-5935ca1bf5af)


## 5. PHPmyadmin
1. phpmyadmin.net/donate에서 phpmyadmin을 다운 받기
2. 압축을 풀고 htdocs 폴더로 이동
3. http://localhost/phpmyadmin
   
![image](https://github.com/kdahun/Apache_server/assets/101082485/bc90013f-83a6-4c01-9a47-ae659a9a46bf)
