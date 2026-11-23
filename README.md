# Blaze

I work on binary-analysis and reverse-engineering tools, with a focus on malformed-input handling in parsers, protocol code, and file-format loaders. I find the bug, build a minimal reproducer, fix it upstream, and document the root cause.

## Selected upstream fixes

| Project | Change | Status |
| --- | --- | --- |
| Ghidra | ISF connection handler exits on client EOF instead of spinning at 100% CPU | [Merged #10185](https://github.com/NationalSecurityAgency/ghidra/pull/10185) |
| Ghidra | Version Tracking preserves backslashes in persisted comments | [Merged #10191](https://github.com/NationalSecurityAgency/ghidra/pull/10191) |
| Ghidra | Swift metadata parsing skips unknown descriptor kinds instead of aborting | [Merged #10167](https://github.com/NationalSecurityAgency/ghidra/pull/10167) |
| radare2 | `psa` string detection stays in bounds on short and odd-sized blocks | [Merged #27376](https://github.com/radareorg/radare2/pull/27376) |
| lzfse | 64-bit FSE input flush avoids a one-byte over-read at end of input | [Open PR #66](https://github.com/lzfse/lzfse/pull/66) |

Ghidra commit history: [commits authored by blaze0089](https://github.com/NationalSecurityAgency/ghidra/commits/master?author=blaze0089)

## Research index

Writeups with root cause, reproducer, impact, and fix:

- [Ghidra ISF: a disconnect that pins a CPU core](https://github.com/blaze0089/security-research/blob/main/ghidra/isf-eof-busy-loop.md)
- [Ghidra Version Tracking: the backslash that disappeared](https://github.com/blaze0089/security-research/blob/main/ghidra/version-tracking-backslash.md)
- [Ghidra Swift: a null descriptor kind](https://github.com/blaze0089/security-research/blob/main/ghidra/swift-null-descriptor.md)
- [radare2: out-of-bounds reads in psa string detection](https://github.com/blaze0089/security-research/blob/main/radare2/psa-oob-read.md)
- [lzfse: one byte past the FSE payload](https://github.com/blaze0089/security-research/blob/main/lzfse/fse-flush64-oob.md)

Repository: [blaze0089/security-research](https://github.com/blaze0089/security-research)

Most of the forks in this account are working branches for upstream pull requests. The findings and patch notes are collected in `security-research`.

## Focus

- Binary format parsers and protocol handlers
- Memory-safety review with AddressSanitizer and custom in-process fuzzers
- Minimal upstream patches with regression tests
- Coordinated disclosure before publishing security-impacting details

## Tooling

Ghidra, radare2, AddressSanitizer, CMake, Gradle, C, C++, Java, Python.

Cybersecurity undergraduate. Open to research collaborations and security internships.

## Contact

GitHub: [@blaze0089](https://github.com/blaze0089)

For corrections or collaboration, open an issue in [security-research](https://github.com/blaze0089/security-research/issues).

Security-impacting issues are reported privately to maintainers first. Technical details are published after a fix or advisory is available.
