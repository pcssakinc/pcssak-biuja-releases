# Known Limitations

[한국어](KNOWN-LIMITATIONS.ko.md)

## Current release

- The public GitHub build is Free Early Access below version 1.0.
- Features, layouts, translations, sorting rules, journal formats, and supported locations may
  change before a stable release.
- Undiscovered defects, classification mistakes, performance problems, and compatibility issues
  may remain.
- Support is provided by a solo developer and has no guaranteed response, repair, or release
  deadline.
- PCssak Biuja is an organizer. It is not backup software, version control, a secure eraser,
  antivirus software, storage repair, or a guaranteed data-recovery service.

## Windows compatibility

- Currently serviced Windows 11 Home/Pro x64 is the recommended environment and planned formal
  validation target. That validation is not complete merely because an installer can be built
  or started.
- Windows 11 is 64-bit only and has no 32-bit edition, as confirmed by
  [Microsoft's Windows architecture FAQ](https://support.microsoft.com/en-us/windows/32-bit-and-64-bit-windows-frequently-asked-questions-c6ca9541-8dce-4d48-0415-94a3faa2e13d).
- The x86 installer has two beta purposes: running on 32-bit Windows 10 and testing 32-bit
  application compatibility on x64 Windows. It is not a Windows 11 32-bit operating-system
  build and has a narrower test base than x64.
- Windows 10 22H2 x64/x86 receives only limited, best-effort beta compatibility from PCSSAK and
  is not a formal validation target. Upgrade to Windows 11 when the device is eligible.
- Native ARM64, Windows S mode, macOS, and Linux are unsupported.
- A Windows-on-ARM device running an x64 application through emulation is not the same as native
  ARM64 support and is not currently an official validation target.
- Required WebView2 Runtime, Windows updates, security policy, filesystem, storage driver, and
  endpoint protection can affect startup and file operations.

[Microsoft ended general Windows 10 support on October 14, 2025](https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/windows-10-support-has-ended-on-october-14-2025).
Eligible consumer devices on Windows 10 version 22H2 receive critical and important security
updates only when enrolled in
[Consumer ESU](https://www.microsoft.com/en-us/windows/extended-security-updates), and that
consumer program runs through October 12, 2027 under Microsoft's current guidance. It provides
neither feature improvements nor technical support. Check the linked Microsoft page for future
lifecycle changes. Commercial ESU years and LTSC editions have separate Microsoft lifecycles;
they do not expand PCssak Biuja's planned formal-validation scope.

Release notes should state the combinations actually tested for that version. No release note
can represent every Windows update, device, drive, filesystem, cloud provider, and security
product combination. PCSSAK application support cannot restore operating-system security or
vendor technical support that Windows 10 no longer receives.

## Installer and updates

- The initial installer is not Windows Authenticode-signed and can show Unknown publisher or
  Microsoft Defender SmartScreen. Use only official PCSSAK sources and verify
  `SHA256SUMS.txt`.
- Do not disable SmartScreen, Microsoft Defender, or another security product to install the
  application.
- The in-app updater verifies a PCSSAK Tauri signature. This is separate from Authenticode and
  does not remove first-install reputation warnings.
- Automatic update checking and download require access to the official GitHub release service.
  Offline sorting does not require that connection.
- If WebView2 Runtime is missing or needs repair, Windows or the installer may need to connect
  to Microsoft's WebView2 distribution service.

## Sorting decisions and preview

- PCssak Biuja can only apply the supported rules and metadata visible to the application. It
  cannot know a user's personal meaning, contractual filing requirement, retention policy, or
  preferred project structure.
- A preview is a plan at a point in time. Another program, synchronization client, user action,
  or filesystem event can change files after preview and before execution.
- Review every preview. Start with a small, non-critical folder and correct rules that do not
  match the intended organization.
- A successful preview does not guarantee every operation will later succeed. Permissions,
  locks, available space, disconnected storage, path restrictions, or a newly created
  destination can cause a safe refusal or partial completion.

## No-overwrite and no-permanent-delete boundary

- PCssak Biuja is designed not to intentionally overwrite an existing destination and not to
  permanently delete user files.
- These controls apply to operations performed by PCssak Biuja. They cannot prevent another
  application, a cloud sync provider, a manual user action, hardware failure, malware, or an
  operating-system problem from changing or deleting files.
- A refused collision, permission failure, or changed destination is a safety outcome and may
  require manual review.
- The application is not intended to bypass Windows access controls or to organize protected
  operating-system and application directories.

## Work journal and rollback

- The work journal records supported completed operations locally. It is not a copy of the file
  and is not a backup.
- Rollback is limited to journaled operations that can still be reversed safely without
  overwriting another file.
- Rollback may be unavailable or refused when the current file no longer matches the recorded
  state, the source or destination has changed, a path is occupied, a drive is missing, a file
  is locked, permissions changed, or an external program moved or deleted the file.
- Rollback of a supported Recycle Bin action requires the corresponding item to remain available
  in the Windows Recycle Bin. PCssak Biuja cannot restore an item after the Recycle Bin, Windows,
  a cleanup utility, or the user has removed it.
- A multi-file plan can stop after some operations have completed. Review the journal and the
  reported result instead of assuming all-or-nothing filesystem behavior.
- Keep a separate, tested backup for irreplaceable data even when rollback is available.

## Locations and filesystem behavior

- Protected system folders, application installation folders, another user's profile, network
  shares, removable media, cloud-synchronized folders, encrypted locations, links, junctions,
  reparse points, unusual long paths, and files open in another application require special
  caution and may be unsupported or refused.
- Moving a file inside a cloud-synchronized folder can be propagated by that provider to other
  devices. PCssak Biuja does not control or reverse the provider's independent history.
- Network and removable storage can disconnect between preview, execution, and rollback.
- Filesystem timestamps, permissions, alternate data, or application-specific references can
  have consequences outside the visible filename. Test the relevant workflow before using it
  on production material.

## Privacy and connectivity

- File organization is processed 100% locally: file names, paths, previews, sorting decisions,
  work journals, and rollback processing remain on the device. User files and their contents
  are not uploaded to PCSSAK for sorting.
- The public Early Access build has no PCSSAK account, advertising, analytics, tracking, cloud
  file index, or automatic crash upload.
- Network exceptions are the official GitHub signed-update check/download and Microsoft
  WebView2 installation or repair when required.
- Public bug reports are not local. Never paste real full paths, directory listings, journals,
  file contents, customer data, or secrets into GitHub Issues.

## Repository and license

- This public repository distributes proprietary binaries and documentation and accepts user
  reports. It is not an open-source release of the private application source.
- Third-party components remain under their own licenses and notices.
- Free Early Access availability does not imply that future editions, features, prices, or
  distribution channels have been announced or guaranteed.
