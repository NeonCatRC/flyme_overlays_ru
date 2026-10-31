# Flyme 12 Russian translation

Base firmware: **Flyme 12.6.0.0A** (Meizu 21 Pro, CN build, Android 16).

Every app folder holds:

- `res/values/` — source strings of the app (as shipped in the firmware);
- `res/values-ru/` — the Russian translation;
- `res/values-en/` — English fixes: only strings whose English is missing or poor in the app;
- `status.tsv` — where every Russian string comes from;
- `status_en.tsv` — English strings this repository adds (`new`), corrects (`fix`) or still lacks (`todo`);
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

## English

Most strings keep the English shipped in the app (Meizu or AOSP). `status_en.tsv` lists only
the exceptions: `new` — the app had Chinese and no English; `fix` — Meizu's English was wrong;
`todo` — Chinese with no English, not done yet.

## State

Translated = `own` + `own_check` + `apk` + `new` out of everything except `unused` and `skip`.

| APP | VERSION | TRANSLATED | OWN | CHECK | APK | NEW | TODO | UNUSED | EN NEW | EN FIX | EN TODO |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| AlarmClock | 12.0.46 | 75% | 353 | 0 | 114 | 0 | 151 | 50 | 0 | 0 | 0 |
| AlphaMe | 12.0.19 | 59% | 12 | 0 | 188 | 0 | 135 | 62 | 0 | 0 | 0 |
| AppCenter | 12.5.1 | 27% | 256 | 2 | 62 | 0 | 850 | 49 | 0 | 0 | 0 |
| Assistant | 13.0.6 | 39% | 398 | 9 | 17 | 0 | 643 | 57 | 0 | 0 | 0 |
| Browser | 12.9.1 | 55% | 506 | 6 | 2538 | 0 | 2435 | 379 | 0 | 0 | 0 |
| Calculator | 12.0.17 | 74% | 388 | 0 | 105 | 0 | 173 | 5 | 0 | 0 | 0 |
| Calendar | 19.3.3 | 51% | 742 | 17 | 34 | 0 | 753 | 70 | 0 | 0 | 0 |
| Camera | 12.7.2 | 100% | 533 | 13 | 83 | 49 | 0 | 16 | 0 | 0 | 0 |
| ConnectivitySettings | 12.15.000 | 93% | 1962 | 50 | 521 | 0 | 188 | 124 | 0 | 0 | 0 |
| CustomizeCenter | 12.5.0 | 69% | 751 | 21 | 16 | 0 | 343 | 28 | 0 | 0 | 0 |
| DataMigration | 12.1.1 | 67% | 742 | 37 | 80 | 0 | 417 | 212 | 0 | 0 | 0 |
| Dialer | 8.2.6 | 100% | 1128 | 10 | 9 | 353 | 0 | 26 | 0 | 0 | 0 |
| Email | 12.1.53 | 88% | 867 | 0 | 99 | 0 | 129 | 93 | 0 | 0 | 0 |
| FileManager | 12.0.21 | 75% | 649 | 0 | 129 | 0 | 254 | 36 | 0 | 0 | 0 |
| FlymeLauncher | 13.0.0 | 100% | 468 | 19 | 272 | 155 | 0 | 30 | 0 | 0 | 0 |
| FlymeMusic | 12.2.0 | 18% | 318 | 3 | 51 | 0 | 1607 | 240 | 0 | 0 | 0 |
| FlymeSoundRecorder | 12.3.7 | 80% | 355 | 7 | 190 | 0 | 133 | 3 | 0 | 0 | 0 |
| framework-res | 16 | 100% | 1320 | 95 | 1312 | 275 | 0 | 0 | 0 | 0 | 0 |
| Gallery | 12.7.3 | 78% | 1305 | 12 | 468 | 0 | 497 | 68 | 0 | 0 | 0 |
| GameCenter | 12.3.0 | 65% | 1062 | 16 | 6 | 0 | 570 | 151 | 0 | 0 | 0 |
| InCallUI | 14.01.07 | 100% | 188 | 7 | 43 | 20 | 0 | 3 | 0 | 0 | 0 |
| mCareNew | 8.0.0 | 42% | 184 | 2 | 71 | 0 | 346 | 28 | 0 | 0 | 0 |
| Mms | 12.3.4 | 100% | 878 | 20 | 0 | 399 | 0 | 225 | 0 | 0 | 0 |
| MusicFX | 5.0.0 | 96% | 213 | 0 | 3 | 0 | 9 | 5 | 0 | 0 | 0 |
| MzAccount | 12.0.14 | 76% | 258 | 4 | 100 | 0 | 111 | 24 | 0 | 0 | 0 |
| MzBatteryManager | 12.0.24 | 61% | 252 | 6 | 8 | 0 | 166 | 76 | 0 | 0 | 0 |
| MzSecurity | 12.1.48 | 56% | 1255 | 26 | 38 | 0 | 1002 | 57 | 0 | 0 | 0 |
| MzSetupWizard | 12.0.25 | 47% | 0 | 256 | 66 | 0 | 358 | 66 | 0 | 0 | 0 |
| MzShare | 6.1.14 | 85% | 471 | 5 | 18 | 0 | 87 | 69 | 0 | 0 | 0 |
| MzUpdate | 12.0.15 | 81% | 651 | 13 | 38 | 0 | 159 | 1 | 0 | 0 | 0 |
| NetAdmin | 11.0.3 | 80% | 308 | 3 | 8 | 0 | 75 | 42 | 0 | 0 | 0 |
| NotePaper | 12.0.68 | 81% | 499 | 9 | 407 | 0 | 201 | 28 | 0 | 0 | 0 |
| PackageInstaller | 16 | 73% | 360 | 18 | 110 | 0 | 177 | 45 | 0 | 0 | 0 |
| Pedometer | 12.0.13 | 73% | 419 | 8 | 44 | 0 | 172 | 55 | 0 | 0 | 0 |
| Picker | 12.2.34 | 56% | 304 | 4 | 7 | 0 | 247 | 78 | 0 | 0 | 0 |
| SDKStage | 5.0.01 | 60% | 128 | 0 | 9 | 0 | 88 | 11 | 0 | 0 | 0 |
| Settings | 12.1.0 | 100% | 4521 | 436 | 4691 | 191 | 0 | 158 | 0 | 0 | 0 |
| Suggestion | 12.5.10 | 15% | 89 | 2 | 0 | 0 | 512 | 3 | 0 | 0 | 0 |
| SystemUI | 16.26.06.25_base | 100% | 1771 | 64 | 1947 | 93 | 0 | 171 | 0 | 0 | 0 |
| SystemUIEx | 12.3.14 | 100% | 267 | 7 | 48 | 14 | 0 | 65 | 0 | 0 | 0 |
| SystemUITools | 13.1.2 | 100% | 314 | 5 | 168 | 165 | 0 | 16 | 0 | 0 | 0 |
| ToolBox | 12.0.15 | 84% | 367 | 0 | 107 | 0 | 88 | 51 | 0 | 0 | 0 |
| Video | 17.23.0 | 52% | 263 | 0 | 30 | 0 | 266 | 29 | 0 | 0 | 0 |
| VoiceAssistant | 12.1.46 | 40% | 754 | 8 | 0 | 0 | 1120 | 234 | 0 | 0 | 0 |
| Weather | 54.3.60 | 100% | 459 | 0 | 111 | 458 | 0 | 61 | 99 | 102 | 0 |
| **Total** | | 76% | 29288 | 1220 | 14366 | 2172 | 14462 | 3300 | 99 | 102 | 0 |
