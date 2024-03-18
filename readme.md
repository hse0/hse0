1. VCS 란 무언인가? : (VCS, Version Control System)이란 파일 변화를 시간에 따라 기록 했>다가 나중에 특정 시점의 버전을 다시 불러올수있는 시스템을 의미함
VSC를 사용하면 선택한 파일을 이전 상태로 되돌릴수 있고 변경 사항을 비교하고, 변경한 >사람 및 변경시기를 추적할수있다.또한 파일을 잃어버리거나 잘못 고쳤을 떄도 쉽게 복구 >할수 있습니다. 또한 코딩을 많이 하다 보면 너무 많은 복사본이 있어서 파일 구분이 안될 때 , 잘어떠한 오류가 발생하여 원상태로 돌리고 싶거나 , 여러 명이서 동시에 작업을 할 >때, 여러 명의 동시 파일 수정을 하여 오류 충돌, 여러 명이서 작업을 할때, 누가 어떤 부>분을 어떻게 수정했는지 알 수가 없을때 이런 문제점을 고안해서 소프트 웨어 개발 및 유지
 보수 과정에서 발생하는 소스 코드, 문서 등의 생성 변경 이력, 삭제 이력 등을 관리하는>것을 말한다.

2. DVCS와 VCS의 차이점은 첫번째로 일단 DVCS는 분산형 버전 관리 시스템이라고하고 git이이>중에 포함이 됩니다. 프로젝트의 전체 파일이 참여자들의 각 컴퓨터와 서버에 분산되어 자>장됩니다. 먼저 로컬 저장소에 프로젝트파일들을 1차적으로 저장하고사용자의 명령에 따라 원격 저장소에도 저장가능. VCS는 중앙 집중형과 분산형으로 나누어져 있는데 중앙집중형VCS는 중앙 서버에서 파일을 관리하는 반면에 분산형은 로컬과 중앙 저장소 모두에서 파일을 관리합니다 따라서 DVCS는 오프라인 작업이 가능하고 중앙 서버에 의존하지 않아도 됩니다. 작업의 독립성입니다 DVCS는 각 개발자가 작업을 독립적으로 수행할 수 있습니다 각 개발자는 자신의 로컬 저장소에서 변경 사항을 커밋하고 브랜치를 만들어 실험적인 작업을 할수 있습니다. 이러한 브랜치는 중앙 서버와 동기화되지 않아도 되므로, 작업을 격리하고 안정성을 유지하는 데 도움이 됩니다.
네트워크의존성: VCS는 중앙 서버에 대한 연결이 필요합니다. 개발자가 중앙서버에 액세스 할수 없는 경우 작업을 계속할 수 없습니다. 그러나 DVCS는 로컬 저장소 를 사용하기 때문에 네트워크 연결이 불안정하거나 없어도 작업을 걔속할 수있습니다.중앙 서버에 변경 사항을 푸시할 때에만 네트워크 연결이 필요합니다.

![initial](https://github.com/hse0/hse0/assets/162945822/647b8627-0ee5-41be-823c-11d4c81cdb41) 처음에폴더를 만든 후 오른쪽 마우스 버튼을 누르면 이런창이 뜨는데 Open git Bash here을 누른다.

![initial](https://github.com/hse0/hse0/assets/162945822/f32db9f3-759f-43e0-9f51-815da00432aa) Open git bash here 을 누르면 최초 화면이 나온다.

![initial](https://github.com/hse0/hse0/assets/162945822/81c9fc57-cf71-4d54-8534-ac806fed17c3) git init 이라는 명령어를 실행하면 현재 디렉토리를 기준으로 Git 저장소가 생성 됩니다 Reinitialized existing Git repository in~ 이라고 뜨면 git remote -v를 입력하여, 원격remote 주소가 새로 생성한 remote repositoy 주소인지 확인을 한다. 다를 경우에 git remote rm origin 으로 삭제하고, 다시 새로 추가하면 문제가 해결된다.

![initial](https://github.com/hse0/hse0/assets/162945822/feb8d789-974a-4e88-b24e-fe45c75a1a46) git config 명령을 사용하여Git 커밋과 연결된 이름을 변경할수 있습니다. git config --global user.name hs0 ,git config --global user.email hacter0304@naver.com

![initial](https://github.com/hse0/hse0/assets/162945822/a1947ac2-f352-437f-a9d4-f81874418d3a)
git status 명령어는 Git 저장소의 상태를 출력하는 명령어입니다. Branch에 이름은 main입니다.
modified readme.md 파일의 출력이 가능해졌습니다.

![initial](https://github.com/hse0/hse0/assets/162945822/6eb3276b-1438-4c82-b171-2069c82e9760)
vim readme.md 파일을 호출합니다.

![initial](https://github.com/hse0/hse0/assets/162945822/77f4d700-307f-4233-9a91-a352eeb03b2f)
git add . 현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때는 .을 인자로 넘깁니다.

![initial](https://github.com/hse0/hse0/assets/162945822/aa0e1fa7-eb74-4a5d-a12f-56c27e816b5b)
hs0 파일안에 텍스트를 만들고 git status 로 호출을 하게 되면 Hw.txt 라는 텍스트를 확인 할수 있습니다.

![initial](https://github.com/hse0/hse0/assets/162945822/69726000-2309-41be-8b42-e76282b7ba4a)
get remote add origin 나의 git Hub주소를 넣으면 됩니다. 원격저장소에 추가한다고 생각하시면 됩니다.

![initial](https://github.com/hse0/hse0/assets/162945822/e563a696-110a-44f8-94ad-34e50988f252)
원격저장소와 연결된 계정, 사용자를 변경하고자 할때 remote origin 브랜치그룹을 삭제해야할 때가 있습니다. 하지만 이미 설정 된 remote origin 이 있어 아래와 같은 문구가 뜨는 경우가 생깁니다
fatal : remote origin already exists 따라서 이 메세지가 뜨면 git remote rm origin 코드를 사용하여 기존의 remote orgin을 삭제를 할수 있습니다.

![initial](https://github.com/hse0/hse0/assets/162945822/0af4baaa-6992-4c25-b7b0-3f1739ae6a4e)
git remote rm origin 코드를 사용한 이후에는 똑같이 git remote add origin 코드를 사용하여 나의 원격 저장소에 추가한다고 생각하시면 됩니다.

![initial](https://github.com/hse0/hse0/assets/162945822/20c5e91e-97cf-4cd9-9668-4a3446fce907)
git commit -m "Home Work" 라는 -m이 뜻하는 것은 어떤 커밋 메세지가 뒤 따른다는 의미입니다.

![initial](https://github.com/hse0/hse0/assets/162945822/3acd0b08-5aaf-4317-9f16-2c43f7836093)
git push 를 사용하여 로컬 리포지토리에서 기록한 내용을 원격 리포지토리로 옮기는 작업니다.
git 로컬 브랜치를 원격저장소로 푸시한다고 생각하시면 됩니다.

![initial](https://github.com/hse0/hse0/assets/162945822/aa0e1fa7-eb74-4a5d-a12f-56c27e816b5b)
이 명령어는 origin이라는 리모트 레포지토리에 main이라는 브랜치를 생성하고 로컬 레포지토리의 main 브랜치의 내용을 리모트 레포지토리의 main에 보내라는 뜻입니다. 그 이후에 아래에 명령어들은 git hup 나의 레포지토리의 저장이 완료 되었다는 얘기입니다.
