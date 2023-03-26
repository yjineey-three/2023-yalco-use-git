# 2023.03[git]
#yalco #git #github #사용법

`참조사이트`
https://www.youtube.com/watch?v=1I3hMwQU6GU
https://www.yalco.kr/lectures/git-github/

`yalco 인강 정리`
* git commit -am '커밋내용'

<!---------------------------------------------------------------------->

* merge 와 fastforward
  1. git merge (브랜치명)
  2. git merge --no-ff (병합할 브랜치명) > ff(Fast forwoard 약자)

* merge 와 rebase 차이
  merge는 이전 branch history가 유지된다 (main으로 이동)
  rebase는 merge시 이전 branch history가 삭제 된다 (rebase 브랜치로 이동)

* git clean
  관리하지 않은 파일 삭제

<!---------------------------------------------------------------------->

* 로컬에서 커밋 reset 위치로 가고 싶을 때, 내가 선택한거 전으로 이동

  git reset --hard (커밋)

* git reset --hard HEAD-2 (두단계 뒤로 reset)
  reset도 HEAD 기준으로 편하게 가능

* 원격저장소에서 현재 reset 위치로 가고 싶을 때 (원격강제 push)
  git push -f origin main

* git reflog
  reset 되돌리기

<!---------------------------------------------------------------------->

* 브랜치 확인
  git branch (로컬)
  git brnach -a (로컬 + 원격)

* 원격 브랜치 삭제
  git push (origin) --delete (브랜치명)

<!---------------------------------------------------------------------->

* 컨벤션
  feat : 새로운 기능 추가
  fix : 버그 수정
  docs : 문서 수정
  style : 공백, 세미콜론 등 스타일 수정
  refactor : 코드 리팩토링
  perf : 성능 개선
  test : 테스트 추가
  chore : 빌드과정, 보조기능 수정

* git stash 하기
  작업중에 추가 작업 요청이 들어오면 (다른공간에 현재 작업물을 치워놓는)
  > 작업중... 이라는 commit 은 별로 좋지 않음
  > 한개의 작업끼리 모아서 commit 하는게 좋으므로

  git stash / git stash pop

* commit 수정하기 (push 단계전에)
  git commit --ament
  
<!---------------------------------------------------------------------->

* GIT HEAD
  git checkout HEAD^ (뒤로 한칸)
  git checkout HEAD^^^ (뒤로 세칸)

  git checkout HEAD~ (뒤로 한칸)
  git checkout HEAD~~~ (뒤로 세칸)  

  git checkout HEAD- (ctrl + z)

* git help (명령어)
  git help >> 간단한 명령어

  브라우저에 해당 사이트 열림
  (ex) git help clone

* git config(설정)
  git config --global (전역, 로컬 전체)
  git config --global user.name

  git config user.name (global을 빼면 해당 프로젝트만)
  (ex) git config user.name hello

  git config --global --list (전역으로 설정된 것들)
  git config --global

  로컬과 원격을 똑같이 push 해두겠다
  git config --global push.default current

* edit 모드로 사용하기
  git config --global -e  (추가 작성)
  [core]
	editor = code --wait

  사용하기 싫으면 해당부분 삭제

<!---------------------------------------------------------------------->
* tag
  list확인: git tag

  annotatied
  git tag -a (tag명)
    
  원격저장소에 tag 달기
  git push origin (tag명)
  git push --delete origin (태그명)

  로컬의 모든 태그 원격에 올리기
  git push --tags