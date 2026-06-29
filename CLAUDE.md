# Liveklass 이메일 템플릿 프로젝트

## 프로젝트 개요
- liveklass 이메일 템플릿 개선 프로젝트
- 기존 템플릿 → 수정된 템플릿으로 교체
- 새 메일도 추가 예정

## 가이드 문서 (새 메일 작성 시 필수 참조)

1. **`_shared/html-patterns.md`** — HTML 스니펫, 스타일 규격, 제목 규칙, 패턴 조합 가이드
2. **`_shared/HEADER-FOOTER-GUIDE.md`** — 헤더/푸터 타입 선택 기준
3. **베이스 파일 4종** (루트 디렉토리에 위치):
   - `base_lk-logo_operator.html` — 운영자 메일 (라이브클래스 로고)
   - `base_lk-logo_operator_unsub.html` — 운영자 광고성 메일 (수신거부 포함)
   - `base_site-logo_learner.html` — 수강생 메일 (사이트 로고)
   - `base_no-header_common.html` — 보안 메일 (헤더 없음)
4. **노션 이메일 템플릿 가이드라인** (페이지 ID: `375c7a52db4f8199b4c8ca7ebcdc3550`)

## 작업 방식
1. `_shared/html-patterns.md`의 패턴 조합 가이드에서 베이스 파일 + 스니펫 선택
2. Vercel 사이트에서 수정 후 내용 확인 (아래 참고 자료 참조)
3. CSV에서 해당 템플릿의 버튼 링크 확인
4. HTML 작성 후 GitHub 레포에 푸시
5. Supabase에 내용 업데이트

## 참고 자료

### CSV 파일 (버튼 링크 참고)
- 위치: `~/Desktop/windy-260527.csv`
- 용도: **버튼 링크 참고용**
- 컬럼: 템플릿 ID, 템플릿 타입, 템플릿 이름, 템플릿 설명, 제목, 발송수, 내용(HTML), 마지막 발송일

### Vercel 미리보기 사이트 (새 메일 내용 기준)
- URL: https://liveklass-templates.vercel.app/
- 용도: **수정된 이메일 내용 기준**
- 중요: "수정 비교" 탭에서 **수정 후(after)** 내용만 사용

### Supabase
- 용도: 최종 메일 내용 저장소
- 작업 후 Supabase에 업데이트 필요

## GitHub 레포
- `windy-pureum/liveklass-templates`
