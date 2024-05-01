## 📚 Stack 선정 및 사용 이유

### Server

Spring Boot
- 다양한 라이브러리와 설정을 제공하여 빠르고 쉽게 스프링 기반 애플리케이션을 개발할 수 있게 해주는 도구입니다.
- 특정 환경이나 서버, 기술에 종속되지 않으며 유연한 애플리케이션을 개발할 수 있습니다.
  
Spring Security 
- 사용자 인증, 권한 관리, 보안 설정 등을 편리하게 처리할 수 있어 안전한 애플리케이션을 개발할 수 있습니다.
  
Spring Data JPA
- 데이터 액세스 계층을 쉽게 구현할 수 있도록 도와주는 스프링 프레임워크의 모듈입니다.
- JPA를 기반으로 데이터베이스 액세스를 추상화하고 개발자가 데이터베이스와 상호작용할 때 생기는 반복적인 작업을 줄여줍니다.
  
QueryDSL
- 타입 안전한 쿼리 작성을 위한 라이브러리로, 동적 쿼리 작성이 용이하고 가독성이 뛰어나므로 복잡한 쿼리를 다룰 때 유용합니다.
  
MySQL
- 오픈 소스 관계형 데이터베이스 관리 시스템(RDBMS)으로, 신뢰성 높은 데이터 저장 및 관리를 위해 선정하였습니다.
- 대용량 데이터베이스와 트랜잭션 처리에 효율적입니다.
- 다양한 운영체제에서 실행될 수 있고, 빠른 응답 속도와 안정성을 제공합니다.

GitHub Actions
- GitHub에서 제공하는 자동화 서비스로, 코드 저장소에 변경 사항이 발생할 때 자동으로 테스트, 빌드, 배포 등의 작업을 수행할 수 있습니다.
- CI/CD 파이프라인을 구축을 위하여 선정하였습니다.
  
Docker
- 컨테이너 기반의 가상화 플랫폼으로, 애플리케이션을 환경과 함께 패키징하여 빠르고 일관된 배포를 가능케 합니다.
- 개발 환경과 운영 환경의 일관성을 유지하고, 확장성과 이식성을 높일 수 있습니다.
- Gitgub actions를 통한 CI/CD 파이프라인 구축을 위하여 선정하였습니다.
  
Nginx
- 경량의 웹 서버 및 리버스 프록시 서버로, HTTP 및 HTTPS 요청을 처리하고 로드 밸런싱을 수행할 수 있습니다.
- Docker 내에서 Nginx를 사용하여 애플리케이션의 트래픽을 관리하고 보안을 강화할 수 있습니다.
  
MongoDB:
- NoSQL 데이터베이스로, 유연한 데이터 모델링과 확장성을 제공합니다. 
- 채팅 서비스를 위하여 선정하였습니다.

## 📝 Naming Rules

- 폴더명 - `LowerCase`
- 파일명 - `PascalCase`
- 타입 메소드 파라미터 변수 등 - `PascalCase`
- 상수 - `UpperCase && snake_case`

## 🔨 Convention

### 💡Type

| commit명 | commit 규칙 |
| --- | --- |
| 📍 Feat | Add a new feature |
| 🔨 Fix | Modify production, UI,UX code |
| 🎨 Style | Add or update code format (not updation production, UI,UX code) |
| 📝 Docs | Add or update documentation |
| ✅ Test | Code change related with tests cases |
| 🤖 Refactor | Code change that neither fixes a bug nor adds a feature |
| 🚚 Chore | Changes to the build process or auxiliary tools\n\t\tand libraries such as documentation generation |
| 🔧 Rename | move file or rename folder names |
| ✂️ Remove | Remove files |

### 💡Commit Message Rule

- `cz-customizable` 사용
    - 일정한 커밋 메시지 관리를 위해 cz-customizable 활용
    - cz-config.js
        
        ```jsx
        module.exports = {
          types: [
            { value: '📍 Feat', name: '📍 Feat:\tAdd a new feature' },
            { value: '🔨 Fix', name: '🔨 Fix:\tModify production, UI,UX code' },
            { value: '📝 Docs', name: '📝 Docs:\tAdd or update documentation' },
            {
              value: '🎨 Style',
              name: '🎨 Style:\tAdd or update code format (not updation production, UI,UX code)',
            },
            { value: '🤖 Refactor', name: '🤖 Refactor:\tCode change that neither fixes a bug nor adds a feature' },
            {
              value: '✅ Test',
              name: '✅ Test:\tCode change related with tests cases',
            },
            {
              value: '🚚 Chore',
              name: '🚚 Chore:\tChanges to the build process or auxiliary tools\n\t\tand libraries such as documentation generation',
            },
        		{
              value: '✂️ Remove',
              name: '✂️ Remove:\tRemove files ',
            },
        		{
              value: '🔧 Rename',
              name: '🔧 Rename:\tmove file or rename folder names',
            },
          ],
          allowCustomScopes: false,
          allowBreakingChanges: ['feat', 'fix'],
          skipQuestions: ['body'],
          subjectLimit: 100,
        }
        ```
        

### 💡Branch Rule

| Header | 기능 |
| --- | --- |
| main | 최종 배포할 서비스 내용의 브랜치 |
| develop | 주요 개발 브랜치, 이 브랜치를 기준으로 각자 작업한 기능을 merge |
| feature | 기능 개발 브랜치, 기능 개발이 완료 시 develop 브랜치에 merge |
| fix | 기능 수정 브랜치, 이미 develop 브랜치에 merge된 기능을 수정하고 완료 시 develop 브랜치에 merge |
| hotfix | master 브랜치로 배포 후에 버그가 생겼을 때 긴급 수정하는 브랜치 |
- **[Header]/[이슈번호]/[내용]**
    - ex) feature/#25/google-login

### 💡Issue & PR Rule

- **Issue Template**

```markdown
## ✨이슈 설명

## 🔥투두리스트
- [ ]
- [ ]

## 🔖기타 사항

```

- **PR Template**
