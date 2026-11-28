# MPL-2.0 구성요소 원본 소스 / MPL-2.0 Component Source

이 안내의 대상은 PCssak Biuja 0.5.0입니다. Windows 패키지는 아래 MPL-2.0 구성요소의 정확한
버전 upstream 원본 소스를 함께 담습니다. 이 안내는 비우자 자체의 라이선스를 바꾸거나 전체 앱
소스 공개를 약속하지 않습니다.

패키지 루트의 안내는 `THIRD-PARTY-SOURCE.md`, 고지는 `THIRD-PARTY-NOTICES.txt`, 장부는
`mpl-source/ledger.json`, 원본은 `mpl-source/archives/<name>-<version>.crate`입니다.
장부에서 제품 버전, Cargo.lock의 SHA-256, 각 원본의 크기·체크섬·출처를 확인할 수 있습니다.

| 구성요소 | 버전 | 원본 소스 |
| --- | ---: | --- |
| cssparser | 0.36.0 | [upstream 원본](https://static.crates.io/crates/cssparser/cssparser-0.36.0.crate) |
| cssparser-macros | 0.6.1 | [upstream 원본](https://static.crates.io/crates/cssparser-macros/cssparser-macros-0.6.1.crate) |
| dtoa-short | 0.3.5 | [upstream 원본](https://static.crates.io/crates/dtoa-short/dtoa-short-0.3.5.crate) |
| option-ext | 0.2.0 | [upstream 원본](https://static.crates.io/crates/option-ext/option-ext-0.2.0.crate) |
| selectors | 0.36.1 | [upstream 원본](https://static.crates.io/crates/selectors/selectors-0.36.1.crate) |

전체 제3자 구성요소, 저작권 및 라이선스 전문은 패키지의 `THIRD-PARTY-NOTICES.txt` 또는
[Windows 0.5.0용 공개 고지](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/windows-v0.5.0/THIRD-PARTY-NOTICES.txt)에서 확인하세요. 설치된 앱의 패키지 파일 또는 제공받은 읽을 수 있는
패키지 사본에서 동봉 자료를 찾으세요. 보호된 Windows 설치 폴더에 접근하려고 소유권이나
권한을 바꾸지 마세요. 접근할 수 없으면 위 upstream 링크를 사용하거나
`pcssak@pcssak.com`으로 제품 버전과 구성요소 이름을 알려 소스 사본을 요청할 수 있습니다.

`.crate`는 gzip으로 압축한 tar 파일입니다. 원문을 읽으려면 원하는 빈 폴더에 사본을 복사하고
사본 확장자를 `.tar.gz`로 바꾼 뒤 호환 보관 유틸리티로 그 폴더에 푸세요. 이름 변경은 내용을
바꾸지 않습니다. Windows 기본 도구의 tar.gz 지원은 OS 버전에 따라 다릅니다. 앱 설치 폴더에
풀거나 리소스를 교체하지 마세요. 소스를 읽으려고 빌드·설치·실행할 필요는 없습니다.

covered source는 MPL-2.0에 따라 제공되며 앱 자체 약관이 해당 권리를 제한하지 않습니다.
원본의 소스 헤더·고지·제공된 라이선스 파일을 읽으세요. 모든 원본에 별도 LICENSE 파일이 있는
것은 아니며 제3자 고지에도 MPL-2.0 전문이 있습니다. 이 출시본은 위 구성요소를 수정하지 않고
그대로 사용합니다. [Mozilla 공식 FAQ Q8·Q10](https://www.mozilla.org/en-US/MPL/2.0/FAQ/)를 참고하세요.

---

This guide applies to PCssak Biuja 0.5.0. The Windows package includes the exact upstream source
archives of the MPL-2.0 components listed below. This does not change Biuja's own license or
promise publication of all app source.

Relative to the package root, find `THIRD-PARTY-SOURCE.md`, `THIRD-PARTY-NOTICES.txt`,
`mpl-source/ledger.json` and `mpl-source/archives/<name>-<version>.crate` in readable app package
files or a supplied package copy. The ledger records the product version,
Cargo.lock SHA-256, archive sizes, exact checksums and source URLs.

| Component | Version | Upstream source |
| --- | ---: | --- |
| cssparser | 0.36.0 | [upstream archive](https://static.crates.io/crates/cssparser/cssparser-0.36.0.crate) |
| cssparser-macros | 0.6.1 | [upstream archive](https://static.crates.io/crates/cssparser-macros/cssparser-macros-0.6.1.crate) |
| dtoa-short | 0.3.5 | [upstream archive](https://static.crates.io/crates/dtoa-short/dtoa-short-0.3.5.crate) |
| option-ext | 0.2.0 | [upstream archive](https://static.crates.io/crates/option-ext/option-ext-0.2.0.crate) |
| selectors | 0.36.1 | [upstream archive](https://static.crates.io/crates/selectors/selectors-0.36.1.crate) |

For the component inventory, copyright notices and license texts, read `THIRD-PARTY-NOTICES.txt` in the
package or the [Windows 0.5.0 notices](https://github.com/pcssakinc/pcssak-biuja-releases/blob/main/windows-v0.5.0/THIRD-PARTY-NOTICES.txt).
Do not change ownership or permissions of protected Windows installation directories. If the
packaged materials are inaccessible, use the exact upstream links above or request a source
copy by emailing `pcssak@pcssak.com` with the product version and component name.

A `.crate` is a gzip-compressed tar archive. Copy it into an empty folder you choose, rename only
that copy to `.tar.gz`, then expand it there with a compatible archive utility. Renaming does not
change its bytes. Built-in tar.gz support depends on the Windows version. Do not extract into
the app installation or replace app resources. Reading source does not require building,
installing or running it.

Covered source remains available under MPL-2.0; proprietary app terms do not restrict those
rights. Read source headers, notices and license files provided upstream. Not every archive has
a separate LICENSE file; the notice also includes full MPL-2.0 text. This release uses the
components listed above without modifying them. See
[Mozilla's official FAQ Q8 and Q10](https://www.mozilla.org/en-US/MPL/2.0/FAQ/).
