# Security Policy / 보안 정책

## Supported releases

Security fixes are evaluated for the **latest public PCssak Biuja Free Early Access release**.
Older beta builds may not receive a separate fix. Confirm the current version on the
[latest release page](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest)
before reporting.

Free Early Access software can contain undiscovered defects. This policy describes the
reporting route; it is not a warranty that the application is free of vulnerabilities.

## Report a vulnerability privately

Do not post exploitable details in a public issue. Email `pcssakinc@gmail.com` when a problem
could enable or contribute to:

- bypassing update-signature verification or substituting an untrusted update;
- escaping the user-selected folder scope through path manipulation, links, junctions, or
  another filesystem edge case;
- unintended overwrite, permanent deletion, arbitrary file move, or access to an unrelated
  file;
- unsafe rollback, work-journal tampering, or replay of a stale operation;
- code execution, privilege escalation, secret exposure, or unauthorized network transfer;
- a denial of service that can repeatedly prevent safe recovery of an in-progress operation.

Include, when safely possible:

- the PCssak Biuja version and exact installer source;
- Windows edition, build, and x64 or x86 architecture;
- the security impact and conditions required to reproduce it;
- minimal steps using synthetic folders and files;
- whether details or proof of concept are already public;
- a safe contact method and any reasonable disclosure constraints.

Do not send passwords, private keys, tokens, payment information, personal identifiers,
customer files, confidential directory listings, or an archive of the affected real folder.
Replace sensitive names and contents with the smallest synthetic example. If a sensitive proof
is necessary, describe it first and agree on a safer transfer method before sending it.

PCSSAK will triage reports according to user impact, file-loss risk, exploitability, and
reproducibility; investigate within solo-maintainer capacity; and prepare a fix and regression
check where practical. This is not a guaranteed response-time, fix-deadline, or bounty program.

## Authenticity checks

- Download only from [pcssak.com/biuja](https://pcssak.com/biuja) or this official `pcssakinc`
  release repository.
- Compare the installer SHA-256 with `SHA256SUMS.txt` from the same release.
- The in-app updater verifies the PCSSAK Tauri update signature before installation.
- A Tauri updater signature and SHA-256 do not replace Windows Authenticode signing.
- The initial Windows installer is not Authenticode-signed and may show Unknown publisher or
  SmartScreen. Do not disable SmartScreen, Microsoft Defender, or another security product.

## 한국어

보안 수정은 **최신 공개 PCssak Biuja 무료 Early Access 버전**을 기준으로 검토합니다. 이전
베타 빌드에는 별도 수정이 제공되지 않을 수 있으므로 제보 전에
[최신 릴리스](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest)를 확인하세요.
Early Access에는 발견되지 않은 오류가 남아 있을 수 있으며, 이 정책은 보안 결함이 없다는
보증이 아니라 안전한 제보 경로를 설명합니다.

다음 문제는 공개 Issue에 악용 가능한 세부 내용을 올리지 말고 `pcssakinc@gmail.com`으로
보내주세요.

- 업데이트 서명 검증 우회 또는 신뢰하지 않은 업데이트 바꿔치기
- 경로 조작, 링크, 정션이나 파일시스템 예외를 이용한 사용자 선택 폴더 범위 이탈
- 의도하지 않은 덮어쓰기·영구 삭제·임의 파일 이동·관계없는 파일 접근
- 안전하지 않은 되돌리기, 작업저널 변조 또는 오래된 작업의 재실행
- 코드 실행, 권한 상승, 비밀정보 노출 또는 승인되지 않은 네트워크 전송
- 진행 중인 작업의 안전한 복구를 반복적으로 방해할 수 있는 서비스 거부

가능하면 PCssak Biuja 버전과 정확한 설치 출처, Windows 에디션·빌드·아키텍처, 보안 영향,
합성 폴더와 파일을 사용한 최소 재현 절차, 이미 공개됐는지 여부와 안전한 연락 방법을
포함하세요.

비밀번호, 개인키, 토큰, 결제 정보, 개인 식별정보, 고객 파일, 비공개 폴더 목록이나 실제 문제
폴더 전체 압축본은 보내지 마세요. 민감한 이름과 내용은 가장 작은 합성 예제로 바꾸세요. 민감한
증거가 꼭 필요하면 먼저 설명만 보내고 더 안전한 전달 방법을 합의한 뒤 전송하세요.

PCSSAK은 사용자 영향, 파일 손실 위험, 악용 가능성과 재현 가능성을 기준으로 우선순위를 정하고
1인 운영 범위에서 조사하며, 가능한 경우 수정과 회귀 검증을 준비합니다. 응답 시간·수정 기한·
포상금을 보장하는 제도는 아닙니다.

공식 설치 파일은 [pcssak.com/biuja](https://pcssak.com/biuja) 또는 이 `pcssakinc` 공식
저장소에서만 받고 같은 릴리스의 `SHA256SUMS.txt`와 비교하세요. 앱 내부 업데이트는 PCSSAK
Tauri 서명을 검증하지만 이 서명과 SHA-256은 Windows Authenticode를 대신하지 않습니다.
최초 설치 파일에는 Authenticode 서명이 없어 알 수 없는 게시자나 SmartScreen이 나타날 수
있으며, 설치를 위해 SmartScreen·Microsoft Defender·다른 보안 제품을 끄면 안 됩니다.
