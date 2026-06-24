# Liveklass 이메일 템플릿 프로젝트

## 프로젝트 개요
- liveklass 이메일 템플릿 개선 프로젝트
- 기존 템플릿 → 수정된 템플릿으로 교체
- 새 메일도 추가 예정

## 참고 자료

### 1. CSV 파일 (기존 메일 데이터)
- 위치: `~/Desktop/windy-260527.csv`
- 용도: **버튼 링크 참고용**
- 컬럼: 템플릿 ID, 템플릿 타입, 템플릿 이름, 템플릿 설명, 제목, 발송수, 내용(HTML), 마지막 발송일

### 2. Vercel 미리보기 사이트 (새 메일 내용 기준)
- URL: https://liveklass-templates.vercel.app/
- 용도: **수정된 이메일 내용 기준**
- 중요: "수정 비교" 탭에서 **수정 후(after)** 내용만 사용

### 3. Supabase
- 용도: 최종 메일 내용 저장소
- 작업 후 Supabase에 업데이트 필요

## 작업 방식
1. Vercel 사이트에서 수정 후 HTML 내용 가져오기
2. CSV에서 해당 템플릿의 버튼 링크 확인
3. HTML 작성 후 GitHub 레포에 푸시
4. Supabase에 내용 업데이트

## GitHub 레포
- `windy-pureum/liveklass-templates`
