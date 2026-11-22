# Forensics challenge tags on CTFtime writeups, 2020–2025

**771 different forensics challenges** are among the 6,859 challenges with tagged writeups from CTFs held in 2020–2025, each counted once: 11.2% of them. 567 carry the `forensics` tag, 180 more were found through its other spellings (forensic, dfir, blueteam, ...) or forensics tools and artifacts (wireshark, pcap, volatility, memory dumps, usb, ...), and 24 were added in a hand review: their tags are too weak to count, but their CTFtime task page or name shows a purely forensics challenge. Steganography is kept as its own category: the 137 challenges tagged as steganography without any forensics keyword are not counted (with them the total would be 908). Companion to [web-tags-summary.md](web-tags-summary.md), [pwn-tags-summary.md](pwn-tags-summary.md), [crypto-tags-summary.md](crypto-tags-summary.md) and [rev-tags-summary.md](rev-tags-summary.md), with the same data and method.

## Data

- **Source:** every writeup listed on [ctftime.org/writeups](https://ctftime.org/writeups) (all 1,309 pages, 39,253 writeups), collected on 30 Oct 2026, 13:31–13:45 UTC; event dates from CTFtime's [events API](https://ctftime.org/api/).
- **File:** [`ctftime_writeups_tasks.xlsx`](ctftime_writeups_tasks.xlsx), one tab (`Tasks`) with the columns Event, Task, Tags and Event start date: 19,494 challenges, all years. Writeups of the same task are merged and their tags combined, so a task solved by several teams counts once.
- **Scope:** challenges whose event started in 2020–2025 (UTC) and whose writeups have at least one tag: 6,859 of the 11,032 challenges from those years. The 4,173 challenges whose writeups have no tags are left out.

## Forensics challenges per year

| Year | Challenges with tags | Tagged `forensics` | Other forensics keywords only | Added by hand | **Forensics challenges** | Share |
| --- | --- | --- | --- | --- | --- | --- |
| 2020 | 2,170 | 167 | 42 | 7 | **216** | 10.0% |
| 2021 | 1,825 | 137 | 37 | 8 | **182** | 10.0% |
| 2022 | 1,025 | 105 | 24 | 3 | **132** | 12.9% |
| 2023 | 1,028 | 77 | 51 | 3 | **131** | 12.7% |
| 2024 | 525 | 56 | 21 | 3 | **80** | 15.2% |
| 2025 | 286 | 25 | 5 | 0 | **30** | 10.5% |
| **Total** | **6,859** | **567** | **180** | **24** | **771** | **11.2%** |

- **Counted once:** a challenge tagged `forensics`, `wireshark` and `pcap` is one challenge. Counting every keyword hit separately would give 1,035 instead of the 747 found through tags.
- **Added by hand:** a hand review of the 268 challenges whose tags have only weak forensics hints (`binwalk`, `pdf`, `powershell`, `memory`, `logs`, `sstv`, `hashcat`, ...) or whose task name has a forensics word kept the 24 that are purely forensics going by their CTFtime task page or name, such as HTB Business CTF 2021's DFIR (`encryption` · `obfuscation` · `powershell` · `python`, task page tagged `forensics`), picoCTF 2021's tunn3l v1s10n (`bmp` · `corrupt` · `repairing`, task page tagged `forensics`) or the three Batman Investigation challenges of bi0sCTF 2024 (task pages tagged `incidentresponse`, `dfir` or both). They are listed in Appendix C.

### With steganography

Steganography is not counted as forensics here: most stego writeups carry no forensics tag (of the 199 tagged challenges with a steganography keyword, 62 are counted as forensics), and many events have a separate stego category. Inside forensics challenges, stego tags count towards the steganography family. If the 137 steganography challenges without a forensics keyword were counted as well:

| Year | Forensics challenges | Steganography only | Together | Share |
| --- | --- | --- | --- | --- |
| 2020 | 216 | 46 | **262** | 12.1% |
| 2021 | 182 | 48 | **230** | 12.6% |
| 2022 | 132 | 15 | **147** | 14.3% |
| 2023 | 131 | 19 | **150** | 14.6% |
| 2024 | 80 | 4 | **84** | 16.0% |
| 2025 | 30 | 5 | **35** | 12.2% |
| **Total** | **771** | **137** | **908** | **13.2%** |

### Is there a dominant tag?

Yes. **`forensics`** is on 567 of the 747 forensics challenges found through tags (75.9%), against 81.9% for `web`, 86.4% for `pwn`, 76.9% for `crypto` and 40.5% for `rev`. The spellings on the forensics challenges found through tags:

| Spelling | Challenges |
| --- | --- |
| `forensics` | 567 |
| `forensic` | 129 |
| `blueteam` | 8 |
| `dfir` | 3 |
| `digital-forensics` | 3 |
| `forensic+crypto` | 3 |
| `incidentresponse` | 3 |
| `fornsics` | 2 |
| `windows-forensics-analysis` | 2 |
| `browser-forensics` | 1 |
| `foren` | 1 |
| `forenc` | 1 |
| `forenciss` | 1 |
| `foreniscs` | 1 |
| `forens` | 1 |
| `incident` | 1 |
| `windows-forensics` | 1 |
| `windowsforensics` | 1 |

- **Several spellings at once:** 600 challenges carry one spelling and 63 carry two or more (`forensics` and `forensic`, say); they are counted once. `blueteam` (8) is the eight-part Blue's Clues investigation of Cyberconférence CTF (24h@CTF '23); `fornsics`, `foreniscs`, `forenciss`, `forenc` and `foren` are misspellings.
- **84 challenges have no forensics spelling** and are found only through a forensics tool or artifact, mostly packet captures and memory dumps (e.g. DEADFACE CTF's seven `pcap` challenges in 2021, or TrollCAT CTF 2021's Mr_evilpepo series, `volatility`).

### How the related tags were chosen

Every tag on the 2020–2025 tagged writeups was checked for how often it appears next to a forensics spelling and next to other categories. Tools and artifacts used almost only in forensics count on their own; tags common in other categories only count inside challenges already identified as forensics; steganography tags are a family inside forensics but do not count on their own. Examples (challenges with the tag, and how many of them also carry a forensics spelling):

| Keyword | Challenges | With a forensics spelling | Categories on the rest (top 3) | How it is used |
| --- | --- | --- | --- | --- |
| `wireshark` | 88 | 46 | misc 4, crypto 2, OSINT 2 | counts on its own |
| `pcap` | 61 | 29 | web 4, rev 2, blockchain 1 | counts on its own |
| `volatility` | 67 | 49 | – | counts on its own |
| `memorydump` | 19 | 18 | – | counts on its own |
| `memory_dump` | 13 | 9 | web 1 | counts on its own |
| `usb` | 10 | 7 | misc 2 | counts on its own |
| `registry` | 6 | 5 | – | counts on its own |
| `autopsy` | 8 | 8 | – | counts on its own |
| `binwalk` | 24 | 12 | stego 2, OSINT 1 | only inside forensics |
| `exiftool` | 11 | 6 | – | only inside forensics |
| `pdf` | 23 | 11 | web 1, misc 1, rev 1 | only inside forensics |
| `powershell` | 21 | 9 | rev 3, web 1, programming 1 | only inside forensics |
| `malware` | 15 | 6 | rev 4, OSINT 1 | only inside forensics |
| `network` | 36 | 15 | crypto 1 | only inside forensics |
| `networking` | 29 | 8 | OSINT 5, web 4, crypto 1 | only inside forensics |
| `password-cracking` | 18 | 4 | web 3, crypto 2, misc 2 | only inside forensics |
| `git` | 34 | 8 | web 9, misc 8, OSINT 3 | only inside forensics |
| `android` | 52 | 4 | rev 29, mobile 7, pwn 2 | only inside forensics |
| `steganography` | 108 | 25 | misc 7, OSINT 3, crypto 3 | stego family, only inside forensics |
| `stego` | 87 | 30 | misc 9, OSINT 2, crypto 2 | stego family, only inside forensics |
| `steghide` | 11 | 4 | stego 4, crypto 1 | stego family, only inside forensics |

- **Counted on their own:** the tools and artifacts in Appendix A without a \* find 84 challenges that have no forensics spelling; all 98 such matches were checked by hand and 14 removed (Appendix B).
- **Left out:** tags that contain a forensics word but mean something else: `discrete-log` (6), `log4j` (5), `log_poisoning` (2), `prefetch` (1) (discrete logarithms in crypto, Log4Shell and log poisoning in web, a CPU prefetch side channel in pwn). Numbers are challenges with no forensics keyword.

## By technique or target

Each row counts a challenge once, even with several spellings (`pcap` and `pcapng`, say). A challenge can be in several rows. Families come from tags only. 406 of the 771 forensics challenges name at least one family; the other 365 are tagged only with a forensics spelling or with words that don't name one.

| Family | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Network traffic & packet captures (pcap, Wireshark) | 45 | 35 | 27 | 22 | 23 | 3 | 155 |
| Memory forensics (Volatility, memory dumps) | 26 | 19 | 3 | 17 | 6 | 1 | 72 |
| Steganography (LSB, steghide, spectrograms) | 22 | 27 | 7 | 8 | 2 | 1 | 67 |
| File carving & file formats (binwalk, broken PNG/PDF/ZIP) | 14 | 11 | 11 | 8 | 3 | 1 | 48 |
| Incident response & malware (maldocs, PowerShell, phishing) | 3 | 10 | 3 | 2 | 4 | 2 | 24 |
| Windows artifacts & event logs (registry, EVTX, timeline) | 6 | 4 | 4 | 2 | 4 | 2 | 22 |
| Disk images & file systems (Autopsy, FTK, file recovery) | 4 | 2 | 3 | 7 | 4 | 0 | 20 |
| Browser, email, Git & database artifacts | 3 | 6 | 6 | 0 | 3 | 0 | 18 |
| Password & archive cracking (John, hashcat, KeePass) | 3 | 7 | 1 | 2 | 2 | 2 | 17 |
| Audio, radio & signals (SSTV, Morse, SDR) | 8 | 2 | 3 | 4 | 0 | 0 | 17 |
| USB, keyboard & Bluetooth captures | 6 | 5 | 3 | 0 | 1 | 1 | 16 |
| Metadata (EXIF, exiftool) | 1 | 3 | 3 | 0 | 0 | 0 | 7 |
| Mobile & cloud (Android, iOS, cloud) | 1 | 0 | 1 | 2 | 0 | 0 | 4 |
| **Name at least one family** | **118** | **103** | **62** | **66** | **48** | **9** | **406** |

Share of the forensics challenges that name a family:

| Family | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
| --- | --- | --- | --- | --- | --- | --- |
| Network traffic & packet captures (pcap, Wireshark) | 38.1% | 34.0% | 43.5% | 33.3% | 47.9% | 33.3% |
| Memory forensics (Volatility, memory dumps) | 22.0% | 18.4% | 4.8% | 25.8% | 12.5% | 11.1% |
| Steganography (LSB, steghide, spectrograms) | 18.6% | 26.2% | 11.3% | 12.1% | 4.2% | 11.1% |
| File carving & file formats (binwalk, broken PNG/PDF/ZIP) | 11.9% | 10.7% | 17.7% | 12.1% | 6.2% | 11.1% |
| Incident response & malware (maldocs, PowerShell, phishing) | 2.5% | 9.7% | 4.8% | 3.0% | 8.3% | 22.2% |
| Windows artifacts & event logs (registry, EVTX, timeline) | 5.1% | 3.9% | 6.5% | 3.0% | 8.3% | 22.2% |
| Disk images & file systems (Autopsy, FTK, file recovery) | 3.4% | 1.9% | 4.8% | 10.6% | 8.3% | 0.0% |
| Browser, email, Git & database artifacts | 2.5% | 5.8% | 9.7% | 0.0% | 6.2% | 0.0% |

## Most used keywords in forensics challenges

Individual keywords, excluding the forensics spellings. A challenge tagged both `pcap` and `wireshark` is in both rows here but counted once in the network row above.

| Keyword | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `wireshark` | 17 | 21 | 16 | 15 | 14 | 1 | 84 |
| `volatility` | 26 | 16 | 2 | 17 | 5 | 1 | 67 |
| `pcap` | 18 | 14 | 9 | 6 | 6 | 1 | 54 |
| `stego` | 7 | 20 | 1 | 3 | 0 | 0 | 31 |
| `steganography` | 10 | 6 | 6 | 1 | 1 | 1 | 25 |
| `memorydump` | 1 | 0 | 1 | 15 | 2 | 0 | 19 |
| `network` | 7 | 3 | 1 | 4 | 3 | 1 | 19 |
| `binwalk` | 1 | 5 | 4 | 3 | 1 | 0 | 14 |
| `networking` | 6 | 2 | 1 | 1 | 4 | 0 | 14 |
| `pdf` | 2 | 4 | 3 | 2 | 1 | 0 | 12 |
| `powershell` | 2 | 3 | 2 | 2 | 2 | 1 | 12 |
| `memory_dump` | 8 | 1 | 2 | 0 | 0 | 0 | 11 |
| `python` | 4 | 3 | 2 | 0 | 2 | 0 | 11 |
| `strings` | 3 | 3 | 1 | 2 | 1 | 0 | 10 |
| `git` | 2 | 2 | 2 | 0 | 3 | 0 | 9 |
| `image` | 1 | 1 | 6 | 0 | 1 | 0 | 9 |
| `memory` | 5 | 2 | 0 | 0 | 2 | 0 | 9 |

## Overlap with rev, crypto, web and pwn

16 forensics challenges also count as rev, 12 as crypto, 8 as web and 3 as pwn (same definitions as the other summaries), for example DamCTF 2021's sneaky-script (`forensics`, `malware` and `rev`), Cyber Apocalypse 2021's Low Energy Crypto (`forensics`, `pcap` and `rsa`), NahamCon CTF 2023's Hidden Figures (`forensics` and `web`) and CyBRICS CTF 2020's Incident (`forensics`, `pwn` and `reverse`).

## What the numbers show

- **Forensics is about one in nine tagged challenges** (11.2%), the smallest of the five categories (web 21.0%, crypto 17.5%, pwn 14.7%, rev 12.7%).
- **Its share rose until 2024:** from 10.0% in 2020 and 2021 to 12.9% in 2022, 12.7% in 2023 and 15.2% in 2024, then back to 10.5% in 2025. Over the same years pwn fell (14.5% to 8.7%), rev fell (13.0% to 8.0%), web rose (19.2% to 36.7%) and crypto stayed between 16.5% and 18.9%.
- **Forensics writeups fall about as fast as writeups overall:** from 216 (2020) to 30 (2025), 86% fewer; all challenges with tagged writeups drop 87%.
- **One tag finds most of the category.** `forensics` is on 75.9% of the forensics challenges found through tags, like `crypto` for crypto; the rest come from other spellings (96) and from forensics tools and artifacts (84).
- **Packet captures lead.** Network traffic and packet captures are named in 155 forensics challenges (38.2% of those naming a family), then memory forensics (72), steganography inside forensics challenges (67) and file carving and file formats (48). Disk images, Windows artifacts and incident response are about 20 each.
- **Steganography changes the total.** 137 tagged challenges are steganography without a forensics keyword; counting them would raise forensics from 771 to 908 (13.2% of tagged challenges).
- **The hand review changes little.** It added 24 challenges, 3.2% on top of the 747 found through tags (web: 29, 2.1%; pwn: 13, 1.3%; crypto: 47, 4.1%; rev: 25, 2.9%).
- **Numbers after 2023 are small** (80 forensics challenges in 2024 and 30 in 2025, 48 and 9 of them naming a family), so read year-to-year shifts as indications rather than firm trends.

## Method

- **Forensics challenge:** a challenge whose tags include a forensics spelling (`forensics`, `forensic`, `digital-forensics`, `windows-forensics`, `dfir`, `incidentresponse`, `blueteam`, misspellings such as `fornsics`, ...) or a keyword used almost only in forensics: a capture, memory, disk or Windows artifact tool or format (wireshark, tshark, tcpdump, pcap, pcapng, volatility, memory dumps, autopsy, ftk imager, sleuthkit, usb, registry, windows timeline, amcache, oletools, carving, ...). The full list is in Appendix A. A challenge the tags miss is added only through the hand review below.
- **Generic words** such as `binwalk`, `exiftool`, `pdf`, `png`, `zip`, `powershell`, `malware`, `logs`, `network`, `memory`, `hashcat`, `keepass`, `audio` or `sstv` are not enough on their own; they only count towards families inside challenges already identified as forensics. Steganography tags (`steganography`, `stego`, `steghide`, `zsteg`, `lsb`, ...) are treated the same way.
- **Manual review of tagged challenges:** the 98 challenges found only through a forensics tool or artifact (no forensics spelling) were checked by hand against their writeup tags and their CTFtime task page; 14 were removed because the capture, dump or artifact is only one step inside another kind of challenge (Appendix B). Packet-capture tasks that an event files under misc, network or hardware were kept, since the capture analysis is the challenge.
- **Hand review:** the 268 tagged challenges outside the count that have only weak forensics hints (205) or a forensics word in the task name (80: forensics, pcap, memory, dump, logs, traffic, usb, incident, investigation, ...) were checked by hand, against their name and against the tags on their CTFtime task page (each event's task list, checked on 6 Nov 2026; these tags often differ from the writeup tags). 24 were added (Appendix C): those whose task page carries a forensics keyword (`forensics`, `forensic`, `dfir`, `incidentresponse`, `packet-analysis`, ...), and those whose name clearly shows a forensics challenge (Log Analysis). Only purely forensics challenges were added: none whose task page or writeup tags also show another category (steganography counts as another category here; `network` and `networking` do not, since traffic analysis is a forensics family), and none that already counts in another summary.
- **The forensics spellings are counted as given**, as `web`, `pwn`, `crypto` and `rev` were. 35 forensics-tagged challenges also carry another category and no other forensics keyword (e.g. NahamCon CTF 2023's Hidden Figures, `forensics` · `web`).
- **Year:** the year the CTF event started (UTC), from the Event start date column. **Tags first:** challenges are identified by their writeup tags; task names and task pages are used only in the reviews.

### Not counted

- **Steganography without a forensics keyword** (137 challenges; see "With steganography" above).
- **244 challenges from the hand review were left out.** For 131 of them the task page shows another category and no forensics keyword (web, misc, crypto, rev, OSINT, ...). Ten show forensics on their task page or in their name but also another category, or already count elsewhere: csictf 2020's Archenemy (writeup tagged stego), VULNCON CTF 2020's Pcaped (task page tagged misc), picoCTF 2021's Milkslap (task page tagged stego), S.H.E.L.L. CTF's Hidden inside 2 (writeup tagged steganography), Cyber Apocalypse 2021's Invitation (task page tagged reverse), HTB Business CTF 2022: Dirty Money's MBCoin (writeup tagged reverse), NahamCon CTF 2022's USB Drive (task page tagged malware), TCP1P CTF 2024: Exploring Nusantara's Digital Realm's [Forensics] Skibidi Format (counted as crypto through aes and gcm), justCTF 2024 teaser's Budget SoC (task page tagged misc), justCTF 2024 teaser's Baby SoC (task page tagged misc). The others have nothing that settles the category, such as MetaCTF CyberGames 2021's My Logs Know What You Did (`base64` · `powershell`) or RaziCTF 2020's Industrial network (`modbus` · `rtu` · ...).
- **Challenges whose writeups have no tags** (4,173) are outside the scope, even when the name shows a forensics challenge: 69 of them have a forensics word in the name; they were not reviewed.
- **Events that started on 31 Dec 2019** (BambooFox CTF, TetCTF 2020) fall outside the range by start date; they have no forensics challenges by these tags.

## Appendix A: Keywords counted

Numbers are 2020–2025 forensics challenges carrying the keyword. Keywords marked \* only count inside challenges already identified as forensics.

| Group | Keywords |
| --- | --- |
| Forensics category (spellings) | `forensics` (567), `forensic` (129), `blueteam` (8), `dfir` (3), `digital-forensics` (3), `forensic+crypto` (3), `incidentresponse` (3), `fornsics` (2), `windows-forensics-analysis` (2), `browser-forensics` (1), `foren` (1), `forenc` (1), `forenciss` (1), `foreniscs` (1), `forens` (1), `incident` (1), `windows-forensics` (1), `windowsforensics` (1) |
| Network traffic & packet captures (pcap, Wireshark) | `wireshark` (84), `pcap` (54), `network`\* (19), `networking`\* (14), `pcapng` (8), `ftp`\* (7), `traffic-analysis` (7), `scapy`\* (6), `icmp`\* (4), `dns`\* (3), `http`\* (3), `packet-analysis` (3), `traffic`\* (3), `packet`\* (2), `tcpdump` (2), `c2traffic`\* (1), `exfiltration`\* (1), `modbus`\* (1), `network_security`\* (1), `networkminer` (1), `packet-capture` (1), `packets`\* (1), `pacp` (1), `pyshark` (1), `sniffing`\* (1), `tcp`\* (1), `tshark` (1), `udp`\* (1) |
| Memory forensics (Volatility, memory dumps) | `volatility` (67), `memorydump` (19), `memory_dump` (11), `memory`\* (9), `memdump` (2), `dumpchk` (1), `lsass`\* (1), `mimikatz`\* (1), `vmem` (1) |
| Steganography (LSB, steghide, spectrograms) | `stego`\* (31), `steganography`\* (25), `steghide`\* (4), `lsb`\* (3), `spectrogram`\* (3), `stegano`\* (3), `stegnography`\* (3), `stenography`\* (3), `deepsound`\* (2), `steg`\* (2), `stegno`\* (2), `stegseek`\* (1), `stegsolve`\* (1), `wav-steg`\* (1), `whitespace`\* (1), `zsteg`\* (1) |
| File carving & file formats (binwalk, broken PNG/PDF/ZIP) | `binwalk`\* (14), `pdf`\* (12), `png`\* (7), `gif`\* (3), `hexedit`\* (3), `zip`\* (3), `7z`\* (2), `corrupt`\* (2), `hex`\* (2), `bmp`\* (1), `carving` (1), `corrupted`\* (1), `file_signature`\* (1), `file_structure`\* (1), `hexeditor`\* (1), `jpeg`\* (1), `jpg`\* (1), `pdfstreamdumper`\* (1), `repairing`\* (1), `tar`\* (1) |
| Incident response & malware (maldocs, PowerShell, phishing) | `powershell`\* (12), `malware`\* (6), `macro`\* (4), `obfuscation`\* (3), `vba`\* (3), `docm`\* (2), `persistence`\* (2), `deobfuscation`\* (1), `macros`\* (1), `microsoft-office`\* (1), `obfuscated`\* (1), `oletools` (1), `phishing`\* (1) |
| Windows artifacts & event logs (registry, EVTX, timeline) | `windows`\* (7), `registry` (6), `logs`\* (5), `log`\* (3), `amcache` (1), `amcacheparser` (1), `prefetch`\* (1), `windows-timeline` (1) |
| Disk images & file systems (Autopsy, FTK, file recovery) | `autopsy` (8), `ftkimager` (4), `disk` (3), `filesystem`\* (3), `sleuthkit` (2), `bitlocker`\* (1), `disk-imaging` (1), `file-recovery` (1), `truecrypt`\* (1), `vhd`\* (1) |
| Browser, email, Git & database artifacts | `git`\* (9), `docker`\* (3), `email`\* (3), `emails`\* (1), `firefox`\* (1), `firefox-history`\* (1), `sqlite`\* (1) |
| Password & archive cracking (John, hashcat, KeePass) | `hashcat`\* (5), `password-cracking`\* (5), `keepass`\* (3), `cracking`\* (2), `hash_cracking`\* (2), `john`\* (2), `johntheripper`\* (2), `fcrackzip`\* (1), `pdfcrack`\* (1) |
| Audio, radio & signals (SSTV, Morse, SDR) | `audio`\* (6), `radio`\* (4), `sstv`\* (4), `dtmf`\* (2), `wav`\* (2), `morse`\* (1), `qsstv`\* (1) |
| USB, keyboard & Bluetooth captures | `usb` (9), `bluetooth`\* (4), `keyboard`\* (2), `keylogger`\* (2), `usb-keyboard` (2), `hid`\* (1), `mouse`\* (1), `usb-exfiltration` (1) |
| Metadata (EXIF, exiftool) | `exiftool`\* (6), `exif`\* (3), `metadata`\* (1) |
| Mobile & cloud (Android, iOS, cloud) | `android`\* (4), `mobile`\* (1) |
| Generic words (only inside forensics challenges) | `python` (11), `strings` (10), `image` (9), `base64` (6), `images` (3), `linux` (2), `qrcode` (2), `analysis` (1), `artifact` (1), `encryption` (1), `files` (1), `qr` (1), `video` (1) |

## Appendix B: Challenges removed after manual review

| Year | Event | Task | Tags | Why it is not a forensics challenge |
| --- | --- | --- | --- | --- |
| 2025 | PwnMe CTF Quals 2025 | Mafia at the end 1 | pcap · solidity · web3 | blockchain (task page tagged misc · network · web3; writeup tagged solidity · web3) |
| 2023 | CyberSecurityRumble Quals | Backup | cryptography · misc · wireshark | crypto (task page tagged misc · crypto; writeup tagged cryptography) |
| 2023 | UTCTF 2023 | Calculator | memdump · proc · procfs | Python jail (task page tagged python-jail · web · pyjail); the memory is read through /proc |
| 2022 | Square CTF 2022 | Hard Copy | crypto · factoring · go · rsa · tls · wireshark · z3 | crypto: RSA factoring (writeup tagged crypto · rsa · factoring · z3); the TLS capture is one step |
| 2021 | BuckeyeCTF 2021 | replay | misc · pwn · pwntools · traffic · wireshark | pwn (task page tagged misc · pwn · wireshark); the capture is one step |
| 2021 | Cyber Santa is Coming to Town | Intercept | asm · assembly · crypto · pcap · reversing | reversing (task page tagged asm · reversing · pcap); the capture is one step |
| 2021 | TAMUctf 2021 | delfi | lfi · linux · memory_dump · rust · web | web: local file inclusion (writeup tagged web · lfi); the memory is read through it |
| 2021 | darkCON CTF | ezpz | android · memory_dump | Android app challenge (task page tagged android); the memory is dumped from the app |
| 2020 | CyberSecurityRumble CTF | EZExfil | misc · net · privesc · usb | privilege escalation and exfiltration task (task page tagged net · misc, writeup tagged privesc) |
| 2020 | DawgCTF 2020 | Free WiFi Part 1 | networking · pcap · web | web challenge (task page tagged web); the capture is one step |
| 2020 | DawgCTF 2020 | free wifi part 2 | jwt · networking · pcap · web | web challenge (task page tagged web; writeup tagged jwt) |
| 2020 | DawgCTF 2020 | Free WiFi Part 3 | networking · pcap · web | web challenge (task page tagged networking · web) |
| 2020 | DawgCTF 2020 | free wifi part 4 | cookies · hash · networking · pcap · web | web challenge (task page tagged web; writeup tagged cookies) |
| 2020 | HackTM CTF Quals 2020 | ananas | pcap · re · tshark · wireshark | reversing (task page tagged rev, writeup tagged re); the capture is one step |

## Appendix C: Challenges added by hand

Their writeup tags are too weak to count on their own, but their CTFtime task page or their name shows a purely forensics challenge. Task page tags are as listed on the event's task list.

| Year | Event | Task | Writeup tags | Task page tags | Why it was added |
| --- | --- | --- | --- | --- | --- |
| 2024 | bi0sCTF 2024 | Batman Investigation I - Like Father Like Son | azr43lkn1ght | incidentresponse · heap · windows · malware-analysis · azfr43lkn1ght · malwarenalaysis · windowsforensics · threathunting · mameoryforensics · stealer | task page tag |
| 2024 | bi0sCTF 2024 | Batman Investigation II - Gotham Underground Corruption | azr43lkn1ght | dfir · forensics · blockchain-forensics · malware-analysis · windows-forensics · incident-response · memory-forensics · password-recovery | task page tag |
| 2024 | bi0sCTF 2024 | Batman Investigation III - Th3 Sw0rd 0f Azr43l | azr43lkn1ght | incidentresponse · recovery · ransomware · windows · azr43lkn1ght · windowsforensics · threathunting · dfir · fileforensics · browserforensics · ransomware-investigation · memoryforensics · ransomware-analysis · malwarenalaysis | task page tag |
| 2023 | DanteCTF 2023 | Almost Perfect Remote Signing | aprs · radio | radio · forensic · forensics | task page tag |
| 2023 | HeroCTF v5 | dev.corp 1/4 | log | forensic | task page tag |
| 2023 | n00bzCTF 2023 | BeepBop | sstv | forensics | task page tag |
| 2022 | DCTF 2022 | Hidden Fox | firefox-history | forensics | task page tag |
| 2022 | DCTF 2022 | Secure Creds | lsass · mimikatz | forensics | task page tag |
| 2022 | KnightCTF 2022 | Let's Walk Together | binwalk | forensics · digital | task page tag |
| 2021 | DawgCTF 2021 | Photo Album | hash_cracking · hashcat · password-cracking | forensics | task page tag |
| 2021 | Digital Overdose 2021 Autumn CTF | Log Analysis - Part 1 - Ingress | access · awk · grep · iis · logs | logs | "Log Analysis" in the name |
| 2021 | Digital Overdose 2021 Autumn CTF | Log Analysis - Part 2 - Investigation | access · awk · grep · iis · logs | logs | "Log Analysis" in the name |
| 2021 | Digital Overdose 2021 Autumn CTF | Log Analysis - Part 3 - Backup Policy | access · awk · grep · iis · logs | logs | "Log Analysis" in the name |
| 2021 | HTB Business CTF 2021 | DFIR | encryption · obfuscation · powershell · python | vm · powershell · forensics · encryption · python · keylogger | task page tag |
| 2021 | HTB Business CTF 2021 | badRansomware | macro · powershell · vba | forensics | task page tag |
| 2021 | S.H.E.L.L. CTF | Cold Compress Inside | binwalk · strings | forensics | task page tag |
| 2021 | picoCTF 2021 | tunn3l v1s10n | bitmap · bmp · corrupt · repairing | forensics | task page tag |
| 2020 | Affinity CTF Lite (Junior/Beginner) | wholeisbetter | pdf | forensics | task page tag |
| 2020 | DarkCTF | Wolfie's Password | john | forensics | task page tag |
| 2020 | RaziCTF 2020 | Can you see thorough the crowd? | hexeditor | forensics | task page tag |
| 2020 | Shakti CTF 2020 | Shark on Wire | network | forensic | task page tag |
| 2020 | Syskron Security CTF 2020 | DoS attack | analysis · packet | packet-analysis | task page tag |
| 2020 | Syskron Security CTF 2020 | Redacted news | image-analysis · imagemagick · png | forensics | task page tag |
| 2020 | rgbCTF 2020 | Alien Transmission | radio · sstv | forensics | task page tag |
