# Rev (reverse engineering) challenge tags on CTFtime writeups, 2020–2025

**874 different rev challenges** are among the 6,859 challenges with tagged writeups from CTFs held in 2020–2025, each counted once: 12.7% of them. 344 carry the `rev` tag, 505 more were found through its other spellings (reversing, reverse, re, reverse_engineering, ...) or reversing tools (ida, binaryninja, jadx, upx, ...), and 25 were added in a hand review: their tags are too weak to count, but their CTFtime task page or name shows a purely rev challenge. Companion to [web-tags-summary.md](web-tags-summary.md), [pwn-tags-summary.md](pwn-tags-summary.md) and [crypto-tags-summary.md](crypto-tags-summary.md), with the same data and method.

## Data

- **Source:** every writeup listed on [ctftime.org/writeups](https://ctftime.org/writeups) (all 1,309 pages, 39,253 writeups), collected on 30 Oct 2026, 13:31–13:45 UTC; event dates from CTFtime's [events API](https://ctftime.org/api/).
- **File:** [`ctftime_writeups_tasks.xlsx`](ctftime_writeups_tasks.xlsx), one tab (`Tasks`) with the columns Event, Task, Tags and Event start date: 19,494 challenges, all years. Writeups of the same task are merged and their tags combined, so a task solved by several teams counts once.
- **Scope:** challenges whose event started in 2020–2025 (UTC) and whose writeups have at least one tag: 6,859 of the 11,032 challenges from those years. The 4,173 challenges whose writeups have no tags are left out.

## Rev challenges per year

| Year | Challenges with tags | Tagged `rev` | Other rev keywords only | Added by hand | **Rev challenges** | Share |
| --- | --- | --- | --- | --- | --- | --- |
| 2020 | 2,170 | 93 | 182 | 8 | **283** | 13.0% |
| 2021 | 1,825 | 110 | 149 | 6 | **265** | 14.5% |
| 2022 | 1,025 | 41 | 78 | 5 | **124** | 12.1% |
| 2023 | 1,028 | 72 | 51 | 5 | **128** | 12.5% |
| 2024 | 525 | 18 | 32 | 1 | **51** | 9.7% |
| 2025 | 286 | 10 | 13 | 0 | **23** | 8.0% |
| **Total** | **6,859** | **344** | **505** | **25** | **874** | **12.7%** |

- **Counted once:** a challenge tagged `rev`, `reversing` and, say, `ida` is one challenge. Counting every keyword hit separately would give 1,214 instead of the 849 found through tags.
- **Added by hand:** a hand review of the 248 challenges whose tags have only weak rev hints (`ghidra`, `angr`, `z3`, `vm`, `apk`, `pyc`, `wasm`, `rust`, ...) or whose task name has a rev word kept the 25 that are purely rev going by their CTFtime task page or name, such as corCTF 2021's babyrev (`ghidra` · `c`, task page tagged `rev`), picoCTF 2021's crackme-py (`easy`, task page tagged `reverse_engineering`) or zer0pts CTF 2023's decompile me. They are listed in Appendix C.

### Is there a dominant tag?

No. **`rev`** is on only 344 of the 849 rev challenges found through tags (40.5%), against 81.9% for `web`, 86.4% for `pwn` and 76.9% for `crypto`. Writeup authors spell the category in many ways:

| Spelling | Challenges |
| --- | --- |
| `rev` | 344 |
| `reversing` | 251 |
| `reverse` | 213 |
| `re` | 83 |
| `reverse_engineering` | 53 |
| `reverse-engineering` | 49 |
| `revesing` | 18 |
| `reverseengineering` | 13 |
| `mobile_reverse` | 7 |
| `reveng` | 2 |
| `revers` | 1 |
| `rever` | 1 |
| `reverseng` | 1 |

- **Several spellings at once:** 618 challenges carry one spelling, 213 carry two or more (`rev` and `reversing`, say) and are counted once. `engineering` (101 challenges) only appears next to `reverse`, from "reverse engineering" split into two tags.
- **Tools are the most common other tags, but most are shared with pwn and crypto:** `ghidra` (46 challenges, 35 with a rev spelling), `z3` (47, 27), `angr` (35, 28), `gdb` (31, 21) and `radare2` (15, 7) also appear in pwn, crypto and misc writeups, so they only count inside challenges already identified as rev. Tools used almost only for reversing (`ida`, `binaryninja`, `x64dbg`, `jadx`, `dnspy`, `upx`, ...) and the words `keygen` and `crackme` count on their own; they find 18 challenges with no rev spelling.
- **Left out:** tags that contain "rev" or "reverse" but are not reverse engineering: `reverseimagesearch` (4), `reverse-shell` (1), `reverse_shell` (1), `trevorc2` (1) (OSINT image search, reverse shells, a C2 framework). Numbers are challenges with no rev keyword.

## By technique or target

Each row counts a challenge once, even with several spellings (`ida` and `idapython`, say). A challenge can be in several rows. Families come from tags only. 342 of the 874 rev challenges name at least one family; the other 532 are tagged only with a rev spelling or with words that don't name one.

| Family | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Decompilers & disassemblers (Ghidra, IDA, Binary Ninja, radare2) | 25 | 28 | 12 | 9 | 3 | 3 | 80 |
| Symbolic execution & solvers (angr, z3) | 28 | 13 | 9 | 8 | 0 | 0 | 58 |
| Debugging & dynamic analysis (gdb, x64dbg, Frida, ltrace) | 17 | 12 | 11 | 6 | 1 | 1 | 48 |
| Mobile apps (Android, APK, iOS) | 19 | 5 | 9 | 5 | 2 | 0 | 40 |
| .NET & Java (dnSpy, JVM) | 16 | 6 | 3 | 12 | 2 | 0 | 39 |
| Custom VMs, bytecode & emulators | 9 | 9 | 0 | 13 | 2 | 3 | 36 |
| Native languages (Rust, Go, C++, Haskell, Nim) | 11 | 6 | 5 | 5 | 3 | 1 | 31 |
| Firmware & hardware (ARM, AVR, Verilog) | 10 | 4 | 2 | 3 | 1 | 1 | 21 |
| Obfuscation, packing & anti-debugging | 4 | 7 | 1 | 6 | 0 | 1 | 19 |
| Games (Unity, Game Boy, game hacking) | 7 | 3 | 2 | 1 | 6 | 0 | 19 |
| Python, Lua & scripts (pyc, PyInstaller, VBA) | 5 | 7 | 3 | 3 | 0 | 0 | 18 |
| Windows, PE & malware | 2 | 5 | 6 | 1 | 0 | 0 | 14 |
| Keygens & crackmes | 2 | 3 | 0 | 5 | 0 | 0 | 10 |
| WebAssembly | 0 | 5 | 2 | 1 | 1 | 0 | 9 |
| **Name at least one family** | **116** | **89** | **52** | **62** | **16** | **7** | **342** |

Share of the rev challenges that name a family:

| Family | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
| --- | --- | --- | --- | --- | --- | --- |
| Decompilers & disassemblers (Ghidra, IDA, Binary Ninja, radare2) | 21.6% | 31.5% | 23.1% | 14.5% | 18.8% | 42.9% |
| Symbolic execution & solvers (angr, z3) | 24.1% | 14.6% | 17.3% | 12.9% | 0.0% | 0.0% |
| Debugging & dynamic analysis (gdb, x64dbg, Frida, ltrace) | 14.7% | 13.5% | 21.2% | 9.7% | 6.2% | 14.3% |
| Mobile apps (Android, APK, iOS) | 16.4% | 5.6% | 17.3% | 8.1% | 12.5% | 0.0% |
| .NET & Java (dnSpy, JVM) | 13.8% | 6.7% | 5.8% | 19.4% | 12.5% | 0.0% |
| Custom VMs, bytecode & emulators | 7.8% | 10.1% | 0.0% | 21.0% | 12.5% | 42.9% |
| Native languages (Rust, Go, C++, Haskell, Nim) | 9.5% | 6.7% | 9.6% | 8.1% | 18.8% | 14.3% |
| Firmware & hardware (ARM, AVR, Verilog) | 8.6% | 4.5% | 3.8% | 4.8% | 6.2% | 14.3% |

## Most used keywords in rev challenges

Individual keywords, excluding the rev spellings. A challenge tagged both `ida` and `idapython` is in both rows here but counted once in the decompilers row above.

| Keyword | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `python` | 15 | 12 | 4 | 13 | 1 | 0 | 45 |
| `ghidra` | 12 | 15 | 6 | 4 | 1 | 1 | 39 |
| `android` | 17 | 5 | 7 | 3 | 2 | 0 | 34 |
| `z3` | 18 | 9 | 3 | 3 | 0 | 0 | 33 |
| `angr` | 12 | 5 | 6 | 5 | 0 | 0 | 28 |
| `java` | 13 | 3 | 3 | 8 | 1 | 0 | 28 |
| `vm` | 6 | 8 | 0 | 8 | 1 | 3 | 26 |
| `gdb` | 4 | 8 | 5 | 5 | 0 | 0 | 22 |
| `ida` | 1 | 10 | 3 | 1 | 1 | 0 | 16 |
| `apk` | 5 | 0 | 8 | 1 | 0 | 0 | 14 |
| `c` | 2 | 1 | 5 | 2 | 0 | 1 | 11 |
| `frida` | 4 | 3 | 4 | 0 | 0 | 0 | 11 |
| `elf` | 1 | 2 | 4 | 1 | 2 | 0 | 10 |
| `bytecode` | 1 | 1 | 0 | 4 | 1 | 2 | 9 |
| `wasm` | 0 | 4 | 2 | 1 | 1 | 0 | 8 |
| `c++` | 3 | 3 | 0 | 2 | 0 | 0 | 8 |
| `binaryninja` | 1 | 2 | 2 | 0 | 1 | 1 | 7 |

## Overlap with crypto, pwn and web

37 rev challenges also count as crypto, 29 as pwn and 9 as web (same definitions as the other summaries), for example 1337UP LIVE CTF 2023's Keyless (`crypto` and `rev`), pbctf 2023's Revenge of LLLattice (`lattice` and `reversing`), UIUCTF 2024's Lost Canary (`pwn` and `rev`) and GPN CTF 2023's what-the-flag (`jsfuck`, `rev` and `web`).

## What the numbers show

- **Rev is about one in eight tagged challenges** (12.7%). Its share peaked at 14.5% in 2021 and fell to 8.0% in 2025, like pwn (14.5% to 8.7%) and unlike web (19.2% to 36.7%) and crypto (steady between 16.5% and 18.9%).
- **Rev writeups fall faster than writeups overall.** Rev challenges drop from 283 (2020) to 23 (2025), 92% fewer; all challenges with tagged writeups drop 87%.
- **The category has no single tag.** Only 40.5% of the rev challenges found through tags carry `rev`; counting `rev` alone would miss more than half of them.
- **The hand review changes little.** It added 25 challenges, 2.9% on top of the 849 found through tags (web: 29, 2.1%; pwn: 13, 1.3%; crypto: 47, 4.1%).
- **Most rev writeups don't say what was reversed.** Only 342 of the 874 rev challenges (39.1%) name a tool, technique or target; for web, pwn and crypto about half or more name an attack type or technique.
- **Decompilers and solvers lead.** Decompilers and disassemblers are named in 80 rev challenges and symbolic execution or solvers (angr, z3) in 58, then debugging and dynamic analysis (48). Solvers appear in 28 challenges in 2020 and in none in 2024–2025.
- **Numbers after 2022 are small** (62, 16 and 7 family-naming rev challenges in 2023–2025), so read year-to-year shifts as indications rather than firm trends.

## Method

- **Rev challenge:** a challenge whose tags include a rev spelling (`rev`, `reversing`, `reverse`, `re`, `reverse_engineering`, `reverse-engineering`, `reverseengineering`, `revesing`, `mobile_reverse`, ...) or a keyword used almost only for reversing: a reversing tool (ida, binaryninja, x64dbg, ollydbg, ltrace, jadx, apktool, dnspy, uncompyle6, upx, ...) or the words keygen and crackme. The full list is in Appendix A. A challenge the tags miss is added only through the hand review below.
- **Generic words** such as `ghidra`, `radare2`, `angr`, `z3`, `gdb`, `frida`, `vm`, `bytecode`, `obfuscation`, `android`, `java`, `wasm` or `rust` are not enough on their own; they only count towards families inside challenges already identified as rev.
- **Manual review of tagged challenges:** 42 borderline challenges (found only through a reversing tool, or tagged only `reverse` or `re` next to another category or next to words like "shell" or "search") were checked by hand; 2 were removed because "reverse" means something else there (Appendix B).
- **Hand review:** the 248 tagged challenges outside the count that have only weak rev hints (235) or a rev word in the task name (18: rev, reverse, crackme, keygen, decompile, flag checker, ...) were checked by hand, against their name and against the tags on their CTFtime task page (each event's task list, checked on 6 Nov 2026; these tags often differ from the writeup tags). 25 were added (Appendix C): those whose task page carries a rev keyword (`rev`, `reverse`, `re`, `reversing`, `reverse_engineering`, ...), and those whose name clearly shows a rev challenge (rev/... prefixes, "Crack Me", "decompile"). Only purely rev challenges were added: none whose task page or writeup tags also show another category.
- **The rev spellings are counted as given**, as `web`, `pwn` and `crypto` were. 67 rev-tagged challenges also carry another category and no rev keyword (e.g. UIUCTF 2024's Lost Canary, `pwn` · `rev`).
- **Year:** the year the CTF event started (UTC), from the Event start date column. **Tags first:** challenges are identified by their writeup tags; task names and task pages are used only in the hand review.

### Not counted

- **Events that started on 31 Dec 2019** (BambooFox CTF, TetCTF 2020) fall outside the range by start date; they have 2 rev challenges (BambooFox CTF's Move or Not and How2decompyle).
- **223 challenges from the hand review were left out:** pwn tasks whose writeups name the tools used to study the binary (`ghidra`, `radare2`, `angr`, `gdb`), crypto and misc tasks solved with `z3`, mobile, forensics and web tasks (for 147 of the candidates the task page shows only another category); mixed challenges whose task page or writeup tags show rev next to another category (0CTF/TCTF 2021 Quals's fea; Cyber Apocalypse 2021's Invitation; hxp CTF 2021's baba is you; Killer Queen CTF 2021's "web, rev, crypto", and 3 more); and challenges with nothing that settles the category, such as zer0pts CTF 2023's mimikyu (`libgmp` · `obfuscation`) or ImaginaryCTF 2021's Password Checker (`javascript` · `deobfuscation`).
- **Challenges whose writeups have no tags** (4,173) are outside the scope, even when the name shows a rev challenge: 54 of them have a rev word in the name; they were not reviewed.

## Appendix A: Keywords counted

Numbers are 2020–2025 rev challenges carrying the keyword. Keywords marked \* only count inside challenges already identified as rev.

| Group | Keywords |
| --- | --- |
| Rev category (spellings) | `rev` (344), `reversing` (251), `reverse` (213), `engineering` (101), `re` (83), `reverse_engineering` (53), `reverse-engineering` (49), `revesing` (18), `reverseengineering` (13), `mobile_reverse` (7), `reveng` (2), `rever` (1), `revers` (1), `reverseng` (1) |
| Decompilers & disassemblers (Ghidra, IDA, Binary Ninja, radare2) | `ghidra`\* (39), `ida` (16), `binaryninja` (7), `radare2`\* (7), `idapython` (5), `decompile`\* (3), `disassembly`\* (3), `r2`\* (3), `radare`\* (3), `binja` (2), `decompilation`\* (1), `jeb` (1), `objdump`\* (1) |
| Symbolic execution & solvers (angr, z3) | `z3`\* (33), `angr`\* (28), `symbolic_execution`\* (4), `smt`\* (1) |
| Debugging & dynamic analysis (gdb, x64dbg, Frida, ltrace) | `gdb`\* (22), `frida`\* (11), `debugging`\* (5), `ltrace` (4), `dynamic`\* (3), `debugger`\* (2), `dynamic-analysis`\* (1), `gdbscript`\* (1), `instrumentationcallback`\* (1), `qiling`\* (1), `strace`\* (1), `windbg`\* (1), `x64dbg` (1) |
| Mobile apps (Android, APK, iOS) | `android`\* (34), `apk`\* (14), `apktool` (3), `apktools` (3), `jadx` (3), `ios`\* (1), `smali` (1) |
| .NET & Java (dnSpy, JVM) | `java`\* (28), `.net`\* (6), `jar`\* (4), `csharp`\* (2), `dnspy` (2), `dotnet`\* (2) |
| Custom VMs, bytecode & emulators | `vm`\* (26), `bytecode`\* (9), `emulation`\* (2), `emulator`\* (2), `brainfuck`\* (1) |
| Native languages (Rust, Go, C++, Haskell, Nim) | `c++`\* (8), `rust`\* (7), `go`\* (5), `golang`\* (5), `haskell`\* (4), `nim`\* (1), `ocaml`\* (1), `swift`\* (1) |
| Firmware & hardware (ARM, AVR, Verilog) | `mips`\* (6), `verilog`\* (5), `arm32`\* (3), `arduino`\* (2), `firmware`\* (2), `xtensa`\* (2), `avr`\* (1), `esp32`\* (1), `fpga`\* (1), `risc-v`\* (1) |
| Obfuscation, packing & anti-debugging | `obfuscation`\* (5), `upx` (5), `selfmodifying` (2), `unpacking` (2), `anti-debug`\* (1), `antidebug`\* (1), `deobfuscating`\* (1), `deobfuscation`\* (1), `nanomites` (1), `obfuscated`\* (1), `obfuscator`\* (1), `protector`\* (1) |
| Games (Unity, Game Boy, game hacking) | `game`\* (7), `gameboy`\* (4), `unity`\* (4), `game-hacking`\* (3), `gamehacking`\* (2), `games`\* (1), `gba`\* (1), `godot`\* (1) |
| Python, Lua & scripts (pyc, PyInstaller, VBA) | `pyc`\* (5), `uncompyle6` (4), `lua`\* (3), `pyinstxtractor` (3), `macro`\* (2), `macros`\* (2), `pyinstaller`\* (2), `vba`\* (2), `cpython`\* (1), `decompyle3` (1) |
| Windows, PE & malware | `malware`\* (6), `windows`\* (4), `dll`\* (3), `ransomware`\* (3), `exe`\* (1), `pe`\* (1), `winapi`\* (1) |
| Keygens & crackmes | `keygen` (7), `crackme` (3), `keygenme` (1) |
| WebAssembly | `wasm`\* (8), `webassembly`\* (2) |
| Generic words (only inside rev challenges) | `python` (45), `c` (11), `elf` (10), `assembly` (7), `linux` (7), `strings` (6), `asm` (5), `x86` (4), `jit` (2), `llvm` (2), `binary` (1), `hexdump` (1), `patching` (1), `x86-64` (1) |

## Appendix B: Challenges removed after manual review

| Year | Event | Task | Tags | Why it is not a rev challenge |
| --- | --- | --- | --- | --- |
| 2020 | TAMUctf 2020 | Blind | blind · exit · reverse · shell | 'reverse' as in a reverse shell (misc) |
| 2020 | riftCTF | Misc 0x0002 | audio · misc · miscellaneous · reverse · search · shazam · youtube | 'reverse' as in a reverse audio search (Shazam, misc) |

## Appendix C: Challenges added by hand

Their writeup tags are too weak to count on their own, but their CTFtime task page or their name shows a purely rev challenge. Task page tags are as listed on the event's task list.

| Year | Event | Task | Writeup tags | Task page tags | Why it was added |
| --- | --- | --- | --- | --- | --- |
| 2024 | SekaiCTF 2024 | Crack Me | android · firebase | – | "Crack Me" in the name |
| 2023 | HeroCTF v5 | Give My Money Back | deobfuscating · vbscript | reverse | task page tag |
| 2023 | JerseyCTF III | all bin/rev challenges | bin | rev · bin | writeup of several rev challenges + task page tag |
| 2023 | Lexington Informatics Tournament CTF 2023 | rev/iloveregex | regex · regularexpression | – | rev/... in the name |
| 2023 | Space Heroes 2023 | everything is wrong | haskell · side-channel | re | task page tag |
| 2023 | zer0pts CTF 2023 | decompile me | calling-convention · disassembly · rc4 | – | "decompile" in the name |
| 2022 | Lexington Informatics Tournament CTF 2022 | rev/not assembly | assembly | assembly · rev | rev/... in the name + task page tag |
| 2022 | Space Heroes 2022 | An Unknown Disassembly | python | re | "Disassembly" in the name + task page tag |
| 2022 | WPICTF 2022 | PokemonRematch | frida · gameboy · gba | gameboy · reverse | task page tag |
| 2022 | ångstromCTF 2022 | dyn | dynamic-analysis | rev | task page tag |
| 2022 | ångstromCTF 2022 | self | frida | reverse | task page tag |
| 2021 | BambooFox CTF 2021 | Flag Checker | verilog | reverse | "Flag Checker" in the name + task page tag |
| 2021 | BambooFox CTF 2021 | Ransomware | pyc · python | reverse | task page tag |
| 2021 | HITB PRO CTF 2021 | cells | z3 | symbolic_execution · vm · reversing | task page tag |
| 2021 | corCTF 2021 | AliceInCeptionland | csharp | rev · csharp · game | task page tag |
| 2021 | corCTF 2021 | babyrev | c · cyberchef · ghidra · python | rev | "rev" in the name + task page tag |
| 2021 | picoCTF 2021 | crackme-py | easy | reverse_engineering | "crackme" in the name + task page tag |
| 2020 | 2020 Defenit CTF | MixMix | rc4 · z3 | rev | task page tag |
| 2020 | Codegate CTF 2020 Preliminary | RS | rust | reversing | task page tag |
| 2020 | CyberSecurityRumble CTF | CSAdventure | build.data.unityweb · data.unity3d · global-metadata.dat · javascript · level0 · unity · unityinstance · webgl | rev | task page tag |
| 2020 | Hexion CTF 2020 Online | Serial Killer | bgb · gameboy | reverse | task page tag |
| 2020 | UIUCTF 2020 | Redd's Art | debugging · gdb | reverse_engineering | task page tag |
| 2020 | UUTCTF 2020 | Flaggy Bird | android | reverse | task page tag |
| 2020 | VolgaCTF 2020 Qualifier | F-Hash | assembly · frida · shellcoding | reverse · engineering | task page tag |
| 2020 | castorsCTF20 | Stacking | ghidra · video | reverse · engineering | task page tag |
