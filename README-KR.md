# 월간 체크리스트 - GitHub Pages 배포 파일

## 포함 파일
- `index.html`: 체크리스트 본체
- `manifest.webmanifest`: 홈 화면 앱 정보
- `sw.js`: 기본 오프라인 캐시 및 PWA 지원
- `icons/`: 홈 화면 아이콘

## GitHub에 올리는 방법
1. GitHub에 로그인합니다.
2. 오른쪽 위 `+` → `New repository`를 선택합니다.
3. 저장소 이름을 예를 들어 `monthly-checklist`로 입력합니다.
4. `Public`을 선택하고 `Create repository`를 누릅니다.
5. 저장소 화면에서 `Add file` → `Upload files`를 선택합니다.
6. 이 폴더 안의 파일과 `icons` 폴더를 모두 업로드합니다. 폴더 구조를 그대로 유지하세요.
7. 아래쪽 `Commit changes`를 눌러 저장합니다.
8. 저장소의 `Settings` → `Pages`로 이동합니다.
9. `Build and deployment`에서 `Deploy from a branch`를 선택합니다.
10. Branch는 `main`, 폴더는 `/(root)`로 선택한 뒤 `Save`를 누릅니다.
11. 잠시 기다린 뒤 Pages 화면에 표시되는 사이트 주소로 접속합니다.

## 아이폰 홈 화면에 추가
1. 아이폰 Safari에서 GitHub Pages 주소를 엽니다.
2. 하단 공유 버튼을 누릅니다.
3. `홈 화면에 추가`를 선택합니다.
4. 이름을 확인하고 `추가`를 누릅니다.

## 데이터 저장 주의
체크리스트 데이터는 현재 사용 중인 브라우저의 로컬 저장 공간에 저장됩니다. 웹사이트 파일을 GitHub에 올리는 것만으로 입력 데이터가 GitHub에 올라가지는 않습니다. Safari의 웹사이트 데이터 삭제 시 기록이 사라질 수 있으므로 앱 안의 `백업` 기능으로 JSON 파일을 가끔 저장하세요.

## 업데이트
HTML 또는 PWA 파일을 수정한 뒤 GitHub 저장소에 같은 경로로 다시 업로드하고 변경 사항을 커밋하면 사이트가 업데이트됩니다. 서비스 워커 캐시를 새로 갱신해야 하는 변경은 `sw.js`의 `CACHE_NAME` 버전 숫자도 올려주세요.
