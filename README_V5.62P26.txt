45결 LEADER V5.62P26

반영 내용
1. 정보수정/저장 중 대기창에 회전 로딩 표시와 점 애니메이션 유지
2. 해당 순 선택 시 순장/리더 역할 순원이 리스트 맨 위에 오도록 정렬 유지
3. 부부매칭을 전체 순 공통으로 순원목록의 배우자명 컬럼 기준만 사용하도록 최종 고정
   - 세젤예순, 여일사랑순, 성엽사랑순 포함
   - 인접순서/주소/전화번호/자녀/수동하드코딩으로 배우자를 추측하지 않음
   - 한쪽 배우자명만 있어도 앱에서는 양방향 부부로 표시
4. 점검 기능 추가
   - ?action=debugSpouseColumnTeamAuditP26 : 세젤예순/여일사랑순/성엽사랑순 점검
   - ?action=debugSpouseColumnGlobalAuditP26 : 전체 순 점검
   - ?action=repairSpouseColumnReciprocalP26 : 한쪽 배우자명만 있을 때 반대쪽 배우자명 보강 및 옛 alias 컬럼 정리

적용 순서
1) Apps Script에서 기존 Code.gs 전체 삭제
2) 02_AppsScript_CodeGS_FULL_REPLACE/Code.gs_FULL_COPY.txt 전체 복사/붙여넣기
3) 저장 후 기존 웹앱 배포를 새 버전으로 업데이트
4) 웹앱 URL?action=debugStatus 에서 V5.62P26_GLOBAL_SPOUSE_COLUMN_CODEGS 확인
5) 필요 시 ?action=debugSpouseColumnTeamAuditP26 로 이상 순 점검
6) 필요 시 ?action=repairSpouseColumnReciprocalP26 실행
7) 01_GitHub_FULL_OVERWRITE 파일 전체를 GitHub 루트에 덮어쓰기
8) 앱 주소 뒤에 ?v=562p26 로 새로 열기

주의: index.html 단독 제공/미리보기 금지. ZIP 안에만 포함.
