# PCssak Biuja Privacy Policy / 개인정보 처리방침

- Last updated / 최종 수정: 2026-11-28
- Operator / 운영자: PCSSAK
- Contact / 문의: `pcssak@pcssak.com`
- Applies to / 적용 대상: PCssak Biuja v0.5.0 for Windows — Microsoft Store Early Access

> The Korean text is authoritative to the extent permitted by applicable law; the English text
> is a reference translation. [The previous policy](docs/LEGACY-v0.1.x-PRIVACY.md) remains available
> for existing v0.1.x free versions.
>
> 적용 법률이 허용하는 범위에서 국문을 기준으로 하며 영문은 참고 번역입니다.
> 기존 v0.1.x 무료판에는 [이전 처리방침](docs/LEGACY-v0.1.x-PRIVACY.md)을 확인하세요.

윈도우 0.5.0 스토어판의 비공개 배포를 준비하면서 공개하는 방침입니다. 고객지원 메일을 보내기 전에 6절의 삭제 절차와 8절의 국외 처리 범위를 확인할 수 있습니다.

This policy describes the Windows 0.5.0 Store edition being prepared for private distribution. Before contacting support, you can review how inquiries are deleted in section 6 and where providers may process them in section 8.

## 국문

### 1. 파일 정리와 외부 연결

파일 검사·분류·이동·복사·휴지통 보내기·되돌리기는 사용자 기기에서 로컬로 처리합니다.
앱은 파일 내용·이름·폴더 경로·규칙·미리보기·작업저널을 PCSSAK 서버로 **자동 전송하지 않습니다**.
PCSSAK 앱 계정, 광고, 사용 분석·추적 SDK나 클라우드 파일 색인은 없으며, PCSSAK 자체 자동 오류
업로드 기능도 없습니다. Microsoft WebView2 Runtime의 별도 진단·충돌 보고는 5절을 확인하세요.
파일을 안전하게 식별하고 되돌리기를 판단하기 위해 일부 파일의 내용에서 로컬 해시를 계산할 수
있으며 이 해시도 자동 전송하지 않습니다.

로컬 처리가 모든 네트워크 연결이 없다는 뜻은 아닙니다. Store판에서는 Microsoft Store가
계정·결제·사용권·설치·업데이트를 처리합니다. Microsoft WebView2와 사용자가 직접 여는 외부
링크·문의 서비스도 각각 연결될 수 있습니다. PCSSAK 자체 기능은 이 연결에 정리 대상 파일
데이터를 자동 첨부하지 않습니다. Runtime의 독립적인 진단 처리는 5절과 Microsoft 정책을 따릅니다.

파일 내용 조건을 설정하면 비우자는 해당 조건을 확인할 수 있는 파일에서 검색어를 기기 안에서
찾습니다. 정리할 위치는 사용자가 정합니다. OneDrive 같은 동기화 폴더에 파일을 복사하거나
이동하면 그 서비스가 동기화 설정에 따라 파일을 업로드할 수 있습니다. 네트워크 공유 폴더를
선택하면 파일과 경로가 해당 파일 서버를 거칠 수 있습니다. 파일을 기기 안에만 두려면
동기화나 네트워크 공유에 연결되지 않은 로컬 폴더를 선택하세요. Windows 또는 다른 백업 앱이 파일·설정을 별도로 복사할 수 있으므로 그 서비스의 백업 대상도 확인하세요.

### 2. Microsoft Store 계정·결제·사용권

Store에서 로그인하거나 체험·구매·환불·설치·업데이트를 이용하면 Microsoft가 해당 서비스 제공에
필요한 계정·거래·기기·연결 정보를 처리합니다. 구체적인 정보, 보관, 권리와 지역별 처리에는
[Microsoft 개인정보처리방침](https://privacy.microsoft.com/privacystatement),
[Microsoft 서비스 계약](https://www.microsoft.com/servicesagreement)과 해당 지역의
[Store 판매 약관](https://www.microsoft.com/ko-KR/store/b/terms-of-sale)이 적용됩니다.

앱은 Windows의 `StoreContext`에서 사용권에 상점 상품 식별값이 있는지 확인한 뒤 사용권 활성
여부와 체험 여부를 확인합니다. 체험이면 종료 시각도 조회합니다. 현재 구현은 이 조회로 Microsoft
계정 이메일·암호·카드 번호·결제 수단을 받아 앱 데이터에 저장하지 않습니다. 앱에서 구매 단추를
제공하는 경우 이 단추는 Microsoft Store 상품 화면을 엽니다. Store 구매에는 PCSSAK의 자체
결제 화면이나 기기 코드 입력 화면을 사용하지 않습니다.

앱이 조회한 Store 사용권은 실행 중 메모리에서 처리하며 PCSSAK 서버로 자동 전송하지 않습니다.
실행 중 일시 조회 오류가 있으면 같은 실행에서 확인한 상태를 유지하지만 Store 구매 상태를
디스크에 별도로 저장하지 않습니다. 앱을 다시 시작하면 다시 조회하며, 조회하지 못하면 기기에
남은 로컬 체험 기록으로 판정할 수 있습니다. 명시적인 Store 만료·권한 회수 응답은 따릅니다.
오프라인에서도 Windows는 기기에 보관한 [Store 사용권](https://learn.microsoft.com/en-us/uwp/api/windows.services.store.storecontext.getapplicenseasync)을
반환할 수 있습니다.

출시 후 PCSSAK은 Microsoft가 Partner Center에서 제공하는 취득·설치 건수와 앱 중단·응답 없음
추이를 확인해 배포와 오류 대응에 사용합니다. 정산 담당자는 판매·환불·지급액을 대조할 때
필요한 범위에서 수익 보고서를 확인합니다. 보고서에는 주문·거래 식별값, 금액·통화, 결제 수단의
유형, 거래 지역 또는 세무상 우편번호가 포함될 수 있습니다. 이 자료는 Microsoft가 작성하며,
앱이 정리하는 파일·경로·저널은 PCSSAK이 보고용으로 전송하지 않습니다. 제공 범위는
[Microsoft 앱 통계](https://learn.microsoft.com/en-us/windows/apps/publish/analyze-app-performance/msix)와
[Store 정산 보고서](https://learn.microsoft.com/en-us/partner-center/earnings/earnings-store)에서 확인할 수 있습니다.

구매 내역은 Microsoft 계정의 [주문 기록](https://account.microsoft.com/billing/orders)에서,
환불 조건은 [Microsoft 환불 안내](https://support.microsoft.com/ko-kr/accounts-billing/subscriptions/get-a-refund-for-apps-and-games-purchased-from-microsoft-store)에서
확인하세요. PCSSAK에 카드 번호, 암호, 인증 코드 또는 영수증 사본을 보낼 필요가 없습니다.

### 3. 기기 코드와 로컬 체험 기록

Store판도 기존 설치형과의 호환성과 일시 Store 조회 실패 시 체험 판정을 위해 로컬 체험 기록과
제품 전용 기기 코드를 만듭니다. Windows `MachineGuid`를 읽어 제품별 해시로 기기 코드를 계산하며
원문 MachineGuid를 앱 파일에 저장하거나 PCSSAK에 자동 전송하지 않습니다. Store 구매에는
이 코드를 입력하거나 PCSSAK에 보내지 않아도 됩니다.

`trial.json`과 현재 사용자 레지스트리 `HKCU\Software\PCssak\Biuja\com.pcssak.biuja.store`의
`TrialRecord` 값에는 체험 시작·마지막 확인 시각·기록 버전·기존 사용자 여부와 기기 코드로 만든
검증값을 저장합니다. Windows는 Store 패키지가 쓴 이 값을 패키지 전용 레지스트리에 둘 수 있습니다.
파일 내용·이름·경로·Microsoft 계정이나 결제 정보는 포함하지 않습니다. 한쪽을 지우거나
재설치해도 남은 기록을 사용할 수 있으며 체험이 새로 시작된다고 보장하지 않습니다.

큰 시계 되돌림은 체험 판정을 잠시 중지할 수 있습니다. Store판과 시험판은 각자의 앱 식별자와
레지스트리 하위 키를 사용합니다. 기본 키 `HKCU\Software\PCssak\Biuja`의 `TrialRecord`와
`com.pcssak.biuja` 폴더는 직접 설치형(NSIS) 앱의 기록입니다. 이 기록은 자동 전송되지 않고 시간 기준으로 자동 삭제되지 않습니다.

### 4. 로컬 데이터와 보관

아래 위치는 Windows에서 사용하는 일반적인 앱별 경로입니다. Store 패키지는 Windows의 앱 데이터
리디렉션으로 `%LOCALAPPDATA%\Packages\<PackageFamilyName>` 아래에 데이터를 둘 수 있어 실제 위치가
설치 방식·Windows 버전에 따라 달라질 수 있습니다. 해당 PC의 앱별 경로를 확인하세요.

| 데이터 | 일반적인 위치 | 내용과 보관 |
|---|---|---|
| 설정과 가져오기 복구 | `%APPDATA%\com.pcssak.biuja.store\config.json`, `config.before-import.json`, `config.before-import.pending.json` | 폴더 경로·규칙·예약·언어·테마 등. 가장 최근 가져오기 직전·직후 설정은 안전한 가져오기 되돌리기를 위해 보관할 수 있음. 시간 기준 만료는 없으며 성공한 되돌리기·오래된 복구점 거부·다음 가져오기 정리 또는 수동 삭제로 제거됨. 손상된 설정의 별도 백업도 생길 수 있음. |
| 안전 검사 전 설정 사본 | 같은 설정 폴더의 `config.before-safety-<지문>.json` | 앱 시작 시 안전 검사로 폴더나 규칙이 제외될 때, 제외한 내용을 검토할 수 있도록 기존 설정 원문(폴더 경로·규칙 등)을 보관합니다. 변경이 없으면 만들지 않고, 원문이 같으면 기존 사본을 재사용합니다. 자동 만료·복원·서버 전송은 없습니다. 사본을 직접 검토한 뒤 필요 없으면 삭제할 수 있습니다. 작성 중에는 같은 폴더에 `config.before-safety-<지문>.<임의값>.tmp`를 씁니다. 정상 완료하면 임시 파일은 정리되지만 강제 종료 시 일부 또는 전체 설정이 남을 수 있습니다. 임시 파일도 자동 복원·전송하지 않습니다. |
| 작업저널과 복사 증명 | `%APPDATA%\com.pcssak.biuja.store\journal.db`와 SQLite 동반 파일 | 원본·목적지·작업 종류·시각·상태·크기·수정 시각·파일 식별자·해시와 복구 위치. 파일 사본은 아님. 약 20,000건을 넘으면 오래된 종료 기록을 정리하지만 진행 중·미확정·따로 둔 복구 기록은 보존할 수 있음. 중복 복사를 막는 `copy_evidence`는 화면 이력 정리 뒤에도 남으며 시간 기준 만료가 없음. 자동 정리가 자기 결과를 다시 처리하지 않도록, 정리된 기록 중 완료된 이동의 목적지와 되돌리기로 남은 위치(이동·휴지통 되돌리기의 복원 위치, 복사 되돌리기의 원본 위치)는 경로·크기·수정 시각·파일 식별자만 담은 `automation_output_receipts_v1`에 남음. 이 기록도 시간 기준 만료가 없으며, 같은 경로에서 다른 파일이 확인되거나 사용자가 `journal.db`와 동반 파일을 지울 때 삭제됨. |
| 체험 기록 | 같은 앱별 폴더의 `trial.json`, 위 Store판 하위 키의 `TrialRecord` 레지스트리 값 | 3절의 체험 시각과 검증 정보. 자동 만료·삭제되지 않으며 앱 데이터 삭제 후에도 레지스트리 값이 남을 수 있음. |
| 호환성용 사용권 | 같은 앱별 폴더의 `license.json`, `license.json.surface` | 이 Store 앱에서 PB1 또는 PB2 키를 입력한 경우에만 존재함(직접 설치형에 입력한 키는 옮겨 오지 않음). 키 원문은 이메일·사용권과 PB2의 기기 코드를 포함할 수 있고 별도 암호화 없이 Windows 사용자 프로필 권한에 의존함. 라이선스 해제나 수동 삭제 전까지 남을 수 있음. surface는 계정 정보 없는 고정 재활성화 화면 표식이며 사용권을 부여하지 않음. Store 구매 자체는 이 파일에 키를 발급하지 않음. |
| 로컬 로그 | `%LOCALAPPDATA%\com.pcssak.biuja.store\logs` 또는 앱별 로그 폴더 | 시작·오류 진단. 오류 상황에서 로컬 경로와 기술적 작업 정보가 포함될 수 있음. 자동 업로드 없음; 수동 삭제 전까지 남을 수 있음. |
| WebView2·창 상태 | 앱별 WebView2 데이터와 설정 폴더 | 화면 캐시·환경설정·창 크기와 위치 등. Microsoft Runtime과 앱 설정에 따라 유지되며 제거·초기화·수동 삭제로 제거될 수 있음. |
| 시작 프로그램 | Store 패키지의 Windows 시작 작업 등록 | 사용자가 켜는 로그인 자동 시작 상태. Windows 설정에서도 관리 가능. |

이 정보는 PCSSAK에 자동 업로드되지 않습니다. 호환성 PB1/PB2 키에 포함된 이메일과 기기 코드도
`license.json`에 로컬 저장되며 자동 전송되지 않습니다. 사용권 키가 있는 설치형의 라이선스 해제는
해당 키 파일을 삭제하고, Store판에서 키 화면이 없으면 앱을 완전히 종료한 뒤 해당 로컬 파일을
삭제할 수 있습니다. Store 구매·환불·Microsoft 계정 삭제는 별도로 Microsoft에서 관리해야 합니다.

앱의 폴더·규칙 설정과 기록 화면에서 등록 경로와 최근 작업을 확인할 수 있습니다. 설정을
내보내면 선택한 위치에 폴더 경로·규칙·검색어가 포함될 수 있는 JSON 파일이 생깁니다. 이 파일은
별도로 암호화하지 않으며, 정리한 파일의 내용이나 작업저널을 담지 않습니다. 내보낸 사본은
앱을 제거해도 저장한 위치에 남을 수 있습니다. 공유 전 내용을 확인하고 필요가 없어지면
그 위치에서 삭제하세요. 설정과 저널을 담은 기기의 사용자 계정과 백업도 접근 권한으로 보호하세요.

### 5. 업데이트와 WebView2

Store판은 Microsoft Store를 통해 업데이트하며 앱의 GitHub `latest.json` 자체 확인·다운로드를
사용하지 않습니다. Store와 Windows 설정에 따라 업데이트가 자동 설치될 수 있습니다.
기존 v0.1.x 직접 설치형의 GitHub 업데이트 처리는 [이전 정책](docs/LEGACY-v0.1.x-PRIVACY.md)을 따릅니다.

화면 표시에 필요한 Microsoft Edge WebView2 Runtime의 설치·복구·독립적인 업데이트는 Microsoft
서비스에 연결될 수 있습니다. Microsoft는 IP 주소와 일반 설치·요청 메타데이터를 자체 정책으로
처리할 수 있습니다. 앱은 WebView2 설치 요청에 정리 대상 파일·이름·경로·저널을 넣지 않습니다.
필요한 Runtime이 없고 인터넷도 차단돼 있으면 설치 또는 실행을 완료하지 못할 수 있습니다.

WebView2 Runtime은 보안·성능·안정성 유지를 위한 필수 진단 데이터를 처리할 수 있으며, 선택
진단 데이터는 Windows의 진단 데이터 설정을 따릅니다. WebView2 프로세스가 중단되면 Windows
동의와 Runtime 설정에 따라 충돌 진단 자료가 Microsoft로 전송될 수 있습니다. 이는 PCSSAK의
자체 자동 오류 업로드 기능과 별개이며 PCSSAK이 Microsoft의 진단 자료를 수신한다는 뜻은 아닙니다.
진단 자료에 개인 정보가 전혀 포함되지 않는다고 보장하지 않습니다. 처리 범위와 사용자 제어는
[Microsoft WebView2 개인정보 안내](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/data-privacy)와
[Microsoft 개인정보처리방침](https://privacy.microsoft.com/privacystatement)을 확인하세요.

### 6. 직접 보내는 문의와 외부 서비스

홈페이지·GitHub Issue·이메일을 열고 내용을 보내면 사용자가 선택한 외부 서비스가 그 내용과
일반 연결 정보를 처리합니다. PCSSAK은 받은 문의에 답변하고 문제를 재현하거나 보안 신고를
처리합니다. 공개 GitHub 이슈에 올린 내용은 다른 사람도 볼 수 있고 이메일 삭제와 별개로 게시물에 남을 수 있습니다. GitHub에는
[GitHub 개인정보 보호정책](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)이
적용됩니다.

이메일 문의는 선택 사항입니다. <mailto:pcssak@pcssak.com>으로 보내면 Cloudflare Email Routing이
발신 주소·표시 이름·메일 본문과 첨부 자료를 고객지원에 사용하는 Google의 개인용 Gmail
수신함으로 전달합니다. PCSSAK은 메일 접근을 고객지원 담당자로 제한합니다. 일반 문의는 처리가
끝나면 받은 메일과 답변, 첨부 자료 및 내려받은 사본을 삭제하고 Gmail 휴지통에서도 해당 메일을
영구 삭제합니다. 법령상 보존할 의무가 있는 기록은 필요한 부분만 따로 보관하고 기간 만료 후
파기합니다. 한국 전자상거래법상 PCSSAK에 의무가 있는 소비자 불만·분쟁처리 기록의 보존 기간은
3년입니다. Gmail 휴지통의 일반 보관 한도 30일과 외부 업체의 로그·백업 보관 기간은 별개입니다.
[전자상거래법 시행령 제6조](https://www.law.go.kr/LSW/lsLawLinkInfo.do?chrClsCd=010202&lsJoLnkSeq=900619372) ·
[Gmail 메일 삭제 안내](https://support.google.com/mail/answer/7401?hl=ko)

파일 정리 문제는 앱 버전, Windows 버전, 가상의 파일명으로 재현한 단계와 오류 문구로 문의할 수
있습니다. 실제 파일·전체 경로·파일 목록·설정 백업·사용권 키·고객 자료·암호·토큰·개인키·결제 정보는
보내지 마세요. 화면이 필요하면 식별 정보를 가리고 보안 문제는 [보안 정책](SECURITY.md)의 비공개 신고 경로를
따르세요. 본인 또는 법정대리인은 고객지원 개인정보 담당자에게 이메일로 문의 자료의 열람·정정·
삭제·처리 정지를 요청할 수 있습니다. 문의를 보낸 날짜와 회신 주소를 알려 주시면 본인이나
대리 권한을 확인하고 처리 결과를 안내합니다. 법령에 따라 요청을 제한하는 경우 사유를 안내합니다.
한국의 침해 상담·분쟁조정 기관은 [개인정보 포털](https://www.privacy.go.kr/front/contents/cntntsView.do?contsNo=408)에서
확인할 수 있습니다. 거주 지역의 개인정보 보호 감독기관에도 문의할 수 있습니다.

### 7. 로컬 데이터 삭제

Store 앱 제거·초기화는 Windows의 패키지 데이터 정책을 따르며 데이터가 제거되거나 일부가 남을
수 있습니다. 모든 기록이 반드시 보존된다고 약속하지 않습니다. 제거·초기화 전에 필요한 기록을
확인하고 설정을 내보내세요. 기존 NSIS 직접 설치형의 제거기는 앱 데이터를 보존합니다.

앱을 완전히 종료한 뒤 위 앱별 데이터 폴더와 Store 패키지별 데이터를 확인해 사용자가 수동
삭제할 수 있습니다. 현재 사용자 레지스트리의 앱별 `TrialRecord`는 파일 삭제나 제거 뒤에도
남을 수 있습니다. 완전 삭제가 필요하면 다른 앱의 값에 영향을 주지 않도록 해당 값만 확인해
삭제하거나 문의하세요. 직접 설치형도 쓰는 PC에서는 기본 키 `HKCU\Software\PCssak\Biuja`의
`TrialRecord`와 `com.pcssak.biuja` 폴더가 직접 설치형의 설정·사용권·되돌리기 기록이므로 Store 앱
데이터를 지울 때 삭제하지 마세요. Windows의 원본 MachineGuid는 앱 데이터가 아니므로 삭제하지 마세요.

삭제하면 설정·사용권 키·복구 기록·중복 복사 증명이 사라질 수 있습니다. 휴지통과 실제로
정리한 파일은 별개이며 앱 데이터 삭제로 되돌려지거나 삭제되지 않습니다. Microsoft 계정·
거래·사용권 정보의 삭제·환불 요청은 Microsoft의 절차를 따릅니다.

### 8. 제3자·국외 처리·아동

PCSSAK은 앱 사용 데이터를 광고업자나 데이터 중개업자에게 판매하지 않습니다. 외부 서비스는
각자의 인프라에 따라 연결 또는 문의 정보를 여러 국가·지역에서 처리할 수 있습니다.

지원 주소에 메일을 보낼 때 Cloudflare, Inc.의 Email Routing이 발신·수신 주소, 표시 이름, 제목,
본문 및 사용자가 직접 첨부한 자료를 Google LLC의 Gmail 수신함으로 전송합니다. Cloudflare는
전달하는 메일 본문을 저장하지 않는다고 안내합니다. 활동 로그에는 전달·인증 결과 등이 표시될 수 있습니다.
관리 화면에서 최근 30일을 선택해 조회할 수 있으며, Cloudflare가 이 지원 주소의 로그와 사본을 최종 삭제하는 시점과 처리 국가는 아직 확인되지 않았습니다.

Google은 전 세계 서버에서 정보를 처리할 수 있으며 이 고객지원용 개인 Gmail 계정의 저장 국가를 특정할 수 없다고 답했습니다.
문의와 답변은 수신함에 보관되고, PCSSAK은 6절에 따라 처리합니다. Google의 일반 정책상 삭제 요청부터 서버의 안전한 삭제까지는 통상 약 2개월이 걸리며,
재해 복구용 암호화 백업에는 최대 6개월 남을 수 있습니다. 보안·법적 의무 등으로 일부 정보를 더 오래 보관할 수 있습니다.
이는 이 계정의 개별 메일에 대한 삭제 완료일을 보장하는 기간이 아닙니다. 개인정보 문의 창구는 아래
각 업체의 방침에서 확인할 수 있습니다. 메일을 보내지 않아도 앱의 정리·되돌리기를 이용할 수
있습니다. 이 경우 해당 문의가 접수되지 않아 이메일 답변은 제공되지 않습니다.
[Cloudflare 전달 서비스](https://www.cloudflare.com/products/email-routing/) · [메일 활동 로그](https://developers.cloudflare.com/email-service/observability/logs/) · [Google의 보관·삭제](https://policies.google.com/technologies/retention?hl=ko).
지원 메일에 관여하는 업체의 운영 범위와 권리는
[Cloudflare 개인정보처리방침](https://www.cloudflare.com/privacypolicy/)과
[Google 개인정보처리방침](https://policies.google.com/privacy?hl=ko)에서 확인하세요.

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
or tracking SDK, or cloud file index. PCSSAK has no automatic error-upload feature of its own.
See section 5 for the separate diagnostics and crash reporting of Microsoft WebView2 Runtime.
Local content hashes used to identify files and evaluate safe rollback are not uploaded automatically.

Local processing does not mean no network use. **Microsoft Store handles account, payment,
licensing, installation, and updates**. Microsoft WebView2 and user-opened external links or
support services may also connect. PCSSAK features do not automatically attach files being organized
to these requests. Independent Runtime diagnostics follow section 5 and Microsoft policies.

If you set a file-content condition, Biuja looks for your search terms on your device in files
it can inspect. You choose where files go. Moving or copying a file to a synced folder such as
OneDrive can cause the sync provider to upload it according to your settings. Selecting a
network share can send files and paths to that file server. To keep files on the device,
choose a local folder outside synced locations and network shares. Windows or another backup service may independently copy files or settings. Review the locations included in those backups.

### 2. Microsoft Store account, payment, and entitlement

Microsoft processes account, transaction, device, and connection information needed for Store
sign-in, trials, purchases, refunds, installation, and updates under the
[Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement),
[Microsoft Services Agreement](https://www.microsoft.com/servicesagreement), and applicable
regional [Store Terms of Sale](https://www.microsoft.com/en-us/store/b/terms-of-sale).

Through Windows `StoreContext`, the app checks whether the license carries a Store product
identifier, then checks whether the entitlement is active, whether it is a trial and, for a trial,
its expiry. The current implementation does not obtain or store a Microsoft account email,
password, card number, or payment method through that query. Where available, the purchase
button opens the Microsoft Store product page without a PCSSAK checkout or device-code form.

The queried Store entitlement is handled in session memory and is not uploaded automatically
to PCSSAK. A temporary query failure preserves a status checked during that session; purchased
Store status is not separately saved to disk. Restart queries again and can fall back to a
remaining local trial when unavailable. Explicit Store expiry and revocation responses apply.
When offline, Windows can still return a [Store license cached on the device](https://learn.microsoft.com/en-us/uwp/api/windows.services.store.storecontext.getapplicenseasync).

After release, PCSSAK reviews Microsoft’s Partner Center acquisition and installation counts
and trends in crashes and unresponsive events to monitor distribution and investigate problems.
Authorized financial staff consult earnings reports as needed to reconcile sales, refunds and
payouts. Reports can include order and transaction identifiers, amounts, currencies, payment
method categories, transaction regions or tax postal codes. Microsoft prepares these reports.
Biuja does not send PCSSAK the files you organize, their paths, or your journal for reporting.
See [Microsoft’s app analytics overview](https://learn.microsoft.com/en-us/windows/apps/publish/analyze-app-performance/msix)
and the [Store earnings report](https://learn.microsoft.com/en-us/partner-center/earnings/earnings-store).

For purchases, view your Microsoft account’s
[order history](https://account.microsoft.com/billing/orders). For refund eligibility, see
[Microsoft’s refund guidance](https://support.microsoft.com/en-us/accounts-billing/subscriptions/get-a-refund-for-apps-and-games-purchased-from-microsoft-store).
You do not need to send PCSSAK a card number, password, verification code, or copy of a receipt.

### 3. Device code and local trial

For standalone compatibility and trial decisions during a Store-query failure, the Store build
also creates a local trial record and product-specific device code. It reads Windows
`MachineGuid` and hashes it for this product. The original MachineGuid is not stored in app files
or uploaded automatically to PCSSAK. Store purchase does not require entering or sending that code.

`trial.json` and the `TrialRecord` value under the current-user registry key
`HKCU\Software\PCssak\Biuja\com.pcssak.biuja.store` store trial start and last-seen times, record
version, legacy-user status, and verification data derived from the device code. Windows can keep
this value, written by the Store package, in the package's private registry. They contain no file data, paths,
Microsoft account, or payment information. Removing one copy or reinstalling can use the
remaining record and is not promised to restart the trial.

A large clock rollback can temporarily suspend the trial decision. The Store build and test
builds each use their own app identifier and registry subkey. The `TrialRecord` under the base key
`HKCU\Software\PCssak\Biuja` and the `com.pcssak.biuja` folders belong to the standalone (NSIS) app. The records are not automatically transmitted or deleted
on a time-based schedule.

### 4. Local data and retention

Typical Windows paths appear below. Store-package redirection may place data under
`%LOCALAPPDATA%\Packages\<PackageFamilyName>`; actual locations vary by installation method and
Windows version. Check the app-specific locations on the device.

| Data | Typical location | Content and retention |
|---|---|---|
| Settings and import recovery | `%APPDATA%\com.pcssak.biuja.store\config.json`, `config.before-import.json`, `config.before-import.pending.json` | Folder paths, rules, schedules, language, and theme. The latest import's before/after settings can be kept for safe Import Undo. No time-based expiry; removal follows successful undo, rejection of a stale point, the next import's cleanup, or manual deletion. Damaged settings can produce a separate backup. |
| Settings saved before a safety check | `config.before-safety-<fingerprint>.json` in the same settings folder | If the safety check at startup excludes a folder or rule, Biuja keeps the original settings, including paths and rules, for your review. Unchanged settings create no copy, and identical originals share one copy. The copy has no automatic expiry. Biuja keeps it locally without restoring it automatically or sending it to a server. You can delete it after review. During the write, Biuja uses `config.before-safety-<fingerprint>.<random-id>.tmp` in the same folder. Normal completion clears the temporary file. A forced exit can leave all or part of the settings there. Biuja does not restore or upload that file. |
| Journal and copy evidence | `%APPDATA%\com.pcssak.biuja.store\journal.db` and SQLite companions | Source/destination paths, operations, times, status, size, modification time, identity, hashes, and recovery locations, not file copies. Older finalized rows are pruned after approximately 20,000 rows; active, pending, and set-aside recovery records can remain. `copy_evidence` preventing duplicate copies survives visible-history pruning and has no time-based expiry. So that automatic organizing does not re-process its own results, pruned rows also leave `automation_output_receipts_v1` entries for each completed Move destination and each location an Undo left a file at (the restored location of an undone Move or Trash, and the source of an undone Copy), holding only the path, size, modification time and file identifier. These also have no time-based expiry and are removed when a different file is later found at that path or when you delete `journal.db` and its companion files. |
| Trial | App-specific `trial.json` and the Store subkey's registry `TrialRecord` | The dates and verification information in section 3. No automatic expiry or deletion; the registry value can remain after app files are deleted. |
| Compatible license | App-specific `license.json`, `license.json.surface` | Present only if a PB1 or PB2 key was entered in this Store app (a key entered in the standalone app is not carried over). The full key can include email, entitlement, and a PB2 device code; it is not separately encrypted and relies on Windows profile permissions. It can remain until license deactivation or manual deletion. The surface marker is a fixed, non-account marker for a reactivation screen and grants no entitlement. A Store purchase does not issue a key into this file. |
| Local logs | `%LOCALAPPDATA%\com.pcssak.biuja.store\logs` or the app-specific log directory | Startup/error diagnostics can include local paths and technical operation context. No automatic upload; data can remain until manual deletion. |
| WebView2 and window state | App-specific WebView2 and settings folders | Rendering cache, preferences, window size/position. Retention and removal follow Runtime, app, uninstall/reset, and manual deletion behavior. |
| Startup state | The package's Windows startup-task registration | User-enabled sign-in launch, also managed through Windows settings. |

This data is not uploaded automatically to PCSSAK. The email and device code in compatible
PB1/PB2 keys are stored locally in `license.json`, not transmitted automatically. Standalone
license deactivation deletes the key file; if the Store build has no key screen, fully close
the app and remove that local file manually. Store purchases, refunds, and Microsoft-account
deletion are managed separately by Microsoft.

Use the folder and rule settings and the History screen to review configured paths and recent
operations. Exporting settings creates a JSON file at the location you choose. It can contain
folder paths, rules and search terms. The export has no separate encryption. It does not
contain the contents of organized files or the journal. Your copy may remain at that location
after uninstall. Review it before sharing and delete it there when you no longer need it.
Protect access to the Windows user account and backups holding settings and the journal.

### 5. Updates and WebView2

The Store build uses Microsoft Store updates, not the app's GitHub `latest.json` check or
download. Updates may install automatically according to Store and Windows settings. Existing
v0.1.x standalone GitHub update behavior is described in the [previous policy](docs/LEGACY-v0.1.x-PRIVACY.md).

Installation, repair, and independent updating of the required Microsoft Edge WebView2 Runtime
can connect to Microsoft services. Microsoft can process IP addresses and ordinary request or
installation metadata under its policies. The app does not include organized files, names,
paths, or the journal in Runtime installation requests. Installation or launch may not complete
offline if a required Runtime is absent.

WebView2 Runtime can process required diagnostic data for security, performance, and reliability.
Optional diagnostic data follows the Windows Diagnostic data setting. If a WebView2 process crashes,
crash diagnostic data may be sent to Microsoft according to Windows consent and Runtime settings.
This is separate from PCSSAK having an automatic error-upload feature, and does not mean PCSSAK
receives Microsoft diagnostic data. We do not guarantee that diagnostic data never contains personal
information. For the scope of processing and user controls, see
[Microsoft WebView2 data and privacy](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/data-privacy) and the
[Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).

### 6. User-initiated support and external services

Opening and submitting a website, GitHub Issue, or email lets the chosen service process entered
contents and ordinary connection information. PCSSAK uses requests to reply, reproduce issues,
and respond to security reports. Other people can see public GitHub issues, and posts can
remain visible after an email has been deleted. GitHub follows its
[Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

Contacting support by email is optional. When you email <mailto:pcssak@pcssak.com>, Cloudflare
Email Routing forwards your sender address, display name, message, and attachments to the personal
Gmail account used for customer support. Only support personnel have access. When an ordinary
inquiry is resolved, PCSSAK deletes the inbound message, replies, attachments and downloaded copies,
including permanent removal of the messages from Gmail Trash. If records must be retained by law,
PCSSAK keeps the necessary parts separately and deletes them at the end of the retention period.
For example, consumer complaint and dispute records are kept for three years when PCSSAK is subject to
that duty under Korean electronic commerce law. Gmail's normal 30-day Trash limit is separate from
providers' log and backup retention. [Korean electronic commerce decree, Article 6](https://www.law.go.kr/LSW/lsLawLinkInfo.do?chrClsCd=010202&lsJoLnkSeq=900619372) · [Gmail deletion guidance](https://support.google.com/mail/answer/7401?hl=en)

For file organization issues, include the app and Windows versions, the steps using an
invented filename, and the error message. Do not send real files, full paths, directory
listings, exported settings, license keys, customer data, passwords, tokens, private keys,
or payment information. If you include a screenshot, redact identifying details. Follow
the [Security Policy](SECURITY.md) for private vulnerability reporting. You or your legal
representative can email the customer support privacy contact to request access to, correction
or deletion of, or restriction of processing of your inquiry data. Include the date you wrote
and the reply address. PCSSAK will verify identity or authority and explain the outcome,
including the reason for any restriction required by law. In Korea, the
[Privacy Portal](https://www.privacy.go.kr/front/contents/cntntsView.do?contsNo=408) lists
complaint and dispute-resolution bodies. You can also contact your local privacy authority.

### 7. Deleting local data

Store uninstall/reset follows Windows package-data policies: some data may be deleted or
remain. Preservation of all records is not promised. Review needed history and export settings
before uninstall or reset. The existing NSIS standalone uninstaller preserves app data.

After fully closing the app, inspect and manually delete its app-specific and package-specific
data. The current-user app-specific `TrialRecord` registry value can remain after deleting
files or uninstalling. For complete removal, remove only the app's own value without affecting
other apps, or request assistance. On a PC that also has the standalone app, the `TrialRecord`
under the base key `HKCU\Software\PCssak\Biuja` and the `com.pcssak.biuja` folders hold that app's
settings, license key and Undo records; do not delete them when removing Store app data. Windows' original MachineGuid is not app data; do not delete it.

Deletion can remove settings, license keys, recovery records, and duplicate-copy evidence.
Organized user files and the Recycle Bin are separate; deleting app data does not undo or delete
them. Microsoft-account, transaction, entitlement deletion, and refunds follow Microsoft's procedures.

### 8. Third parties, international processing, and children

PCSSAK does not sell app-usage data to advertisers or data brokers. External services may process
connection or contact data in countries and regions where their infrastructure operates.

When a message reaches the support address, Cloudflare, Inc. forwards the sender and recipient
addresses, display name, subject, body and any attachments supplied by the sender to Google LLC's
Gmail service. Cloudflare says it does not store forwarded message bodies. Its activity log can show
the results of delivery and authentication. The dashboard offers
a view of the past 30 days. We have not confirmed the processing countries for this address or when
Cloudflare permanently deletes its routing logs and copies.

Google told us it may process information on servers worldwide and could not specify the country
where this personal Gmail account stores messages. Gmail holds the inquiry and our reply, which
PCSSAK handles as described in section 6. Under Google's general policy, safe deletion from its
servers usually takes about two months after deletion is requested. Encrypted disaster-recovery
backups can retain data for up to six months. Google may keep some information longer for security
or legal reasons. The policy does not give a guaranteed deletion date for any individual email.
Each provider's privacy policy lists its privacy contact.
You may use organization and rollback without emailing support. If you do not send a message,
PCSSAK cannot receive or answer that inquiry.
[Cloudflare Email Routing](https://www.cloudflare.com/products/email-routing/) · [Email activity logs](https://developers.cloudflare.com/email-service/observability/logs/) · [Google retention and deletion](https://policies.google.com/technologies/retention?hl=en).
See the [Cloudflare Privacy Policy](https://www.cloudflare.com/privacypolicy/) and
[Google Privacy Policy](https://policies.google.com/privacy?hl=en) for those providers'
practices and privacy rights.

The app provides no child-directed account, advertising, or analytics service and does not
intentionally collect children's personal data in the app. Store accounts, purchases, family
features, and external services remain subject to their providers' policies.

### 9. Changes and contact

Changes to storage, connections, distribution, or legal requirements will update this policy
and the official product page with a new date. Product page:
[https://pcssak.com/biuja](https://pcssak.com/biuja). Privacy contact: `pcssak@pcssak.com`.
