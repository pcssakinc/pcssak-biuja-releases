# Quality and Safety

[한국어](QUALITY-AND-SAFETY.ko.md)

This document explains the PCssak Biuja safety model and the checks expected before a public
release. It is evidence of engineering intent and process, not a promise that the application
has no defects or that rollback can recover every external filesystem change.

## File-operation safety model

PCssak Biuja is built around a reviewable sequence:

1. The user selects the intended scope.
2. The application inspects supported entries and prepares a sorting plan.
3. The user reviews a preview before applying changes.
4. The native file-operation boundary rechecks conditions needed for each supported action.
5. An existing destination is not intentionally overwritten, and user files are not
   permanently deleted.
6. Completed supported actions are recorded in a local work journal.
7. Rollback uses the journal only when the current filesystem state permits a safe reverse
   operation without overwriting another file.

A refusal is preferable to guessing when the path, identity, permission, destination, or
current state is no longer safe. This model reduces risk but does not turn a sequence of
filesystem operations into an atomic transaction or a backup.

## Preview is a decision checkpoint

The preview is intended to show what PCssak Biuja plans to move before mutation. Users should
review category, source, and destination information and begin with a small, non-critical
folder. A plan can become stale when another application, synchronization service, or user
changes the filesystem after the preview.

Execution must therefore treat the preview as a proposal, not unconditional authority. A
changed source, newly occupied destination, missing drive, insufficient permission, or locked
file should produce a safe failure or refusal rather than an overwrite.

## No overwrite and no permanent deletion

- PCssak Biuja does not intentionally replace an existing destination file.
- It does not perform permanent deletion as part of its sorting workflow; supported cleanup
  actions use the Windows Recycle Bin.
- A naming or destination collision is surfaced for review or safely refused.
- These protections govern operations performed by PCssak Biuja; they cannot control a cloud
  provider, another application, malware, hardware failure, or a manual user action.

The application is not a secure deletion product, and “no permanent deletion” must not be
interpreted as a guarantee that data cannot be lost through causes outside the application.

## Work journal and rollback

The local work journal records the supported actions that were completed. Rollback is based on
those records and must not overwrite a currently existing path merely to recreate an earlier
layout.

Rollback is best-effort and condition-dependent. It can be refused when the recorded item was
changed, replaced, removed, renamed, locked, synchronized elsewhere, or placed on unavailable
storage. A Recycle Bin action can be restored only while Windows still retains the corresponding
item. The journal is metadata about work, not a second copy of the file. Users still need a
separate tested backup for irreplaceable data.

## Local-first privacy boundary

- File names, paths, sorting decisions, preview generation, work-journal data, and rollback
  processing remain on the device.
- PCSSAK does not receive user files or file contents to provide sorting.
- The public Free Early Access build has no PCSSAK account, advertising, analytics, tracking,
  cloud file index, or automatic crash upload.
- Public issue reports are outside this boundary. Users must remove personal paths, filenames,
  directory listings, customer data, secrets, and document contents before posting.

## Narrow network exceptions

The local-processing statement has two delivery exceptions:

- A standalone build can contact the official `pcssakinc` GitHub release to check for and
  download an update signed with the PCSSAK Tauri updater key.
- When the required Microsoft Edge WebView2 Runtime is absent or requires repair, Windows or
  the installer may contact Microsoft's WebView2 distribution service.

Neither exception is a PCSSAK service for uploading or analyzing file contents. Core file
sorting should remain usable when the GitHub update check is unavailable.

## Update and release integrity

The release process is designed to require:

- consistent application versions across JavaScript, Tauri, Rust, and updater metadata;
- dependency lockfiles and review of bundled third-party licenses and notices;
- architecture-specific x64 and x86 build artifacts where that release claims support;
- PCSSAK Tauri signatures for update artifacts;
- `latest.json`, detached signature files, and `SHA256SUMS.txt` generated from the final files;
- comparison of published file sizes and hashes with the locally approved artifacts;
- an explicit release approval step rather than an accidental upload of a development build;
- rejection of tracked private keys, signing passwords, tokens, or unrelated internal files.

The updater signature protects the in-app update path. It does **not** make the installer
Authenticode-signed. The initial installer remains unsigned at the Windows publisher level and
can show Unknown publisher or SmartScreen. Users must verify SHA-256 and must not disable
Windows security controls.

## Verification layers

A public build should be released only after the results for that exact version are recorded
and reviewed. The relevant layers include:

- sorting-plan, collision, journal, rollback, and stale-state regression tests;
- TypeScript type checking and production frontend build;
- Rust tests, formatting, linting, and native file-boundary checks;
- localization completeness and placeholder consistency across supported languages;
- clean x64 build and installed-application smoke testing on the documented Windows 11
  Home/Pro x64 target;
- separate Windows 10 best-effort beta checks where a release claims them;
- x86 build and beta smoke testing on 32-bit Windows 10 and x64 Windows compatibility mode
  before an x86 artifact is offered;
- installer, update-manifest, signature, checksum, upgrade, and rollback-path checks;
- tests involving locked files, permissions, occupied destinations, external changes, cloud or
  removable storage warnings, and interrupted multi-file work where supported.

Exact test counts and performance results belong in dated release records. They are not
advertised here as permanent facts, and a successful automated test does not replace a real
installed-app check.

## Compatibility claims

Currently serviced Windows 11 Home/Pro x64 is the recommended and planned official-validation
target. Windows 11 is 64-bit only and has no 32-bit edition. The x86 installer is a narrower
beta artifact for 32-bit Windows 10 and for testing 32-bit-application compatibility on x64
Windows; it is not a Windows 11 32-bit build.

Windows 10 22H2 x64/x86 receives limited, best-effort beta compatibility only. Microsoft ended
[general Windows 10 support on October 14, 2025](https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/windows-10-support-has-ended-on-october-14-2025)
and recommends upgrading to Windows 11. Eligible Windows 10 version 22H2 consumer devices
receive critical and important security updates through October 12, 2027 under Microsoft's
current guidance only when enrolled in
[Consumer ESU](https://www.microsoft.com/en-us/windows/extended-security-updates); feature
improvements and technical support are not included. Check the linked Microsoft page for future
lifecycle changes. Commercial ESU and LTSC lifecycles remain separate and outside the planned
PCssak Biuja validation scope.

Native ARM64, Windows S mode, macOS, and Linux are unsupported. Microsoft also confirms in its
[Windows architecture FAQ](https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d)
that Windows 11 is 64-bit only.

Until a release note records a completed validation result, “planned” must not be presented as
“verified.” Even after validation, support describes tested configurations, not every possible
device, filesystem, driver, policy, or third-party program.

## What users should still do

- Download only from the official PCSSAK product page or `pcssakinc` release repository.
- Verify the installer filename and SHA-256 against `SHA256SUMS.txt`.
- Do not disable SmartScreen, Microsoft Defender, or another security product.
- Keep a separate tested backup of irreplaceable data.
- Begin with a small, non-critical local folder and review every preview.
- Check the work journal after partial success, refusal, interruption, or rollback.
- Report reproducible defects and send exploitable security details through the documented
  private route.

See [Known limitations](KNOWN-LIMITATIONS.md), [Security](../SECURITY.md), and
[Support](../SUPPORT.md).
