# Flyme 12 Russian translation

Base firmware: **Flyme 12.6.0.0A** (Meizu 21 Pro, CN build, Android 16).

Every app folder holds:

- `res/values/` — source strings of the app (as shipped in the firmware);
- `res/values-ru/` — the Russian translation;
- `status.tsv` — where every string comes from;
- `overlay.json` — target package and app version.

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

## State

Translated = `own` + `own_check` + `apk` + `new` out of everything except `unused` and `skip`.

| APP | VERSION | TRANSLATED | OWN | CHECK | APK | NEW | TODO | UNUSED |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| AlarmClock | 12.0.46 | 75% | 353 | 0 | 114 | 0 | 151 | 50 |
| AlphaMe | 12.0.19 | 59% | 12 | 0 | 188 | 0 | 135 | 62 |
| AppCenter | 12.5.1 | 27% | 256 | 2 | 62 | 0 | 850 | 49 |
| Assistant | 13.0.6 | 39% | 398 | 9 | 17 | 0 | 643 | 57 |
| Browser | 12.9.1 | 55% | 506 | 6 | 2538 | 0 | 2435 | 379 |
| Calculator | 12.0.17 | 74% | 388 | 0 | 105 | 0 | 173 | 5 |
| Calendar | 19.3.3 | 51% | 742 | 17 | 34 | 0 | 753 | 70 |
| Camera | 12.7.2 | 82% | 533 | 13 | 83 | 0 | 133 | 16 |
| ConnectivitySettings | 12.15.000 | 93% | 1962 | 50 | 521 | 0 | 188 | 124 |
| CustomizeCenter | 12.5.0 | 69% | 751 | 21 | 16 | 0 | 343 | 28 |
| DataMigration | 12.1.1 | 67% | 742 | 37 | 80 | 0 | 417 | 212 |
| Dialer | 8.2.6 | 73% | 1128 | 10 | 9 | 0 | 404 | 26 |
| Email | 12.1.53 | 88% | 867 | 0 | 99 | 0 | 129 | 93 |
| FileManager | 12.0.21 | 75% | 649 | 0 | 129 | 0 | 254 | 36 |
| FlymeLauncher | 13.0.0 | 70% | 468 | 19 | 272 | 0 | 311 | 30 |
| FlymeMusic | 12.2.0 | 18% | 318 | 3 | 51 | 0 | 1607 | 240 |
| FlymeSoundRecorder | 12.3.7 | 80% | 355 | 7 | 190 | 0 | 133 | 3 |
| framework-res | 16 | 100% | 1320 | 95 | 1312 | 215 | 0 | 0 |
| Gallery | 12.7.3 | 78% | 1305 | 12 | 468 | 0 | 497 | 68 |
| GameCenter | 12.3.0 | 65% | 1062 | 16 | 6 | 0 | 570 | 151 |
| InCallUI | 14.01.07 | 77% | 188 | 7 | 43 | 0 | 68 | 3 |
| mCareNew | 8.0.0 | 42% | 184 | 2 | 71 | 0 | 346 | 28 |
| Mms | 12.3.4 | 63% | 878 | 20 | 0 | 0 | 520 | 225 |
| MusicFX | 5.0.0 | 96% | 213 | 0 | 3 | 0 | 9 | 5 |
| MzAccount | 12.0.14 | 76% | 258 | 4 | 100 | 0 | 111 | 24 |
| MzBatteryManager | 12.0.24 | 61% | 252 | 6 | 8 | 0 | 166 | 76 |
| MzSecurity | 12.1.48 | 56% | 1255 | 26 | 38 | 0 | 1002 | 57 |
| MzSetupWizard | 12.0.25 | 47% | 0 | 256 | 66 | 0 | 358 | 66 |
| MzShare | 6.1.14 | 85% | 471 | 5 | 18 | 0 | 87 | 69 |
| MzUpdate | 12.0.15 | 81% | 651 | 13 | 38 | 0 | 159 | 1 |
| NetAdmin | 11.0.3 | 80% | 308 | 3 | 8 | 0 | 75 | 42 |
| NotePaper | 12.0.68 | 81% | 499 | 9 | 407 | 0 | 201 | 28 |
| PackageInstaller | 16 | 73% | 360 | 18 | 110 | 0 | 177 | 45 |
| Pedometer | 12.0.13 | 73% | 419 | 8 | 44 | 0 | 172 | 55 |
| Picker | 12.2.34 | 56% | 304 | 4 | 7 | 0 | 247 | 78 |
| SDKStage | 5.0.01 | 60% | 128 | 0 | 9 | 0 | 88 | 11 |
| Settings | 12.1.0 | 95% | 4521 | 436 | 4691 | 0 | 424 | 158 |
| Suggestion | 12.5.10 | 15% | 89 | 2 | 0 | 0 | 512 | 3 |
| SystemUI | 16.26.06.25_base | 93% | 1771 | 64 | 1947 | 0 | 249 | 171 |
| SystemUIEx | 12.3.14 | 84% | 267 | 7 | 48 | 0 | 58 | 65 |
| SystemUITools | 13.1.2 | 69% | 314 | 5 | 168 | 0 | 214 | 16 |
| ToolBox | 12.0.15 | 84% | 367 | 0 | 107 | 0 | 88 | 51 |
| Video | 17.23.0 | 52% | 263 | 0 | 30 | 0 | 266 | 29 |
| VoiceAssistant | 12.1.46 | 40% | 754 | 8 | 0 | 0 | 1120 | 234 |
| Weather | 54.3.60 | 49% | 461 | 0 | 111 | 0 | 592 | 61 |
| **Total** | | 72% | 29290 | 1220 | 14366 | 215 | 17435 | 3300 |
