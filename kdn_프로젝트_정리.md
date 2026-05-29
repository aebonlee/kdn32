# KDN 수강생 프로젝트 정리 (kdn01 ~ kdn32)

> GitHub: `https://github.com/aebonlee/kdnNN` · 사이트: `https://aebonlee.github.io/kdnNN/`
> 전 프로젝트 GitHub Pages에서 표시 가능. 백엔드 앱은 정적 변환(Streamlit→stlite, Express→정적 렌더, Next→export)으로 화면 노출.

## 1차 배치 (kdn01 ~ kdn13)

| 번호 | 원본 zip | 유형 | 내용 | Supabase |
|---|---|---|---|---|
| kdn01 | web-test-main | Vite/React | 사주·운세앱(Suyoung's Secret) | ✅ kdn01_ 게시판(코드 적용) |
| kdn02 | kdn-web-main | Vite/React | 전력설비 현황 대시보드 | ✅ kdn02_inspection_reports |
| kdn03 | kdn-vuln-main | Vite/React | KDN-VULN 취약점 진단 | ✅ kdn03_ 6테이블+버킷 |
| kdn04 | AMIMAPER-main | Vite/React | AMIMAPER | — |
| kdn05 | security-main | 정적+env주입 | 보안관제 실무 가이드 | 자체 Supabase(jxrs…) |
| kdn06 | realzero-main | Next.js | Real Zero 에코 SNS | ✅ kdn06_feed_items+버킷 |
| kdn07 | lotto-main | PyQt6 데스크톱 | Lotto(웹데모 부분 표시) | — |
| kdn08 | web-test | 정적 HTML | 한전KDN 홍보 페이지 | — |
| kdn09 | web-test-main(1) | 정적 HTML | 포트폴리오(미터링 엔지니어) | — |
| kdn10 | webtest-main | Express→정적 | TechCorp 보안 데모 | — |
| kdn11 | packetanalyzer-main | Streamlit→stlite | 패킷 분석 | (scapy 브라우저 제한) |
| kdn12 | streamit-main | Streamlit→stlite | Streamlit 앱 | — |
| kdn13 | web-kdn-main | Streamlit→stlite | Streamlit 앱 | — |

## 2차 배치 (kdn14 ~ kdn32, Downloads\kdn)

| 번호 | 원본 zip | 유형 | 내용 | Supabase |
|---|---|---|---|---|
| kdn14 | 20260527-vibe-coding | 정적 HTML | KDN 사업관리 시스템 | (자체) |
| kdn15 | ai-news-dashboard | 정적 HTML | AI 뉴스 요약 대시보드 | — |
| kdn16 | ccw | 정적 HTML | Frontend Developer 포트폴리오 | — |
| kdn17 | chatbot | Streamlit→stlite | 챗봇 | (openai 키 필요) |
| kdn18 | day3-test | CRA React | day3-test 앱 | (자체) |
| kdn19 | kdn3 | Streamlit→stlite | Streamlit 앱 | — |
| kdn20 | kdn-vivecoding2 | Vite/React | KDN 업무 일지 | ⚠ kdn20_ 스크립트(코드 미적용) |
| kdn21 | kdn-vivecoding4 | Streamlit→stlite | Streamlit 앱 | (supabase-py) |
| kdn22 | kdn-vuln | Vite/React | 취약점 진단(kdn03 동일계열) | ⚠ kdn22_ 스크립트(코드 미적용) |
| kdn23 | MaintenanceWeb | NestJS+Next→export | 유지보수 예방점검 일정 관리 | (백엔드 필요) |
| kdn24 | nursing-room | Vite/React | KDN 바이브코딩(대형 템플릿) | ⚠ 폴백(스키마 대부분 누락) |
| kdn25 | python-web | Streamlit→stlite | Streamlit 앱 | — |
| kdn26 | streamlit-korea | Streamlit→stlite | Streamlit 앱(folium/geopandas 제한) | — |
| kdn27 | streamlit-test | Streamlit→stlite | Streamlit 앱 | — |
| kdn28 | test3 | Vite/React | Worklog 업무일지 | ⚠ kdn28_report_summaries(코드 미적용) |
| kdn29 | web-kdn | Vite/React | 게시판 | ⚠ kdn29_ 스크립트(코드 미적용) |
| kdn30 | web-test2 | 정적 HTML | 전기차 충전서비스 | (자체) |
| kdn31 | webtest | Express→정적 | TechCorp 보안 데모(kdn10 동일) | — |
| kdn32 | web-test-main | 정적 HTML | 포트폴리오(송*우) + **문서·SQL 보관소** | — |

## 참고
- **stlite 앱**(Streamlit): 최초 로딩 10~30초(브라우저에서 Python 실행). 일부 네이티브 패키지(scapy, geopandas 등)는 미지원이라 해당 기능만 제한, 화면은 정상.
- **Supabase 통합 셋업**: 이 리포의 `supabase_setup_all.sql` — Supabase SQL Editor에 전체 붙여넣고 Run(접두사·재실행 안전).
- **⚠ 표시 앱(kdn20·22·28·29)**: 테이블 SQL은 준비됐으나 앱 코드가 접두사 미적용 → 데이터 연동하려면 코드 수정·재배포 필요.
- 학생 CI(.github/workflows)는 제거하고 repo Actions 비활성화(docs 덮어쓰기 방지).

## 운영 메모
- 공유 Supabase: `aebonlee's Project` (ref `hcmgdztsgjvzcyxyayaj`), Google/Kakao/Email 가입 활성, redirect 허용 `https://aebonlee.github.io/**`.
- 배포 도구: PortableGit + GitHub REST API. TLS는 `http.schannelCheckRevoke=false`.
