# Behringer Master Presets

| Inputs   |                | Outputs  | Physical        | Channels   |            | DCA   |          | MixBus    |              | Matrix   |              |
| -------- | -------------- | -------- | --------------- | ---------- | ---------- | ----- | -------- | --------- | ------------ | -------- | ------------ |
| XLR 1    | Mic 1          | Output 1 | IFB Stage       | Channel 1  | Mic 1      | DCA 1 | Mics     | MixBus 1  | Free         | Matrix 1 | IFB Stage    |
| XLR 2    | Mic 2          | Output 2 | Oper. Listen    | Channel 2  | Mic 2      | DCA 2 | Remote 3 | MixBus 2  | Regie        | Matrix 2 | IFB Remote 1 |
| XLR 3    | Mic 3          | Output 3 | Free            | Channel 3  | Mic 3      | DCA 3 | Remote 4 | MixBus 3  | Mic's delay  | Matrix 3 | IFB Remote 2 |
| XLR 4    | Mic 4          | Output 4 | Free            | Channel 4  | Mic 4      | DCA 4 | Playout  | MixBus 4  | Talkback 1   | Matrix 4 | IFB Remote 3 |
| XLR 5    | Mic 5          | Output 5 | Free            | Channel 5  | Mic 5      | DCA 5 | PPT      | MixBus 5  | Operator 1   | Matrix 5 | IFB Remote 4 |
| XLR 6    | Mic 6          | Output 6 | Free            | Channel 6  | Mic 6      | DCA 6 | Jingle   | MixBus 6  | Operator 2   | Matrix 6 | Regie        |
| XLR 7    |                | Output 7 | Main L (Stream) | Channel 7  | Remote 1   | DCA 7 | Stage    | MixBus 7  | Talkback 2   |          |              |
| XLR 8    |                | Output 8 | Main R (Stream) | Channel 8  | Remote 2   | DCA 8 | Regie    | MixBus 8  | M-1 Stage    |          |              |
| XLR 15   | Talkback Mic 1 |          | P16 (dante)     | Channel 9  | Remote 3   |       |          | MixBus 9  | M-1 Remote 1 |          |              |
| XLR 16   | Talkback Mic 2 | Dante 1  | IFB Remote 1    | Channel 10 | Remote 4   |       |          | MixBus 10 | M-1 Remote 2 |          |              |
|          |                | Dante 2  | IFB Remote 2    | Channel 11 | Playout L  |       |          | MixBus 11 | M-1 Remote 3 |          |              |
| Dante 1  | Remote 1       | Dante 3  | IFB Remote 3    | Channel 12 | Playout R  |       |          | MixBus 12 | M-1 Remote 4 |          |              |
| Dante 2  | Remote 2       | Dante 4  | IFB Remote 4    | Channel 13 | PPT L      |       |          | FX 1      | Reverb Mics  |          |              |
| Dante 3  | Remote 3       | Dante 5  | IFB Stage       | Channel 14 | PPT R      |       |          | FX 2      | Delay 1      |          |              |
| Dante 4  | Remote 4       | Dante 6  | Oper. Listen    | Channel 15 | Jingle L   |       |          | FX 3      | Delay 2      |          |              |
| Dante 5  | Playout L      | Dante 7  |                 | Channel 16 | Jingle R   |       |          | FX 4      | Delay 3      |          |              |
| Dante 6  | Playout R      | Dante 8  |                 | Channel 17 | Music L    |       |          |           |              |          |              |
| Dante 7  | PPT L          | Dante 9  |                 | Channel 18 | Music R    |       |          |           |              |          |              |
| Dante 8  | PPT R          | Dante 10 |                 | Channel 19 |            |       |          |           |              |          |              |
| Dante 9  | Jingle L       | Dante 11 |                 | Channel 20 |            |       |          |           |              |          |              |
| Dante 10 | Jingle R       | Dante 12 |                 | Channel 21 |            |       |          |           |              |          |              |
| Dante 11 | Music L        | Dante 13 |                 | Channel 22 |            |       |          |           |              |          |              |
| Dante 12 | Music R        | Dante 14 |                 | Channel 23 |            |       |          |           |              |          |              |
|          |                | Dante 15 | Main L          | Channel 24 |            |       |          |           |              |          |              |
|          |                | Dante 16 | Main R          | Channel 25 |            |       |          |           |              |          |              |
|          |                |          |                 | Channel 26 |            |       |          |           |              |          |              |
|          |                |          |                 | Channel 27 |            |       |          |           |              |          |              |
|          |                |          |                 | Channel 28 | Mic delay  |       |          |           |              |          |              |
|          |                |          |                 | Channel 29 | PGM L      |       |          |           |              |          |              |
|          |                |          |                 | Channel 30 | PGM R      |       |          |           |              |          |              |
|          |                |          |                 | Channel 31 | Talkback 1 |       |          |           |              |          |              |
|          |                |          |                 | Channel 32 | Talkback 2 |       |          |           |              |          |              |

## Todo:

- 2 talkback mics ipv 1 (✅ as of 28th of march 2022)
- 2 prefade listen channels ipv 1 (remote 4 vervangen) (✅ as of 28th of march 2022)

## Info:
- Channel presets = alleen het geselecteerde kanaal
- Scene = hele tafel
- Dante patching gaat via het tabje P16 (ultranet)
- Fysieke patching gaat via Out 1-16 waarvan de eerste 8 actief, de rest zijn (behalve bij gebruik van stagebox) virtueel.
