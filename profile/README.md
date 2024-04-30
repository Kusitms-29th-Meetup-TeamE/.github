## 📚 Stack 선정 및 사용 이유



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
