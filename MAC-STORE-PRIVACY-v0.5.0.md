# PCssak Biuja Mac App Store Privacy Policy / 개인정보 처리방침

- Last updated / 최종 수정: 2026-11-15
- Operator / 운영자: PCSSAK
- Privacy contact / 개인정보 보호 담당(고객지원): `pcssak@pcssak.com`
- Applies to / 적용 대상: PCssak Biuja v0.5.0 for macOS — Mac App Store

> The Korean text is authoritative to the extent permitted by applicable law; the English text
> is a reference translation. The Windows editions are covered by
> [STORE-PRIVACY-v0.5.0.md](STORE-PRIVACY-v0.5.0.md) and [PRIVACY.md](PRIVACY.md).
>
> 적용 법률이 허용하는 범위에서 국문을 기준으로 하며 영문은 참고 번역입니다.
> Windows판은 [STORE-PRIVACY-v0.5.0.md](STORE-PRIVACY-v0.5.0.md)와 [PRIVACY.md](PRIVACY.md)를 확인하세요.

## 국문

이 개인정보 안내(개인정보 처리방침)는 PCSSAK(이하 "회사")가 Mac App Store에서 제공하는 PCssak Biuja(이하 "앱")와 관련해 어떤 정보를 어디서 처리하는지 설명합니다. 앱은 회사의 서버로 개인정보를 보내지 않습니다. 회사가 개인정보를 받는 경우는 사용자가 직접 문의를 보낼 때뿐입니다.

### 1. 기기 안에서만 처리하는 파일

파일 검사·분류·이동·복사·휴지통 보내기·되돌리기는 사용자의 Mac 안에서 처리합니다. 앱은 파일 내용·이름·경로·규칙·미리보기·작업 기록을 회사 서버로 자동 전송하지 않습니다. 회사 계정, 광고·추적 도구, 사용 분석, 쿠키 또는 자동 오류 업로드 기능이 없습니다. 파일을 정확히 식별하고 안전하게 복사·되돌리기 위해 일부 파일 내용의 해시를 기기 안에서 계산할 수 있으며, 이 해시도 전송하지 않습니다.

앱은 macOS 선택창에서 사용자가 고른 폴더와 가져오기·내보내기 파일만 사용합니다. 고른 폴더를 계속 쓰기 위한 macOS 권한 북마크와 파일 식별 정보를 앱의 비공개 데이터에 저장합니다. 권한 북마크는 설정 내보내기 파일에 들어가지 않습니다. 내보낸 설정에는 폴더 경로와 규칙이 들어 있을 수 있으니 공유하기 전에 확인하세요.

화면 표시를 위해 macOS WebKit의 송신 연결 권한을 사용합니다. 이 권한은 앱 내부 화면 연결에도 필요하며, 회사로 파일·경로·작업 기록을 보내는 기능은 없습니다.

### 2. 기기 안에 저장되는 자료와 보관

앱 데이터는 보통 `~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`에 저장됩니다. 실제 위치와 WebKit·로그 관리 방식은 macOS에 따라 달라질 수 있습니다. 앱 데이터는 macOS 사용자 계정과 앱 샌드박스 보호를 받으며, 앱이 별도 암호화를 추가하지는 않습니다.

- `config.json`과 설정 복구·백업: 등록 폴더, 규칙, 언어, 화면 설정, 예약 설정. 사용자가 바꾸거나 지울 때까지 남습니다.
- `journal.db`와 SQLite 동반 파일: 작업 종류·시각·상태, 원래 위치와 옮긴 위치, 파일 크기·수정 시각·식별자·해시, 되돌리기 정보. 파일 사본은 아닙니다. 오래된 완료 기록은 약 20,000건을 기준으로 정리되며, 진행 중·확인 필요·복구 기록은 더 오래 남을 수 있습니다. 자동 정리가 자기 결과를 다시 처리하지 않도록 완료된 이동의 목적지와 되돌린 위치는 경로·크기·수정 시각·식별자만 담은 기록으로 남고, 같은 경로에서 다른 파일이 확인되면 삭제됩니다.
- `macos-approved-roots.sqlite3`와 동반 파일: 고른 폴더·파일의 권한 북마크, 경로, 식별자. 재시작 뒤 자동 정리와 되돌리기에 필요하며 설정 내보내기에 들어가지 않습니다.
- 로그·WebKit 데이터·창 상태: 시작·오류 진단과 화면 표시. 로그는 경로를 대부분 가린 식별값으로 남기지만 일부 기술 정보에 로컬 경로가 들어갈 수 있습니다. 자동으로 업로드하지 않으며, 로그 파일은 크기 한도에 따라 앱이 교체합니다.

Mac App Store 판은 사용권 키, 체험 기록, 기기 코드나 기기 해시를 만들지 않습니다.

### 3. 회사가 처리하는 개인정보(문의할 때만)

- 처리 항목: 사용자가 보낸 이메일 주소, 적어 보낸 이름, 문의 내용과 첨부 자료
- 처리 목적: 문의 응답, 문제 재현과 해결, 보안 신고 대응, 분쟁 대응과 기록
- 보유 기간: 문의 처리를 마친 뒤 3년간 보관하고 파기합니다. 소비자 불만·분쟁 처리 기록 보존 기간을 고려한 기간입니다. 삭제를 요청하시면 법령상 보관할 필요가 없는 정보는 지체 없이 삭제합니다.

실제 파일, 전체 경로, 파일 목록, 고객 자료, 암호, 토큰, 개인키, 결제 정보는 보내지 마세요. 가상의 예시와 가린 화면을 사용해 주세요.

### 4. 처리 위탁과 국외 이전

회사는 개인정보를 다른 사람에게 판매하거나 제공하지 않습니다. 문의 메일을 받기 위해 다음 서비스를 이용하며, 이 과정에서 개인정보가 국외 서버에서 처리될 수 있습니다.

- Cloudflare, Inc.(Cloudflare Email Routing): `pcssak@pcssak.com`으로 온 메일을 회사 수신함으로 전달합니다. 이전 항목은 이메일 주소와 메일 내용이며, 메일을 보내는 시점에 네트워크로 전송됩니다.
- Google LLC(Gmail): 전달된 문의 메일을 보관합니다. 이전 항목과 시점은 위와 같고, 보관 기간은 3항의 보유 기간을 따릅니다.

각 서비스의 서버는 미국 등 여러 국가에 있을 수 있습니다. 국외 처리를 원하지 않으면 이메일 문의를 보내지 않을 수 있으며, 이 경우 앱 사용에는 아무 제한이 없고 문의 응답만 받을 수 없습니다.

### 5. Apple과 사용자가 직접 고른 외부 서비스

구매·설치·업데이트·환불과 Apple 계정은 Apple이 관리합니다. 앱은 Apple 계정 암호나 카드 번호를 받지 않고, 결제·영수증 기록을 따로 저장하지 않습니다. Apple의 처리는 [App Store 개인정보 안내](https://www.apple.com/legal/privacy/data/en/app-store/)를 확인하세요. 회사가 Apple로부터 받는 판매·정산 보고는 Apple의 정책을 따르며, 앱이 파일을 업로드하는 것과는 관계가 없습니다.

웹사이트·GitHub·이메일을 직접 열면 해당 서비스가 연결과 보낸 내용을 처리합니다. 앱은 이런 링크에 파일·경로·기록을 자동으로 붙이지 않습니다. 사용자가 iCloud나 다른 동기화 폴더로 파일을 복사·이동하면 그 서비스의 설정에 따라 파일이 동기화될 수 있으며, 이는 앱의 업로드 기능이 아닙니다.

### 6. 정보주체의 권리와 행사 방법

사용자는 회사가 처리하는 자신의 개인정보에 대해 열람, 정정, 삭제, 처리 정지를 요청할 수 있습니다. `pcssak@pcssak.com`으로 요청하시면 본인 확인 뒤 법령이 정한 기간 안에 조치하고 결과를 알려 드립니다. 법령이 보관을 요구하는 정보는 삭제가 제한될 수 있으며, 이 경우 그 이유를 알려 드립니다.

### 7. 파기 절차와 방법

보유 기간이 끝나거나 처리 목적을 이룬 개인정보는 지체 없이 파기합니다. 전자적 자료는 복구할 수 없는 방법으로 삭제하고, 종이 자료는 만들지 않습니다.

### 8. 안전성 확보 조치

회사는 문의 자료에 접근할 수 있는 사람을 담당자로 제한하고, 계정 보안 설정을 유지하며, 보유 기간이 지난 자료를 파기합니다. 앱이 기기 안에 저장하는 자료는 macOS 사용자 계정과 앱 샌드박스의 보호를 받습니다.

### 9. 아동

앱은 아동을 대상으로 한 계정·광고·분석 기능이 없고, 14세 미만 아동의 개인정보를 의도적으로 수집하지 않습니다.

### 10. 기기 안의 자료 삭제

앱의 설정을 바꾸거나 등록 폴더를 지우면 새 정리를 멈출 수 있습니다. 일부 권한 북마크와 작업·복구 기록은 남을 수 있습니다. macOS 시스템 설정에서 앱 권한을 바꿔도 앱의 기존 기록이 모두 지워지지는 않습니다.

앱을 완전히 종료한 뒤 위 앱 데이터 폴더를 직접 지울 수 있습니다. 지우면 규칙, 권한 북마크, 되돌리기 기록, 중복 복사 확인 기록이 사라집니다. 앱을 지우는 것만으로 정리한 파일, 휴지통, 외부 백업이 지워지지는 않습니다. 다른 앱의 데이터나 상위 `Library` 폴더 전체를 지우지 마세요.

### 11. 개인정보 보호책임자

- 담당: 개인정보 보호 담당(고객지원)
- 연락처: `pcssak@pcssak.com`

### 12. 권익 침해 구제

개인정보 침해에 대한 상담이나 분쟁 조정이 필요하면 다음 기관에 문의할 수 있습니다.

- 개인정보분쟁조정위원회: 국번 없이 1833-6972, www.kopico.go.kr
- 개인정보침해신고센터: 국번 없이 118, privacy.kisa.or.kr
- 대검찰청: 국번 없이 1301, www.spo.go.kr
- 경찰청: 국번 없이 182, ecrm.police.go.kr

### 13. 변경

처리하는 정보나 방법이 바뀌면 공개본과 앱 안의 이 문서를 함께 고치고 최종 수정일을 바꿉니다. 제품 안내: https://pcssak.com/biuja · 개인정보 문의: `pcssak@pcssak.com`

## English reference translation

This Privacy Policy explains what information PCSSAK ("we") processes, and where, for PCssak Biuja ("the app") distributed through the Mac App Store. The app does not send personal information to our servers. We receive personal information only when you contact us yourself. The Korean version prevails to the extent permitted by applicable law; this English text is a reference translation.

### 1. Files are processed only on your Mac

Inspection, classification, moves, copies, Trash and Undo run on your Mac. The app does not automatically send file contents, names, paths, rules, previews or its operation records to us. There is no account with us, no advertising or tracking tool, no usage analytics, no cookies and no automatic error upload. To identify files precisely and to copy or undo safely, the app may compute hashes of some file contents on your Mac; these hashes are not sent anywhere.

The app uses only the folders and import/export files you choose in macOS panels. It stores macOS permission bookmarks and file identifiers for the folders you chose in its private app data, so it can keep using them. Permission bookmarks are never included in exported settings. Exported settings can contain folder paths and rules, so review them before sharing.

The app uses the macOS WebKit outgoing-connection permission to display its interface. This permission is also required for the app's internal page connection; the app has no feature that sends files, paths or records to us.

### 2. Data stored on your Mac and how long it stays

App data is normally stored in `~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`. The exact location and how WebKit and logs are managed can vary with macOS. App data is protected by your macOS user account and the app sandbox; the app does not add its own encryption.

- `config.json` and settings recovery/backup copies: your folders, rules, language, appearance and schedule. They stay until you change or delete them.
- `journal.db` and its SQLite companion files: operation type, time and status, original and new locations, file size, modification time, identifiers, hashes and undo information. They are not copies of your files. Old completed records are trimmed at about 20,000 entries; in-progress, needs-review and recovery records can stay longer. So that automatic organizing does not process its own results again, the destinations of completed moves and the locations restored by Undo remain as records containing only path, size, modification time and identifier, and are removed when a different file is found at that path.
- `macos-approved-roots.sqlite3` and companion files: permission bookmarks, paths and identifiers of the folders and files you chose. They are needed for automatic organizing and Undo after a restart and are never exported with settings.
- Logs, WebKit data and window state: startup and error diagnostics and the interface. Logs mostly record paths as masked identifiers, but some technical details can include local paths. Logs are never uploaded, and the app replaces log files according to a size limit.

The Mac App Store edition does not create licence keys, trial records, device codes or device hashes.

### 3. Personal information we process (only when you contact us)

- Items: the email address you write from, any name you include, and the content and attachments of your message.
- Purposes: answering you, reproducing and fixing problems, handling security reports, and handling and recording disputes.
- Retention: kept for 3 years after your inquiry is closed and then destroyed, considering the retention period for consumer complaint and dispute records. If you ask us to delete it, we delete without delay whatever the law does not require us to keep.

Do not send real files, full paths, file lists, customer data, passwords, tokens, private keys or payment details. Please use made-up examples and masked screenshots.

### 4. Service providers and international transfer

We do not sell or give personal information to anyone. We use the following services to receive email inquiries, and your information may be processed on servers outside Korea in the process.

- Cloudflare, Inc. (Cloudflare Email Routing): forwards mail sent to `pcssak@pcssak.com` to our mailbox. Items transferred are your email address and message, sent over the network when you send the email.
- Google LLC (Gmail): stores the forwarded inquiry. Items and timing are the same as above; retention follows section 3.

These providers' servers may be in the United States and other countries. If you do not want your information processed abroad, you can choose not to email us; the app works without any restriction, but we will not be able to reply to you.

### 5. Apple and external services you choose

Apple manages purchases, installation, updates, refunds and your Apple Account. The app never receives your Apple Account password or card number and does not store separate payment or receipt records. See the [App Store privacy information](https://www.apple.com/legal/privacy/data/en/app-store/) for Apple's processing. Sales and settlement reports we receive from Apple follow Apple's policies and have nothing to do with the app uploading files.

When you open a website, GitHub or an email link yourself, that service processes the connection and what you send. The app never attaches files, paths or records to such links. If you copy or move files into iCloud or another sync folder, the files may sync according to that provider's settings; this is not an upload by the app.

### 6. Your rights and how to exercise them

You can ask to access, correct, delete or stop the processing of the personal information we hold about you. Email `pcssak@pcssak.com`; after confirming it is you, we act within the period required by law and tell you the result. Deletion can be limited where the law requires us to keep information, and we will tell you why.

### 7. Destruction

Personal information is destroyed without delay when its retention period ends or its purpose has been achieved. Electronic data is deleted so that it cannot be recovered; we do not create paper copies.

### 8. Security measures

We limit access to inquiry data to the people handling it, maintain account security settings, and destroy data after its retention period. Data the app stores on your Mac is protected by your macOS user account and the app sandbox.

### 9. Children

The app has no accounts, advertising or analytics aimed at children and does not knowingly collect personal information from children under 14.

### 10. Deleting data on your Mac

You can stop new organizing by changing the app's settings or removing a registered folder. Some permission bookmarks and operation or recovery records can remain. Changing the app's permissions in macOS System Settings does not delete the app's existing records.

After quitting the app completely, you can delete the app data folder above yourself. Doing so removes your rules, permission bookmarks, undo records and duplicate-copy evidence. Deleting the app alone does not delete the files it organized, the Trash or external backups. Do not delete other apps' data or the whole parent `Library` folder.

### 11. Privacy officer

- Contact point: Privacy contact (customer support)
- Email: `pcssak@pcssak.com`

### 12. Remedies

For advice or dispute mediation about privacy infringement in Korea, you can contact the Personal Information Dispute Mediation Committee (1833-6972, www.kopico.go.kr), the Personal Information Infringement Report Center (118, privacy.kisa.or.kr), the Supreme Prosecutors' Office (1301, www.spo.go.kr) or the Korean National Police Agency (182, ecrm.police.go.kr).

### 13. Changes

If what we process or how we process it changes, we update the public copy and this in-app document together and change the last-updated date. Product information: https://pcssak.com/biuja · Privacy contact: `pcssak@pcssak.com`
