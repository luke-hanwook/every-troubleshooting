# github-issue-management-practice
## github issue 기반 프로젝트 관리

### 1. 이슈 발급

모든 것이 이슈이다. (전용 템플릿을 만들어 사용하면 편리하다..)

등록된 이슈에 3개의 설정을 한다.

- Assignees: 해당 작업의 담당자
- Labels: 해당 작업의 성격
- Milestone: 해당 작업이 속한 파트 (이거 잘 모르겠음..)

***로컬 리파지토리에 생성된 이슈기반 브랜치를 생성하는 것이 핵심이다.***

이슈 번호 기반으로 브랜치를 생성하면 브랜치 네이밍을 통해 해당 작업의 의도를 명확하게 할 수 있다.

VS Code에서는 **GitHub Pull Requests and Issues** 플러그인을 사용하여 위 작업을 자동화 할 수 있다. (JetBrains에서는 Task 연동기능)

### 2. 풀 리퀘스트

브랜치를 생성했으면 풀 리퀘스트를 통해 해당 이슈와 연동한다.

VS Code에서는 **GitHub Pull Requests and Issues** 플러그인의 Create Pull Request 기능을 사용할 수 있다. (JetBrains에서 Create Pull Reqeust 기능)

첫 변경 작업을 커밋 한뒤 풀 리퀘스트를 생성하고 * resolved: #이슈번호 를 적어주면 자동으로 연동된다.

resolved: #이슈번호 master branch에 반영되면 자동으로 Close issue된다.  원치 않을 시 issue: #이슈번호로 적어준다.

풀 리퀘스트에도 이슈넘버가 생성된다. 풀 리퀘스트는 제목을 브랜치 명으로 하여 무슨 이슈에 의한 풀 리퀘스트인지를 명확히 하는 것이 좋다. (추적 용이)

### 3. 코드리뷰(optional)

코드리뷰가 필요하다면 풀리퀘스트의 리뷰어를 선정한다.

리뷰어는 요청받은 풀 리퀘스트로 가서 Add your review 버튼을 선택한다.

- Approve: 승인
- Comment: 간단한 피드백
- Request changes: 반드시 코드 수정을 요구

해당 리뷰는 풀 리퀘스트에 남아 계속해서 추적할 수 있다. 

### 4. 머지 풀 리퀘스트

풀 리퀘스트 하단 머지 풀 리퀘스트를 선택하여 해당 작업을 마스터에 반영한다.

반영 후 필요 없는 브랜치는 삭제한다.

위에서 작성한 resolved 키워드로 인해 연동된 이슈는 자동으로 close 처리된다.
