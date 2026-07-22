# PCssak Biuja Privacy Policy / 개인정보 처리방침

- Last updated / 최종 수정: 2026-07-22
- Applies to / 적용 대상: PCssak Biuja Free Early Access for Windows
- Operator / 운영자: PCSSAK
- Contact / 문의: `pcssakinc@gmail.com`

> **Pre-release draft / 공개 전 초안**
>
> This document describes the current implementation but is neither final legal advice nor a
> professionally reviewed final text. It requires the operator's final
> approval before publication. The Korean text is authoritative to the extent permitted by
> applicable law; the English text is a reference translation.
>
> 이 문서는 현재 구현을 설명하지만 최종 법률 자문이나 전문 법률 검토를 마친 문서가 아닙니다.
> 공개 전에 운영자의 최종 승인이 필요합니다. 적용 법률이 허용하는 범위에서 국문을
> 기준으로 하며 영문은 참고 번역입니다.

## 국문

### 1. 핵심 요약

PCssak Biuja의 파일 정리 자체는 **100% 로컬 처리**합니다. 파일, 파일 내용, 파일 이름, 폴더
경로, 정리 판단과 작업저널을 PCSSAK 서버로 올리지 않습니다. 공개 무료 Early Access에는
PCSSAK 계정, 광고, 사용 분석, 추적 SDK, 클라우드 파일 색인이나 자동 오류 업로드가 없습니다.

다만 “로컬 처리”가 네트워크를 전혀 사용하지 않는다는 뜻은 아닙니다. 다음의 제한된 전달·연락
예외가 있습니다.

1. 앱 시작 약 3.5초 뒤 공식 GitHub의 업데이트 `latest.json` 자동 확인
2. 사용자가 승인한 경우에만 공식 GitHub 업데이트 설치 파일 다운로드
3. 필요한 Microsoft Edge WebView2 Runtime 설치·복구와 독립적인 업데이트
4. 사용자가 직접 여는 홈페이지·GitHub Issue·이메일 등 외부 서비스

이 예외에서도 PCssak Biuja는 정리를 위해 파일 내용·파일 이름·폴더 경로·작업저널을
전송하지 않습니다.

### 2. 운영자가 앱에서 수집하지 않는 정보

공개 무료 Early Access 앱은 다음 정보를 PCSSAK에 자동 전송하거나 중앙 데이터베이스에
수집하지 않습니다.

- 정리 대상 파일과 파일 내용
- 파일 이름, 전체 폴더 경로와 폴더 목록
- 정리 규칙, 미리보기, 작업저널과 되돌리기 기록
- 사용 횟수, 버튼 사용, 화면 체류 시간 등의 분석 정보
- 자동 오류 보고서나 로그 업로드
- 계정, 로그인, 결제 또는 유료 라이선스 정보

현재 무료 배포본은 앱 안에서 결제를 처리하거나 구매 이메일을 수집하지 않습니다. 향후 별도
유료 기능이 출시되면 실제 처리 방식이 확정된 뒤 이 방침과 관련 약관을 먼저 갱신해야 합니다.

### 3. GitHub 자동 업데이트 확인과 다운로드

GitHub 배포용 독립형 빌드는 앱 시작 약 **3.5초 후** 다음 공식 릴리스의 `latest.json`을 자동으로
확인합니다.

- `https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest/download/latest.json`

이 확인 요청은 업데이트 버전·서명·설치 파일 위치를 담은 공개 명세를 읽기 위한 것입니다.
PCssak Biuja는 이 요청에 사용자의 파일 내용, 파일 이름, 폴더 경로, 정리 규칙, 미리보기나
작업저널을 넣지 않습니다.

일반적인 인터넷 요청과 마찬가지로 GitHub는 사용자의 IP 주소와 요청 시각, 요청 URL,
User-Agent와 같은 통상적인 요청·보안 메타데이터를 처리할 수 있습니다. 이 처리는 GitHub가
독립적으로 수행하며 [GitHub 개인정보 보호정책](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)이
적용됩니다. PCSSAK은 이 자동 확인을 위한 별도 추적 서버나 분석 식별자를 운영하지 않습니다.

새 버전이 있어도 설치 파일은 자동으로 내려받지 않습니다. 사용자가 앱에서 다운로드·설치를
명시적으로 승인한 경우에만 공식 GitHub 릴리스 자산을 내려받습니다. 이때도 GitHub는 IP와
일반 요청 메타데이터를 처리할 수 있으며, 앱은 설치 전 PCSSAK Tauri 업데이트 서명을
검증합니다.

네트워크 차단이나 GitHub 장애로 확인에 실패하면 시작 시 오류를 조용히 처리하고 핵심 로컬
정리 기능은 계속 사용할 수 있어야 합니다. 네트워크를 차단하면 자동 확인과 다운로드는 사용할
수 없습니다.

### 4. Microsoft WebView2 연결

PCssak Biuja 화면에는 Microsoft Edge WebView2 Runtime이 필요합니다. Runtime이 없거나
설치·복구가 필요하면 Windows 또는 설치 프로그램에 포함된 Microsoft 공식 부트스트래퍼가
Microsoft 배포 서비스에 연결해 Runtime을 내려받을 수 있습니다. 설치된 WebView2 Runtime은
Microsoft의 독립적인 업데이트 절차를 사용할 수 있습니다.

PCssak Biuja는 WebView2 설치 요청에 정리 대상 파일, 파일 이름, 폴더 경로나 작업저널을 넣지
않습니다. Microsoft는 IP와 일반 설치·요청 메타데이터를 자체 정책에 따라 처리할 수 있으며
[Microsoft 개인정보처리방침](https://privacy.microsoft.com/privacystatement)이 적용됩니다.
인터넷이 차단된 환경에서는 필요한 Runtime이 이미 없으면 설치나 실행을 완료하지 못할 수
있습니다.

### 5. 기기에 저장되는 로컬 데이터

다음 정보는 사용자의 Windows 기기에 저장되며 PCSSAK으로 자동 업로드되지 않습니다. Windows
버전과 설치 환경에 따라 실제 표시 경로가 조금 다를 수 있습니다.

| 데이터 | 일반적인 위치 | 내용과 보관 |
|---|---|---|
| 설정 | `%APPDATA%\com.pcssak.biuja\config.json` | 사용자가 선택한 폴더 경로, 정리 규칙, 일정, 언어·테마 등. 손상된 설정은 같은 위치에 백업 파일이 생길 수 있습니다. |
| 작업저널 | `%APPDATA%\com.pcssak.biuja\journal.db`와 SQLite 보조 파일 | 원본·대상 경로, 작업 종류·시각·상태, 안전한 되돌리기를 위한 크기·수정 시각·파일 식별·지문 정보 등. 현재 최대 20,000개 작업 행을 유지하고 오래된 행을 정리합니다. 파일 내용 사본은 아닙니다. |
| 로컬 로그 | `%LOCALAPPDATA%\com.pcssak.biuja\logs` | 시작·오류 진단용 기술 로그. 문제 상황에 따라 로컬 경로나 작업 관련 기술 정보가 포함될 수 있지만 자동 전송되지 않습니다. |
| WebView2 데이터 | `%LOCALAPPDATA%\com.pcssak.biuja\EBWebView` 등 앱별 WebView2 위치 | 화면 렌더링에 필요한 Microsoft WebView2 캐시와 환경설정 |
| 창·자동 시작 상태 | 앱별 로컬 설정과 사용자가 켠 경우 Windows 자동 시작 등록 | 창 크기·위치와 Windows 로그인 시 실행 여부 |

작업저널의 파일 지문은 안전한 작업 확인과 되돌리기 판단을 위한 로컬 증거이며 PCSSAK으로
전송되지 않습니다. 작업저널은 파일 사본이나 백업이 아닙니다.

### 6. 사용자가 직접 연락하거나 공개하는 정보

사용자가 GitHub Issue를 작성하거나 `pcssakinc@gmail.com`으로 이메일을 보내면 사용자가
입력한 내용은 각각 GitHub 또는 이메일 서비스가 처리하고 PCSSAK이 문의 대응을 위해 보게
됩니다. 이 동작은 자동 수집이 아니며 사용자가 직접 시작합니다.

실제 전체 경로, 파일 이름, 폴더 목록, 파일 내용, 고객 자료, 비밀번호·토큰·개인키나 회사
비밀을 보내지 마세요. 합성 예제와 가린 화면을 사용하세요. 보안 문제는 `SECURITY.md`의 비공개
절차를 따르세요.

운영자는 문의에서 받은 연락처와 내용을 답변, 오류 재현, 보안 대응과 필요한 기록 보존 범위에서
사용합니다. 삭제 요청은 `pcssakinc@gmail.com`으로 보낼 수 있으나 법적 의무, 보안 조사 또는
분쟁 대응에 필요한 최소 정보는 허용되는 기간 동안 보존될 수 있습니다.

### 7. 로컬 데이터 삭제

작업저널은 현재 최대 20,000개 작업 행을 유지하며 한도를 넘은 오래된 행을 정리합니다. 설정,
로그와 WebView2 데이터는 사용자가 삭제하거나 앱 제거 과정에서 삭제를 선택할 때까지 남을 수
있습니다.

NSIS 제거 화면에서 **앱 데이터 삭제**를 선택할 수 있습니다. 선택하지 않으면 업데이트 또는
재설치를 위해 로컬 데이터가 남을 수 있습니다. 앱을 완전히 종료하고 제거한 뒤 다음 앱별 폴더를
직접 삭제할 수도 있습니다.

- `%APPDATA%\com.pcssak.biuja`
- `%LOCALAPPDATA%\com.pcssak.biuja`

폴더를 삭제하면 설정과 작업저널을 되돌릴 수 없으므로 필요한 기록을 먼저 확인하세요. Windows
휴지통에 있는 파일과 PCssak Biuja가 정리한 실제 사용자 폴더는 위 앱 데이터 폴더와 별개이며,
앱 제거 또는 앱 데이터 삭제로 함께 삭제되지 않습니다.

### 8. 제3자 처리와 국외 처리 가능성

PCSSAK은 앱 사용 데이터를 광고업체나 데이터 중개업체에 판매하지 않습니다. 자동 업데이트를
위한 GitHub, WebView2를 위한 Microsoft, 사용자가 선택한 이메일·GitHub Issue는 각 사업자가
독립적으로 제공합니다. 해당 사업자는 자신의 인프라 위치와 정책에 따라 통상적인 네트워크·
문의 데이터를 여러 국가 또는 지역에서 처리할 수 있습니다. 구체적인 범위와 권리는 각 사업자의
공식 개인정보 정책을 확인하세요.

### 9. 아동의 개인정보

PCssak Biuja는 아동을 대상으로 계정·광고·분석 서비스를 제공하지 않으며 앱에서 아동의 개인
정보를 의도적으로 수집하지 않습니다. 다만 업데이트·WebView2·사용자가 직접 이용하는 외부
서비스에는 해당 사업자의 정책이 적용됩니다.

### 10. 방침 변경과 문의

네트워크 동작, 로컬 저장 항목, 배포 방식 또는 법적 요구가 바뀌면 이 문서와 공식 제품 페이지를
갱신하고 최종 수정일을 변경합니다.

- 제품 페이지: [https://pcssak.com/biuja](https://pcssak.com/biuja)
- 개인정보 문의: `pcssakinc@gmail.com`

---

## English reference translation

### 1. Summary

PCssak Biuja processes file organization **100% locally**. It does not upload files, file
contents, filenames, folder paths, sorting decisions, or work journals to a PCSSAK server. Free
Early Access has no PCSSAK account, advertising, analytics, tracking SDK, cloud file index, or
automatic crash upload.

“Local processing” does not mean that the application never uses a network. The limited
delivery and contact exceptions are:

1. an automatic request for the official GitHub update `latest.json` approximately 3.5 seconds
   after application startup;
2. download of an official GitHub update asset only after the user approves it;
3. installation, repair, or independent updating of Microsoft Edge WebView2 Runtime when
   required; and
4. an external website, GitHub Issue, or email that the user chooses to open.

PCssak Biuja does not include file contents, filenames, folder paths, or work-journal data in
these requests.

### 2. Information the application does not collect for PCSSAK

The public Free Early Access application does not automatically send to PCSSAK or collect in a
central PCSSAK database the files being organized; file contents; filenames; full folder paths;
directory listings; rules; previews; journal or rollback records; product-usage analytics;
automatically uploaded error logs; account information; login information; payment details; or
paid-license information.

The current free build does not process payment or collect a purchase email in the application.
If a separate paid feature is released later, this policy and the relevant terms must be updated
after the actual processing and distribution model is decided.

### 3. GitHub automatic update check and download

Approximately **3.5 seconds after startup**, the standalone GitHub build automatically requests
the official release manifest:

- `https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest/download/latest.json`

The public manifest supplies update version, signature, and asset-location information. PCssak
Biuja does not put file contents, filenames, folder paths, sorting rules, previews, or work
journals in this request.

As with an ordinary internet request, GitHub may process the user's IP address and customary
request and security metadata such as request time, requested URL, and User-Agent. GitHub
performs that processing independently under the
[GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
PCSSAK operates no separate tracking server or analytics identifier for this update check.

Finding a new version does not automatically download the installer asset. PCssak Biuja
downloads the official GitHub release asset only after the user explicitly approves download
and installation. GitHub may again process the IP address and ordinary request metadata. The
application verifies the PCSSAK Tauri updater signature before installation.

If GitHub is unavailable or the network is blocked, startup handles the automatic-check failure
silently and the core local sorting workflow should remain available. Blocking the connection
prevents update checking and downloading.

### 4. Microsoft WebView2 connection

PCssak Biuja requires Microsoft Edge WebView2 Runtime to display its interface. If the Runtime
is absent or requires installation or repair, Windows or the official Microsoft bootstrapper
bundled with the installer can connect to Microsoft's distribution service. The installed
Runtime can use Microsoft's independent updating process.

PCssak Biuja does not include organized files, filenames, folder paths, or the work journal in a
WebView2 installation request. Microsoft may process IP address and ordinary installation or
request metadata under the
[Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement). Installation or
startup may not complete offline when a required Runtime is not already available.

### 5. Local data stored on the device

The following data remains on the user's Windows device and is not automatically uploaded to
PCSSAK. Displayed paths can vary slightly by Windows version and installation environment.

| Data | Typical location | Contents and retention |
|---|---|---|
| Settings | `%APPDATA%\com.pcssak.biuja\config.json` | User-selected folder paths, organization rules, schedules, language, theme, and related settings. A damaged configuration can produce a backup beside it. |
| Work journal | `%APPDATA%\com.pcssak.biuja\journal.db` and SQLite companion files | Source and destination paths, operation type, time, status, and size, modification time, file identity, and fingerprint evidence needed for safe rollback. The current implementation keeps up to 20,000 action rows and prunes older rows. It is not a copy of file contents. |
| Local logs | `%LOCALAPPDATA%\com.pcssak.biuja\logs` | Technical startup and error diagnostics. A local path or operation-related technical context can appear in an error case, but logs are not automatically uploaded. |
| WebView2 data | `%LOCALAPPDATA%\com.pcssak.biuja\EBWebView` and related app-specific WebView2 locations | Microsoft WebView2 cache and settings needed to render the interface. |
| Window and startup state | App-specific local settings and, when enabled by the user, Windows startup registration | Window size and position and whether to launch at Windows sign-in. |

Journal fingerprints are local evidence used for safe operation and rollback decisions. They are
not sent to PCSSAK, and the journal is not a file copy or backup.

### 6. Information the user chooses to send or publish

When a user opens a GitHub Issue or emails `pcssakinc@gmail.com`, GitHub or the email provider
processes what the user enters, and PCSSAK receives it to handle the request. This is a
user-initiated action, not automatic application collection.

Do not send real full paths, filenames, directory listings, file contents, customer data,
passwords, tokens, private keys, or confidential business material. Use a synthetic example and
redacted screenshot. Follow `SECURITY.md` for a private vulnerability report.

PCSSAK uses contact information and report contents for support, reproduction, security
response, and necessary recordkeeping. A deletion request can be sent to
`pcssakinc@gmail.com`; minimal information needed for a legal obligation, security
investigation, or dispute may be retained for the permitted period.

### 7. Deleting local data

The current journal keeps up to 20,000 action rows and prunes older rows beyond the limit.
Settings, logs, and WebView2 data can remain until the user removes them or selects deletion
during uninstall.

The NSIS uninstaller offers a **Delete app data** option. If it is not selected, local data can
remain for an update or reinstallation. After fully closing and uninstalling the application,
the user can also remove:

- `%APPDATA%\com.pcssak.biuja`
- `%LOCALAPPDATA%\com.pcssak.biuja`

Deleting these folders permanently removes settings and the journal, so review any needed
records first. Files in the Windows Recycle Bin and actual user folders organized by PCssak
Biuja are separate from these app-data folders and are not removed with application data.

### 8. Independent third parties and possible international processing

PCSSAK does not sell application-usage data to advertisers or data brokers. GitHub provides the
update-delivery service, Microsoft provides WebView2, and the user chooses any email or GitHub
Issue interaction. Each provider can process ordinary network or contact data in countries or
regions used by its infrastructure and policies. Consult each provider's official privacy
statement for the applicable scope and rights.

### 9. Children's privacy

PCssak Biuja does not provide a child-directed account, advertising, or analytics service and
does not intentionally collect children's personal information in the application. External
update, WebView2, and user-initiated services remain subject to their providers' policies.

### 10. Changes and contact

If network behavior, local storage, distribution, or legal requirements change, this document
and the official product page will be updated with a new last-updated date.

- Product page: [https://pcssak.com/biuja](https://pcssak.com/biuja)
- Privacy inquiry: `pcssakinc@gmail.com`
