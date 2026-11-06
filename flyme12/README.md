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
| AlarmClock | 12.0.46 | 100% | 347 | 0 | 82 | 120 | 0 | 50 | 0 | 3 | 0 |
| AliveWallPaper | 13.0.5 | 100% | 0 | 0 | 6 | 39 | 0 | 7 | 1 | 0 | 0 |
| AlphaMe | 12.0.19 | 100% | 10 | 0 | 140 | 140 | 0 | 62 | 0 | 1 | 0 |
| AppCenter | 12.5.1 | 100% | 258 | 0 | 57 | 705 | 0 | 49 | 53 | 14 | 0 |
| Assistant | 13.0.6 | 100% | 382 | 0 | 20 | 357 | 0 | 57 | 7 | 3 | 0 |
| Browser | 12.9.1 | 55% | 505 | 6 | 2538 | 0 | 2435 | 379 | 0 | 0 | 0 |
| Calculator | 12.0.17 | 100% | 386 | 0 | 78 | 101 | 0 | 5 | 0 | 6 | 0 |
| Calendar | 19.3.3 | 100% | 750 | 0 | 23 | 642 | 0 | 70 | 115 | 20 | 0 |
| Camera | 12.7.2 | 100% | 493 | 0 | 93 | 85 | 0 | 16 | 1 | 2 | 0 |
| ConnectivitySettings | 12.15.000 | 100% | 1822 | 0 | 529 | 252 | 0 | 124 | 0 | 6 | 0 |
| CustomizeCenter | 12.5.0 | 100% | 754 | 0 | 10 | 255 | 0 | 28 | 44 | 9 | 0 |
| DataMigration | 12.1.1 | 100% | 519 | 0 | 150 | 540 | 0 | 212 | 1 | 9 | 0 |
| Dialer | 8.2.6 | 100% | 1132 | 0 | 2 | 364 | 0 | 26 | 64 | 45 | 0 |
| Email | 12.1.53 | 100% | 867 | 0 | 78 | 52 | 0 | 93 | 0 | 4 | 0 |
| FileManager | 12.0.21 | 100% | 646 | 0 | 93 | 178 | 0 | 36 | 45 | 4 | 0 |
| FlymeLauncher | 13.0.0 | 100% | 451 | 0 | 258 | 205 | 0 | 30 | 45 | 13 | 0 |
| FlymeSoundRecorder | 12.3.7 | 100% | 358 | 0 | 80 | 177 | 0 | 3 | 1 | 8 | 0 |
| framework-res | 16 | 100% | 1394 | 0 | 1275 | 332 | 0 | 0 | 65 | 11 | 0 |
| Gallery | 12.7.3 | 100% | 1308 | 0 | 335 | 511 | 0 | 68 | 42 | 52 | 0 |
| GameCenter | 12.3.0 | 100% | 186 | 0 | 130 | 1266 | 0 | 151 | 123 | 30 | 0 |
| InCallUI | 14.01.07 | 100% | 190 | 0 | 41 | 27 | 0 | 3 | 0 | 0 | 0 |
| mCareNew | 8.0.0 | 100% | 186 | 0 | 61 | 292 | 0 | 28 | 161 | 8 | 0 |
| Mms | 12.3.4 | 100% | 828 | 0 | 0 | 465 | 0 | 225 | 74 | 16 | 0 |
| MusicFX | 5.0.0 | 100% | 211 | 0 | 3 | 0 | 0 | 5 | 0 | 0 | 0 |
| MzAccount | 12.0.14 | 100% | 262 | 0 | 83 | 85 | 0 | 24 | 0 | 2 | 0 |
| MzBatteryManager | 12.0.24 | 100% | 253 | 0 | 5 | 132 | 0 | 76 | 0 | 0 | 0 |
| MzSecurity | 12.1.48 | 100% | 1264 | 0 | 30 | 546 | 0 | 57 | 101 | 140 | 0 |
| MzSetupWizard | 12.0.25 | 100% | 237 | 0 | 51 | 291 | 0 | 66 | 12 | 1 | 0 |
| MzShare | 6.1.14 | 100% | 469 | 0 | 6 | 65 | 0 | 69 | 0 | 2 | 0 |
| MzUpdate | 12.0.15 | 100% | 391 | 0 | 218 | 159 | 0 | 1 | 1 | 3 | 0 |
| NativeLockScreen | 12.2.2 | 100% | 0 | 0 | 154 | 277 | 0 | 35 | 85 | 16 | 0 |
| NetAdmin | 11.0.3 | 100% | 309 | 0 | 5 | 30 | 0 | 42 | 0 | 0 | 0 |
| NotePaper | 12.0.68 | 100% | 503 | 0 | 366 | 177 | 0 | 28 | 31 | 3 | 0 |
| PackageInstaller | 16 | 100% | 308 | 0 | 108 | 140 | 0 | 45 | 31 | 5 | 0 |
| Pedometer | 12.0.13 | 100% | 399 | 0 | 33 | 113 | 0 | 55 | 41 | 5 | 0 |
| Picker | 12.2.34 | 100% | 305 | 0 | 4 | 194 | 0 | 78 | 2 | 0 | 0 |
| SDKStage | 5.0.01 | 100% | 127 | 0 | 8 | 45 | 0 | 11 | 0 | 1 | 0 |
| Settings | 12.1.0 | 100% | 4848 | 0 | 4391 | 572 | 0 | 158 | 9 | 29 | 0 |
| Suggestion | 12.5.10 | 100% | 91 | 0 | 0 | 429 | 0 | 3 | 125 | 2 | 0 |
| SystemUI | 16.26.06.25_base | 100% | 1804 | 0 | 1912 | 143 | 0 | 171 | 3 | 0 | 0 |
| SystemUIEditor | 3.5.45 | 100% | 0 | 0 | 142 | 212 | 0 | 105 | 10 | 34 | 0 |
| SystemUIEx | 12.3.14 | 100% | 270 | 0 | 40 | 26 | 0 | 65 | 0 | 0 | 0 |
| SystemUITools | 13.1.2 | 100% | 205 | 0 | 170 | 274 | 0 | 16 | 27 | 13 | 0 |
| ToolBox | 12.0.15 | 100% | 367 | 0 | 85 | 61 | 0 | 51 | 7 | 0 | 0 |
| Video | 17.23.0 | 100% | 261 | 0 | 26 | 168 | 0 | 29 | 46 | 2 | 0 |
| VoiceAssistant **MOD** | 12.1.46 | 39% | 497 | 8 | 0 | 217 | 1120 | 234 | 0 | 0 | 0 |
| WallpaperSetting | 3.2.0 | 100% | 0 | 0 | 20 | 142 | 0 | 17 | 0 | 16 | 0 |
| Weather **MOD** | 54.3.60 | 100% | 312 | 0 | 92 | 624 | 0 | 61 | 99 | 102 | 0 |
| **Total** | | 93% | 27465 | 14 | 14031 | 12227 | 3555 | 3224 | 1472 | 640 | 0 |

### Why a modification is required

- **VoiceAssistant**: speech recognition and the assistant's answers are Chinese-only (server side); about 860 Chinese texts are written in code (replies, date formats like M月d日, stock up/down); resource keywords used to parse Chinese speech (weekdays, SIM 1/2, carriers, Hong Kong/Macao, wallet category) must stay Chinese. Code check on 2026-11-01.
- **Weather**: city names and weather conditions come from the server in Chinese; day labels (yesterday/today/tomorrow, weekdays) are written in code; one settings banner is text inside a layout. Checked on a 21 Pro on 2026-10-31.

### Not translated

- **FlymeMusic**: third-party streaming service; not worth translating
