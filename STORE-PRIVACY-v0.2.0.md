# PCssak Biuja Privacy Policy / 개인정보 처리방침

- Last updated / 최종 수정: 2026-10-02
- Operator / 운영자: PCSSAK
- Contact / 문의: `pcssak@pcssak.com`
- Applies to / 적용 대상: PCssak Biuja v0.2.0 for Windows — Microsoft Store Early Access

> The Korean text is authoritative to the extent permitted by applicable law; the English text
> is a reference translation. [The previous policy](docs/LEGACY-v0.1.x-PRIVACY.md) remains available
> for existing v0.1.x free versions.
>
> 적용 법률이 허용하는 범위에서 국문을 기준으로 하며 영문은 참고 번역입니다.
> 기존 v0.1.x 무료판에는 [이전 처리방침](docs/LEGACY-v0.1.x-PRIVACY.md)을 확인하세요.

## 국문

### 1. 파일 정리와 외부 연결

파일 검사·분류·이동·복사·휴지통 보내기·되돌리기는 사용자 기기에서 로컬로 처리합니다.
앱은 파일 내용·이름·폴더 경로·규칙·미리보기·작업저널을 PCSSAK 서버로 **자동 전송하지 않습니다**.
PCSSAK 앱 계정, 광고, 사용 분석·추적 SDK, 클라우드 파일 색인이나 자동 오류 업로드가 없습니다.
파일을 안전하게 식별하고 되돌리기를 판단하기 위해 일부 파일의 내용에서 로컬 해시를 계산할 수
있으며 이 해시도 자동 전송하지 않습니다.

로컬 처리가 모든 네트워크 연결이 없다는 뜻은 아닙니다. Store판에서는 Microsoft Store가
계정·결제·사용권·설치·업데이트를 처리합니다. Microsoft WebView2와 사용자가 직접 여는 외부
링크·문의 서비스도 각각 연결될 수 있습니다. 이 연결에 앱이 정리한 파일 데이터를 첨부하지 않습니다.

### 2. Microsoft Store 계정·결제·사용권

Store에서 로그인하거나 체험·구매·환불·설치·업데이트를 이용하면 Microsoft가 해당 서비스 제공에
필요한 계정·거래·기기·연결 정보를 처리합니다. 구체적인 정보, 보관, 권리와 지역별 처리에는
[Microsoft 개인정보처리방침](https://privacy.microsoft.com/privacystatement),
[Microsoft 서비스 계약](https://www.microsoft.com/servicesagreement)과 해당 지역의
[Store 판매 약관](https://www.microsoft.com/ko-KR/store/b/terms-of-sale)이 적용됩니다.

앱은 Windows의 `StoreContext`를 통해 앱 사용권이 활성인지, 체험인지, 체험 종료 시각이 언제인지
조회합니다. 현재 구현은 이 조회로 Microsoft 계정 이메일·암호·카드 번호·결제 수단을 받아
앱 데이터에 저장하지 않습니다. 구매 단추는 Microsoft Store 상품 화면을 열며 PCSSAK의 자체
결제 화면이나 기기 코드 입력 화면을 사용하지 않습니다.

앱이 조회한 Store 사용권은 실행 중 메모리에서 처리하며 PCSSAK 서버로 자동 전송하지 않습니다.
실행 중 일시 조회 오류가 있으면 같은 실행에서 확인한 상태를 유지하지만 Store 구매 상태를
디스크에 별도로 저장하지 않습니다. 앱을 다시 시작하면 다시 조회하며, 조회하지 못하면 기기에
남은 로컬 체험 기록으로 판정할 수 있습니다. 명시적인 Store 만료·권한 회수 응답은 따릅니다.

Microsoft가 판매자에게 제공하는 거래·정산·보고 정보에는 Microsoft의 관련 계약과 정책이
적용됩니다. 이는 앱이 사용자 파일이나 사용 분석을 수집한다는 뜻이 아닙니다.

### 3. 기기 코드와 로컬 체험 기록

Store판도 기존 설치형과의 호환성과 일시 Store 조회 실패 시 체험 판정을 위해 로컬 체험 기록과
제품 전용 기기 코드를 만듭니다. Windows `MachineGuid`를 읽어 제품별 해시로 기기 코드를 계산하며
원문 MachineGuid를 앱 파일에 저장하거나 PCSSAK에 자동 전송하지 않습니다. Store 구매에는
이 코드를 입력하거나 PCSSAK에 보내지 않아도 됩니다.

`trial.json`과 현재 사용자 레지스트리 `HKCU\Software\PCssak\Biuja`의 `TrialRecord` 값에는 체험
시작·마지막 확인 시각·기록 버전·기존 사용자 여부와 기기 코드로 만든 검증값을 저장합니다.
파일 내용·이름·경로·Microsoft 계정이나 결제 정보는 포함하지 않습니다. 한쪽을 지우거나
재설치해도 남은 기록을 사용할 수 있으며 체험이 새로 시작된다고 보장하지 않습니다.

큰 시계 되돌림은 체험 판정을 잠시 중지할 수 있습니다. 시험판은 별도 앱 식별자와 레지스트리
하위 키를 사용합니다. 이 기록은 자동 전송되지 않고 시간 기준으로 자동 삭제되지 않습니다.

### 4. 로컬 데이터와 보관

아래 위치는 Windows에서 사용하는 일반적인 앱별 경로입니다. Store 패키지는 Windows의 앱 데이터
리디렉션으로 `%LOCALAPPDATA%\Packages\<PackageFamilyName>` 아래에 데이터를 둘 수 있어 실제 위치가
설치 방식·Windows 버전에 따라 달라질 수 있습니다. 해당 PC의 앱별 경로를 확인하세요.

| 데이터 | 일반적인 위치 | 내용과 보관 |
|---|---|---|
| 설정과 가져오기 복구 | `%APPDATA%\com.pcssak.biuja\config.json`, `config.before-import.json`, `config.before-import.pending.json` | 폴더 경로·규칙·예약·언어·테마 등. 가장 최근 가져오기 직전·직후 설정은 안전한 가져오기 되돌리기를 위해 보관할 수 있음. 시간 기준 만료는 없으며 성공한 되돌리기·오래된 복구점 거부·다음 가져오기 정리 또는 수동 삭제로 제거됨. 손상된 설정의 별도 백업도 생길 수 있음. |
| 작업저널과 복사 증명 | `%APPDATA%\com.pcssak.biuja\journal.db`와 SQLite 동반 파일 | 원본·목적지·작업 종류·시각·상태·크기·수정 시각·파일 식별자·해시와 복구 위치. 파일 사본은 아님. 약 20,000건을 넘으면 오래된 종료 기록을 정리하지만 진행 중·미확정·따로 둔 복구 기록은 보존할 수 있음. 중복 복사를 막는 `copy_evidence`는 화면 이력 정리 뒤에도 남으며 시간 기준 만료가 없음. |
| 체험 기록 | 같은 앱별 폴더의 `trial.json`, 위 `TrialRecord` 레지스트리 값 | 3절의 체험 시각과 검증 정보. 자동 만료·삭제되지 않으며 앱 데이터 삭제 후에도 레지스트리 값이 남을 수 있음. |
| 호환성용 사용권 | 같은 앱별 폴더의 `license.json`, `license.json.surface` | 이전 설치형에서 활성화한 PB1 또는 PB2 키가 존재할 수 있음. 키 원문은 이메일·사용권과 PB2의 기기 코드를 포함할 수 있고 별도 암호화 없이 Windows 사용자 프로필 권한에 의존함. 라이선스 해제나 수동 삭제 전까지 남을 수 있음. surface는 계정 정보 없는 고정 재활성화 화면 표식이며 사용권을 부여하지 않음. Store 구매 자체는 이 파일에 키를 발급하지 않음. |
| 로컬 로그 | `%LOCALAPPDATA%\com.pcssak.biuja\logs` 또는 앱별 로그 폴더 | 시작·오류 진단. 오류 상황에서 로컬 경로와 기술적 작업 정보가 포함될 수 있음. 자동 업로드 없음; 수동 삭제 전까지 남을 수 있음. |
| WebView2·창 상태 | 앱별 WebView2 데이터와 설정 폴더 | 화면 캐시·환경설정·창 크기와 위치 등. Microsoft Runtime과 앱 설정에 따라 유지되며 제거·초기화·수동 삭제로 제거될 수 있음. |
| 시작 프로그램 | Store 패키지의 Windows 시작 작업 등록 | 사용자가 켜는 로그인 자동 시작 상태. Windows 설정에서도 관리 가능. |

이 정보는 PCSSAK에 자동 업로드되지 않습니다. 호환성 PB1/PB2 키에 포함된 이메일과 기기 코드도
`license.json`에 로컬 저장되며 자동 전송되지 않습니다. 사용권 키가 있는 설치형의 라이선스 해제는
해당 키 파일을 삭제하고, Store판에서 키 화면이 없으면 앱을 완전히 종료한 뒤 해당 로컬 파일을
삭제할 수 있습니다. Store 구매·환불·Microsoft 계정 삭제는 별도로 Microsoft에서 관리해야 합니다.

### 5. 업데이트와 WebView2

Store판은 Microsoft Store를 통해 업데이트하며 앱의 GitHub `latest.json` 자체 확인·다운로드를
사용하지 않습니다. Store와 Windows 설정에 따라 업데이트가 자동 설치될 수 있습니다.
기존 v0.1.x 직접 설치형의 GitHub 업데이트 처리는 [이전 정책](docs/LEGACY-v0.1.x-PRIVACY.md)을 따릅니다.

화면 표시에 필요한 Microsoft Edge WebView2 Runtime의 설치·복구·독립적인 업데이트는 Microsoft
서비스에 연결될 수 있습니다. Microsoft는 IP 주소와 일반 설치·요청 메타데이터를 자체 정책으로
처리할 수 있습니다. 앱은 WebView2 설치 요청에 정리 대상 파일·이름·경로·저널을 넣지 않습니다.
필요한 Runtime이 없고 인터넷도 차단돼 있으면 설치 또는 실행을 완료하지 못할 수 있습니다.

### 6. 직접 보내는 문의와 외부 서비스

홈페이지·GitHub Issue·이메일을 열고 내용을 보내면 사용자가 선택한 외부 서비스가 그 내용과
일반 연결 정보를 처리하고, PCSSAK은 전달된 문의를 지원·재현·보안 대응·필요한 기록 보관을 위해
처리합니다. 이는 자동 앱 수집과 별개입니다. GitHub에는
[GitHub 개인정보 보호정책](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)이
적용됩니다. `pcssak@pcssak.com` 수신 메일은 Cloudflare Email Routing을 통해 Gmail 수신함으로
전달되어 이 업체가 전달·보안에 필요한 내용을 처리할 수 있습니다.

실제 파일·전체 경로·파일 목록·고객 자료·암호·토큰·개인키·결제 정보는 보내지 마세요.
가상의 예시와 가린 화면을 사용하고 보안 문제는 [보안 정책](SECURITY.md)의 비공개 신고 경로를
따르세요. 문의 기록 삭제는 `pcssak@pcssak.com`으로 요청할 수 있으며 법적 의무·보안 조사·분쟁에
필요한 최소 정보는 해당 사유에 필요한 기간 보관할 수 있습니다.

### 7. 로컬 데이터 삭제

Store 앱 제거·초기화는 Windows의 패키지 데이터 정책을 따르며 데이터가 제거되거나 일부가 남을
수 있습니다. 모든 기록이 반드시 보존된다고 약속하지 않습니다. 제거·초기화 전에 필요한 기록을
확인하고 설정을 내보내세요. 기존 NSIS 직접 설치형의 제거기는 앱 데이터를 보존합니다.

앱을 완전히 종료한 뒤 위 앱별 데이터 폴더와 Store 패키지별 데이터를 확인해 사용자가 수동
삭제할 수 있습니다. 현재 사용자 레지스트리의 앱별 `TrialRecord`는 파일 삭제나 제거 뒤에도
남을 수 있습니다. 완전 삭제가 필요하면 다른 앱의 값에 영향을 주지 않도록 해당 값만 확인해
삭제하거나 문의하세요. Windows의 원본 MachineGuid는 앱 데이터가 아니므로 삭제하지 마세요.

삭제하면 설정·사용권 키·복구 기록·중복 복사 증명이 사라질 수 있습니다. 휴지통과 실제로
정리한 파일은 별개이며 앱 데이터 삭제로 되돌려지거나 삭제되지 않습니다. Microsoft 계정·
거래·사용권 정보의 삭제·환불 요청은 Microsoft의 절차를 따릅니다.

### 8. 제3자·국외 처리·아동

PCSSAK은 앱 사용 데이터를 광고업자나 데이터 중개업자에게 판매하지 않습니다. Microsoft,
GitHub, Cloudflare와 Gmail 등 외부 서비스는 각 정책과 인프라에 따라 여러 국가·지역에서 연결
또는 문의 정보를 처리할 수 있습니다. 해당 공식 처리방침에서 처리 범위와 권리를 확인하세요.

앱은 아동 대상 계정·광고·분석 서비스를 제공하거나 앱에서 아동 개인정보를 의도적으로 수집하지
않습니다. Microsoft Store 계정·구매·가족 기능과 외부 서비스에는 각 제공자의 정책이 적용됩니다.

### 9. 변경과 문의

로컬 저장·연결·배포·법적 요구가 바뀌면 이 문서와 공식 제품 페이지의 최종 수정일을 갱신합니다.
제품 페이지: [https://pcssak.com/biuja](https://pcssak.com/biuja). 개인정보 문의: `pcssak@pcssak.com`.

---

## English reference translation

### 1. Local organization and connections

Inspection, classification, moves, copies, recycling, and rollback run locally on the user's
device. The app does not automatically send file contents, filenames, paths, rules, previews,
or the journal to a PCSSAK server. There is no PCSSAK app account, advertising, usage-analytics
or tracking SDK, cloud file index, or automatic error upload. Local content hashes used to
identify files and evaluate safe rollback are not uploaded automatically.

Local processing does not mean no network use. **Microsoft Store handles account, payment,
licensing, installation, and updates**. Microsoft WebView2 and user-opened external links or
support services may also connect. The app does not attach organized file data to these requests.

### 2. Microsoft Store account, payment, and entitlement

Microsoft processes account, transaction, device, and connection information needed for Store
sign-in, trials, purchases, refunds, installation, and updates under the
[Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement),
[Microsoft Services Agreement](https://www.microsoft.com/servicesagreement), and applicable
regional [Store Terms of Sale](https://www.microsoft.com/en-us/store/b/terms-of-sale).

Through Windows `StoreContext`, the app queries whether its entitlement is active, whether it
is a trial, and the trial expiry. The current implementation does not obtain or store a
Microsoft account email, password, card number, or payment method through that query. The
purchase button opens the Microsoft Store product page, without a PCSSAK checkout or device-code form.

The queried Store entitlement is handled in session memory and is not uploaded automatically
to PCSSAK. A temporary query failure preserves a status checked during that session; purchased
Store status is not separately saved to disk. Restart queries again and can fall back to a
remaining local trial when unavailable. Explicit Store expiry and revocation responses apply.

Transaction, settlement, and reporting information Microsoft provides to sellers follows the
relevant Microsoft agreements and policies. It is separate from collecting user files or app analytics.

### 3. Device code and local trial

For standalone compatibility and trial decisions during a Store-query failure, the Store build
also creates a local trial record and product-specific device code. It reads Windows
`MachineGuid` and hashes it for this product. The original MachineGuid is not stored in app files
or uploaded automatically to PCSSAK. Store purchase does not require entering or sending that code.

`trial.json` and the `TrialRecord` value under the current-user registry key
`HKCU\Software\PCssak\Biuja` store trial start and last-seen times, record version, legacy-user
status, and verification data derived from the device code. They contain no file data, paths,
Microsoft account, or payment information. Removing one copy or reinstalling can use the
remaining record and is not promised to restart the trial.

A large clock rollback can temporarily suspend the trial decision. Test builds use separate
app identifiers and registry subkeys. The records are not automatically transmitted or deleted
on a time-based schedule.

### 4. Local data and retention

Typical Windows paths appear below. Store-package redirection may place data under
`%LOCALAPPDATA%\Packages\<PackageFamilyName>`; actual locations vary by installation method and
Windows version. Check the app-specific locations on the device.

| Data | Typical location | Content and retention |
|---|---|---|
| Settings and import recovery | `%APPDATA%\com.pcssak.biuja\config.json`, `config.before-import.json`, `config.before-import.pending.json` | Folder paths, rules, schedules, language, and theme. The latest import's before/after settings can be kept for safe Import Undo. No time-based expiry; removal follows successful undo, rejection of a stale point, the next import's cleanup, or manual deletion. Damaged settings can produce a separate backup. |
| Journal and copy evidence | `%APPDATA%\com.pcssak.biuja\journal.db` and SQLite companions | Source/destination paths, operations, times, status, size, modification time, identity, hashes, and recovery locations, not file copies. Older finalized rows are pruned after approximately 20,000 rows; active, pending, and set-aside recovery records can remain. `copy_evidence` preventing duplicate copies survives visible-history pruning and has no time-based expiry. |
| Trial | App-specific `trial.json` and registry `TrialRecord` | The dates and verification information in section 3. No automatic expiry or deletion; the registry value can remain after app files are deleted. |
| Compatible license | App-specific `license.json`, `license.json.surface` | An existing standalone PB1 or PB2 key can be present. The full key can include email, entitlement, and a PB2 device code; it is not separately encrypted and relies on Windows profile permissions. It can remain until license deactivation or manual deletion. The surface marker is a fixed, non-account marker for a reactivation screen and grants no entitlement. A Store purchase does not issue a key into this file. |
| Local logs | `%LOCALAPPDATA%\com.pcssak.biuja\logs` or the app-specific log directory | Startup/error diagnostics can include local paths and technical operation context. No automatic upload; data can remain until manual deletion. |
| WebView2 and window state | App-specific WebView2 and settings folders | Rendering cache, preferences, window size/position. Retention and removal follow Runtime, app, uninstall/reset, and manual deletion behavior. |
| Startup state | The package's Windows startup-task registration | User-enabled sign-in launch, also managed through Windows settings. |

This data is not uploaded automatically to PCSSAK. The email and device code in compatible
PB1/PB2 keys are stored locally in `license.json`, not transmitted automatically. Standalone
license deactivation deletes the key file; if the Store build has no key screen, fully close
the app and remove that local file manually. Store purchases, refunds, and Microsoft-account
deletion are managed separately by Microsoft.

### 5. Updates and WebView2

The Store build uses Microsoft Store updates, not the app's GitHub `latest.json` check or
download. Updates may install automatically according to Store and Windows settings. Existing
v0.1.x standalone GitHub update behavior is described in the [previous policy](docs/LEGACY-v0.1.x-PRIVACY.md).

Installation, repair, and independent updating of the required Microsoft Edge WebView2 Runtime
can connect to Microsoft services. Microsoft can process IP addresses and ordinary request or
installation metadata under its policies. The app does not include organized files, names,
paths, or the journal in Runtime installation requests. Installation or launch may not complete
offline if a required Runtime is absent.

### 6. User-initiated support and external services

Opening and submitting a website, GitHub Issue, or email lets the chosen service process entered
contents and ordinary connection information. PCSSAK uses received requests for support,
reproduction, security response, and necessary recordkeeping, separately from automatic app
collection. GitHub follows its [Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
Mail to `pcssak@pcssak.com` is forwarded through Cloudflare Email Routing to a Gmail inbox;
those providers can process contents needed for delivery and security.

Do not send real files, full paths, directory listings, customer data, passwords, tokens,
private keys, or payment information. Use synthetic examples and redacted images, and follow
the [Security Policy](SECURITY.md) for private vulnerability reporting. Contact
`pcssak@pcssak.com` to request deletion of support records; minimal information required for
legal duties, security investigations, or disputes can be retained as needed for those purposes.

### 7. Deleting local data

Store uninstall/reset follows Windows package-data policies: some data may be deleted or
remain. Preservation of all records is not promised. Review needed history and export settings
before uninstall or reset. The existing NSIS standalone uninstaller preserves app data.

After fully closing the app, inspect and manually delete its app-specific and package-specific
data. The current-user app-specific `TrialRecord` registry value can remain after deleting
files or uninstalling. For complete removal, remove only the app's own value without affecting
other apps, or request assistance. Windows' original MachineGuid is not app data; do not delete it.

Deletion can remove settings, license keys, recovery records, and duplicate-copy evidence.
Organized user files and the Recycle Bin are separate; deleting app data does not undo or delete
them. Microsoft-account, transaction, entitlement deletion, and refunds follow Microsoft's procedures.

### 8. Third parties, international processing, and children

PCSSAK does not sell app-usage data to advertisers or data brokers. Microsoft, GitHub,
Cloudflare, Gmail, and other chosen providers can process connection or contact data in countries
or regions used by their infrastructure and policies. Consult their official policies for scope
and rights.

The app provides no child-directed account, advertising, or analytics service and does not
intentionally collect children's personal data in the app. Store accounts, purchases, family
features, and external services remain subject to their providers' policies.

### 9. Changes and contact

Changes to storage, connections, distribution, or legal requirements will update this policy
and the official product page with a new date. Product page:
[https://pcssak.com/biuja](https://pcssak.com/biuja). Privacy contact: `pcssak@pcssak.com`.
