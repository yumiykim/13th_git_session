# GIT 세션 요약

**GIT** : 오픈 소스 분산 버전 제어 시스템
GIT은 로컬 / GITHUB는 온라인 공유 플랫폼

**GIT 개인 레포지토리**
1. 폴더 생성 후, VScode 터미널에서 Git bash 클릭
2. git config --global user.name 본인 깃허브 아이디 (*작성자 정보 저장*)
3. git config --global user.email 본인 깃허브 이메일 (*작성자 정보 저장*)
4. git init : 해당 폴더를 저장소로 변환한다
5. git remote add origin 레포지토리 주소 : 원격 저장소 연결
6. git remote -v : 원격 저장소 연결 확인
7. git branch -M main : 기본 브랜치 이름 master-> main
8. git pull origin main : 연결한 레포지토리의 main 브랜치의 최신 사항을 불러오기
9. git add . : 현재 디렉토리( . ) 아래의 모든 변경 파일을 Git이 추적
10. git commit -m “커밋 메시지" : 추적한 파일들을 실제 Git 이력에 기록
11. git push origin main : 컴퓨터의 커밋 내용을 원격 저장소 (origin의 main 브랜치)에 올린다


**GITHUB 협업**
*프로젝트 초기 세팅*
1.Gihub 중앙 레포지토리 생성
2.해당 중앙 레포지토리를 fork하여 개인 레포지토리 생성
3.폴더 생성 후, 중앙 레포지토리와 개인 레포지토리 연결

*변경사항 업데이트*
1.브랜치 생성
2.폴더 수정사항 개인 레포지토리에 반영하기
(git add . / git commit -m “” / git push origin main)
3. 개인 레포지토리에서 중앙 레포지토리로 Pull Request
4. 중앙 레포지토리에서 코드 확인 후 Merge
5. 로컬 폴더 main 브랜치에 수정사항 반영

*절대적인 협업 방식은 없음.

*브랜치란*
작업을 나누어 하기 위해 기존 코드 (main)에서 갈라져 나온 독립적인 작업 공간

-관련 명령어 모음
git branch : branch 목록 확인
git branch 새 브랜치 이름 : 새 브랜치 생성
git switch 브랜치 이름 : 브랜치 이동
git branch -d 브랜치 이름 : 해당 브랜치 삭제

*push 이전에는 꼭 pull을 할 것*
*main 최신화 후에는 사용한 브랜치를 삭제할 것*

**DJANGO**
<알아두면 좋은 터미널 명령어모음>
pwd : 현재 작업 중인 디렉토리 경로 출력
cd : 디렉토리 이동
ls : 현재 디렉토리 안의 파일 및 폴더 목록 출력
rm : 파일 또는 폴더 삭제
clear : 터미널 화면을 깨끗하게 정리
mkdir : 새 폴더 (디렉토리) 생성 (Make Directory)
touch : 새 파일 생성 또는 기존 파일 시간 갱신
exit : 터미널 종료

PROJECT : 웹사이트 전체
APP : 게시판, 로그인 기능의 집합 단위 (모델, 뷰, URL 등)

<살펴보기>
_ _init__.py : python package로 인식되도록 하는 빈 파일
asgi.py : web server, framework, application을 연결해주는 파일
settings.py : 프로젝트에 관련한 다양한 설정을 하는 파일 (앱 등록, 타임존 등록, static url 설정 등)
url.py : 웹 서버에서 들어온 신호를 받아 특정한 view를 보내주는 파일
wsgi.py : 웹 서버와 장고를 연결해주는 파일
manage.py : 장고와 상호작용하며 다양한 기능을 제공하는 파일 (형식: python manage.py 명령어)
admin.py : 관리자 사이트와 관련된 설정을 담고 있는 파일
apps.py : 해당 앱의 설정 정보를 담고 있는 파일
models.py : 테이블을 정의하는 파일로 모델을 정의
tests.py : 테스트 코드를 작성하는 파일
views.py : 가장 많이 사용하는 파일로 함수 형태로 로직을 작성하는 파일

<manage.py 명령어 모음>
runserver : 서버 켜기
startapp [앱 이름] : app 만들기
makemigrations / migrate : db 초기화 및 변경사항 반영
createsuperuser - 관리자 계정 생성