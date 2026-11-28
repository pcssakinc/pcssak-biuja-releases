# PCssak Biuja v0.5.0 — Microsoft Store guide / Store 안내

**Preparation status:** v0.5.0 is a Store submission candidate. Store publication, installation,
and purchase verification remain pending. The product ID is reserved. We will add a public
Store link after the listing is available to customers. Existing free v0.1.x downloads remain available.

## English

### How to begin

1. After the Store edition is available to your account, install it through the confirmed official
   Microsoft Store listing. The Store handles signing and updates.
2. Choose Downloads or another folder as an **inbox**. Review its rules and destinations.
3. Select **Organize**, review the preview, exclude files if needed, and approve the work.
4. Answer questions about new file types, or choose **Keep in inbox**. Picking the inbox itself
   keeps that type there.
5. Check History. Use Undo only while its recorded file and safety conditions still hold.
6. Enable automation when ready. It handles new arrivals after a 60-second grace period;
   existing files and edits of pre-existing files need manual review.

Keep a separate tested backup. File organization is local; Undo is a safety convenience, not a
backup. Protected, locked, unavailable, changed, or ambiguous files can be left for review.
Originally empty folders stay in place rather than being silently deleted.

**Why is my Recycle Bin restore still pending?** If Windows or another app locks the file after it leaves the Recycle Bin, Biuja may keep it in a temporary folder. Close the app using the file. If Biuja shows the recovery screen, select **Check again**. In **History → All**, look for **Waiting to restore to original folder**, review the **Recorded holding location** and the original path, then select **Retry** on that item. This also applies to older records that reported a temporary-folder restore and to items with this status after you set them aside.

If you already moved the file back yourself, leave it there and retry. Biuja checks that the file at the recorded location matches the original before it marks the restore complete. If it cannot verify the file or its location, the restore stays pending. Keep the file and its record. A different file with the same name will not be overwritten.

**Where did my copy go after I chose Restore in the Windows Recycle Bin?** Undoing a copy leaves the source file in place. Explorer may return the copy to a temporary location inside the folder where Biuja had placed it. If it is still in the Recycle Bin, you can drag it into an empty folder of your choice. [How to find the restored copy](../SUPPORT.md)

**A copy or move stopped before it finished. Where can I check the file?** When Biuja identifies a working file at startup, select **View details in History** in the notice. **Work retained at startup** shows the affected entries. Compare the original path with the recorded location. Keep the original and the working file until you have verified the contents. A working file can have the expected size even when its contents have not been verified. If you already closed the app again, look in **History → All** for the interrupted operation.

### Trial and purchase FAQ

**How much does it cost?** Each user gets a 30-day trial. In the US, the planned one-time price
is US$9.99 for the first 100 days after the app first becomes generally available worldwide (UTC),
then US$14.99 starting at the same UTC time on day 101. Starting a trial does not reserve a price.
In South Korea, the planned prices for the same periods are ₩8,900 and ₩14,200. The date of
general availability and the changeover date have not been set.
Before buying, check the price and taxes shown in your Store market. There is no subscription.

**What should I do before the trial ends?** Review History, undo any operations you want to reverse and export
your settings before the expiry date. If the trial ends while Biuja is running, organization and preview stop.
You can still use History, eligible Undo actions and settings export in that session. If you open the app after
expiry, Windows may take you to the Store to buy it. You can access your organized files directly in File Explorer.

**Do I need a key or a PCSSAK account?** No. Buy through **Settings → Plan and license → Buy in
Microsoft Store**, then return to Biuja. The license follows your Microsoft account and Microsoft
Store terms; it is not Biuja's one-PC PB2 device-code license.

**I paid, but Biuja still shows a trial.** Check that Microsoft Store is signed in to the account
that bought Biuja. Return to Biuja and open **Settings → Plan and license → Check purchase status**.
This checks the existing entitlement without placing another order. If it is still missing, check
your [Microsoft order history](https://account.microsoft.com/billing/orders) before contacting support.

**What if I replace my PC?** Sign in to Microsoft Store with the account that purchased Biuja and install it from your library on a compatible PC. Microsoft's general app rules currently allow up to 10 compatible Windows devices, subject to the applicable Store terms. Biuja adds no single-PC activation. Installing the app on another PC does not copy your settings, history or files. [Digital goods usage rules](https://support.microsoft.com/en-us/windows/apps/usage-rules-for-digital-goods-rules)

**I bought it by mistake. How do I request a refund?** Sign in to the account used for the
purchase, find Biuja in [order history](https://account.microsoft.com/billing/orders), and follow
the [Windows app refund guide](https://support.microsoft.com/en-us/accounts-billing/subscriptions/get-a-refund-for-apps-and-games-purchased-from-microsoft-store).
If the option is missing, contact Microsoft Store support for your market. Eligibility depends
on the offer and applicable law. The 30-day trial does not automatically bill you or give every
purchase a 30-day return period. Section 4 of the [Biuja Store EULA](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-EULA-v0.5.0.md)
explains Korean consumer rights, including eligible purchases by minors without the required consent.

**Why are there two charges or a charge I do not recognize?** Biuja has no recurring fee.
Compare completed orders first. For an unfamiliar charge, use Microsoft's
[billing investigation](https://support.microsoft.com/en-us/accounts-billing/how-to-investigate-a-billing-charge-from-microsoft).
For an app defect or a consumer-rights issue, contact `pcssak@pcssak.com`. Describe what
happened and omit card details, account credentials, full receipts and personal file paths.

**Can I use it offline?** File operations are local, but the Store confirms your license.
A temporary query failure preserves the last confirmed state during that app run. Purchased
status is not stored as a permanent offline license: after restarting offline, access can fall
back to the local trial state until the Store can confirm the purchase.

**What updates are included?** Stability updates continue and at least one feature update is
included within the scope of the [Store EULA](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-EULA-v0.5.0.md). This is not a promise that every future
separate product or paid major version is included. Microsoft Store delivers this edition's updates. To check manually, open Downloads or Library in Microsoft Store and check for updates.

**A folder or rule disappeared after an update. How do I review it?** If the safety check excluded it, look for `config.before-safety-<fingerprint>.json` beside `config.json` in the Store edition’s settings folder. Section 4 of the [Store privacy policy](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-PRIVACY-v0.5.0.md#4-local-data-and-retention) lists the usual folder and explains when Windows redirects it. Open the copy in a text editor and leave the active `config.json` in place. In Biuja, add back only folders and rules that meet the current safety checks, then check the preview before enabling automation. Once you save the reviewed settings, you can delete the copy. If the saved settings still contain an excluded item, the next launch can create the copy again.

If Biuja was forced to close, a temporary file named `config.before-safety-<fingerprint>.<random-id>.tmp` may remain. Fully close Biuja and check both `config.json` and the finished safety copy before deleting only the temporary file. Biuja does not use it for automatic recovery. These files can contain personal paths and rules, so leave them out of support requests.

**Will my free version become paid?** Existing v0.1.x versions remain free in those versions and
are not updated automatically into the Store edition. v0.5.0 has no old free tier. Avoid having
both editions automatically organize the same folder. Back up/export settings before switching;
do not assume the Store and standalone data locations are identical.

**What reaches the network?** Installation, licensing, purchase, and updates use Microsoft Store.
Biuja does not upload user files for organization. Read the [Privacy Policy](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-PRIVACY-v0.5.0.md).
The app creates compatibility device-code and trial records locally; these are not Store purchase inputs.

Windows 11 x64 is recommended. On Windows 10, the 32-bit and 64-bit Store packages require version 22H2 (build 19045). To check the version and build, press **Windows + R**, enter **winver**, and press **Enter**. Older Windows 10 builds cannot install this Store update. Windows 10 and x86 are limited compatibility targets. Biuja requires Microsoft Edge WebView2 Runtime version 111 or later. Do not disable
SmartScreen, Microsoft Defender, or another security product to install an app.

## 한국어

**준비 상태:** v0.5.0 Store 제출 후보의 안내입니다. Store 공개·설치·구매 검증 완료를 의미하지 않습니다.
상품 ID를 예약했습니다. 고객에게 공개된 실제 목록을 확인하면 Store 주소를 안내합니다. 기존 무료 v0.1.x 다운로드는 유지합니다.

### 처음 사용하기

1. 계정에 Store판이 제공되면 확인한 공식 Microsoft Store 목록에서 설치합니다. Store가 서명·업데이트를 맡습니다.
2. 다운로드 폴더 등을 **받는 곳**으로 고르고 규칙·목적지를 확인합니다.
3. **정리하기**에서 미리보기를 읽고 필요 없는 파일을 제외한 뒤 실행합니다.
4. 처음 보는 파일 종류의 질문에 답하거나 **받는 곳에 그대로 두기**를 고릅니다. 받는 곳 자신을 골라도 그대로 둡니다.
5. 기록을 확인하고 현재 파일·안전 조건이 맞을 때 되돌립니다.
6. 익숙해지면 자동 정리를 켭니다. 켠 뒤 도착한 파일을 60초 뒤 처리합니다. 기존 파일과 기존 파일 편집은 수동으로 확인합니다.

중요한 파일은 별도 백업을 유지하세요. 정리는 로컬 처리하고 되돌리기는 백업이 아닙니다. 보호·잠금·접속 실패·객체 변경·
여러 복구 후보 때문에 파일을 그대로 둘 수 있습니다. 원래 빈 폴더는 조용히 지우지 않고 원래 위치에 남깁니다.

**휴지통에서 꺼낸 파일이 왜 복원 대기로 남나요?** 파일이 휴지통에서 나온 뒤 Windows나 다른 앱이 파일을 잠그면 임시 폴더에 남을 수 있습니다. 파일을 사용 중인 앱을 닫고, 비우자에 복구 화면이 열려 있다면 **다시 확인**을 누르세요. **기록 → 전체**에서 **원위치 복원 대기** 항목의 **기록된 보관 위치**와 원래 경로를 확인한 뒤 해당 항목의 **다시 시도**를 누르세요. 이전 버전에서 임시 폴더에 복원됐다고 안내한 기록이나, ‘따로 두기’ 후 이 상태로 표시된 항목도 같은 방법으로 확인할 수 있습니다.

이미 직접 파일을 원래 위치에 옮겼다면 그대로 두고 다시 시도하세요. 비우자는 기록된 위치의 파일이 원본과 일치한 것을 확인해야 복원을 완료로 표시합니다. 파일이나 위치를 확인할 수 없으면 대기가 유지됩니다. 이때는 파일과 기록을 보관하세요. 이름이 같은 다른 파일은 덮어쓰지 않습니다.

**복사 되돌리기 후 Windows 휴지통에서 ‘복원’을 눌렀는데 복사본은 어디 있나요?** 원본 파일은 그대로 있습니다. 탐색기는 복사본을 비우자가 복사했던 폴더 안의 임시 위치로 돌려놓을 수 있습니다. 아직 휴지통에 있다면 원하는 빈 폴더로 끌어 놓을 수 있습니다. [복원된 복사본을 찾는 방법](../SUPPORT.md)

**복사나 이동이 도중에 끊겼습니다. 파일을 어디서 확인하나요?** 비우자가 시작하면서 작업 파일을 확인하면 안내에서 **기록에서 자세히 보기**를 누르세요. **이번 시작에서 보존된 작업**에 해당 항목이 표시됩니다. 원래 경로와 **중단 파일 보존 위치**를 대조하고, 내용을 확인할 때까지 원본과 작업 파일을 함께 보관하세요. 크기가 원본과 같아도 복사가 끝났는지는 별도로 확인해야 합니다. 앱을 다시 닫았다면 **기록 → 전체**에서 중단된 작업을 찾으세요.

### 체험·구매 자주 묻는 질문

**가격은 얼마인가요?** 체험은 사용자마다 30일입니다. 미국 일회 구매 예정가는 전 세계 첫 일반 공개
시각(UTC)부터 100일간 9.99달러, 101일째 같은 시각부터 14.99달러입니다. 체험을 시작해도 그날의
가격이 예약되지는 않습니다. 한국의 같은 기간 예정가는 각각 8,900원과 14,200원입니다. 일반 공개일과 가격 전환일은 아직 정해지지 않았습니다.
구매를 확정할 때 해당 지역 Store에 표시된 가격과 세금을 확인하세요. 구독료는 없습니다.

**체험이 끝나기 전에 무엇을 해야 하나요?** 기록에서 필요한 작업을 되돌리고 설정을 내보내 두세요.
앱을 쓰는 도중 체험이 끝나면 정리와 미리보기가 멈춥니다. 열린 앱에서는 기록, 안전 조건을 충족한 되돌리기,
설정 내보내기를 계속 쓸 수 있습니다. 종료 후 다시 열면 Windows가 구매 화면을 먼저 표시할 수 있습니다.
정리한 파일은 파일 탐색기에서 직접 열 수 있습니다.

**기기 코드·사용권 키·PCSSAK 계정이 필요한가요?** 아닙니다. **설정 → 요금제·사용권 → Microsoft Store에서 구매**
후 앱으로 돌아오면 확인합니다. 사용권은 Microsoft 계정과 Store 조건에 따르며 PC 1대 PB2 기기 코드 사용권이 아닙니다.

**결제했는데 아직 체험 중으로 표시돼요.** 구매에 사용한 계정으로 Microsoft Store에 로그인했는지 확인한 뒤,
비우자로 돌아와 **설정 → 요금제·사용권 → 구매 상태 다시 확인**을 누르세요. 이 버튼은 추가 결제 없이
기존 사용권을 조회합니다. 계속 확인되지 않으면 [Microsoft 주문 기록](https://account.microsoft.com/billing/orders)을 확인한 뒤 문의하세요.

**PC를 바꾸면 다시 사야 하나요?** 구매한 Microsoft 계정으로 새 PC의 Store에 로그인해 라이브러리에서 다시 설치하세요. Microsoft의 현재 일반 앱 규칙은 호환 Windows 기기 최대 10대를 안내합니다. 비우자 자체의 1대 활성화 제한은 없습니다. 새 PC에는 파일·설정·기록이 자동으로 옮겨지지 않습니다. [기기 사용 규칙](https://support.microsoft.com/en-us/windows/apps/usage-rules-for-digital-goods-rules)

**실수로 구입했어요. 어디에서 환불을 요청하나요?** 구매한 Microsoft 계정으로 로그인해
[주문 기록](https://account.microsoft.com/billing/orders)에서 비우자를 찾은 뒤
[Windows 앱 환불 안내](https://support.microsoft.com/ko-kr/accounts-billing/subscriptions/get-a-refund-for-apps-and-games-purchased-from-microsoft-store)를 따르세요.
요청 버튼이 보이지 않으면 구매 지역의 Microsoft Store 지원에 문의하세요. 환불은 상품 조건과
적용 법률을 따릅니다. 30일 체험이 끝나도 자동 결제되지 않으며, 체험 기간과 구매 후 환불 기간은
별개입니다. 법정대리인의 동의가 필요한 미성년자의 구매를 포함한 한국 소비자의 권리는
[비우자 Store판 이용약관](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-EULA-v0.5.0.md) 제4조에서 확인하세요.

**두 번 결제됐거나 모르는 금액이 청구됐어요.** 비우자는 갱신료가 없습니다. 주문 기록에서 결제가
완료된 거래를 대조하세요. 출처를 알 수 없는 청구는 Microsoft의
[결제 조사](https://support.microsoft.com/ko-kr/accounts-billing/how-to-investigate-a-billing-charge-from-microsoft)에서 확인할 수 있습니다.
앱 결함이나 소비자 권리에 관해 `pcssak@pcssak.com`에 문의할 때는 증상 위주로 알려주세요.
카드 정보·계정 인증 정보·영수증 전체·개인 파일 경로는 보내지 마세요.

**인터넷 없이 쓸 수 있나요?** 파일 작업은 로컬이지만 Store가 사용권을 확인합니다. 실행 중 일시 조회 실패는 마지막
확인 상태를 유지합니다. 구매 상태를 영구 오프라인 사용권으로 저장하지 않으므로 오프라인 재시작 때는 Store가 구매를
다시 확인할 때까지 로컬 체험 상태로 제한될 수 있습니다.

**업데이트도 포함되나요?** 안정성 업데이트 계속 제공·기능 업데이트 1회 이상 포함의 범위는
[Store EULA](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-EULA-v0.5.0.md)에 따릅니다. 모든 미래 별도 제품·유료 주요 버전이 포함된다는 뜻은 아닙니다.
이 판의 업데이트는 Microsoft Store가 제공합니다. 수동으로 확인하려면 Store의 다운로드 또는 라이브러리에서 업데이트를 확인하세요.

**업데이트 후 폴더나 규칙이 보이지 않으면 어떻게 확인하나요?** 안전 검사로 제외됐다면 Store판 설정 폴더에서 `config.json` 옆의 `config.before-safety-<지문>.json`을 텍스트 편집기로 열어 보세요. [개인정보 처리방침](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-PRIVACY-v0.5.0.md#4-로컬-데이터와-보관) 제4절에서 일반적인 폴더와 Windows가 저장 위치를 바꾸는 경우를 확인할 수 있습니다. 사용 중인 `config.json`은 그대로 두세요. 앱에서 현재 안전 기준에 맞는 폴더와 규칙만 다시 설정하고, 자동 정리를 켜기 전에 미리보기로 확인하세요. 검토한 설정을 저장하면 사본을 삭제할 수 있습니다. 저장된 설정에 제외 대상이 남아 있으면 다음 실행 때 사본이 다시 생길 수 있습니다.

앱이 강제 종료됐다면 `config.before-safety-<지문>.<임의값>.tmp`가 남을 수 있습니다. 앱을 완전히 닫은 뒤 `config.json`과 완성된 사본을 확인하고 임시 파일만 삭제하세요. 임시 파일은 자동 복원에 쓰이지 않습니다. 두 파일 모두 개인 경로와 규칙을 담을 수 있으니 지원 문의에 첨부하지 마세요.

**기존 무료판이 유료로 바뀌나요?** 쓰던 v0.1.x 버전은 계속 무료이며 Store판으로 자동 업데이트하지 않습니다.
v0.5.0 안에는 기존 무료 범위가 없습니다. 두 판이 같은 폴더를 자동 정리하지 않게 하세요. 전환 전 설정을 백업·
내보내기하고 Store판과 설치형의 데이터 위치가 같다고 가정하지 마세요.

**네트워크로 무엇을 보내나요?** Store 설치·사용권·구매·업데이트는 Microsoft와 연결합니다. Biuja는 정리를 위해
사용자 파일을 업로드하지 않습니다. [개인정보 처리방침](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-PRIVACY-v0.5.0.md)을 확인하세요. 호환성 기기 코드·체험 기록은
로컬에 만들며 Store 구매 입력값으로 요구하지 않습니다.

Windows 11 x64를 권장합니다. Windows 10에서 32비트·64비트 Store 패키지를 설치하려면 버전 22H2(빌드 19045)가 필요합니다. **Windows 키 + R**을 누르고 **winver**를 입력한 뒤 **Enter**를 누르면 버전과 빌드가 표시됩니다. 더 오래된 Windows 10 빌드에서는 이 Store 업데이트를 설치할 수 없습니다. Windows 10과 x86은 제한적 호환성 대상입니다. 비우자 화면을 사용하려면 Microsoft Edge WebView2 Runtime 111 이상이 필요합니다. 설치를 위해 Windows 보안 기능을 끄지 마세요.

Previously valid PCSSAK license keys may retain their compatibility rights under their own terms;
they do not replace a Store transaction or change Microsoft account rules. See the EULA. / 기존 유효 PCSSAK 키의
호환 권한은 해당 키의 조건에 따라 별도로 인정될 수 있으며 Store 구매·환불이나 Microsoft 계정 범위를 바꾸지 않습니다.

## Related documents / 함께 읽기

- [Store EULA / Store 약관](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-EULA-v0.5.0.md)
- [Store Privacy Policy / Store 개인정보 처리방침](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/STORE-PRIVACY-v0.5.0.md)
- [Windows third-party notices / 윈도우 제3자 라이선스 고지 전문](https://raw.githubusercontent.com/pcssakinc/pcssak-biuja-releases/main/windows-v0.5.0/THIRD-PARTY-NOTICES.txt)
- [Windows component source / 윈도우 구성요소 원본 소스 이용 안내](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/windows-v0.5.0/THIRD-PARTY-SOURCE.md)
- [Legacy v0.1.x EULA / 기존 무료판 약관](https://github.com/pcssakinc/pcssak-biuja-releases/blob/0ff2bfedfd276697dfc88f6376e0510258e2a4c1/EULA.md)
- [Legacy v0.1.x Privacy Policy / 기존 무료판 개인정보](LEGACY-v0.1.x-PRIVACY.md)
- [Support / 문의](../SUPPORT.md)

Support: `pcssak@pcssak.com`. Use synthetic examples and remove personal paths, names, document
contents, and secrets from reports. / 제보에는 가상 예시를 쓰고 개인 경로·이름·문서 내용·비밀값을 제거하세요.
