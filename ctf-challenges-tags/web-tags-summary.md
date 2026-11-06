# Web challenge tags on CTFtime writeups, 2020–2025

**1,410 different web challenges** come from CTFs held in 2020–2025, each counted once. 1,155 carry the `web` tag and 255 more were found only through other web keywords (xss, sqli, ssti, xxe, ...). That is 20.6% of the 6,859 challenges that have tags.

## Data

- **Source:** every writeup listed on [ctftime.org/writeups](https://ctftime.org/writeups) (all 1,309 pages, 39,253 writeups), collected on 30 Oct 2026, 13:31–13:45 UTC; event dates from CTFtime's [events API](https://ctftime.org/api/).
- **File:** [`ctftime_writeups_tasks.xlsx`](ctftime_writeups_tasks.xlsx), one tab (`Tasks`) with the columns Event, Task, Tags and Event start date: 19,494 challenges, all years.
- **One row per challenge:** writeups of the same task (same CTF, same task name ignoring case) are merged, and their tags combined, so a task solved by several teams counts once.
- **Scope of this summary:** challenges whose event started in 2020–2025 (UTC): 11,032 challenges, 6,859 of them with at least one tag.

## Web challenges per year

| Year | Challenges | With tags | Tagged `web` | Other web keywords only | **Web challenges** | Share of tagged | Share of all |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2020 | 3,355 | 2,170 | 329 | 81 | **410** | 18.9% | 12.2% |
| 2021 | 2,995 | 1,825 | 298 | 60 | **358** | 19.6% | 12.0% |
| 2022 | 1,749 | 1,025 | 162 | 37 | **199** | 19.4% | 11.4% |
| 2023 | 1,559 | 1,028 | 178 | 37 | **215** | 20.9% | 13.8% |
| 2024 | 896 | 525 | 96 | 28 | **124** | 23.6% | 13.8% |
| 2025 | 478 | 286 | 92 | 12 | **104** | 36.4% | 21.8% |
| **Total** | **11,032** | **6,859** | **1,155** | **255** | **1,410** | **20.6%** | **12.8%** |

A challenge tagged `web` and also, say, `xss` and `sqli` is counted once. Counting every keyword hit separately would give 2,444 instead of 1,410.

### The keyword `web`

- **Exactly `web`:** 1,155 challenges.
- **Other spellings:** 17 more challenges use `websec`, `web-exploitation`, `web_exploitation`, `webexploitation`, `webexp`, `ssrf#web` or `web_recon_1` instead (included in "Other web keywords only").
- **Left out:** tags that contain "web" but are not web exploitation: `web3` (7), `web3py` (3), `webassembly` (2), `webgl` (1), `webgpu` (1), `webcam` (2), `build.data.unityweb` (1) (blockchain, WebAssembly reversing, graphics, hardware, Unity game files). Numbers are challenges with no other web keyword.

## By attack type

Each row counts a challenge once, even if it carries several spellings (`sqli` and `sqlinjection`, say). A challenge can be in several rows, so rows add up to more than the total. 670 of the 1,410 web challenges name at least one attack type; the other 740 are tagged only `web` or with a technology.

| Attack type | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| XSS | 35 | 32 | 20 | 26 | 16 | 13 | 142 |
| SQL injection | 42 | 35 | 11 | 19 | 10 | 7 | 124 |
| Command injection / RCE | 21 | 29 | 18 | 12 | 5 | 9 | 94 |
| Auth, sessions & tokens (JWT, cookies, OAuth, IDOR) | 20 | 17 | 17 | 14 | 12 | 7 | 87 |
| LFI / path traversal | 25 | 22 | 13 | 12 | 7 | 4 | 83 |
| SSTI (template injection) | 11 | 12 | 11 | 12 | 8 | 7 | 61 |
| Other client-side (CSP bypass, XS-Leaks, DOM clobbering, CSS injection, postMessage) | 8 | 14 | 1 | 16 | 11 | 7 | 57 |
| HTTP tricks (smuggling, cache poisoning, CRLF, headers, WAF bypass) | 8 | 13 | 4 | 11 | 5 | 4 | 45 |
| SSRF | 9 | 17 | 8 | 2 | 2 | 1 | 39 |
| XXE / XML / XPath injection | 9 | 11 | 5 | 2 | 3 | 1 | 31 |
| CSRF / CORS / open redirect | 5 | 9 | 3 | 4 | 2 | 0 | 23 |
| Prototype pollution | 5 | 6 | 2 | 2 | 3 | 1 | 19 |
| Deserialization | 10 | 6 | 1 | 1 | 0 | 1 | 19 |
| NoSQL injection | 3 | 7 | 0 | 3 | 1 | 1 | 15 |
| File upload | 0 | 5 | 4 | 1 | 2 | 0 | 12 |
| **Name at least one type** | **172** | **185** | **90** | **99** | **69** | **55** | **670** |

Share of the web challenges that name an attack type:

| Attack type | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
| --- | --- | --- | --- | --- | --- | --- |
| XSS | 20.3% | 17.3% | 22.2% | 26.3% | 23.2% | 23.6% |
| SQL injection | 24.4% | 18.9% | 12.2% | 19.2% | 14.5% | 12.7% |
| Command injection / RCE | 12.2% | 15.7% | 20.0% | 12.1% | 7.2% | 16.4% |
| Auth, sessions & tokens (JWT, cookies, OAuth, IDOR) | 11.6% | 9.2% | 18.9% | 14.1% | 17.4% | 12.7% |
| LFI / path traversal | 14.5% | 11.9% | 14.4% | 12.1% | 10.1% | 7.3% |
| SSTI (template injection) | 6.4% | 6.5% | 12.2% | 12.1% | 11.6% | 12.7% |
| Other client-side (CSP bypass, XS-Leaks, DOM clobbering, CSS injection, postMessage) | 4.7% | 7.6% | 1.1% | 16.2% | 15.9% | 12.7% |
| HTTP tricks (smuggling, cache poisoning, CRLF, headers, WAF bypass) | 4.7% | 7.0% | 4.4% | 11.1% | 7.2% | 7.3% |

## Most used keywords in web challenges

Individual tags, excluding `web`. A challenge tagged both `sqli` and `sqlinjection` is in both rows here but counted once in the SQL injection row above.

| Keyword | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `xss` | 35 | 32 | 19 | 25 | 16 | 10 | 137 |
| `php` | 32 | 33 | 13 | 13 | 2 | 7 | 100 |
| `sqli` | 33 | 29 | 7 | 9 | 8 | 4 | 90 |
| `rce` | 15 | 17 | 13 | 7 | 2 | 7 | 61 |
| `ssti` | 8 | 12 | 11 | 10 | 7 | 7 | 55 |
| `lfi` | 18 | 20 | 7 | 6 | 3 | 1 | 55 |
| `sqlinjection` | 16 | 10 | 5 | 10 | 5 | 1 | 47 |
| `javascript` | 19 | 4 | 5 | 7 | 6 | 1 | 42 |
| `flask` | 15 | 5 | 6 | 8 | 0 | 6 | 40 |
| `ssrf` | 9 | 16 | 6 | 1 | 2 | 1 | 35 |
| `jwt` | 9 | 6 | 6 | 6 | 7 | 1 | 35 |
| `xxe` | 9 | 9 | 4 | 2 | 2 | 1 | 27 |
| `nodejs` | 4 | 5 | 5 | 4 | 2 | 1 | 21 |
| `csrf` | 5 | 8 | 3 | 3 | 1 | 0 | 20 |
| `graphql` | 4 | 7 | 0 | 6 | 1 | 1 | 19 |
| `sql-injection` | 5 | 6 | 1 | 3 | 2 | 2 | 19 |
| `prototype-pollution` | 5 | 5 | 2 | 2 | 3 | 1 | 18 |

`sql injection` (with a space) does not appear on any 2020–2025 challenge; SQL injection is written as `sqli`, `sqlinjection`, `sql-injection`, `sql_injection`, `blindsqli`, `sqlinj` or `sqlmap`.

## Technology

| Technology | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| PHP | 35 | 41 | 13 | 16 | 2 | 7 | 114 |
| JavaScript / Node.js | 33 | 25 | 16 | 18 | 15 | 4 | 111 |
| Python | 35 | 18 | 13 | 18 | 9 | 13 | 106 |
| Java | 6 | 4 | 3 | 1 | 3 | 0 | 17 |

## What the numbers show

- **Web is about one in five tagged challenges.** It held at 18.9%–20.9% in 2020–2023, then 23.6% in 2024 and 36.4% in 2025; 2025 has only 286 tagged challenges, so that jump rests on a small base.
- **Raw counts fall because there are fewer writeups, not fewer web challenges.** Web challenges drop from 410 (2020) to 104 (2025), but all challenges with writeups drop from 3,355 to 478.
- **SQL injection led in 2020–2021; XSS has led every year since 2022.** SQL injection fell from 24% of the web challenges that name an attack type (2020) to 13% (2025); XSS stayed between 17% and 26%.
- **Browser-side attacks and SSTI are growing.** Client-side attacks other than XSS went from 5% (2020) to 13–16% (2023–2025); SSTI doubled, from about 6% (2020–2021) to about 12% (2022–2025).
- **SSRF, XXE and deserialization are fading.** SSRF peaked at 17 challenges in 2021 and has been 1–2 a year since 2023; XXE fell from 11 (2021) to 1 (2025), and deserialization barely appears after 2021.
- **Technology:** PHP (114 challenges), JavaScript/Node.js (111) and Python (106) are about equally common; Java appears in 17.
- Numbers after 2022 are small, so read year-to-year changes as broad trends.

## Method

- **Web challenge:** a challenge whose tags include `web`, another spelling of it, or a web keyword: an attack type (xss, sqli, ssti, xxe, ssrf, lfi, csrf, jwt, ...), a web framework or server (flask, php, node.js, graphql, nginx, ...), a web tool (burpsuite, dirbuster, ...) or a web application with a known CVE. The full list is in Appendix A.
- **Generic words** such as `javascript`, `sql`, `rce`, `python` or `command_injection` are not enough on their own; they only count towards attack types and technologies inside challenges already identified as web.
- **Manual review:** 70 borderline challenges (a web keyword next to another category, or only a weak web keyword) were checked by hand; 17 were removed because the web-looking tag describes a technology or tool rather than a web attack (Appendix B). Challenges that name a real web attack stay in even when another category is also tagged.
- **Year:** the year the CTF event started (UTC), from the Event start date column.
- **Tags only:** task names are not used. Tags are free-form labels added by writeup authors, so many challenges have none.

### Not counted

- **Events that started on 31 Dec 2019** (BambooFox CTF, TetCTF 2020) fall outside the range by start date; they have 5 web challenges.
- **M\*CTF 2023 Junior Quals** has no start date on CTFtime (its event page no longer exists), so its 2 challenges are left out, including one web challenge (Catalog, `ejs` · `ssti`).
- **52 challenges have "web" in the task name but no web tags** (38 have no tags at all).

## Appendix A: Keywords counted

Numbers are 2020–2025 web challenges carrying the keyword. Keywords marked \* only count inside challenges already identified as web.

| Group | Keywords |
| --- | --- |
| XSS | `xss` (137), `mxss` (3), `stored-xss` (3), `crosssitescripting` (2), `blind-xss` (1), `reflected-xss` (1), `selfxss` (1), `xssauditor` (1) |
| SQL injection | `sqli` (90), `sqlinjection` (47), `sql-injection` (19), `blindsqli` (4), `sqlinj` (4), `sqlmap` (4), `blind-sql-injection` (2), `blindsql` (2), `sql_injection` (2), `blind-sqli` (1), `bsqli` (1), `md5-sqli` (1) |
| Command injection / RCE | `rce`\* (61), `command_injection`\* (17), `command-injection`\* (6), `log4j` (5), `code-injection`\* (3), `escapeshellcmd` (3), `php-comand-injection` (3), `webshell` (2), `argument_injection`\* (1), `commandinjection`\* (1), `oscommandinjection`\* (1), `php-shell` (1), `shellshock` (1) |
| Auth, sessions & tokens (JWT, cookies, OAuth, IDOR) | `jwt` (35), `cookie` (17), `cookies` (15), `idor` (8), `flask-session` (5), `cookie-forgery` (2), `oauth` (2), `phpsession` (2), `2fa`\* (1), `broken_access_control` (1), `cookie-tossing` (1), `hs256`\* (1), `jwks-spoofing` (1), `mass-assignment` (1), `oauth2` (1), `oauth2.0` (1), `rs256`\* (1), `session-hijacking` (1), `sso`\* (1), `webauthn` (1) |
| LFI / path traversal | `lfi` (55), `path-traversal` (13), `directory-traversal` (7), `local_file_inclusion` (5), `pathtraversal` (5), `file_path_traversal` (3), `directorylisting` (2), `log_poisoning` (2), `inclusion`\* (1) |
| SSTI (template injection) | `ssti` (55), `template-injection` (8), `server-side-template-injection` (2), `spel` (1) |
| Other client-side (CSP bypass, XS-Leaks, DOM clobbering, CSS injection, postMessage) | `csp` (11), `csp-bypass` (11), `client-side` (8), `dom-clobbering` (8), `cssinjection` (7), `xsleaks` (6), `dompurify` (3), `jsonp` (3), `puppeteer` (2), `sop`\* (2), `xs-leak` (2), `bfcache` (1), `clobbering` (1), `content-injection` (1), `content-spoofing` (1), `cross-frame-scripting` (1), `dom-purify` (1), `mime-sniffing` (1), `postmessage` (1), `rpo` (1), `shadowdom` (1), `xhr` (1), `xs-search` (1) |
| HTTP tricks (smuggling, cache poisoning, CRLF, headers, WAF bypass) | `waf-bypass` (11), `headers` (8), `cache-poisoning` (7), `waf` (6), `crlf` (3), `http_request_smuggling` (3), `crlf-injection` (2), `json_interoperability` (2), `cache-poisning` (1), `cache-probing` (1), `crlfinjection` (1), `desync`\* (1), `esi`\* (1), `hostheaderinjection` (1), `http-desync-attack` (1), `http-headers` (1), `http-smuggling` (1), `referer` (1), `request-smuggling` (1), `request-splitting` (1), `smuggling` (1), `x-forwarded-for` (1) |
| SSRF | `ssrf` (35), `dnsrebinding` (3), `gopher` (3), `cve-2024-34351` (1), `imdsv2` (1) |
| XXE / XML / XPath injection | `xxe` (27), `xml-injection` (3), `xpath` (2), `blind-xxe` (1), `xmlexternalentity` (1), `xxeinjection` (1) |
| CSRF / CORS / open redirect | `csrf` (20), `cors` (1), `cross-site-request-forgery` (1), `open-redirect` (1), `xsrf` (1) |
| Prototype pollution | `prototype-pollution` (18), `prototypepollution` (2), `class-pollution` (1) |
| Deserialization | `deserialization`\* (7), `pickle`\* (7), `deserialize`\* (3), `phar` (3), `java-serialization`\* (2), `unserialize`\* (2), `ysoserial` (2), `pickle-deserialization`\* (1) |
| NoSQL injection | `nosql` (9), `nosqli` (8), `nosql-injection` (7), `blindnosqlinjection` (2), `nosql_injection` (2), `no-sql-injection` (1), `nosqlinjection` (1) |
| File upload | `file_upload` (6), `zip-slip` (3), `fileupload` (2), `upload` (2) |
| Web category (other spelling) | `websec` (17), `webexploitation` (7), `web_exploitation` (5), `web-exploitation` (3), `ssrf#web` (1), `web_recon_1` (1), `webexp` (1) |
| PHP web | `php` (100), `type-juggling` (4), `preg_replace` (2), `disable_functions` (1), `dompdf-rce` (1), `magic-hashes` (1), `php-wrappers` (1), `preg_match` (1), `strip_tags` (1) |
| Web frameworks, servers & template engines | `flask` (40), `nodejs` (21), `graphql` (19), `node.js` (14), `nginx` (12), `jinja2` (9), `werkzeug` (6), `jinja` (5), `apache` (4), `cgi` (4), `express` (4), `htaccess` (4), `nextjs` (4), `caddy` (3), `socket.io` (3), `spring` (3), `apache2` (2), `django` (2), `fastapi` (2), `laravel` (2), `tomcat` (2), `tornado` (2), `dustjs` (1), `ejs` (1), `ghostcat` (1), `handlebars` (1), `hhvm` (1), `htpasswd` (1), `mod_rewrite` (1), `nostromo` (1), `symfony` (1), `thinkphp` (1), `thymeleaf` (1), `varnish` (1), `wsgi` (1) |
| Web applications (CVE targets) | `jenkins` (3), `airflow` (1), `cve-2019-16278` (1), `cve-2020-1938` (1), `cve-2021-35464` (1), `cve-2024-33883` (1), `horizontcms` (1), `jolokia` (1), `openam` (1), `rocket-chat` (1), `youtrack` (1), `zabbix` (1) |
| Web testing tools | `burpsuite` (15), `burp` (2), `inspect-element` (2), `beeceptor` (1), `dirbuster` (1), `gittools` (1), `wappalyzer` (1) |
| Web pages, robots.txt & WebSockets | `html` (8), `robots.txt` (8), `robots` (7), `websocket` (5), `websockets` (5), `web-source-code` (1) |

## Appendix B: Challenges removed after manual review

| Year | Event | Task | Tags | Why it is not a web challenge |
| --- | --- | --- | --- | --- |
| 2025 | Platypwn 2025 | Pool Party | heap · linux · nginx · pwn | nginx heap exploitation (pwn) |
| 2024 | UofTCTF 2024 | Baby JS Blacklist | babel · jail · jailjavascript · javascript · js · node.js | Node.js jail (misc) |
| 2022 | VishwaCTF 2022 | I don't need sleep | discord · inspect-element · miscellaneous | inspect element on Discord (misc) |
| 2021 | DamCTF 2021 | cookie-monster | 32-bit · bof · canary · cookie · fmt · format-string · pwn · ret2libc | 'cookie' is a stack canary (pwn) |
| 2021 | H@cktivityCon 2021 CTF | Phonetic | analysis · deobfuscation · malware · php | PHP malware deobfuscation |
| 2021 | H@cktivityCon 2021 CTF | Read The Rules | html · inspect · warmup | flag in the rules page source (warm-up) |
| 2021 | Midnight Sun CTF 2021 Quals | Labyrevnt | algorithms · bfs · coding · php · rev | PHP reversing / algorithms |
| 2021 | N1CTF 2021 | ctfhub2 | php · pwn | PHP interpreter pwn |
| 2021 | TAMUctf 2021 | Seventh Core of Hell | coredump · flask · pwn | Flask app core dump (pwn) |
| 2020 | ASIS CTF Quals 2020 | Adventure | accept-ranges · forensics | HTTP range responses in forensics |
| 2020 | Affinity CTF Lite (Junior/Beginner) | Lost Head | forensics · http-header · wireshark | HTTP header in a pcap (forensics) |
| 2020 | BatPwn - BSides Ahmedabad CTF 2020 | Scripting Fassst | misc · websocket | WebSocket only carries a scripting task |
| 2020 | DefCamp CTF 2020 Online | Hunting into the wild | forensics · kibana | Kibana log analysis (forensics) |
| 2020 | RaziCTF 2020 | CTF Coin | android · burp · burpsuite · frida | Android app, Burp only to watch traffic |
| 2020 | RaziCTF 2020 | Crypto PHP | bitcoin · php · reverse-engineering | PHP reversing |
| 2020 | RaziCTF 2020 | Friends | android · burp · burpsuite · revesing | Android app, Burp only to watch traffic |
| 2020 | redpwnCTF 2020 | CaaSINO | javascript · misc · node · node.js · pwn | Node.js sandbox escape (misc) |
