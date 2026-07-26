# Sunrise EIASS

> EIASS 환경영향평가 사업 검색, 사업개요 확인, 원문 문서 분류·미리보기·다운로드를 하나의 Windows 데스크톱 화면에서 처리하는 업무지원 프로그램입니다.

![Version](https://img.shields.io/badge/version-4.0.0-1668c7)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D4)
![Python](https://img.shields.io/badge/Python-3.12%20x64-3776AB)
![UI](https://img.shields.io/badge/UI-PyQt5-41CD52)

## 개요

**Sunrise EIASS**는 환경영향평가 실무자가 EIASS 공개 사업자료를 더 빠르고 일관되게 조회할 수 있도록 제작된 Windows 전용 데스크톱 프로그램입니다.

사업명·사업지주소·사업코드·사업시행자 등의 검색, 평가유형별 결과 구분, 사업개요 확인, 초안·본안·보완·변경협의 등 원문 분류, PDF 미리보기와 일괄 다운로드를 하나의 작업 흐름으로 제공합니다.

> 이 프로그램은 EIASS 운영기관의 공식 프로그램이 아닌 독립적인 업무지원 도구입니다. EIASS 서버의 공개 범위, 응답 형식, 비공개 정책 및 서비스 상태에 따라 일부 자료가 조회되지 않을 수 있습니다.

## 현재 버전

| 항목 | 내용 |
|---|---|
| 제품명 | Sunrise EIASS |
| 버전 | `4.0.0` |
| 릴리즈 코드 | `PDF_READER_NAVER_MAP_STABILIZED` |
| 실행파일 | `Sunrise EIASS.exe` |
| 대상 운영체제 | Windows 10/11 x64 |
| 소스 기준 | CPython 3.12 x64 |
| 패키징 | PyInstaller onefile |

## 주요 기능

### 1. EIASS 사업 검색

- 전략환경영향평가
- 환경영향평가
- 소규모환경영향평가
- 사후환경영향조사
- 사전환경성검토
- 사업명 또는 통합항목 검색
- 전체 문자열 포함, 정확히 일치, 모든 단어 포함, 하나 이상의 단어 포함, 정규식 검색
- 협의기관 및 사업구분 필터
- 평가유형별 결과 탭과 페이지 단위 표시
- 대량 검색 중 부분결과 우선 표시 및 검색 중지

### 2. 사업개요 및 원문 확인

- 사업명, 사업위치, 사업시행자, 협의기관, 접수일 등 사업개요 표시
- 초안·본안·보완·재보완·변경협의·사후조사 등 원문 분류
- 문서별 PDF 미리보기
- 선택 문서 다운로드
- 현재 목록 전체 다운로드
- 실패 문서 재시도
- 다운로드 일시중지·재개·중지
- 다운로드 결과와 SHA-256 무결성 기록

### 3. PDF 원문 뷰어

- 좌측 원문 목록에서 다른 문서 즉시 전환
- 원문 분류별 목록 필터
- 기본 `페이지 맞춤` 표시
- 마우스 휠로 이전·다음 페이지 이동
- `Ctrl + 마우스 휠`로 확대·축소
- 폭 맞춤, 페이지 맞춤, 90도 회전
- PDF 본문검색 및 검색결과 이동
- 한쪽 보기
- 고정 두쪽 모아보기

두쪽 모아보기는 페이지가 겹치지 않도록 다음 순서로 이동합니다.

```text
1·2쪽 → 3·4쪽 → 5·6쪽 → 7·8쪽
```

### 4. 네이버지도 연동

- 일반 사업의 사업위치를 네이버지도에서 검색
- 도로사업 상세정보에 `시점`과 `종점`이 존재하는 경우 각각 주소로 인식
- 시점과 종점을 별도의 네이버지도 탭으로 열기

### 5. 공지사항 및 자동 업데이트

- GitHub 기반 공지사항 확인
- 최신 버전 확인
- Release 실행파일 다운로드
- 실행파일명·크기·MZ 헤더·SHA-256 검증
- Windows onefile 교체 방식 업데이트

| 구분 | 주소 |
|---|---|
| 저장소 | <https://github.com/Peter-msk/Sunrise-EIASS> |
| 최신 Release | <https://github.com/Peter-msk/Sunrise-EIASS/releases/latest> |
| 업데이트 정보 | <https://raw.githubusercontent.com/Peter-msk/Sunrise-EIASS/main/latest.json> |
| 공지사항 | <https://raw.githubusercontent.com/Peter-msk/Sunrise-EIASS/main/notice.txt> |

## 사용자 설치 및 실행

### 배포 EXE 사용

1. 저장소의 **Releases**에서 최신 `Sunrise EIASS.exe`를 받습니다.
2. 사용자 쓰기 권한이 있는 폴더에 저장합니다.
3. `Sunrise EIASS.exe`를 실행합니다.
4. Windows 보안 경고가 표시되면 게시자와 파일 해시를 확인한 후 실행합니다.

프로그램 설정, 로그, 검색 진단자료는 기본적으로 다음 경로에 저장됩니다.

```text
%LOCALAPPDATA%\Sunrise Group\Sunrise EIASS
```

## 기본 사용 순서

1. 검색어를 입력합니다.
2. 검색방식과 검색대상을 선택합니다.
3. 평가구분, 협의기관, 사업구분을 지정합니다.
4. **검색**을 실행합니다.
5. 결과 탭에서 사업을 선택합니다.
6. 우측 사업개요와 원문 문서 목록을 확인합니다.
7. `PDF 보기`로 원문을 검토하거나 필요한 문서를 선택해 다운로드합니다.
8. 사업위치는 네이버지도 버튼으로 확인합니다.

## 소스 실행

### 요구 환경

- Windows 10/11 x64
- CPython 3.12 x64
- 인터넷 연결

### 의존성 설치

```bat
py -3.12 -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 소스 실행

```bat
run_windows.bat
```

또는 다음 명령으로 실행할 수 있습니다.

```bat
.venv\Scripts\python.exe main.py
```

## Windows onefile 빌드

```bat
build_windows.bat
```

빌드 파이프라인은 다음 순서로 진행됩니다.

```text
의존성·메타데이터 사전검증
→ PyInstaller onefile 생성
→ Authenticode 서명
→ 서명 검증
→ EXE startup self-test
→ 서명 후 SHA-256 계산
→ latest.json 및 notice.txt 생성
```

정상 완료 시 주요 산출물은 `dist_release` 폴더에 생성됩니다.

```text
dist_release/
├─ Sunrise EIASS.exe
├─ latest.json
└─ notice.txt
```

### 빌드 기준 의존성

주요 고정 버전은 `requirements-build-lock.txt`에서 관리합니다.

- PyQt5 5.15.11
- PyMuPDF 1.26.7
- requests 2.32.5
- beautifulsoup4 4.14.3
- aiohttp 3.13.3
- PyInstaller 6.21.0

## 프로젝트 구조

```text
Sunrise-EIASS/
├─ main.py                         # 프로그램 진입점
├─ eiass_report_reviewer/          # 메인 애플리케이션 패키지
│  ├─ controllers/                 # UI 작업 흐름 제어
│  ├─ services/                    # 검색·상세·다운로드·업데이트 서비스
│  ├─ parsers/                     # EIASS HTML 및 원문 파서
│  ├─ workers/                     # 비동기 작업 스레드
│  └─ ui/                          # PyQt5 화면과 테마
├─ tests/                          # 회귀시험
├─ docs/                           # UI 및 운영자료
├─ release_templates/              # latest.json·notice.txt 템플릿
├─ build_windows.bat               # Windows 공식 빌드 진입점
├─ requirements.txt                # 실행·개발 의존성
└─ requirements-build-lock.txt     # 공식 빌드 고정 의존성
```

## 진단 및 문제 해결

### 프로그램 실행 오류

```text
%LOCALAPPDATA%\Sunrise Group\Sunrise EIASS\last_crash.txt
%LOCALAPPDATA%\Sunrise Group\Sunrise EIASS\sunrise_eiass.log
```

### 검색 결과 또는 파서 문제

```text
%LOCALAPPDATA%\Sunrise Group\Sunrise EIASS\search_diagnostics
%LOCALAPPDATA%\Sunrise Group\Sunrise EIASS\html_diagnostics
```

오류를 등록할 때 다음 자료를 함께 첨부하면 원인 확인이 빨라집니다.

- 사용한 프로그램 버전
- Windows 버전과 화면 배율
- 검색어 및 선택한 검색조건
- `sunrise_eiass.log`
- 최신 검색 진단 JSON
- 필요한 경우 HTML 진단파일

민감한 사업정보나 개인정보가 포함되어 있는지 확인한 뒤 첨부해야 합니다.

## 제한사항

- EIASS 서버 응답속도와 운영상태에 따라 검색시간이 달라질 수 있습니다.
- 진행 중, 반려, 취하, 비공개 사업은 원문 열람 또는 다운로드가 제한될 수 있습니다.
- EIASS HTML 또는 다운로드 방식이 변경되면 일부 기능에 보완이 필요할 수 있습니다.
- PDF 본문검색 결과는 PDF에 실제 텍스트 레이어가 존재하는 경우에 가장 정확합니다.
- 네이버지도 검색결과는 입력된 주소 문자열과 네이버지도 검색결과에 따라 달라질 수 있습니다.

## 개발 방향

- EIASS 검색 정확도와 응답 구조 적응력 강화
- 대량 원문 수집의 안정성 및 재개 기능 개선
- 검색·상세·원문 캐시 진단 강화
- PDF 검토 편의기능 지속 개선
- Windows 배포·서명·업데이트 자동검증 강화

## 변경내역

세부 변경사항은 저장소의 `CHANGELOG_*.md`와 각 버전 인수인계서를 참고하십시오.

- v4.0.0: PDF 뷰어 조작 강화, 고정 두쪽 보기, 네이버지도 전환
- v3.9.5: PDF 미리보기 좌우 레이아웃 및 원문 목록 개선
- v3.9.4: 검색·상세·파서 병목 방지
- v3.9.2: Windows 실행 초기화 및 startup self-test 안정화

## 문의 및 오류 제보

오류·개선 요청은 GitHub 저장소의 **Issues**에 등록해 주세요.

<https://github.com/Peter-msk/Sunrise-EIASS/issues>

---

**Sunrise EIASS** · Developed by **Sunrise Group**
