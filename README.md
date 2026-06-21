45결 LEADER V5.62P8 적용 안내

이번 P8은 P7 저장 오류(Unknown action: debugMemberSaveAudit)를 막고,
정보수정/신규등록이 반드시 순원목록 시트에만 저장되도록 다시 정리한 버전입니다.

중요 원칙
1. 정보수정/신규등록: 순원목록 기존 행 업데이트 또는 마지막 행 신규 추가
2. 순원수정/순원추가 시트: 생성/기록하지 않음
3. 삭제: 삭제순원 시트에 백업 후 순원목록에서 제거
4. 부부매칭: 순원목록의 배우자명 기준
5. 구글시트 ID 반영 완료: 1gs0aOTtlONuo9NwDU1XVuqwmRjCULs0sUKIw0lmCc2o

적용 순서
1. 01_GitHub_FULL_OVERWRITE 폴더 안의 모든 파일을 GitHub 저장소 루트에 덮어쓰기
2. Apps Script 편집기 열기
3. 기존 Code.gs 내용 전체 삭제
4. 02_AppsScript_CodeGS_FULL_REPLACE/Code.gs_FULL_COPY.txt 전체 복사 후 붙여넣기
5. 저장
6. 배포 > 배포 관리 > 기존 웹앱 배포 선택 > 연필 아이콘 > 버전: 새 버전 > 배포
7. 앱 주소 뒤에 ?v=562p8 붙여서 새로 열기

중요: 새 배포를 만들면 GitHub index.html의 기존 API_URL과 다른 주소가 되어 반영되지 않을 수 있습니다.
반드시 기존 웹앱 배포를 새 버전으로 업데이트해야 합니다.

확인용 주소
- Apps Script 웹앱 URL?action=debugStatus
  정상 기준: ok:true, version에 V5.62P8 포함

- Apps Script 웹앱 URL?action=debugMemberSaveAudit
  정상 기준: saveMemberRecordTargetSheet=순원목록, createsMemberAddSheet=false, createsMemberEditSheet=false

- Apps Script 웹앱 URL?action=debugSpouseReport
  부부매칭 점검용
