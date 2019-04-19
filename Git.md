# Git 정리

Kernal (커널) 
= 하드웨어 응용 프로그램을 이어주는 운영체제의 핵심 시스템 소프트웨어.

Shell (커맨드 기반)
= 운영체제의 커널과 사용자를 이어주는 소프트웨어
= sh (Bourne Shell) 유닉스 쉘
= csh
= bash (Bourne Again Shell)
= zsh 
	
VSC (version control system)
== SCM (Source Code Management)

ls 		= 현재 파일 상태 (list select) 
ls -a 		= 숨겨진 파일
ls -l 		= 부가정보
ls -al 		= 숨겨진, 부가정보 모두 보기
.. 		= (전) 상위 폴더 이동
cd 		= 이동
	mkdir 		= Make directory (파일 생성)
	cd .. /.. 	= 제일 상단 이동
cd ~  		= 제일 상단 이동
	touch 		= 파일 안에서 html 생성 (파일)
	mv 		= Move (mv [파일명] [어디로])
	cp 		= Copy
	rm 		= Remove
	rm -r 		= 디렉토리 지우기 
	rm -rf ( .git )	= 강제로 지우기 (git 끊기)
	pwd 		= 위치 출력(절대)
vim(vi) 파일명 	= (mode/normal) vim 모드 열기 
dd 		= 잘라내기
p 		= 붙어 넣기
:wq 		= 저장
: q! 		= 저장 없이 나가기
cat 		= 인덱스 파일 출력
Git config --global user.name “user name”			= 깃 서버 연결 (최초만)
	Git config  --global user.email “user email address”	= 깃 서버 연결 (최초만)
	
	Git remote get-url origin					= 깃 링크 확인
	Git config --global –list					= 깃 서버 연결 확인
Git pull “new” master --allow-unrelated-histories 		= 불러오기

[Git Repository 생성 후 연결]
echo "# git_class_2" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/hyho942/git_class_2.git
git push -u origin master

git status 			= 연결된 깃 상태
git -rm				= 언 스테이징
vim(vi) “ 파일명”		= vim 모드 실행 (깃)
	
[GIT 올리기 순서]
git add . 			= 한번에 다수 파일 올리기
git add [index.html] 		= 깃 올리기
git commit			= 내용 서술
git push -u origin master


[협업 깃 받아서 작업 하기]
git remote add rmorigin [원본link] // 

git branch develop
git checkout develop
git fetch [rmorigin] develop (pull 역할, 중간 브랜치 필요)
	= Git pull origin develop (and ckeck index.html)
git add [파일명]
git commit
git push origin develop
git merge [rmorigin/develop]

[Git flow]
<pre>$ brew install git-flow-avh = 설치하기</pre>

Git flow strategy
-master -develop -feature -feature

git init
touch [file.name] 원본 만들기
git flow init 				
git flow feature start [file.name]
vi [file.name]
git branch
git add [file.name]
git commit -m “feat: Add [file.name]
		~ 내용”
git flow feature finish [file.name]
	[To master branch]
git flow release start v0.0.1…
git flow feature finish v0.0.1…
-develop-mode-
git flow release finish v0.0.1…

[Hexo를 이용하여 gitblog 글 작성하기]

1.	자신의 [github name].github.io로 Repository를 생성한다
2.	Hexo 설치
3.	Hexo init [blog]
4.	Cd [blog]
5.	Npm install
6.	Hexo new “post”
7.	Hexo generate [파일명]
8.	Hexo deploy
