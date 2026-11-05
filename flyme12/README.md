# Flyme 12 Russian translation

Base firmware: **Flyme 12.6.0.0A** (Meizu 21 Pro, CN build, Android 16).

Every app folder holds:

- `res/values/` — source strings of the app (as shipped in the firmware);
- `res/values-ru/` — the Russian translation;
- `res/values-en/` — English fixes: only strings whose English is missing or poor in the app;
- `status.tsv` — where every Russian string comes from;
- `status_en.tsv` — English strings this repository adds (`new`), corrects (`fix`) or still lacks (`todo`);
- `overlay.json` — target package and app version; `mod_required` when an overlay is not enough.

## Origins (`status.tsv`)

| Origin | Meaning |
| ------ | ------ |
| `own` | Flyme 9 translation from this repository, same source text |
| `own_check` | Flyme 9 translation matched by name only (source text changed or unknown). Needs a check |
| `apk` | Russian already shipped in the app (Meizu or AOSP). Partly machine-made, needs a check |
| `new` | Translated anew for Flyme 12 |
| `todo` | Not translated yet |
| `unused` | Not translated; the app never references the string |
| `skip` | Nothing to translate (numbers, symbols) |

When a string is checked or fixed, its origin becomes `own`.

## English

Most strings keep the English shipped in the app (Meizu or AOSP). `status_en.tsv` lists only
the exceptions: `new` — the app had Chinese and no English; `fix` — Meizu's English was wrong;
`todo` — Chinese with no English, not done yet.

## Mod required (Обязательная модификация)

Apps marked **MOD** show less than ~90% of their text from string resources: the rest comes from
the server or is written in code or layouts. An overlay translates only the resources, so a full
translation of these apps needs a modified app. Reasons are listed under the table.

## State

Translated = `own` + `own_check` + `apk` + `new` out of everything except `unused` and `skip`.

| APP | VERSION | TRANSLATED | OWN | CHECK | APK | NEW | TODO | UNUSED | EN NEW | EN FIX | EN TODO |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| AlarmClock | 12.0.46 | 75% | 353 | 0 | 106 | 8 | 151 | 50 | 0 | 0 | 0 |
| AliveWallPaper | 13.0.5 | 100% | 0 | 0 | 6 | 39 | 0 | 7 | 1 | 0 | 0 |
| AlphaMe | 12.0.19 | 59% | 12 | 0 | 141 | 47 | 135 | 62 | 0 | 0 | 0 |
| AppCenter | 12.5.1 | 27% | 256 | 2 | 62 | 0 | 850 | 49 | 0 | 0 | 0 |
| Assistant | 13.0.6 | 39% | 397 | 9 | 17 | 1 | 643 | 57 | 0 | 0 | 0 |
| Browser | 12.9.1 | 55% | 506 | 6 | 2538 | 0 | 2435 | 379 | 0 | 0 | 0 |
| Calculator | 12.0.17 | 74% | 388 | 0 | 96 | 9 | 173 | 5 | 0 | 0 | 0 |
| Calendar | 19.3.3 | 51% | 742 | 17 | 34 | 0 | 753 | 70 | 0 | 0 | 0 |
| Camera | 12.7.2 | 100% | 532 | 13 | 67 | 65 | 0 | 16 | 1 | 2 | 0 |
| ConnectivitySettings | 12.15.000 | 100% | 1849 | 0 | 529 | 225 | 0 | 124 | 0 | 6 | 0 |
| CustomizeCenter | 12.5.0 | 69% | 751 | 21 | 13 | 3 | 343 | 28 | 0 | 0 | 0 |
| DataMigration | 12.1.1 | 67% | 742 | 37 | 80 | 0 | 417 | 212 | 0 | 0 | 0 |
| Dialer | 8.2.6 | 100% | 1128 | 10 | 2 | 360 | 0 | 26 | 64 | 45 | 0 |
| Email | 12.1.53 | 88% | 867 | 0 | 88 | 11 | 129 | 93 | 0 | 0 | 0 |
| FileManager | 12.0.21 | 75% | 649 | 0 | 113 | 16 | 254 | 36 | 0 | 0 | 0 |
| FlymeLauncher | 13.0.0 | 100% | 468 | 19 | 239 | 188 | 0 | 30 | 45 | 13 | 0 |
| FlymeMusic | 12.2.0 | 18% | 318 | 3 | 48 | 3 | 1607 | 240 | 0 | 0 | 0 |
| FlymeSoundRecorder | 12.3.7 | 80% | 355 | 7 | 184 | 6 | 133 | 3 | 0 | 0 | 0 |
| framework-res | 16 | 100% | 1320 | 95 | 1275 | 312 | 0 | 0 | 65 | 11 | 0 |
| Gallery | 12.7.3 | 100% | 1309 | 0 | 335 | 510 | 0 | 68 | 42 | 52 | 0 |
| GameCenter | 12.3.0 | 65% | 1062 | 16 | 3 | 3 | 570 | 151 | 0 | 0 | 0 |
| InCallUI | 14.01.07 | 100% | 188 | 7 | 39 | 24 | 0 | 3 | 0 | 0 | 0 |
| mCareNew | 8.0.0 | 42% | 184 | 2 | 71 | 0 | 346 | 28 | 0 | 0 | 0 |
| Mms | 12.3.4 | 100% | 867 | 20 | 0 | 410 | 0 | 225 | 74 | 16 | 0 |
| MusicFX | 5.0.0 | 100% | 211 | 0 | 3 | 0 | 0 | 5 | 0 | 0 | 0 |
| MzAccount | 12.0.14 | 76% | 258 | 4 | 99 | 1 | 111 | 24 | 0 | 0 | 0 |
| MzBatteryManager | 12.0.24 | 100% | 253 | 0 | 5 | 132 | 0 | 76 | 0 | 0 | 0 |
| MzSecurity | 12.1.48 | 100% | 1267 | 0 | 30 | 543 | 0 | 57 | 101 | 140 | 0 |
| MzSetupWizard | 12.0.25 | 47% | 0 | 256 | 66 | 0 | 358 | 66 | 0 | 0 | 0 |
| MzShare | 6.1.14 | 85% | 471 | 5 | 6 | 12 | 87 | 69 | 0 | 0 | 0 |
| MzUpdate | 12.0.15 | 81% | 651 | 13 | 36 | 2 | 159 | 1 | 0 | 0 | 0 |
| NativeLockScreen | 12.2.2 | 100% | 0 | 0 | 154 | 277 | 0 | 35 | 85 | 16 | 0 |
| NetAdmin | 11.0.3 | 100% | 310 | 0 | 5 | 29 | 0 | 42 | 0 | 0 | 0 |
| NotePaper | 12.0.68 | 81% | 499 | 9 | 405 | 2 | 201 | 28 | 0 | 0 | 0 |
| PackageInstaller | 16 | 100% | 312 | 0 | 108 | 136 | 0 | 45 | 31 | 5 | 0 |
| Pedometer | 12.0.13 | 73% | 403 | 8 | 34 | 26 | 172 | 55 | 0 | 0 | 0 |
| Picker | 12.2.34 | 56% | 304 | 4 | 4 | 3 | 247 | 78 | 0 | 0 | 0 |
| SDKStage | 5.0.01 | 60% | 128 | 0 | 9 | 0 | 88 | 11 | 0 | 0 | 0 |
| Settings | 12.1.0 | 100% | 4521 | 435 | 4377 | 500 | 0 | 158 | 9 | 29 | 0 |
| Suggestion | 12.5.10 | 15% | 89 | 2 | 0 | 0 | 512 | 3 | 0 | 0 | 0 |
| SystemUI | 16.26.06.25_base | 100% | 1771 | 62 | 1911 | 129 | 0 | 171 | 3 | 0 | 0 |
| SystemUIEditor | 3.5.45 | 100% | 0 | 0 | 142 | 212 | 0 | 105 | 10 | 34 | 0 |
| SystemUIEx | 12.3.14 | 100% | 267 | 7 | 40 | 22 | 0 | 65 | 0 | 0 | 0 |
| SystemUITools | 13.1.2 | 100% | 314 | 5 | 120 | 213 | 0 | 16 | 27 | 13 | 0 |
| ToolBox | 12.0.15 | 84% | 367 | 0 | 94 | 13 | 88 | 51 | 0 | 0 | 0 |
| Video | 17.23.0 | 52% | 263 | 0 | 26 | 4 | 266 | 29 | 0 | 0 | 0 |
| VoiceAssistant **MOD** | 12.1.46 | 39% | 497 | 8 | 0 | 217 | 1120 | 234 | 0 | 0 | 0 |
| WallpaperSetting | 3.2.0 | 100% | 0 | 0 | 20 | 142 | 0 | 17 | 0 | 16 | 0 |
| Weather **MOD** | 54.3.60 | 100% | 459 | 0 | 86 | 483 | 0 | 61 | 99 | 102 | 0 |
| **Total** | | 79% | 28858 | 1102 | 13866 | 5338 | 12348 | 3464 | 657 | 500 | 0 |

### Why a modification is required

- **VoiceAssistant**: speech recognition and the assistant's answers are Chinese-only (server side); about 860 Chinese texts are written in code (replies, date formats like M月d日, stock up/down); resource keywords used to parse Chinese speech (weekdays, SIM 1/2, carriers, Hong Kong/Macao, wallet category) must stay Chinese. Code check on 2026-11-01.
- **Weather**: city names and weather conditions come from the server in Chinese; day labels (yesterday/today/tomorrow, weekdays) are written in code; one settings banner is text inside a layout. Checked on a 21 Pro on 2026-10-31.
