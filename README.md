45결 LEADER V5.62P9 적용 안내

핵심 변경:
- GitHub index.html의 Apps Script 웹앱 URL을 아래 주소로 변경함.
  https://script.google.com/macros/s/AKfycbzp0wC45d_DfHjn4EngMiDO296gy6CaOHwem9swZhs18IW0aL9s52YWGylRxD5S6A-lLQ/exec
- Code.gs 상단 SPREADSHEET_ID에 아래 구글시트 ID 반영 완료.
  1gs0aOTtlONuo9NwDU1XVuqwmRjCULs0sUKIw0lmCc2o
- 기존 순원 정보수정/신규등록은 순원목록 시트에만 저장.
- 순원수정/순원추가 시트로 저장하지 않음.
- 순원삭제만 삭제순원 시트에 백업 후 순원목록에서 삭제.

적용 순서:
1. 01_GitHub_FULL_OVERWRITE 폴더 안 파일 전체를 GitHub 저장소 루트에 덮어쓰기.
2. Apps Script 편집기에서 기존 Code.gs 내용 전체 삭제.
3. 02_AppsScript_CodeGS_FULL_REPLACE/Code.gs_FULL_COPY.txt 전체 복사 후 붙여넣기.
4. 저장.
5. 배포 > 배포 관리 > 현재 웹앱 배포 선택 > 연필 아이콘 > 버전: 새 버전 > 배포.
6. 앱 주소 뒤에 ?v=562p9 붙여 새로 열기.

배포 후 확인:
- 웹앱 URL 뒤에 ?action=debugStatus 를 붙여 열었을 때 version에 V5.62P9가 보여야 함.
- 정보수정 후 구글시트 순원목록이 직접 업데이트되어야 함.
