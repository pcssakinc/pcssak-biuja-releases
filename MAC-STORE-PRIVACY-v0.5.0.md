[한국어](#korean) · [English](#english)

<a name="korean"></a>

# PCssak Biuja Mac App Store 개인정보 처리방침

- 최종 수정일: 2026-11-25 · 적용: PCssak Biuja 0.5.0 Mac App Store 판부터
- 운영자: PCSSAK · 개인정보 보호 담당(고객지원): <mailto:pcssak@pcssak.com>
- 사업장 주소: 대한민국 서울시 도봉구 노해로65길 7-12, 7층 75-B호

이 개인정보 안내(개인정보 처리방침)는 PCssak Biuja의 Mac App Store 판에 적용됩니다. 앱은 사용자의 Mac에서 파일을 정리합니다. PCSSAK(이하 “회사”)에 이메일로 문의하면 회사는 3항과 4항에 따라 사용자가 보낸 내용을 처리합니다. 영문은 참고 번역이며, 내용이 다를 경우 적용 법률이 허용하는 범위에서 한국어본이 우선합니다.

## 1. 기기 안에서만 처리하는 파일

파일 검사·분류·이동·복사·휴지통 보내기·되돌리기는 사용자의 Mac 안에서 처리합니다. 앱은 파일 내용·이름·경로·규칙·미리보기·작업 기록을 회사 서버로 자동 전송하지 않습니다. 회사 계정, 광고·추적 도구, 사용 분석, 쿠키 또는 자동 오류 업로드 기능이 없습니다. 파일을 정확히 식별하고 안전하게 복사·되돌리기 위해 일부 파일 내용의 해시를 기기 안에서 계산할 수 있으며, 이 해시도 전송하지 않습니다.

정리할 폴더와 가져오거나 내보낼 파일은 사용자가 macOS 선택창에서 고릅니다. 고른 폴더를 계속 쓰기 위한 macOS 권한 북마크와 파일 식별 정보를 앱의 비공개 데이터에 저장합니다. 권한 북마크는 설정 내보내기 파일에 들어가지 않습니다. 내보낸 설정에는 폴더 경로와 규칙이 들어 있을 수 있으니 공유하기 전에 확인하세요.

화면 표시를 위해 macOS WebKit의 송신 연결 권한을 사용합니다. 이 권한은 앱 내부 화면 연결에도 필요하며, 회사로 파일·경로·작업 기록을 보내는 기능은 없습니다.

## 2. 기기 안에 저장되는 자료와 보관

앱 데이터는 보통 `~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`에 저장됩니다. 실제 위치와 WebKit·로그 관리 방식은 macOS에 따라 달라질 수 있습니다. 앱 데이터는 macOS 사용자 계정과 앱 샌드박스 보호를 받으며, 앱이 별도 암호화를 추가하지는 않습니다.

- `config.json`과 설정 복구·백업: 등록 폴더, 규칙, 언어, 화면 설정, 예약 설정. 사용자가 바꾸거나 지울 때까지 남습니다.
- `journal.db`와 SQLite 동반 파일: 작업 종류·시각·상태, 원래 위치와 옮긴 위치, 파일 크기·수정 시각·식별자·해시, 되돌리기 정보. 파일 사본은 아닙니다. 오래된 완료 기록은 약 20,000건을 기준으로 정리되며, 진행 중·확인 필요·복구 기록은 더 오래 남을 수 있습니다. 자동 정리가 자기 결과를 다시 처리하지 않도록 이동하거나 되돌린 파일의 경로·크기·수정 시각·식별자 등 일부 정보를 따로 보관합니다. 이 보관 기록도 저장 한도에 이르면 오래된 항목부터 삭제될 수 있습니다.
- `macos-approved-roots.sqlite3`와 동반 파일: 고른 폴더·파일의 권한 북마크, 경로, 식별자. 재시작 뒤 자동 정리와 되돌리기에 필요하며 설정 내보내기에 들어가지 않습니다.
- 로그·WebKit 데이터·창 상태: 시작·오류 진단과 화면 표시. 로그는 경로를 대부분 가린 식별값으로 남기지만 일부 기술 정보에 로컬 경로가 들어갈 수 있습니다. 자동으로 업로드하지 않으며, 로그 파일은 크기 한도에 따라 앱이 교체합니다.

Mac App Store 판은 사용권 키나 체험 기록을 만들지 않습니다. 구매 확인에 쓰는 기기 검증값은 아래 5항과 같이 처리합니다.

## 3. 회사가 처리하는 개인정보(문의할 때만)

- 처리 항목: 사용자가 보낸 이메일 주소, 적어 보낸 이름, 문의 내용과 첨부 자료
- 처리 목적: 문의에 답하고, 사용자가 알려 준 문제나 보안 신고에 대응하는 데 사용합니다.
- 보관과 삭제: 일반 문의는 마지막 답변으로 처리를 마치면 받은 메일, 보낸 답변, 첨부 자료와 내려받은 업무용 사본을 삭제합니다. 해당 메일은 Gmail 휴지통에서도 개별 영구 삭제합니다. 일반 문의 내역은 따로 보관하지 않습니다.

법령에 따라 보존해야 하는 기록은 필요한 범위만 분리해 접근을 제한하고, 의무 기간이 끝나면 파기합니다. 예를 들어 한국 전자상거래법상 PCSSAK에 보존 의무가 적용되는 소비자의 불만 또는 분쟁처리 기록은 3년간 보관합니다. [전자상거래법 시행령 제6조](https://www.law.go.kr/법령/전자상거래등에서의소비자보호에관한법률시행령/제6조)

실제 파일, 전체 경로, 파일 목록, 고객 자료, 암호, 토큰, 개인키, 결제 정보는 보내지 마세요. 가상의 예시와 가린 화면을 사용해 주세요.

## 4. 이메일로 문의할 때의 국외 처리

문의 메일을 보내면 발신 주소, 표시 이름(있는 경우), 수신 주소, 제목, 본문과 직접 첨부한 자료가 아래 경로를 거칩니다. 앱이 파일·경로·작업 기록을 자동으로 첨부하는 기능은 없습니다.

- **받은 메일 전달 — Cloudflare, Inc.** 사용자가 지원 주소로 보낸 메일이 도착하면 Cloudflare Email Routing이 인터넷 메일로 PCSSAK의 지원 메일함에 전달합니다. Cloudflare는 전달 서비스가 메일 본문을 저장하지 않는다고 설명합니다. 전달 결과와 메일 인증 결과는 별도 활동 로그에 기록될 수 있습니다. PCSSAK이 메일함을 지워도 이 로그가 함께 삭제되지는 않습니다. [이메일 전달](https://www.cloudflare.com/products/email-routing/) · [활동 로그](https://developers.cloudflare.com/email-service/observability/logs/) · Cloudflare 개인정보 문의 (privacyquestions@cloudflare.com)
- **받은 메일과 답변 — Google LLC.** PCSSAK은 전달받은 문의를 개인용 Gmail 계정에서 읽고, 그 계정에서 문의자에게 답변합니다. Google은 받은 메일과 보낸 답변 및 첨부를 처리합니다. PCSSAK은 일반 문의가 마지막 답변으로 마무리되면 3항에 따라 삭제합니다. Google은 자체 삭제 절차를 적용하며, 재해 복구용 암호화 백업에는 데이터가 최대 6개월 남을 수 있다고 설명합니다. [Google 개인정보처리방침](https://policies.google.com/privacy?hl=ko) · [Google의 삭제 및 보관 기준](https://policies.google.com/technologies/retention?hl=ko) · Google 개인정보 문의 (googlekrsupport@google.com)

**처리 장소.** PCSSAK의 사업장은 대한민국에 있습니다. 메일 전달과 메일함 처리는 대한민국 밖에서 이루어질 수 있습니다. Google은 여러 나라의 서버를 사용합니다. 현재 두 서비스의 공개 자료만으로는 이 지원 주소의 메일과 처리 기록이 거치는 국가 전체 또는 Cloudflare 전달 로그의 최종 삭제 시점을 특정할 수 없습니다.

**메일을 보내고 싶지 않을 때.** 메일을 보내기 전에는 창을 닫아도 됩니다. 그러면 해당 문의는 PCSSAK에 접수되지 않으며 이메일 답변도 제공되지 않습니다. 비우자의 파일 정리·되돌리기는 그대로 사용할 수 있습니다. 이미 보낸 자료의 열람·삭제 등은 6항에서 안내합니다. PCSSAK은 개인정보를 판매하지 않습니다.

## 5. Apple과 사용자가 직접 고른 외부 서비스

구매·설치·업데이트·환불과 Apple 계정은 Apple이 관리합니다. 정식 앱은 Apple의 StoreKit을 통해 앱 구입에 관한 서명된 정보(AppTransaction)를 확인합니다. 앱 식별자와 배포 환경을 확인하고, Apple이 제공하는 기기 검증값을 메모리에서 계산·대조해 이 Mac에 해당하는 정보인지 검사합니다. 이 과정에서 StoreKit이 Apple과 통신할 수 있습니다. PCSSAK은 Apple 계정 암호나 카드 번호를 받지 않으며, 앱은 거래 원문이나 기기 검증값을 별도 파일에 저장하거나 PCSSAK 서버에 보내지 않습니다. Apple의 처리는 [App Store 개인정보 안내](https://www.apple.com/legal/privacy/data/en/app-store/)를 확인하세요. 회사가 Apple로부터 받는 판매·정산 보고는 Apple의 정책을 따르며, 앱이 파일을 업로드하는 것과는 관계가 없습니다.

웹사이트·GitHub·이메일을 직접 열면 해당 서비스가 연결과 보낸 내용을 처리합니다. 앱은 이런 링크에 파일·경로·기록을 자동으로 붙이지 않습니다. 사용자가 iCloud나 다른 동기화 폴더로 파일을 복사·이동하면 그 서비스의 설정에 따라 파일이 동기화될 수 있으며, 이는 앱의 업로드 기능이 아닙니다.

## 6. 정보주체의 권리와 행사 방법

사용자는 회사가 처리하는 자신의 개인정보에 대해 열람, 정정, 삭제, 처리 정지를 요청할 수 있습니다. <mailto:pcssak@pcssak.com>으로 요청하시면 본인 확인 뒤 법령이 정한 기간 안에 조치하고 결과를 알려 드립니다. 법령이 보관을 요구하는 정보는 삭제가 제한될 수 있으며, 이 경우 그 이유를 알려 드립니다.

## 7. 문의 자료 삭제

Gmail에서 일반 삭제한 메일은 휴지통에 최대 30일간 남을 수 있습니다. PCSSAK은 3항에 따라 일반 문의를 마칠 때 해당 메일을 휴지통에서도 지웁니다. 메일함에서의 영구 삭제와 제공업체의 로그·백업 삭제 시점은 다를 수 있습니다. [Gmail 삭제 안내](https://support.google.com/mail/answer/7401?hl=ko) · [Google의 보관 및 삭제 안내](https://policies.google.com/technologies/retention?hl=ko)

답변을 받기 전에 문의로 보낸 개인정보를 지우려면 6항의 연락처로 요청할 수 있습니다. Mac에 저장된 설정과 작업 기록은 기기에 남으며, 이를 지우는 방법은 10항에 있습니다.

## 8. 안전성 확보 조치

회사는 문의 자료에 접근할 수 있는 사람을 담당자로 제한하고 계정 보안 설정을 유지합니다. 앱이 기기 안에 저장하는 자료는 macOS 사용자 계정과 앱 샌드박스의 보호를 받습니다.

## 9. 아동

앱은 아동을 대상으로 한 계정·광고·분석 기능이 없고, 14세 미만 아동의 개인정보를 의도적으로 수집하지 않습니다.

## 10. 기기 안의 자료 삭제

앱의 설정을 바꾸거나 등록 폴더를 지우면 새 정리를 멈출 수 있습니다. 일부 권한 북마크와 작업·복구 기록은 남을 수 있습니다. macOS 시스템 설정에서 앱 권한을 바꿔도 앱의 기존 기록이 모두 지워지지는 않습니다.

앱을 완전히 종료한 뒤 위 앱 데이터 폴더를 직접 지울 수 있습니다. 지우면 규칙, 권한 북마크, 되돌리기 기록, 중복 복사 확인 기록이 사라집니다. 앱을 지우는 것만으로 정리한 파일, 휴지통, 외부 백업이 지워지지는 않습니다. 다른 앱의 데이터나 상위 `Library` 폴더 전체를 지우지 마세요.

## 11. 개인정보 보호책임자

- 담당: 개인정보 보호 담당(고객지원)
- 연락처: <mailto:pcssak@pcssak.com>

## 12. 권익 침해 구제

한국에서 분쟁 조정은 개인정보분쟁조정위원회(1833-6972), 침해 상담은 개인정보침해신고센터(118), 사이버범죄 신고는 경찰청(182)에 문의할 수 있습니다. [개인정보 포털의 권익침해 구제 안내](https://www.privacy.go.kr/front/contents/cntntsView.do?contsNo=408)에서 기관별 연락처를 확인할 수 있습니다. 다른 국가나 지역에 거주하는 경우에는 적용 법령에 따라 현지 개인정보 보호 감독기관에도 문의할 수 있습니다.

## 13. 변경

처리하는 정보나 방법이 바뀌면 공개본과 앱 안의 이 문서를 함께 고치고 최종 수정일을 바꿉니다. 제품 안내: <https://pcssak.com/biuja> · 개인정보 문의: <mailto:pcssak@pcssak.com>

---

<a name="english"></a>

# PCssak Biuja Mac App Store Privacy Policy

- Last updated: 2026-11-25 · Applies from: PCssak Biuja 0.5.0, Mac App Store edition
- Operator: PCSSAK · Privacy contact (customer support): <mailto:pcssak@pcssak.com>
- Business address: 7F, Unit 75-B, 7-12 Nohae-ro 65-gil, Dobong-gu, Seoul, Republic of Korea

This Privacy Policy covers the Mac App Store edition of PCssak Biuja. The app organizes your files on your Mac. If you email PCSSAK for support, we process what you send as described in sections 3 and 4. This English text is a reference translation. If the two versions differ, the Korean version prevails to the extent permitted by applicable law.

## 1. Files are processed only on your Mac

Inspection, classification, moves, copies, Trash and Undo run on your Mac. The app does not automatically send file contents, names, paths, rules, previews or its operation records to us. There is no account with us, no advertising or tracking tool, no usage analytics, no cookies and no automatic error upload. To identify files precisely and to copy or undo safely, the app may compute hashes of some file contents on your Mac; these hashes are not sent anywhere.

You choose the folders to organize and the files to import or export using the macOS picker. It stores macOS permission bookmarks and file identifiers for the folders you chose in its private app data, so it can keep using them. Permission bookmarks are never included in exported settings. Exported settings can contain folder paths and rules, so review them before sharing.

The app uses the macOS WebKit outgoing-connection permission to display its interface. This permission is also required for the app's internal page connection; the app has no feature that sends files, paths or records to us.

## 2. Data stored on your Mac and how long it stays

App data is normally stored in `~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`. The exact location and how WebKit and logs are managed can vary with macOS. App data is protected by your macOS user account and the app sandbox; the app does not add its own encryption.

- `config.json` and settings recovery/backup copies: your folders, rules, language, appearance and schedule. They stay until you change or delete them.
- `journal.db` and its SQLite companion files: operation type, time and status, original and new locations, file size, modification time, identifiers, hashes and undo information. They are not copies of your files. Old completed records are trimmed at about 20,000 entries; in-progress, needs-review and recovery records can stay longer. So that automatic organizing does not process its own results again, the app keeps compact records such as the path, size, modification time and identifier of moved or restored files. Older records can expire as the archives fill.
- `macos-approved-roots.sqlite3` and companion files: permission bookmarks, paths and identifiers of the folders and files you chose. They are needed for automatic organizing and Undo after a restart and are never exported with settings.
- Logs, WebKit data and window state: startup and error diagnostics and the interface. Logs mostly record paths as masked identifiers, but some technical details can include local paths. The app does not upload its logs, and the app replaces log files according to a size limit.

The Mac App Store edition does not create licence keys or trial records. Section 5 explains how it handles the device verification values used to check a purchase.

## 3. Personal information we process (only when you contact us)

- Items: the email address you write from, any name you include, and the content and attachments of your message.
- Purpose: to answer your inquiry and address problems or security reports you send us.
- Retention and deletion: once our final reply resolves a routine inquiry, we delete the incoming messages, sent replies, attachments and any copies downloaded for support. We also permanently delete those messages from Gmail Trash. We keep no separate archive of routine inquiries.

When the law requires us to keep a record, we retain only the information required, keep it separate with restricted access and delete it when the required period ends. For example, where Korean e-commerce law requires PCSSAK to retain records of consumer complaints or disputes, the retention period is three years. [Article 6 of the Korean Enforcement Decree (in Korean)](https://www.law.go.kr/법령/전자상거래등에서의소비자보호에관한법률시행령/제6조)

Do not send real files, full paths, file lists, customer data, passwords, tokens, private keys or payment details. Please use made-up examples and masked screenshots.

## 4. Cross-border processing when you email support

When you email support, the sender address, display name (if supplied), recipient address, subject, message and any attachments you choose to send follow the route below. The app does not automatically attach files, paths or operation records.

- **Forwarding incoming mail — Cloudflare, Inc.** When your message arrives at our support address, Cloudflare Email Routing forwards it to our support inbox over the internet. Cloudflare says its routing service does not store message content. Its separate activity log may record delivery and email authentication results. Deleting the message from our inbox does not delete that log. [Email Routing](https://www.cloudflare.com/products/email-routing/) · [Activity log](https://developers.cloudflare.com/email-service/observability/logs/) · Contact Cloudflare about privacy (privacyquestions@cloudflare.com)
- **Receiving and replying — Google LLC.** PCSSAK reads forwarded inquiries in a personal Gmail account and uses that account to reply to you. Google processes incoming messages, sent replies and attachments. We delete routine inquiries when our final reply resolves them, as described in section 3. Google follows its own deletion process and says data can remain in encrypted disaster-recovery backups for up to six months. [Google Privacy Policy](https://policies.google.com/privacy?hl=en) · [How Google retains and deletes data](https://policies.google.com/technologies/retention?hl=en) · Contact Google about privacy in Korea (googlekrsupport@google.com)

**Where processing takes place.** PCSSAK is based in the Republic of Korea. Mail forwarding and mailbox processing can take place outside Korea. Google uses servers in multiple countries. Neither provider’s public documentation identifies every country involved for this support address, and Cloudflare’s routing documentation does not specify when its delivery logs are finally deleted.

**If you prefer not to send email.** You can close the message before sending it. In that case PCSSAK will not receive the inquiry or reply to it by email. You can still organize files and use Undo. For access to or deletion of information you have already sent, see section 6. PCSSAK does not sell personal information.

## 5. Apple and external services you choose

Apple manages purchases, installation, updates, refunds and your Apple Account. The release app uses Apple’s StoreKit to check signed information about the purchase of the app (AppTransaction). It checks the app identifier and distribution environment and computes and compares Apple’s device verification values in memory to confirm that the information belongs to this Mac. StoreKit may contact Apple during this process. PCSSAK does not receive your Apple Account password or card number. The app does not write the signed transaction or the device verification values to a separate file or send them to PCSSAK servers. See the [App Store privacy information](https://www.apple.com/legal/privacy/data/en/app-store/) for Apple's processing. Sales and settlement reports we receive from Apple follow Apple's policies and have nothing to do with the app uploading files.

When you open a website, GitHub or an email link yourself, that service processes the connection and what you send. The app never attaches files, paths or records to such links. If you copy or move files into iCloud or another sync folder, the files may sync according to that provider's settings; this is not an upload by the app.

## 6. Your rights and how to exercise them

You can ask to access, correct, delete or stop the processing of the personal information we hold about you. Email <mailto:pcssak@pcssak.com>; after confirming it is you, we act within the period required by law and tell you the result. Deletion can be limited where the law requires us to keep information, and we will tell you why.

## 7. Deleting information you send us

Messages deleted normally in Gmail can remain in Trash for up to 30 days. When we close a routine inquiry, we also remove its messages from Trash as described in section 3. Providers may delete their logs and backups on a different schedule. [Gmail deletion guide](https://support.google.com/mail/answer/7401?hl=en) · [How Google retains and deletes data](https://policies.google.com/technologies/retention?hl=en)

If you want us to delete the personal information you sent before we reply, use the contact in section 6. Settings and operation records stored on your Mac stay on your device. Section 10 explains how to remove them.

## 8. Security measures

We limit access to inquiries to the people handling them and maintain account security settings. Data the app stores on your Mac is protected by your macOS user account and the app sandbox.

## 9. Children

The app has no accounts, advertising or analytics aimed at children and does not knowingly collect personal information from children under 14.

## 10. Deleting data on your Mac

You can stop new organizing by changing the app's settings or removing a registered folder. Some permission bookmarks and operation or recovery records can remain. Changing the app's permissions in macOS System Settings does not delete the app's existing records.

After quitting the app completely, you can delete the app data folder above yourself. Doing so removes your rules, permission bookmarks, undo records and duplicate-copy evidence. Deleting the app alone does not delete the files it organized, the Trash or external backups. Do not delete other apps' data or the whole parent `Library` folder.

## 11. Privacy officer

- Contact point: Privacy contact (customer support)
- Email: <mailto:pcssak@pcssak.com>

## 12. Remedies

In Korea, you can contact the Personal Information Dispute Mediation Committee for mediation (1833-6972), the Personal Information Infringement Report Center for advice (118), or the police to report cybercrime (182). The [Korean Privacy Portal](https://www.privacy.go.kr/front/contents/cntntsView.do?contsNo=408) lists their contact details in Korean. If you live elsewhere, you can also contact your local data protection authority where applicable.

## 13. Changes

If what we process or how we process it changes, we update the public copy and this in-app document together and change the last-updated date. Product information: <https://pcssak.com/biuja> · Privacy contact: <mailto:pcssak@pcssak.com>
