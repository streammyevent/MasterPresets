# Atem Master Preset

![ready](https://img.shields.io/badge/status-ready-green)
![version](https://img.shields.io/badge/version-1.0-green)

## Contents

- [✨ Features](#-features)
- [🏎️ Getting started](#%EF%B8%8F-getting-started)
- [👍👎 Do's & Donts](#-dos--donts)
- [🧑‍🏫 FAQ's](#-faqs)
- [⚙️ Standaardconfiguratie](#%EF%B8%8F-standaardconfiguratie)
- [🗺️ Input mapping](#%EF%B8%8F-input-mapping)
- [📡 Output mapping](#-output-mapping)
- [📺 MultiView Layouts](#-multiview-layouts)
- [▶️ Media Files](#%EF%B8%8F-media-files)
- [🕹️ Macro's](#%EF%B8%8F-macros)

## ✨ Features

- Logische standaardconfigs en multiviews
- SuperSource layouts op basis van het SuperSources master preset
- SuperSource layouts configureerbaar via Macros (zie Macro's hieronder)
- Standaard artwork included
- 'Go Playout' macro met dip to black die DSK1 weghaalt
- 2 aparte remote return feeds instelbaar via Companion

## 🏎️ Getting started

1.  Open Atem Software Control
2.  Stel de gewenste videomode in (indien anders dan 1080p50)
3.  Ga naar File > Restore (Cmd + R)
4.  Selecteer het [Master Preset bestand](https://github.com/streammyevent/MasterPresets/blob/master/Atem/Atem%202ME%20Master%20Preset.xml)
5.  Zorg dat alles geselecteerd is (en selecteer desgewenst de videomode in)
6.  Het kost ongeveer 20 seconden om de volledige preset in te laden en alle mediafiles te uploaden naar de Atem

## 👍👎 Do's & Donts

```diff
+ DO: Pas de namen van inputs aan (bvb namen van camguys) voor je productie

+ DO: Pas de MultiViewer aan op de eisen van je productie

+ DO: Delete of verander de macro's die je nodig hebt voor je eigen productie

- DONT: Verander liever niet de toewijzingen van input 9 t/m 20, dan werken geen van de standaard macro's meer

- DONT: De SuperSource layouts werken alleen op 16:9 aspect ratios en zijn alleen getest op 1920x1080
```

## 🧑‍🏫 FAQ's

### ❓ **Hoe kan ik het beste de artwork images vervangen?**

Als artwork is aangeleverd met exact dezelfde filenames, kun je heel simpel de files vervangen en vervolgens de restore doen.

### ❓ **Wat als ik alle SuperSource layouts op hetzelfde background artwork wil hebben?**

Je hebt 2 opties:

1.  De macro's aanpassen met een XML editor zodat de background niet veranderd word bij een schakeling tussen layouts
2.  Je background artwork uploaden naar Media Pool index 11 t/m 21 zodat die allemaal toegewezen zijn

### ❓ **Wat als ik de resolutie of framerate moet aanpassen ná de restore**

Het enige dat dan uit je configuratie verdwijnt zijn de MediaFiles, die moet je zelf opnieuw uploaden. Zie [hieronder](#%EF%B8%8F-media-files) de standaard toewijzing van Media Files.

Je kunt ook een gedeeltelijke restore doen. Volg de zelfde procedure als [hierboven](#%EF%B8%8F-getting-started), maar selecteer bij Stap 5 alleen 'Media Pool'.

## ⚙️ Standaardconfiguratie

- **Color1**: Instelbaar, oranje bij default
- **Color2**: Zwart, in gebruik voor de dip to black
- **Transition**: Dip to black
- **DSK1**: Key & Fill voor Graphics en playout
- **DSK2**: Media Player 1
- **MediaPlayer1**: In gebruik voor standaardartwork 'start soon' etc
- **MediaPlayer2**: In gebruik voor SuperSource backgrounds
- **VideoMode**: 1080p50

## 🗺️ Input mapping

| Input     | Toewijzing         |
| --------- | ------------------ |
| HD-SDI 1  | Camera 1           |
| HD-SDI 2  | Camera 2           |
| HD-SDI 3  | Camera 3           |
| HD-SDI 4  | Camera 4           |
| HD-SDI 5  | Camera 5           |
| HD-SDI 6  | Camera 6           |
| HD-SDI 7  | Camera 7           |
| HD-SDI 8  | Camera 8           |
| HD-SDI 9  | Remote 1           |
| HD-SDI 10 | Remote 2           |
| HD-SDI 11 | Remote 3           |
| HD-SDI 12 | Remote 4           |
| HD-SDI 13 | Playout / GFX Key  |
| HD-SDI 14 | Playout / GFX Fill |
| HD-SDI 15 | PPT                |
| HD-SDI 16 | PPT Notes          |
| HD-SDI 17 | Interactive        |
| HD-SDI 18 | Flex 1             |
| HD-SDI 19 | Flex 2             |
| HD-SDI 20 | Flex 3             |

## 📡 Output mapping

| Outputs | Toewijzing   |
| ------- | ------------ |
| AUX 1   | ENCODER      |
| AUX 2   | RECORDING    |
| AUX 3   | MONITOR 1    |
| AUX 4   | MONITOR 2    |
| AUX 5   | REMOTE RTN 1 |
| AUX 6   | REMOTE RTN 2 |

## 📺 MultiView Layouts

| Multiviewer 1 | Source             | Multiviewer 2 | Source |
| ------------- | ------------------ | ------------- | ------ |
| Window 1      | Camera 1           | Window 1      | AUX 1  |
| Window 2      | Camera 2           | Window 2      | AUX 2  |
| Window 3      | Camera 3           | Window 3      | AUX 3  |
| Window 4      | Camera 4           | Window 4      | AUX 4  |
| Window 5      | Remote 1           | Window 5      | AUX 5  |
| Window 6      | Remote 2           | Window 6      | AUX 6  |
| Window 7      | Playout / GFX Fill | Window 7      | Blank  |
| Window 8      | SuperSource        | Window 8      | Blank  |

## ▶️ Media Files

| Media File Index | Toewijzing                 |
| ---------------- | -------------------------- |
| Slot 1           | Background leeg            |
| Slot 2           | StartSoon                  |
| Slot 3           | Break                      |
| Slot 4           | Standby                    |
| Slot 5           | End                        |
| Slot 6           | Leeg                       |
| Slot 7           | Leeg                       |
| Slot 8           | Leeg                       |
| Slot 9           | Leeg                       |
| Slot 10          | Leeg                       |
| Slot 11          | SrS 01: 1x 16:9            |
| Slot 12          | SrS 02: 16:9 big & small L |
| Slot 13          | SrS 03: 16:9 big & small R |
| Slot 14          | SrS 04: 2x 16:9            |
| Slot 15          | SrS 05: 3x 16:9            |
| Slot 16          | SrS 06: 4x 16:9            |
| Slot 17          | SrS 11: 4:3 big & small L  |
| Slot 18          | SrS 12: 4:3 big & small R  |
| Slot 19          | SrS 13: 2x 4:3             |
| Slot 20          | SrS 14: 3x 4:3             |
| Slot 21          | SrS 15: 4x 4:3             |

## 🕹️ Macro's

| Macros   | Toewijzing                 | Omschrijving                      |
| -------- | -------------------------- | --------------------------------- |
| Macro 1  | Box 1 ME2                  | SrS Box 1 op ME2                  |
| Macro 2  | Box 1 Playout              | SrS Box 1 op Playout              |
| Macro 3  | Box 1 PPT                  | SrS Box 1 op PPT                  |
| Macro 4  | Box 1 Interactive          | SrS Box 1 op Interactive          |
| Macro 5  | Box 2 ME2                  | SrS Box 2 op ME2                  |
| Macro 6  | Box 1 Remotes              | Schakelen tussen Remotes op Box 1 |
| Macro 7  | Box 2 Remotes              | Schakelen tussen Remotes op Box 2 |
| Macro 8  | Box 3 Remotes              | Schakelen tussen Remotes op Box 3 |
| Macro 9  | Box 4 Remotes              | Schakelen tussen Remotes op Box 4 |
| Macro 10 | Go Playout                 | Dip naar Playout met DSK1 op Tie  |
| Macro 11 | SrS 01: 1x 16:9            | Activeer SrS Layout 01            |
| Macro 12 | SrS 02: 16:9 big & small L | Activeer SrS Layout 02            |
| Macro 13 | SrS 03: 16:9 big & small R | Activeer SrS Layout 03            |
| Macro 14 | SrS 04: 2x 16:9            | Activeer SrS Layout 04            |
| Macro 15 | SrS 05: 3x 16:9            | Activeer SrS Layout 05            |
| Macro 16 | SrS 06: 4x 16:9            | Activeer SrS Layout 06            |
| Macro 17 | SrS 11: 4:3 big & small L  | Activeer SrS Layout 11            |
| Macro 18 | SrS 12: 4:3 big & small R  | Activeer SrS Layout 12            |
| Macro 19 | SrS 13: 2x 4:3             | Activeer SrS Layout 13            |
| Macro 20 | SrS 14: 3x 4:3             | Activeer SrS Layout 14            |
| Macro 21 | SrS 15: 4x 4:3             | Activeer SrS Layout 15            |
