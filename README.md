# 2022.07 [css]
#html #css #git #github #사용법 #yalco

`참조사이트`
https://www.youtube.com/watch?v=1I3hMwQU6GU
https://www.yalco.kr/lectures/git-github/

`마크다운 문법`
https://www.markdownguide.org/cheat-sheet/
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

`yalco 인강 정리`
* git commit -am '커밋내용'

* 로컬에서 커밋 reset 위치로 가고 싶을 때, 내가 선택한거 전으로 이동
  git reset --hard (커밋)

* 원격저장소에서 현재 reset 위치로 가고 싶을 때 (원격강제 push)
  git push -f origin main

* merge 와 rebase 차이
  merge는 이전 branch history가 유지된다 (main으로 이동)
  rebase는 merge시 이전 branch history가 삭제 된다 (rebase 브랜치로 이동)

* 브랜치 확인
  git branch (로컬)
  git brnach -a (로컬 + 원격)

* 원격 브랜치 삭제
  git push (origin) --delete (브랜치명)

* GIT HEAD
  git checkout HEAD^ (뒤로 한칸)
  git checkout HEAD^^^ (뒤로 세칸)

  git checkout HEAD~ (뒤로 한칸)
  git checkout HEAD~~~ (뒤로 세칸)  

  git checkout HEAD- (ctrl + z)

* git reset --hard HEAD-2 (두단계 뒤로 reset)
  reset도 HEAD 기준으로 편하게 가능

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

  