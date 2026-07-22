# PCssak Biuja - Official Windows Downloads

[한국어](README.ko.md) · [Product website](https://pcssak.com/biuja) ·
[Latest release](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest)

**Review first, organize safely, and keep control of your files.** PCssak Biuja prepares a
sorting preview for files in a user-selected scope, records completed work, and supports
rollback without intentionally overwriting or permanently deleting the originals.

> **Repository scope:** This is the official public binary distribution, documentation, and
> issue-tracking repository for PCssak Biuja. The application source is private and
> proprietary. A public repository does not make the application open source, and this
> repository does not contain the product source code.

## Download

Download only from the
[latest official release](https://github.com/pcssakinc/pcssak-biuja-releases/releases/latest)
or the [PCssak Biuja product page](https://pcssak.com/biuja).

- Choose **x64** for normal use on Windows 11 Home/Pro. Windows 11 x64 is the recommended and
  planned official-validation target.
- Windows 10 x64 is limited, best-effort beta compatibility because Microsoft ended general
  Windows 10 support on October 14, 2025. Upgrading to Windows 11 is recommended.
- Use **x86** only for beta testing on 32-bit Windows 10 or for testing 32-bit-application
  compatibility on x64 Windows. Windows 11 has no 32-bit edition; an x86 PCssak Biuja process
  on Windows 11 still runs on a 64-bit operating system.
- Native ARM64, Windows S mode, macOS, and Linux are not supported.
- Compare the installer filename and SHA-256 with `SHA256SUMS.txt` in the same release before
  running it.

In PowerShell, a downloaded installer can be checked with:

```powershell
Get-FileHash -Algorithm SHA256 '.\DOWNLOADED-INSTALLER.exe'
```

Replace the example with the exact filename from the release. The value must match the
corresponding entry in `SHA256SUMS.txt`.

> [!WARNING]
> The initial Windows installer is not yet Authenticode-signed. Windows may show **Unknown
> publisher** or a **Microsoft Defender SmartScreen** warning. Download only from the official
> locations above and verify the SHA-256. Do not disable SmartScreen, Microsoft Defender, or
> another security product to install PCssak Biuja. If the source, filename, or hash cannot be
> confirmed, do not run the file.

## Current Free Early Access features

1. Inspect files within a scope selected by the user and automatically prepare an organization
   plan from the supported rules.
2. Preview intended sorting actions before files are changed.
3. Apply supported moves and copies. Supported cleanup actions use the Windows Recycle Bin
   instead of permanent deletion, and existing destinations are not intentionally overwritten.
4. Record completed actions in a local work journal.
5. Roll back supported journaled actions when the recorded source, destination, and current
   filesystem state still allow a safe reversal.
6. Avoid permanent deletion. PCssak Biuja is an organizer, not a secure eraser, backup, or
   guaranteed recovery tool.

The current public build is **Free Early Access** below version 1.0. Features, translations,
and file-handling rules may change before a stable release, and undiscovered defects may remain.

## Local processing and network exceptions

- File organization itself is processed **100% locally**: file names, paths, sorting decisions,
  previews, work journals, and rollback processing stay on the device. PCSSAK does not upload
  user files or their contents for sorting.
- There is no PCSSAK account, advertising, analytics, tracking, cloud file index, or automatic
  crash upload in the public Early Access build.
- A standalone build may connect to the official `pcssakinc` GitHub release to check for and
  download an update package signed with the PCSSAK Tauri updater key.
- If the required Microsoft Edge WebView2 Runtime is missing or must be repaired, Windows or
  the installer may connect to Microsoft's WebView2 distribution service.
- Failure of an update check does not grant remote access to files and should not block the
  local sorting workflow.

These are network-delivery exceptions, not file-content processing services. Read
[Quality and safety](docs/QUALITY-AND-SAFETY.md) and
[Known limitations](docs/KNOWN-LIMITATIONS.md) before using the beta on important folders.

## Update integrity is not Authenticode

The in-app updater verifies a PCSSAK Tauri signature before installing an update, and each
release publishes SHA-256 values. This protects the update channel, but it is separate from a
Windows Authenticode publisher signature. Until Authenticode signing is added, the installer
can still show Unknown publisher or SmartScreen reputation warnings.

## Compatibility status

- **Recommended and planned official-validation target:** currently serviced Windows 11
  Home/Pro x64.
- **Limited, best-effort beta:** Windows 10 22H2 x64 and 32-bit Windows 10 x86. Windows 10 is
  not an official-validation target for PCssak Biuja.
- **x86 installer purpose:** beta testing on 32-bit Windows 10 and testing 32-bit-application
  compatibility on x64 Windows. It does not mean that a 32-bit Windows 11 edition exists.
- **Unsupported:** native ARM64, Windows S mode, macOS, and Linux.

[Microsoft ended general Windows 10 support on October 14, 2025](https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/windows-10-support-has-ended-on-october-14-2025)
and recommends moving to Windows 11. For eligible Windows 10 version 22H2 consumer devices,
[Consumer ESU](https://www.microsoft.com/en-us/windows/extended-security-updates) supplies
critical and important security updates through October 12, 2027, according to Microsoft's
current guidance, but not feature improvements or technical support. Check the linked Microsoft
page for future lifecycle changes. Commercial ESU and LTSC editions have separate lifecycles and
are outside the planned PCssak Biuja validation scope.

[Microsoft confirms that Windows 11 is 64-bit only](https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d).
“Planned official validation” is not a claim that every edition, update, filesystem, storage
provider, or device combination has already been verified. Release-specific test results belong
in the dated release notes.

## Important safety limits

- Preview and rollback reduce risk but are not a backup or version-control system.
- Rollback can be unavailable if a file was deleted, renamed, edited, locked, moved by another
  program, synchronized by a cloud provider, or if the destination is no longer safe.
- Protected folders, network locations, removable drives, cloud-synchronized folders, unusual
  paths, insufficient permissions, and files used by another program can fail or behave
  differently from ordinary local folders.
- Keep a separate tested backup of irreplaceable files and begin with a small, non-critical
  folder.
- Do not use PCssak Biuja as the only recovery plan for important data.

See [Known limitations](docs/KNOWN-LIMITATIONS.md) for the complete Early Access boundary.

## Help improve the beta

- Use the [bug report form](../../issues/new?template=bug-report.yml) for a reproducible defect.
- Use the [feature request form](../../issues/new?template=feature-request.yml) to describe the
  user problem before proposing a solution.
- Read [Support](SUPPORT.md) before attaching screenshots, paths, journals, or logs.
- Report exploitable security details privately under [Security](SECURITY.md).

Never post full personal paths, file names, directory listings, customer data, credentials, or
confidential documents in a public issue. Replace them with the smallest synthetic example.

## Documentation

- [Quality and safety](docs/QUALITY-AND-SAFETY.md)
- [Known limitations](docs/KNOWN-LIMITATIONS.md)
- [Support](SUPPORT.md)
- [Security reporting](SECURITY.md)
- [Issue and contribution guidelines](CONTRIBUTING.md)
- [Privacy Policy](PRIVACY.md)
- [End User License Agreement](EULA.md)
- [Release notes](https://github.com/pcssakinc/pcssak-biuja-releases/releases)

PCssak Biuja binaries are proprietary software and are licensed under the terms included with
the release. Third-party open-source components remain under their own licenses and notices.
For general inquiries, contact `pcssakinc@gmail.com`.
