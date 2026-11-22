# 비우자 Mac 고객지원 · PCssak Biuja Support for Mac

Mac App Store판 0.5.0 · [English](#english)

## 폴더에 접근할 수 없다고 나와요

외장 드라이브의 폴더라면 먼저 드라이브를 다시 연결하세요. 안내가 계속되면 비우자 **홈 → 해당 폴더의 규칙 → 설정 더 보기 → 폴더 다시 선택**을 열고 macOS 선택창에서 원래 폴더를 선택하세요. 규칙의 목적지가 그 폴더 밖에 있다면 규칙 편집 화면에서 목적지 폴더도 다시 선택하세요. 폴더를 다시 선택하는 동안에는 파일이 이동하지 않습니다. 다음 실행 전에 미리보기에서 출발 위치와 목적지를 확인할 수 있습니다.

## 업데이트 후 예전 규칙 하나가 보이지 않아요

비우자가 시작할 때 안전 검사로 규칙을 제외하면 변경 전 설정의 사본을 남깁니다. Finder에서 **이동 → 폴더로 이동**(⇧⌘G)을 열고 아래 경로를 붙여 넣으세요.

`~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`

`config.json` 옆에서 이름이 `config.before-safety-`로 시작하고 `.json`으로 끝나는 파일을 찾으세요. 사본을 텍스트 편집기로 열어 예전 규칙 이름과 조건을 확인하세요. 사본 전체를 가져오거나 `config.json`을 덮어쓰지 마세요. 필요한 규칙은 비우자의 해당 폴더 **규칙**에서 현재 목적지를 다시 선택해 만들고, 실행 전에 **미리보기**에서 결과를 확인하세요.

## 되돌리기가 일부 파일에서 멈췄어요

**기록**에서 해당 실행을 열고 파일별 결과와 실패 이유를 확인하세요. 예를 들어 파일 3개를 옮긴 뒤 한 개를 직접 삭제했다면, 다른 파일의 되돌리기가 성공해도 삭제한 파일은 복원하지 못할 수 있습니다. 실패한 항목의 원래 폴더와 드라이브를 확인하세요. 드라이브를 다시 연결한 뒤 재시도 동작이 표시되면 그 항목을 다시 시도하세요. 파일 내용이 바뀌었다면 현재 파일과 백업을 먼저 확인하세요.

비우자로 휴지통에 보낸 파일은 Finder에서 ‘되돌려 놓기’가 보이지 않을 수 있습니다. 휴지통을 비우기 전에 비우자의 **기록**에서 되돌리기를 사용하세요. 휴지통까지 비웠다면 독립적으로 보관한 백업에서 복원할 수 있는지 확인하세요.

## 구입·재다운로드·환불

**이미 비우자를 쓰고 있다면** Mac App Store의 **업데이트**에서 비우자를 업데이트하세요. 자동 업데이트를 켜 두면 App Store가 처리합니다. 같은 Mac에서 업데이트할 때는 앱과 데이터를 지우지 말고 그대로 두세요. 업데이트 뒤 기존 규칙이나 기록이 보이지 않으면 새 규칙을 만들기 전에 고객지원으로 알려주세요. [Mac 앱 업데이트 방법](https://support.apple.com/ko-kr/102629)

구입과 업데이트는 Mac의 App Store에서 진행합니다. 구입한 앱이 보이지 않으면 구입할 때 사용한 Apple 계정으로 로그인해 확인하세요. 환불은 Apple에 요청할 수 있습니다. [앱 다시 다운로드하기](https://support.apple.com/ko-kr/102417) · [환불 요청하기](https://support.apple.com/ko-kr/118223)

같은 금액이 두 번 보이면 다시 결제하기 전에 App Store 구입 내역을 확인하세요. 청구가 보류 중이면 Apple 영수증을 받은 뒤 환불을 신청할 수 있습니다. 가족 구입은 구입 항목 공유 설정과 해당 앱의 공유 가능 여부를 확인하세요. [구입 내역](https://support.apple.com/ko-kr/118212) · [가족 구입 확인](https://support.apple.com/ko-kr/108911) · [환불 요청 상태](https://support.apple.com/ko-kr/118224)

비우자에서 ‘구입을 확인하지 못했다’는 안내가 계속 보이면 앱의 **설정 → 구입 다시 확인**을 선택하세요. Apple의 로그인 창이 열릴 수 있습니다. 구입 정보를 확인하는 동안에는 **기록**에서 이전 작업을 보고 가능한 되돌리기와 복구를 진행할 수 있습니다.

환불 자체로 비우자가 이미 정리한 파일이나 작업 기록을 삭제하지 않습니다. 사용권이 철회되면 새 파일 정리가 제한될 수 있습니다. 환불을 신청한 뒤에도 제품 오류나 소비자 권리에 관한 문의는 PCSSAK에 보내 주세요.

## 개인정보 안내와 이용안내

비우자의 **설정 → 개인정보·이용안내**에서 ‘개인정보 안내’ 또는 ‘이용안내’를 여세요. ‘전문 언어’에서 한국어와 영어를 선택할 수 있습니다.

## 문의하기

문의할 때 앱 버전과 macOS 버전, 선택한 동작, 예상한 결과와 실제 결과, 표시된 오류 문구를 알려주세요. 파일 이름이나 경로는 `테스트/예시.pdf`처럼 바꿔 주세요. 스크린샷은 이름·경로·이메일 등 개인 정보를 가릴 수 있을 때만 첨부하세요. 실제 문서, 암호, 인증 코드, 결제 정보는 보내지 마세요. [PCSSAK 고객지원에 이메일 보내기](mailto:pcssak@pcssak.com)

문의는 Cloudflare Email Routing을 통해 개인용 Gmail로 전달됩니다. PCSSAK은 답변 후 문의 메일과 첨부를 메일함에서 삭제하며 별도 문의 기록을 보관하지 않습니다. 일반 삭제한 메일과 첨부는 Gmail 휴지통에 최대 30일간 남을 수 있습니다.

<a name="english"></a>

# PCssak Biuja Support for Mac

Mac App Store edition · Version 0.5.0

## Biuja can’t access my folder

If the folder is on an external drive, reconnect the drive first. If the message persists, open **Home → Rules** for that folder, then choose **More settings → Select folder again**. Select the original folder in the macOS picker. If the rule sends files outside that folder, select its destination again under **Where to** in the rule editor. Selecting a folder again does not move files. Before your next run, use the preview to check the source and destination.

## An older rule is missing after an update

When Biuja leaves out a rule during its startup safety check, it keeps a copy of the original settings. In Finder, choose **Go → Go to Folder** (⇧⌘G) and paste this path.

`~/Library/Containers/com.pcssak.biuja.macstore/Data/Library/Application Support/com.pcssak.biuja.macstore/`

Beside `config.json`, look for a file whose name starts with `config.before-safety-` and ends in `.json`. Open the copy in a text editor and find the old rule by name to review its conditions. Leave `config.json` in place and avoid importing the entire copy. Recreate the rule under **Rules** for that folder, select its current destination, and check the **Preview** before running it.

## Undo stopped for some files

Open the run in **History** and check the result and reason for each file. For example, if you moved three files and later deleted one yourself, Undo may restore the others while the deleted file remains missing. Check the original folder and drive for the affected item. After reconnecting a drive, retry the item if that action is available. If the contents changed, check your current file and backup first.

Finder may not offer Put Back for a file Biuja sent to the Trash. Use Undo in Biuja’s **History** before emptying the Trash. If you have already emptied it, check whether you can restore the file from a separate backup.

## Purchases, downloads and refunds

**Already using Biuja?** Open **Updates** in the Mac App Store or turn on automatic updates. Leave the app and its data in place when updating on the same Mac. If existing rules or history appear to be missing afterward, contact support before creating new rules. [Update apps on Mac](https://support.apple.com/en-us/102629)

Use the App Store on your Mac to purchase or update Biuja. If a purchase is missing, make sure you are signed in with the Apple Account you used to buy it. You can request a refund from Apple. [Redownload apps](https://support.apple.com/en-us/102417) · [Request a refund](https://support.apple.com/en-us/118223)

If you see the same amount twice, check your App Store purchase history before paying again. If the charge is pending, wait for the Apple receipt before requesting a refund. For family purchases, check your purchase sharing settings and whether the app can be shared. [Purchase history](https://support.apple.com/en-us/118212) · [Family purchases](https://support.apple.com/en-us/108911) · [Refund status](https://support.apple.com/en-us/118224)

If Biuja says it can’t verify your purchase, open **Settings → Recheck purchase**. Apple may ask you to sign in. While the purchase is being checked, you can still open **History**, review previous runs and use any available undo and recovery actions.

A refund does not cause Biuja to delete files it has organized or its operation history. New organizing may be restricted if the purchase is revoked. You can still contact PCSSAK about a product defect or your consumer rights after you request a refund.

## Privacy and terms

In Biuja, open **Settings → Privacy and terms**, then choose **Privacy notice** or **Terms and consumer guide**. Use **Full text language** to read either document in Korean or English.

## Contact support

Include the app version, macOS version, the action you took, what you expected, what happened and any error message. Replace personal filenames or paths with examples such as `Test/Example.pdf`. Only attach screenshots if you can obscure personal information such as names, paths and email addresses. Please leave out original documents, passwords, verification codes and payment details. [Email PCSSAK support](mailto:pcssak@pcssak.com)

Cloudflare Email Routing forwards support messages to a personal Gmail account. After replying, PCSSAK deletes the message and its attachments from the support mailbox and keeps no separate inquiry archive. Messages and attachments deleted normally may remain in Gmail Trash for up to 30 days.
