VCS 란 무언인가? : (VCS, Version Control System)이란 파일 변화를 시간에 따라 기록 했>다가 나중에 특정 시점의 버전을 다시 불러올수있는 시스템을 의미함
VSC를 사용하면 선택한 파일을 이전 상태로 되돌릴수 있고 변경 사항을 비교하고, 변경한 >사람 및 변경시기를 추적할수있다.또한 파일을 잃어버리거나 잘못 고쳤을 떄도 쉽게 복구 >할수 있습니다. 또한 코딩을 많이 하다 보면 너무 많은 복사본이 있어서 파일 구분이 안될 때 , 잘어떠한 오류가 발생하여 원상태로 돌리고 싶거나 , 여러 명이서 동시에 작업을 할 >때, 여러 명의 동시 파일 수정을 하여 오류 충돌, 여러 명이서 작업을 할때, 누가 어떤 부>분을 어떻게 수정했는지 알 수가 없을때 이런 문제점을 고안해서 소프트 웨어 개발 및 유지
 보수 과정에서 발생하는 소스 코드, 문서 등의 생성 변경 이력, 삭제 이력 등을 관리하는>것을 말한다.

DVCS와 VCS의 차이점은 첫번째로 일단 DVCS는 분산형 버전 관리 시스템이라고하고 git이이>중에 포함이 됩니다. 프로젝트의 전체 파일이 참여자들의 각 컴퓨터와 서버에 분산되어 자>장됩니다. 먼저 로컬 저장소에 프로젝트파일들을 1차적으로 저장하고사용자의 명령에 따라 원격 저장소에도 저장가능. VCS는 중앙 집중형과 분산형으로 나누어져 있는데 중앙집중형VCS는 중앙 서버에서 파일을 관리하는 반면에 분산형은 로컬과 중앙 저장소 모두에서 파일을 관리합니다 따라서 DVCS는 오프라인 작업이 가능하고 중앙 서버에 의존하지 않아도 됩니다. 작업의 독립성입니다 DVCS는 각 개발자가 작업을 독립적으로 수행할 수 있습니다 각 개발자는 자신의 로컬 저장소에서 변경 사항을 커밋하고 브랜치를 만들어 실험적인 작업을 할수 있습니다. 이러한 브랜치는 중앙 서버와 동기화되지 않아도 되므로, 작업을 격리하고 안정성을 유지하는 데 도움이 됩니다.
네트워크의존성: VCS는 중앙 서버에 대한 연결이 필요합니다. 개발자가 중앙서버에 액세스 할수 없는 경우 작업을 계속할 수 없습니다. 그러나 DVCS는 로컬 저장소 를 사용하기 때문에 네트워크 연결이 불안정하거나 없어ㅓ도 작업을 걔속할 수있습니다.중앙 서버에 변경 사항을 푸시할 때에만 네트워크 연결이 필요합니다.
