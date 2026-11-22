# Pwn (binary exploitation) challenge tags on CTFtime writeups, 2020–2025

**1,006 different pwn challenges** are among the 6,859 challenges with tagged writeups from CTFs held in 2020–2025, each counted once: 14.7% of them. 858 carry the `pwn` tag, 135 more were found through other pwn keywords (bof, rop, format-string, heap, shellcode, ...), and 13 were added in a hand review: their tags are too weak to count, but their CTFtime task page or name shows a purely pwn challenge. Companion to [web-tags-summary.md](web-tags-summary.md), with the same data and method.

## Data

- **Source:** every writeup listed on [ctftime.org/writeups](https://ctftime.org/writeups) (all 1,309 pages, 39,253 writeups), collected on 30 Oct 2026, 13:31–13:45 UTC; event dates from CTFtime's [events API](https://ctftime.org/api/).
- **File:** [`ctftime_writeups_tasks.xlsx`](ctftime_writeups_tasks.xlsx), one tab (`Tasks`) with the columns Event, Task, Tags and Event start date: 19,494 challenges, all years. Writeups of the same task are merged and their tags combined, so a task solved by several teams counts once.
- **Scope:** challenges whose event started in 2020–2025 (UTC) and whose writeups have at least one tag: 6,859 of the 11,032 challenges from those years. The 4,173 challenges whose writeups have no tags are left out.

## Pwn challenges per year

| Year | Challenges with tags | Tagged `pwn` | Other pwn keywords only | Added by hand | **Pwn challenges** | Share |
| --- | --- | --- | --- | --- | --- | --- |
| 2020 | 2,170 | 265 | 45 | 4 | **314** | 14.5% |
| 2021 | 1,825 | 256 | 46 | 5 | **307** | 16.8% |
| 2022 | 1,025 | 161 | 27 | 2 | **190** | 18.5% |
| 2023 | 1,028 | 109 | 7 | 0 | **116** | 11.3% |
| 2024 | 525 | 42 | 10 | 2 | **54** | 10.3% |
| 2025 | 286 | 25 | 0 | 0 | **25** | 8.7% |
| **Total** | **6,859** | **858** | **135** | **13** | **1,006** | **14.7%** |

- **Counted once:** a challenge tagged `pwn` and also, say, `bof` and `rop` is one challenge. Counting every keyword hit separately would give 1,988 instead of the 993 found through tags.
- **Added by hand:** a hand review of the 92 challenges whose tags have only broad pwn words (`binary`, `kernel`, `seccomp`, `pwntools`, ...) or whose task name has a pwn word kept the 13 that are purely pwn going by their CTFtime task page or name, such as Codegate CTF 2020 Preliminary's babyllvm (`jit`, task page tagged `pwnable`), UIUCTF 2024's Syscalls (`seccomp`, task page tagged `pwn`) or picoCTF 2022's buffer overflow 0 (`binary`). They are listed in Appendix C.

### Is there a dominant tag?

Yes: **`pwn`**, on 858 of the 993 pwn challenges found through tags (86.4%), even more dominant than `web` was for web challenges (81.9%).

- **Other spellings:** 22 more challenges have no `pwn` tag but one of its other spellings: `binaryexploitation`, `pwnable`, `binary-exploitation`, `binexploit`, `clone-and-pwn`, `binary-exploitaion`, `babypwn`, `auto_pwn`, `binaryexploit`, `pwnables`, `kernel#pwn`, `babypwn2`, `binex` (included in "Other pwn keywords only").
- **`bof`** (109 challenges, 103 also tagged `pwn`), **`rop`** (129, 111) and **`bufferoverflow`** (43, 34) are the main technique tags; they count on their own.
- **`binary` is not a pwn tag:** only 6 of its 27 challenges are also tagged `pwn`; the rest are mostly reversing, binary-number encodings or stego. It only counts inside challenges already identified as pwn. Two more, picoCTF 2022's buffer overflow 0 and ALLES! CTF 2021's ccanary, are pwn going by their names and task pages and were added by hand. The same goes for `exploit`, `exploitation` (also used for web and system exploitation) and `pwntools` (also used to script crypto and misc challenges).

## By technique

Each row counts a challenge once, even with several spellings (`bof` and `bufferoverflow`, say). A challenge can be in several rows. Techniques come from tags only. 658 of the 1,006 pwn challenges name at least one technique; the other 348 are tagged only `pwn` (or a spelling of it) or with broad words.

| Technique | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| ROP / ret2* (ret2libc, SROP, ret2dlresolve, stack pivot) | 57 | 75 | 40 | 15 | 6 | 1 | 194 |
| Stack buffer overflow | 71 | 57 | 33 | 13 | 10 | 3 | 187 |
| Heap exploitation (tcache, UAF, double free, house of ...) | 38 | 46 | 23 | 9 | 3 | 7 | 126 |
| Format string | 42 | 31 | 14 | 8 | 5 | 1 | 101 |
| Shellcode (incl. seccomp / ORW) | 27 | 22 | 20 | 5 | 4 | 0 | 78 |
| Kernel exploitation | 6 | 10 | 11 | 2 | 6 | 7 | 42 |
| GOT overwrite / arbitrary write | 3 | 18 | 8 | 5 | 2 | 1 | 37 |
| Mitigation bypass (canary, ASLR, PIE, NX, CET) | 10 | 9 | 11 | 3 | 2 | 0 | 35 |
| Sandbox / VM / hypervisor escape | 6 | 9 | 5 | 4 | 3 | 1 | 28 |
| FILE / exit-handler hijacking (FSOP, vtables, fini_array) | 9 | 7 | 6 | 2 | 2 | 1 | 27 |
| Browser / JS engine exploitation | 6 | 6 | 3 | 2 | 2 | 2 | 21 |
| Integer bugs / out-of-bounds | 3 | 8 | 4 | 2 | 1 | 0 | 18 |
| **Name at least one technique** | **216** | **200** | **127** | **61** | **34** | **20** | **658** |

Share of the pwn challenges that name a technique:

| Technique | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
| --- | --- | --- | --- | --- | --- | --- |
| ROP / ret2* (ret2libc, SROP, ret2dlresolve, stack pivot) | 26.4% | 37.5% | 31.5% | 24.6% | 17.6% | 5.0% |
| Stack buffer overflow | 32.9% | 28.5% | 26.0% | 21.3% | 29.4% | 15.0% |
| Heap exploitation (tcache, UAF, double free, house of ...) | 17.6% | 23.0% | 18.1% | 14.8% | 8.8% | 35.0% |
| Format string | 19.4% | 15.5% | 11.0% | 13.1% | 14.7% | 5.0% |
| Shellcode (incl. seccomp / ORW) | 12.5% | 11.0% | 15.7% | 8.2% | 11.8% | 0.0% |
| Kernel exploitation | 2.8% | 5.0% | 8.7% | 3.3% | 17.6% | 35.0% |

## Most used keywords in pwn challenges

Individual pwn keywords, excluding `pwn`. A challenge tagged both `bof` and `bufferoverflow` is in both rows here but counted once in the Stack buffer overflow row above.

| Keyword | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `rop` | 42 | 45 | 26 | 10 | 4 | 0 | 127 |
| `bof` | 51 | 43 | 10 | 2 | 0 | 3 | 109 |
| `heap` | 25 | 30 | 21 | 6 | 0 | 6 | 88 |
| `format-string` | 32 | 29 | 14 | 5 | 1 | 0 | 81 |
| `shellcode` | 24 | 14 | 16 | 3 | 0 | 0 | 57 |
| `bufferoverflow` | 21 | 8 | 6 | 5 | 3 | 0 | 43 |
| `pwntools` | 18 | 16 | 5 | 4 | 0 | 0 | 43 |
| `ret2libc` | 14 | 14 | 7 | 4 | 1 | 0 | 40 |
| `kernel` | 6 | 8 | 7 | 2 | 6 | 5 | 34 |
| `ret2win` | 3 | 8 | 13 | 3 | 5 | 0 | 32 |
| `binaryexploitation` | 14 | 1 | 6 | 2 | 0 | 0 | 23 |
| `pwnscripts` | 14 | 9 | 0 | 0 | 0 | 0 | 23 |
| `ropchain` | 6 | 13 | 1 | 0 | 1 | 1 | 22 |
| `uaf` | 8 | 8 | 1 | 2 | 2 | 0 | 21 |
| `seccomp` | 5 | 6 | 7 | 1 | 2 | 0 | 21 |
| `canary` | 5 | 6 | 7 | 2 | 1 | 0 | 21 |
| `tcache` | 7 | 7 | 1 | 1 | 1 | 2 | 19 |

## Architecture and language

Only inside pwn challenges. Architecture tags are rare: most writeups don't say which CPU the binary runs on.

| Tag group | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| x86 / x86-64 | 2 | 5 | 4 | 2 | 1 | 0 | 14 |
| ARM / AArch64 | 1 | 6 | 5 | 0 | 0 | 2 | 14 |
| RISC-V | 2 | 2 | 2 | 1 | 0 | 0 | 7 |
| MIPS | 2 | 0 | 0 | 0 | 1 | 0 | 3 |
| Other CPUs (SPARC, 6502, PowerPC, AVR, s390 ...) | 4 | 0 | 1 | 3 | 0 | 0 | 8 |
| Windows | 2 | 0 | 0 | 1 | 0 | 1 | 4 |
| Rust | 3 | 2 | 0 | 1 | 0 | 0 | 6 |
| C++ | 2 | 2 | 1 | 1 | 0 | 1 | 7 |

## Overlap with web

11 challenges count as both pwn and web (same definitions as [web-tags-summary.md](web-tags-summary.md)), for example DiceCTF 2023's chess.rs (`uaf` and `xss`), Google CTF 2021's tridroid (`ropchain` and `xss`), IJCTF 2020's built_in_http (`bof`, `sqli` and `directory-traversal`) and corCTF 2024's corchatv3 (`uaf` and `sqlinjection`).

## What the numbers show

- **Pwn is about one in seven tagged challenges** (14.7%). Its share rose from 14.5% (2020) to 18.5% (2022), then fell to 8.7% in 2025, the opposite of web, which rose to 36.7% in 2025.
- **Pwn writeups fall faster than writeups overall.** Pwn challenges drop from 314 (2020) to 25 (2025), 92% fewer; all challenges with tagged writeups drop 87%.
- **The hand review changes little.** It added 13 challenges, 1.3% on top of the 993 found through tags (web: 29, 2.1%).
- **Classic stack attacks dominate:** ROP (194) and stack buffer overflows (187) are the most common techniques, then heap exploitation (126) and format strings (101).
- **Stack techniques are fading; kernel and heap take a larger share.** ROP fell from 26–38% of technique-tagged pwn challenges (2020–2021) to 5% (2025), and format strings from 19% to 5%. Kernel exploitation grew from 3% (2020) to 18% (2024) and 35% (2025, 7 of 20); heap was 35% in 2025 (7 of 20).
- **Numbers after 2022 are small** (61, 34 and 20 technique-tagged challenges in 2023–2025), so read those shifts as indications rather than firm trends.

## Method

- **Pwn challenge:** a challenge whose tags include `pwn`, another spelling of it (`pwnable`, `binaryexploitation`, `binexploit`, ...), or a pwn keyword: a technique (bof, rop, ret2libc, format-string, heap, tcache, uaf, shellcode, srop, fsop, ...), a mitigation (canary, aslr, ...), a pwn tool (one_gadget, pwnscripts, libc-database) or a glibc version. `buffer` and `overflow` together count as a buffer overflow. The full list is in Appendix A. A challenge the tags miss is added only through the hand review below.
- **Broad words** such as `binary`, `exploit`, `exploitation`, `pwntools`, `kernel`, `seccomp`, `jit`, `sandbox`, `overflow`, `leak` or `gdb` are not enough on their own; they only count towards techniques inside challenges already identified as pwn.
- **Manual review of tagged challenges:** 83 borderline challenges (a pwn keyword next to another category, or only a broad pwn keyword such as `shellcode` or `heap`) were checked by hand; 17 were removed because the tag means something else there, such as reversing a ROP chain or analysing malware shellcode (Appendix B). Challenges that name a real exploitation technique stay in even when another category is also tagged.
- **Hand review:** the 92 tagged challenges outside the count that carry only broad pwn words (73) or have a pwn word in the task name (21: pwn, heap, rop, ret2, shellcode, buffer overflow, format string, bof) were checked by hand, against their name and against the tags on their CTFtime task page (each event's task list, checked on 6 Nov 2026; these tags often differ from the writeup tags). 13 were added (Appendix C): those whose task page carries a pwn keyword (`pwn`, `pwnable`, `binex`, `fmtstr`, ... as in Appendix A), and those whose name clearly shows a pwn challenge ("pwn", "heap", "ROP" or "buffer overflow" in the name). Only purely pwn challenges were added: none whose task page or writeup tags also show another category. One more, TAMUctf 2021's Handshake, was added for its writeup tags `nx` and `overflow`.
- **The `pwn` tag is counted as given**, as `web` was for web. 35 pwn-tagged challenges also carry another category and no exploitation keyword; some of them use `pwn` loosely (e.g. CSAW 2021's Gotta Decrypt em All, a crypto challenge).
- **Year:** the year the CTF event started (UTC), from the Event start date column. **Tags first:** challenges are identified by their writeup tags; task names and task pages are used only in the hand review.

### Not counted

- **79 challenges from the hand review were left out:** crypto, misc and scripting tasks that only use `pwntools`; stego, encoding and forensics tasks tagged `binary`; tasks with "pwn" in the name whose tags show another category (UTCTF 2020's Epic Admin Pwn, `web`; redpwnCTF 2020's 12-shades-of-redpwn, `crypto`; WolvCTF 2024's Eternally Pwned tasks, `forensics`; SpookyCTF 2024's [Pwn] Loab´s House of Horrors, `pyjail`); mixed challenges whose task page shows pwn next to another category (hxp CTF 2021's 日本旅行 (`misc` and `pwn`)); words like "cheap" that only contain "heap" (Really Awesome CTF 2020's Cheap Facades, `steganography`); and challenges with nothing that settles the category, such as HeroCTF v3's Kernel module tasks (`kernel-module`). m0leCon CTF 2021 Teaser's m0lang (`interpreter` · `overflow`, no task page tags) was left out after checking its writeup: the overflow is part of a reversing task.
- **Challenges whose writeups have no tags** (4,173) are outside the scope, even when the name shows a pwn challenge: 66 of them have a pwn word in the name, and 51 of those are pwn challenges going by their name or task page (e.g. SekaiCTF 2024's speedpwn).

## Appendix A: Keywords counted

Numbers are 2020–2025 pwn challenges carrying the keyword. Keywords marked \* only count inside challenges already identified as pwn.

| Group | Keywords |
| --- | --- |
| ROP / ret2* (ret2libc, SROP, ret2dlresolve, stack pivot) | `rop` (127), `ret2libc` (40), `ropchain` (22), `srop` (17), `one_gadget` (14), `ret2dlresolve` (11), `ret2csu` (10), `stack-pivot` (5), `ret2puts` (4), `stack_pivot` (4), `ropgadget` (3), `sigreturn` (3), `autorop` (2), `ret2shellcode` (2), `ret2syscall` (2), `ret2text` (2), `sigrop` (2), `babyrop` (1), `onegagdet` (1), `ret2dl` (1), `roppy` (1), `without_automaticrops` (1) |
| Stack buffer overflow | `bof` (109), `bufferoverflow` (43), `ret2win` (32), `buffer-overflow` (10), `stack_overflow` (10), `stackoverflow` (5), `buffer_overflow` (4), `stack-buffer-overflow` (3), `ret4win` (1), `stack-smash` (1) |
| Heap exploitation (tcache, UAF, double free, house of ...) | `heap` (88), `uaf` (21), `tcache` (19), `heap-overflow` (8), `tcache-poisoning` (7), `doublefree` (6), `use-after-free` (6), `off-by-one` (5), `__free_hook` (4), `tcache_perthread_struct` (4), `heap-feng-shui` (3), `safe-linking` (3), `tcache-dup` (3), `calloc`\* (2), `fastbin` (2), `fastbindup` (2), `houseofforce` (2), `mallocng` (2), `musl-1.2.2` (2), `offbyone` (2), `tcache-stash-unlink` (2), `unsorted_bin` (2), `unsortedbin` (2), `__malloc_hook` (1), `babyheap` (1), `babytcache` (1), `custom-heap` (1), `fake_chunk` (1), `fastbins` (1), `house-of-force` (1), `house_of_orange` (1), `malloc`\* (1), `mimalloc` (1), `null-byte-poisoning` (1), `off-by-null` (1), `off_by_one` (1), `poison-null-byte` (1), `unlink`\* (1) |
| Format string | `format-string` (81), `fmtstr` (10), `fsb` (9), `formatstring` (7), `fmt`\* (4), `fms`\* (2), `format-strings` (2), `format_string` (2), `__printf_arginfo_table` (1), `fmt_string` (1), `string-format` (1) |
| Shellcode (incl. seccomp / ORW) | `shellcode` (57), `seccomp`\* (21), `shellcoding` (7), `seccomp-tools`\* (2), `shellcraft` (2), `ascii_shellcode` (1), `orw` (1) |
| Kernel exploitation | `kernel`\* (34), `uefi`\* (4), `bpf`\* (3), `optee`\* (2), `kernel#pwn` (1), `netfilter` (1), `nftables` (1), `ring0` (1), `userfaultfd` (1), `windows-kernel` (1) |
| GOT overwrite / arbitrary write | `write-what-where` (15), `got-overwrite` (14), `got`\* (5), `arbitrary-write` (4), `got-ov` (1), `got_overwrite` (1) |
| Mitigation bypass (canary, ASLR, PIE, NX, CET) | `canary` (21), `pie`\* (9), `aslr` (4), `stackcanary` (4), `stack_canaries` (3), `cet` (2), `nx`\* (2), `shadowstack` (2), `cfi`\* (1) |
| Sandbox / VM / hypervisor escape | `sandbox`\* (16), `escape`\* (6), `docker-escape` (2), `hypervisor`\* (2), `kvm`\* (2), `sbx`\* (2), `chroot`\* (1), `hypervisor-exploitation` (1), `vm-escape` (1) |
| FILE / exit-handler hijacking (FSOP, vtables, fini_array) | `fsop` (8), `vtable`\* (5), `environ_ptr` (4), `fini_array` (4), `io_file` (3), `io_file_struct` (2), `__exit_funcs` (1), `dl_fini` (1), `dtor` (1), `fini`\* (1), `setcontext`\* (1) |
| Browser / JS engine exploitation | `v8` (8), `browser`\* (5), `jit`\* (4), `firefox`\* (3), `spidermonkey` (3), `chrome`\* (2), `chromium`\* (2), `mujs` (2), `luajit`\* (1), `turbofan` (1) |
| Integer bugs / out-of-bounds | `oob`\* (9), `integer-overflow`\* (3), `integeroverflow`\* (3), `integer_overflow`\* (2), `underflow`\* (2) |
| Pwn category (other spelling) | `binaryexploitation` (23), `pwnable` (18), `binary-exploitation` (12), `binexploit` (8), `babypwn` (2), `binary-exploitaion` (2), `clone-and-pwn` (2), `auto_pwn` (1), `babypwn2` (1), `binaryexploit` (1), `binex` (1), `kernel#pwn` (1), `pwnables` (1) |
| Pwn tools and glibc versions | `pwnscripts` (23), `glibc` (4), `libc-2.31` (4), `aeg` (3), `2.32` (2), `libc-2.27` (2), `libc-database` (2), `libc_database` (2), `auto_pwn` (1), `glibc-2.32` (1), `glibc-2.35` (1), `glibc2.23` (1), `libc-2.23` (1), `libc-2.28` (1), `libc-2.29` (1), `libc-2.35` (1) |
| Broad words (only inside pwn challenges) | `pwntools` (43), `leak` (16), `overflow` (15), `exploitation` (11), `binary` (10), `gdb` (10), `buffer` (8), `libc` (5), `exploit` (4), `gef` (1) |

## Appendix B: Challenges removed after manual review

| Year | Event | Task | Tags | Why it is not a pwn challenge |
| --- | --- | --- | --- | --- |
| 2025 | QnQSec CTF 2025 | Shadow Cache | forensic · shellcode | shellcode analysis (forensics) |
| 2024 | Midnight Sun CTF 2024 Quals | roprot | rev · rop | reversing a ROP chain (rev) |
| 2024 | SwampCTF 2024 | Reptilian Server | javascript · nodejs · vm-escape | Node.js vm sandbox escape (web/misc) |
| 2023 | CyberSecurityRumble Quals | shellcode-ception | gdb · rev · shellcode | shellcode analysis (rev) |
| 2021 | BlueHens CTF 2021 | Transforms | python · scripting · string-format | Python string formatting in a scripting task |
| 2021 | HeroCTF v3 | Magic Render | formatstringexploiter · python · web | Python format-string bug in a web app |
| 2021 | Intent CTF 2021 | Keep Safe | macro40 · reverse-engineering · shellcode | Excel 4.0 macro malware (rev) |
| 2021 | Real World CTF 3rd | Re:Montagy | blockchain · jop | jump-oriented code in an Ethereum contract (blockchain) |
| 2020 | CSAW CTF Qualification Round 2020 | baby_mult | gdb · re · rev · shellcode | reversing given shellcode (rev) |
| 2020 | DEF CON CTF Qualifier 2020 | dogooos | format-string · python · rce · web | Python format-string bug in a web app |
| 2020 | Hacktober CTF | ShellCode Extraction | analysis · shellcode | extracting shellcode from a file (forensics) |
| 2020 | InCTF 2020 | RE warmup | fini_array | reversing: check hidden in .fini_array |
| 2020 | Ledger Donjon CTF 2020 | picoHSM Speed Dating (1/3) | arm · hardware · shellcode · unicorn | hardware security module (hardware) |
| 2020 | Ledger Donjon CTF 2020 | picoHSM on Steroids (3/3) | arm · clock · fault · glitch · hardware · shellcode | hardware fault injection |
| 2020 | PlaidCTF 2020 | golf.so | elf · golf · ld_preload · misc · nasm · python · shellcode · z3 | code golf for a shared object (misc) |
| 2020 | VolgaCTF 2020 Qualifier | F-Hash | assembly · frida · shellcoding | reversing: assembly patch to speed up a hash |
| 2020 | nullcon HackIM 2020 | returminator | engineer · reverse · rop · z3 | reversing a ROP chain (rev) |

## Appendix C: Challenges added by hand

Their writeup tags are too weak to count on their own, but their CTFtime task page or their name shows a purely pwn challenge. Task page tags are as listed on the event's task list.

| Year | Event | Task | Writeup tags | Task page tags | Why it was added |
| --- | --- | --- | --- | --- | --- |
| 2024 | BlackHat MEA CTF Qualification 2024 | CPL0 | kernel · qemu | pwn | task page tag |
| 2024 | UIUCTF 2024 | Syscalls | seccomp | pwn | task page tag |
| 2022 | Space Heroes 2022 | SATisfied | gdb · ghidra · pwntools | pwn | task page tag |
| 2022 | picoCTF 2022 | buffer overflow 0 | binary | binary-exploitation | "buffer overflow" in the name + task page tag |
| 2021 | 0CTF/TCTF 2021 Quals | BabyHeap 2021 | integeroverflow | musl-1.1.24 · pwn · heap | "heap" in the name + task page tag |
| 2021 | ALLES! CTF 2021 | ccanary | binary · ctf | pwn | "canary" in the name + task page tag |
| 2021 | HackPack CTF 2021 | Mind Blown | pwntools | brainfuck · pwn · aslr · buffer-overflow | task page tag |
| 2021 | TAMUctf 2021 | Handshake | nx · overflow | – | writeup tags nx (a binary mitigation) and overflow |
| 2021 | m0leCon CTF 2021 Teaser | Puncher | afl · fortran · overflow | pwn | task page tag |
| 2020 | Codegate CTF 2020 Preliminary | babyllvm | jit | pwnable | task page tag |
| 2020 | PlaidCTF 2020 | Back to the Future | browser · exploitation · netscape | pwn | task page tag |
| 2020 | SCTF-XCTF 2020 | EasyWinHeap | windows | pwn | "heap" in the name + task page tag |
| 2020 | SunshineCTF 2020 | Florida-Forecaster | ghidra · pwntools | linux · 64bit · pwn | task page tag |
