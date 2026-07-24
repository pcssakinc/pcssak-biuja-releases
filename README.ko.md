# PCssak Biuja - 공식 Windows 다운로드

[English](README.md) · [제품 홈페이지](https://pcssak.co.kr/biuja) ·
[최신 릴리스](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest)

> **현재 배포본: 1.0 이전 무료 얼리 액세스** — 기능·번역·파일 처리 규칙이 바뀔 수 있고
> 발견되지 않은 오류가 남아 있을 수 있습니다. 중요한 파일은 항상 별도로 백업하세요.

**먼저 확인하고, 안전하게 정리하며, 내 파일을 내가 통제합니다.** PCssak Biuja는 사용자가
선택한 범위의 파일 정리 계획을 미리 보여주고, 완료한 작업을 기록하며, 원본을 의도적으로
덮어쓰거나 영구 삭제하지 않는 되돌리기를 지원합니다.

> **저장소 범위:** 이곳은 PCssak Biuja의 공식 바이너리 배포·문서·이슈 접수 저장소입니다.
> 애플리케이션 소스는 비공개 독점 소프트웨어입니다. 저장소가 공개되어 있다는 이유만으로
> 애플리케이션이 오픈소스가 되는 것은 아니며, 이 저장소에는 제품 소스 코드가 없습니다.

## 다운로드

[최신 공식 릴리스](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest) 또는
[PCssak Biuja 제품 페이지](https://pcssak.co.kr/biuja)에서만 내려받으세요.

- 일반 사용에는 Windows 11 Home/Pro용 **x64**를 선택합니다. Windows 11 x64가 권장 환경이자
  공식 검증 예정 대상입니다.
- Windows 10 x64는 Microsoft 일반 지원이 2025년 10월 14일 종료됐으므로 제한적·최선 노력
  베타 호환성만 제공합니다. Windows 11 업그레이드를 권장합니다.
- **x86**은 32비트 Windows 10 베타 시험 또는 Windows x64에서 32비트 앱 호환성을 시험할
  때만 사용하세요. Windows 11에는 32비트 에디션이 없으며 Windows 11에서 x86 PCssak Biuja를
  실행해도 운영체제는 64비트입니다.
- ARM64 네이티브, Windows S 모드, macOS, Linux는 지원하지 않습니다.
- 실행하기 전에 같은 릴리스의 `SHA256SUMS.txt`와 설치 파일 이름·SHA-256을 비교하세요.

PowerShell에서는 내려받은 설치 파일을 다음과 같이 확인할 수 있습니다.

```powershell
Get-FileHash -Algorithm SHA256 '.\DOWNLOADED-INSTALLER.exe'
```

예제 부분을 실제 릴리스의 정확한 파일 이름으로 바꾸고, 출력값이 `SHA256SUMS.txt`의 해당
항목과 완전히 일치하는지 확인합니다.

> [!WARNING]
> 최초 Windows 설치 파일에는 아직 Authenticode 서명이 없습니다. Windows에 **알 수 없는
> 게시자** 또는 **Microsoft Defender SmartScreen** 경고가 나타날 수 있습니다. 위 공식
> 경로에서만 내려받고 SHA-256을 확인하세요. 설치를 위해 SmartScreen, Microsoft Defender,
> 다른 보안 제품을 끄지 마세요. 출처·파일 이름·해시를 확인할 수 없다면 실행하지 마세요.

앱 화면은 11개 언어를 지원하지만 현재 법률·안전 문서는 한국어와 영어로 제공합니다. 적용
법률이 허용하는 범위에서 한국어 법률 문구를 기준으로 하며 영어는 참고 번역입니다. 적용 약관과
안전 한계를 이해할 수 있을 때만 Early Access를 설치하세요.

## 현재 무료 Early Access 기능

1. 사용자가 선택한 범위의 파일을 확인하고 지원 규칙에 따라 자동 정리 계획을 준비합니다.
2. 파일을 변경하기 전에 예정된 정리 작업을 미리 보여줍니다.
3. 지원되는 이동·복사를 실행합니다. 지원되는 정리 작업은 영구 삭제 대신 Windows 휴지통을
   사용하고 기존 대상 파일을 의도적으로 덮어쓰지 않습니다.
4. 완료된 작업을 로컬 작업저널에 기록합니다.
5. 기록된 원본·대상과 현재 파일시스템 상태가 안전한 역작업을 허용할 때 지원되는 작업을
   되돌립니다.
6. 영구 삭제를 하지 않습니다. PCssak Biuja는 정리 도구이며 보안 삭제기·백업·복구 보장
   도구가 아닙니다.

현재 공개 빌드는 1.0 이전의 **무료 Early Access**입니다. 안정 버전 전에는 기능·번역·파일
처리 규칙이 바뀔 수 있고 아직 발견되지 않은 오류가 남아 있을 수 있습니다.

## 로컬 처리와 네트워크 예외

- 파일 정리 자체는 **100% 로컬 처리**합니다. 파일 이름·경로·정리 판단·미리보기·작업저널·
  되돌리기는 기기에 머물며 PCSSAK은 정리를 위해 사용자 파일이나 내용을 업로드하지 않습니다.
- 공개 Early Access에는 PCSSAK 계정, 광고, 사용 분석, 추적, 클라우드 파일 색인, 자동 오류
  업로드가 없습니다.
- 독립형 빌드는 업데이트를 확인하고 내려받기 위해 공식 `pcssakinc` GitHub 릴리스에 연결할
  수 있습니다. 업데이트 패키지는 PCSSAK Tauri 업데이트 키 서명을 검증합니다.
- 필요한 Microsoft Edge WebView2 Runtime이 없거나 복구가 필요하면 Windows 또는 설치
  프로그램이 Microsoft의 WebView2 배포 서비스에 연결할 수 있습니다.
- 업데이트 확인에 실패해도 파일에 대한 원격 접근 권한이 생기지 않으며 로컬 정리 작업을
  막아서는 안 됩니다.

위 연결은 네트워크를 통한 설치·업데이트 전달 예외이며 파일 내용을 처리하는 서비스가
아닙니다. 중요한 폴더에 베타를 사용하기 전에 [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md)과
[알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)를 확인하세요.

## 업데이트 서명과 Authenticode는 다릅니다

앱 내부 업데이트는 설치 전에 PCSSAK Tauri 서명을 검증하고 각 릴리스는 SHA-256도
공개합니다. 이 장치는 업데이트 경로를 보호하지만 Windows Authenticode 게시자 서명과는
별개입니다. Authenticode를 적용하기 전까지는 설치 파일에 알 수 없는 게시자 또는
SmartScreen 평판 경고가 나타날 수 있습니다.

## 호환성 상태

- **권장 및 공식 검증 예정:** 현재 지원 중인 Windows 11 Home/Pro x64
- **제한적·최선 노력 베타:** Windows 10 22H2 x64 및 32비트 Windows 10 x86. Windows 10은
  PCssak Biuja 공식 검증 대상이 아닙니다.
- **x86 설치기 용도:** 32비트 Windows 10 베타 시험과 Windows x64의 32비트 앱 호환 시험.
  Windows 11 32비트 에디션을 뜻하지 않습니다.
- **미지원:** ARM64 네이티브, Windows S 모드, macOS, Linux

[Microsoft는 Windows 10 일반 지원을 2025년 10월 14일 종료했으며](https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/windows-10-support-has-ended-on-october-14-2025)
Windows 11로 전환할 것을 권장합니다. 조건을 충족한 Windows 10 버전 22H2 소비자 기기는
[소비자 ESU](https://www.microsoft.com/en-us/windows/extended-security-updates)에 등록한
경우에만 Microsoft의 현재 안내 기준 2027년 10월 12일까지 긴급·중요 보안 업데이트를 받을 수
있으며 기능 개선이나 기술 지원은 포함되지 않습니다. 향후 기간 변경은 링크한 Microsoft 공식
페이지에서 다시 확인해야 합니다. 상용 ESU와 LTSC 에디션은 별도 수명주기를 따르며 PCssak
Biuja의 공식 검증 예정 범위에 포함하지 않습니다.

[Microsoft 공식 안내와 같이 Windows 11은 64비트 전용입니다](https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d).
“공식 검증 예정”은 모든 에디션·업데이트·파일시스템·저장소 공급자·기기 조합을 이미 검증했다는
뜻이 아닙니다. 릴리스별 실제 검증 결과는 날짜가 표시된 릴리스 노트에 기록합니다.

## 반드시 알아야 할 안전 한계

- 미리보기와 되돌리기는 위험을 줄이지만 백업이나 버전 관리 시스템이 아닙니다.
- 파일이 삭제·이름 변경·수정·잠김·외부 프로그램에 의해 이동되거나 클라우드에서 동기화됐거나
  대상 위치가 더 이상 안전하지 않으면 되돌릴 수 없을 수 있습니다.
- 보호 폴더, 네트워크 위치, 이동식 드라이브, 클라우드 동기화 폴더, 특수 경로, 부족한 권한,
  다른 프로그램이 사용 중인 파일은 일반 로컬 폴더와 다르게 실패하거나 동작할 수 있습니다.
- 대체할 수 없는 파일은 별도의 검증된 백업을 유지하고, 중요하지 않은 작은 폴더에서 먼저
  시험하세요.
- PCssak Biuja만을 중요한 데이터의 유일한 복구 수단으로 사용하지 마세요.

전체 Early Access 범위는 [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)를 확인하세요.

## 베타 개선에 참여하기

- 재현 가능한 오류는 [버그 제보 양식](../../issues/new?template=bug-report.yml)을 사용하세요.
- 기능 제안은 해결 방법보다 사용자 문제를 먼저
  [기능 제안 양식](../../issues/new?template=feature-request.yml)에 적어주세요.
- 화면·경로·작업저널·로그를 첨부하기 전에 [지원 안내](SUPPORT.md)를 확인하세요.
- 악용 가능한 보안 문제는 [보안 안내](SECURITY.md)에 따라 비공개로 알려주세요.

전체 개인 경로, 파일 이름, 폴더 목록, 고객 자료, 자격증명, 비공개 문서는 공개 이슈에 올리지
마세요. 가장 작은 합성 예제로 바꾸세요.

## 문서

- [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md)
- [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)
- [지원 안내](SUPPORT.md)
- [보안 제보](SECURITY.md)
- [이슈·기여 원칙](CONTRIBUTING.md)
- [개인정보 처리방침](PRIVACY.md)
- [최종 사용자 이용약관](EULA.md)
- [제3자 소프트웨어 라이선스 고지](THIRD-PARTY-NOTICES.txt)
- [MPL 구성요소의 정확한 원본 소스](docs/THIRD-PARTY-SOURCE.md)
- [릴리스 노트](https://github.com/pcssakinc/pcssak-biuja-releases/releases)

PCssak Biuja 바이너리는 독점 소프트웨어이며 릴리스에 포함된 조건에 따라 사용합니다. 제3자
오픈소스 구성요소는 각각의 라이선스와 고지문을 따릅니다. 일반 문의는
`pcssakinc@gmail.com`으로 보내주세요.

앱 UI는 외부 웹 글꼴이나 글꼴 파일을 포함하지 않고 Windows의 언어별 기본 글꼴을 사용합니다.
