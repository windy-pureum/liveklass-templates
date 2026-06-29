# 라이브클래스 이메일 HTML 패턴 가이드

새 이메일 템플릿을 만들 때 아래 스니펫을 복사해서 사용하세요.

---

## 메일 제목 규칙

### 태그 체계
제목 앞에 대괄호 태그를 반드시 붙입니다.

| 태그 | 적용 대상 | 수신자 |
|------|---------|------|
| `[결제 안내]` | 결제 완료, 실패, 부가서비스 결제 | 운영자 |
| `[플랜 알림]` | 자동 결제 예정 알림 | 운영자 |
| `[플랜 변경]` | 무료 플랜 전환 등 | 운영자 |
| `[정산 안내]` | 정산 정보 요청, 본인인증 | 운영자 |
| `[수강 안내]` | 수강신청, 취소, 대기 | 수강생 |
| `[$%content%$ 초대]` | 수강생/강사 초대 | 수강생 |
| `[$%site_name%$]` | 수강생 알림, 보안 메일 | 수강생·공통 |
| `[$%L00014%$]` | 온보딩 메일 (라이브클래스 브랜드 강조) | 운영자 |

### 문체
| 상황 | 문체 | 예시 |
|------|------|------|
| 결제 실패, 플랜 변경 | `~요` | `결제 정보를 확인해 주세요.` |
| 그 외 (결제 완료, 플랜 알림, 알림 등) | `~습니다` | `5일 후 자동 결제됩니다.` |

### 제목 예시
```
[결제 안내] $%site_name%$ - $%plan_name%$ 플랜 결제가 완료되었습니다.
[플랜 알림] $%site_name%$ - $%plan_name%$ 플랜이 5일 후 자동 결제됩니다.
[플랜 알림] $%site_name%$ - $%plan_name%$ 플랜이 1일 후 자동 결제됩니다.
[플랜 변경] $%site_name%$ - 무료 플랜으로 변경되었어요.
[정산 안내] $%site_name%$ - 정산 정보 및 서류 제출을 요청드립니다.
[수강 안내] $%class_name%$ $%content%$ 수강신청이 완료되었습니다.
[$%content%$ 초대] $%class_name%$ $%content%$에 초대되었습니다.
[$%site_name%$] $%class_name%$ - 댓글이 달렸습니다.
[$%site_name%$] 로그인 코드는 $%otp_code%$입니다.
[$%site_name%$] 이메일 인증 코드는 $%authentication_code%$입니다.
```

### 운영자 메일은 사이트명 포함
운영자가 여러 사이트를 운영할 수 있으므로, 어떤 사이트의 메일인지 제목에서 바로 파악할 수 있도록 `$%site_name%$`을 포함합니다.

```
[태그] $%site_name%$ - 제목 내용
```

---

## 스타일 규격 요약

| 항목 | 값 |
|------|-----|
| 버튼 배경색 | `#2E8CFF` |
| 버튼 border-radius | `8px` |
| 버튼 padding | `14px 20px 11px` |
| 버튼 텍스트 색 | `#ffffff` |
| 버튼 텍스트 크기 | `16px` |
| 헤더 구분선 padding | `padding:15px;` |
| 푸터 구분선 padding (커뮤니티) | `padding:5px 15px;` |
| 푸터 구분선 padding (그 외) | `padding:15px;` |
| CTA↔푸터 구분선 스페이서 (커뮤니티) | `height:0px` |
| CTA↔푸터 구분선 스페이서 (그 외) | `height:50px` |
| 기본 폰트 패밀리 | `AppleSDGothic, apple sd gothic neo, noto sans korean, ...sans-serif` |
| 본문 텍스트 색 | `#333333` |
| 본문 텍스트 크기 | `14px` (운영자) / `16px` (수강생·커뮤니티) |
| 본문 line-height | `1.8` |
| 본문 padding | `20px 15px` |

---

## 1. CTA 버튼 — 일반 (class, plan-billing)

```html
<div class="stb-block-outer"><table class="stb-block stb-cols-1" border="0" cellpadding="0" cellspacing="0"
  style="overflow:hidden;margin:0px auto;padding:0px;width:100%;max-width:630px;clear:both;background:none;line-height:1.7;border:0;font-size:14px;box-sizing:border-box;" width="100%">
<tbody><tr><td><table class="stb-cell-wrap" border="0" cellpadding="0" cellspacing="0" width="100%">
<tbody><tr><td style="text-align:center;font-size:0;"><div class="stb-left-cell" style="max-width:630px;width:100%!important;margin:0;vertical-align:top;display:inline-block;"><div class="stb-cta-box" style="clear:both;"><table border="0" cellpadding="0" cellspacing="0" style="width:100%;"><tbody><tr><td style="padding:15px;border:0;width:100%;text-align:center;"><table class="stb-cell-wrap-cta" border="0" cellpadding="0" cellspacing="0"
  style="border-collapse:separate!important;background:#2E8CFF;border-radius:8px;border:0;margin:0 auto;table-layout:fixed;" align="center">
<tbody><tr><td style="line-height:1.5;padding:14px 20px 11px;" align="center">
<a href="$%LINK_URL%$" style="font-size:16px;display:inline;color:#ffffff;border-radius:50px;text-decoration:none;outline:0;font-family:AppleSDGothic, apple sd gothic neo, noto sans korean, noto sans korean regular, noto sans cjk kr, noto sans cjk, nanum gothic, malgun gothic, dotum, arial, helvetica, MS Gothic, sans-serif;text-align:center;" target="_blank">버튼 텍스트</a>
</td></tr></tbody></table></td></tr></tbody></table></div></div></td></tr></tbody></table></td></tr></tbody></table></div>
```

> `$%LINK_URL%$`와 `버튼 텍스트` 교체

---

## 2. CTA 버튼 — 커뮤니티 (stb-cta-only)

```html
<div class="stb-block-outer"><table class="stb-block stb-cta-only" border="0" cellpadding="0" cellspacing="0"
  style="overflow:hidden;margin:0px auto;padding:0px 10px;max-width:630px;clear:both;background:none;border:0;" width="100%">
<tbody><tr><td style="padding:5px 0 5px 0;text-align:center;line-height:1.8;border:0;" width="100%">
<br>
<div class="stb-cta-only-wrap" style="padding:10px 10px"><table class="stb-cell-wrap-cta" border="0" cellpadding="0" cellspacing="0"
  style="border-collapse:separate!important;background:#2E8CFF;border-radius:8px;border:0;margin:0 auto;table-layout:fixed;" align="center">
<tbody><tr><td style="line-height:1.5;padding:14px 20px 11px;" align="center">
<a href="$%LINK_URL%$" style="font-size:16px;display:inline;color:#ffffff;border-radius:50px;text-decoration:none;outline:0;font-family:AppleSDGothic, apple sd gothic neo, noto sans korean, noto sans korean regular, noto sans cjk kr, noto sans cjk, nanum gothic, malgun gothic, dotum, arial, helvetica, MS Gothic, sans-serif;text-align:center;" target="_blank">버튼 텍스트</a>
</td></tr></tbody></table></div>
</td></tr></tbody></table></div>
```

---

## 3. 회색 박스 — 인증코드 / OTP

배경: `#F3F3F3`, 텍스트 크기 20px bold, 가운데 정렬

```html
<div class="stb-block-outer"><table class="stb-block stb-cols-1" border="0" cellpadding="0" cellspacing="0"
  style="overflow:hidden;margin:0px auto;padding:0px;width:100%;max-width:630px;clear:both;background:none;line-height:1.7;border:0;font-size:14px;box-sizing:border-box;" width="100%">
<tbody><tr><td><table class="stb-cell-wrap" border="0" cellpadding="0" cellspacing="0" width="100%">
<tbody><tr><td style="text-align:center;padding:20px 15px;">
<table border="0" cellpadding="0" cellspacing="0" align="center" style="margin:0 auto;background:#F3F3F3;border-collapse:separate;border-radius:4px;">
<tbody><tr><td style="padding:16px 32px;text-align:center;white-space:nowrap;">
<span style="font-size:20px;font-family:AppleSDGothic, apple sd gothic neo, noto sans korean, noto sans korean regular, noto sans cjk kr, noto sans cjk, nanum gothic, malgun gothic, dotum, arial, helvetica, MS Gothic, sans-serif;color:rgb(0,0,0);font-weight:700;">$%authentication_code%$</span>
</td></tr></tbody></table>
</td></tr></tbody></table></td></tr></tbody></table></div>
```

---

## 4. 회색 박스 — 커뮤니티 본문 (글/댓글 내용)

배경: `#F3F4F6`, 텍스트 14px, 좌측 정렬

```html
<table border="0" cellpadding="0" cellspacing="0" style="width:100%;background:#F3F4F6;border-collapse:separate;border-radius:8px;">
<tbody><tr><td style="padding:16px 18px;font-size:14px;font-family:AppleSDGothic, apple sd gothic neo, noto sans korean, noto sans korean regular, noto sans cjk kr, noto sans cjk, nanum gothic, malgun gothic, dotum, arial, helvetica, MS Gothic, sans-serif;color:#374151;line-height:1.75;word-break:break-word;">
$%post_body%$
</td></tr></tbody></table>
```

> `$%post_body%$` 또는 `$%comment_body%$` 사용

---

## 5. 결제 정보 카드 — 클래스 수강신청 (2컬럼)

좌측 42%: 클래스 썸네일 + 이름 / 우측 58%: 결제 상세 정보

```html
<div style="font-family:AppleSDGothic,sans-serif;font-size:16px;font-weight:700;color:#1a1a2e;margin-bottom:8px;text-align:left;">결제 정보</div>
<table border="0" cellpadding="0" cellspacing="0" style="width:100%;border-collapse:separate;border-spacing:0;table-layout:fixed;">
<tbody><tr>
  <!-- 좌측: 클래스 이미지 + 이름 -->
  <td style="width:42%;vertical-align:top;padding-right:6px;border:0;background:#f7f8fa;border-radius:6px;">
    <div style="padding:8px 8px 0 8px;">
      <img src="$%class_logoUrl%$" style="border:0;width:100%;height:auto;display:block;border-radius:4px;" width="100%"/>
    </div>
    <div style="padding:6px 8px 8px;font-family:AppleSDGothic,sans-serif;font-size:12px;font-weight:700;color:#1a1a2e;line-height:1.4;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;">$%class_name%$</div>
  </td>
  <!-- 우측: 결제 정보 테이블 -->
  <td style="width:58%;vertical-align:top;padding-left:6px;border:0;background:#f7f8fa;border-radius:6px;">
    <div style="padding:14px;">
      <table border="0" cellpadding="0" cellspacing="0" style="width:100%;border-collapse:collapse;"><tbody>
        <tr>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;color:#888888;white-space:nowrap;width:1px;">결제자명</td>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;font-weight:600;color:#1a1a2e;text-align:right;">$%user_name%$</td>
        </tr>
        <tr>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;color:#888888;white-space:nowrap;width:1px;">결제 금액</td>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;font-weight:600;color:#3A79E3;text-align:right;">$%payment_amount%$</td>
        </tr>
        <tr>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;color:#888888;white-space:nowrap;width:1px;">결제 수단</td>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;font-weight:600;color:#1a1a2e;text-align:right;">$%payment_method%$</td>
        </tr>
        <tr>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;color:#888888;white-space:nowrap;width:1px;">결제 일자</td>
          <td style="padding:5px 0;border-top:1px solid #eeeeee;border-bottom:0;border-left:0;border-right:0;font-family:AppleSDGothic,sans-serif;font-size:12px;font-weight:600;color:#1a1a2e;text-align:right;">$%paid_at%$</td>
        </tr>
      </tbody></table>
    </div>
  </td>
</tr></tbody></table>
```

---

## 6. 운영자 메일 정보 섹션 (구분선 + 텍스트 테이블)

플랜 결제, 정산 등 운영자 메일에서 정보를 나열할 때 사용

```html
<div style="font-family:AppleSDGothic,sans-serif;font-size:14px;color:#333333;line-height:1.8;">
──────────────────────<br/>
■ 결제 정보<br/>
──────────────────────<br/>
적용 사이트&nbsp;&nbsp;&nbsp;&nbsp;$%site_name%$<br/>
플랜명&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$%plan_name%$<br/>
결제 일시&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$%pay_at%$<br/>
결제 금액&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$%pay_price%$ (VAT 포함)<br/>
다음 결제 예정일&nbsp;$%repay_at%$<br/>
──────────────────────
</div>
```

---

## 7. 구분선 (Divider)

### 헤더 구분선 (로고 아래)
```html
<td style="padding:15px;border:0;">
  <table class="stb-partition" style="width:100%;height:0;background:none;padding:0;border-top:1px solid #999999;margin:0;border-collapse:separate;"></table>
</td>
```

### 푸터 구분선 (커뮤니티 메일)
```html
<td style="padding:5px 15px;border:0;">
  <table class="stb-partition" style="width:100%;height:0;background:none;padding:0;border-top:1px solid #999999;margin:0;border-collapse:separate;"></table>
</td>
```

### 푸터 구분선 (그 외 메일)
```html
<td style="padding:15px;border:0;">
  <table class="stb-partition" style="width:100%;height:0;background:none;padding:0;border-top:1px solid #999;margin:0;border-collapse:separate;"></table>
</td>
```

---

## 8. 스페이서 (CTA↔푸터 구분선 사이)

### 커뮤니티 메일
```html
<td style="height:0px"></td>
```

### 그 외 메일 (class, plan-billing 등)
```html
<td style="height:50px"></td>
```

---

## 9. 본문 텍스트 블록

모든 본문 텍스트는 이 블록 안에 작성합니다. 운영자/수강생에 따라 색상과 패딩이 다릅니다.

### 수강생 클래스 메일 (color:#333333, padding:20px 15px)
```html
<div class="stb-block-outer"><table class="stb-block stb-cols-1" border="0" cellpadding="0" cellspacing="0"
  style="overflow:hidden;margin:0px auto;padding:0px;width:100%;max-width:630px;clear:both;background:none;line-height:1.7;border:0;font-size:14px;box-sizing:border-box;" width="100%">
<tbody><tr><td><table class="stb-cell-wrap" border="0" cellpadding="0" cellspacing="0" width="100%">
<tbody><tr><td style="text-align:center;font-size:0;"><div class="stb-left-cell" style="max-width:630px;width:100%!important;margin:0;vertical-align:top;display:inline-block;"><div class="stb-text-box" style="text-align:left;margin:0px;line-height:1.7;word-break:break-word;font-size:16px;font-family:AppleSDGothic,sans-serif;color:#333333;clear:both;border:0;">
<table border="0" cellpadding="0" cellspacing="0" style="width:100%;"><tbody><tr><td style="padding:20px 15px;font-size:16px;line-height:1.7;color:#333333;border:0;font-family:AppleSDGothic,sans-serif;width:100%;">
본문 텍스트 내용
</td></tr></tbody></table></div></div></td></tr></tbody></table></td></tr></tbody></table></div>
```

### 운영자 메일 (color:#000000, padding:15px)
```html
<div class="stb-block-outer"><table class="stb-block stb-cols-1" border="0" cellpadding="0" cellspacing="0"
  style="overflow:hidden;margin:0px auto;padding:0px;width:100%;max-width:630px;clear:both;background:none;line-height:1.7;border:0;font-size:14px;box-sizing:border-box;" width="100%">
<tbody><tr><td><table class="stb-cell-wrap" border="0" cellpadding="0" cellspacing="0" width="100%">
<tbody><tr><td style="text-align:center;font-size:0;"><div class="stb-left-cell" style="max-width:630px;width:100%!important;margin:0;vertical-align:top;display:inline-block;"><div class="stb-text-box" style="text-align:left;margin:0px;line-height:1.7;word-break:break-word;font-size:16px;font-family:AppleSDGothic,sans-serif;color:#000000;clear:both;border:0;">
<table border="0" cellpadding="0" cellspacing="0" style="width:100%;"><tbody><tr><td style="padding:15px;font-size:16px;line-height:1.7;color:#000000;border:0;font-family:AppleSDGothic,sans-serif;width:100%;">
본문 텍스트 내용
</td></tr></tbody></table></div></div></td></tr></tbody></table></td></tr></tbody></table></div>
```

---

## 10. 인사말

인사말은 본문 텍스트 블록(9번) 안의 `<td>` 내부에 `<div>` 태그로 작성합니다.

### 운영자 메일 (라이브클래스 브랜드)
```html
<div>$%user_name%$님, 안녕하세요.</div>
<div>라이브클래스입니다.</div>
<div><br/></div>
```

### 수강생 클래스 메일 (사이트 브랜드)
```html
<div>$%user_name%$님, 안녕하세요.</div>
<div>$%site_name%$입니다.</div>
<div><br/></div>
```

---

## 11. 수신거부 푸터 (광고성 메일 전용)

광고성 메일에만 추가. `base_lk-logo_operator_unsub.html` 베이스 파일 사용 시 자동 포함됨.
수동으로 추가할 경우, 푸터 회사 정보 텍스트 `<br/>` 바로 아래에 붙여 넣습니다.

```html
<br/>
<span style="color:#747579;font-size:12px;">본 메일은 회원님의 수신 동의를 받아 발송된 광고성 메일입니다.</span><br/>
<span style="color:#747579;font-size:12px;">메일 수신을 원치 않으시면 <a href="$%unsubscribe%$" style="color:#747579;font-size:12px;text-decoration:underline;font-weight:normal;" target="_blank">여기[수신거부]</a>를 클릭해 주세요.</span><br/>
<span style="color:#747579;font-size:12px;">If you don't want to receive this e-mail anymore, <a href="$%unsubscribe%$" style="color:#747579;font-size:12px;text-decoration:underline;font-weight:normal;" target="_blank">click here</a>.</span>
```

> 변수: `$%unsubscribe%$` — Stibee에서 자동 생성하는 수신거부 링크

---

## 패턴 조합 가이드

| 메일 유형 | 베이스 파일 | CTA 버튼 | 스페이서 | 푸터 구분선 |
|----------|------------|---------|---------|-----------|
| 운영자 결제·정산 | `base_lk-logo_operator.html` | 일반 CTA | 50px | `padding:15px` |
| 운영자 광고성 (수강생 규모 등) | `base_lk-logo_operator_unsub.html` | 일반 CTA | 50px | `padding:15px` |
| 수강생 클래스 | `base_site-logo_learner.html` | 일반 CTA | 50px | `padding:15px` |
| 수강생 커뮤니티·공지 | `base_site-logo_learner.html` | 커뮤니티 CTA | 0px | `padding:5px 15px` |
| 보안 (OTP·인증코드) | `base_no-header_common.html` | 없음 | 50px | `padding:15px` |
