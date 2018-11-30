# SynoEPG

시놀로지 비디오스테이션 DTV를 위한 EPG
https://www.else.co.nz/words/real-epg-for-synologys-video-station/  페이지의 자료를 참조하였다.

# 시놀로지 DTV 구조
비디오 스테이션의 폴더는 아래와 같다.  
/var/packages/VideoStation  
각종 설정 파일은 etc 폴더에 있다.  
참고할 파일은 /etc/channels/ 의 0channel.conf 파일이다. 튜너의 수에 따라서 같은 이름으로 번호만 달리한다.  
EPG 파일은 /etc/EPGS 폴더 밑에 튜너수만큼 0EPG 라는 폴더안에 존재하며 파일명은 0channel.conf 파일의 frequency, service_id 를 이용하며 만들어진다.  
EPG 파일은 json 구조를 가지며 duration, event_id, event_name, start_time, text_name의 항목을 가지고 있다.  

duration은 프로그램 방영시간으로 단위는 초, event_name은 프로그램 제목, start_time은 방영시작시간으로 유닉스타임, text_name은 프로그램 내용이다  
