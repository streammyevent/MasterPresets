# RFC: V-Mix Master Preset

## Probleemstelling

V-Mix is lastig in te stellen en te integreren in workflows met andere audio en video gear. Daardoor verliezen we veel tijd bij de setup en is er meer ervaring benodigd dan je enkel voor de bediening nodig zou hebben.

## Voorgestelde oplossing

Een goed V-Mix master preset moet:

- Met name de lastige functies voorzien, namelijk IFB audio routing en SuperSources
- Weerbaar zijn tegen veranderingen (andere input volgorde, andere soorten media of inputs)
- Compatibel zijn met Zoom, MS Teams en V-Mix Call remotes
- Snel herconfigureerbaar zijn
- Goed geïntegreerd zijn met de andere master presets, in bijzonder Dante, Companion en de Atem SuperSource layout
- Kunnen fungeren als standalone virtual event systeem maar ook als onderdeel van een chain
- Goede documentatie hebben
- Snel gesnoeid kunnen worden (onnodige inputs weghalen) bij minder complexe producties

## Overzichtstabel

| Inputs       | Standaard type     | Outputs       |                                | Audio  |                                |
| ------------ | ------------------ | ------------- | ------------------------------ | ------ | ------------------------------ |
| Input 1      | Blank              | Output 1      | PGM                            | Master | PGM Audio                      |
| Input 2      | Blank              | Output 2      | -                              | Bus A  | Call Conference (operator M-1) |
| Input 3      | Blank              | Output 3      | -                              | Bus B  | Call Conference                |
| Input 4      | Blank              | Output 4      | Remote Return                  | Bus C  | External M-1 input             |
| Remote 1     | Call 1             | External 1    | Output 1                       |        |                                |
| Remote 2     | Call 2             | External 2    | -                              |        |                                |
| Remote 3     | Call 3             | Fullscreen 1  | MultiView                      |        |                                |
| Remote 4     | Call 4             | Fullscreen 2  | -                              |        |                                |
| Remote 5     | Call 5             | Stream        | mistserver / restream endpoint |        |                                |
| Remote 6     | Call 6             | SRT (std uit) | mistserver endpoint            |        |                                |
| Remote 7     | Call 7             |               |                                |        |                                |
| Remote 8     | Call 8             |               |                                |        |                                |
| Playout      | Blank              |               |                                |        |                                |
| PPT          | Blank              |               |                                |        |                                |
| PPT Notes    | Blank              |               |                                |        |                                |
| Interactive  | Blank              |               |                                |        |                                |
| GFX 1        | Holographics Local |               |                                |        |                                |
| GFX 2        | Holographics Clock |               |                                |        |                                |
| Flex 1       | Blank              |               |                                |        |                                |
| Flex 2       | Blank              |               |                                |        |                                |
| Flex 3       | Blank              |               |                                |        |                                |
| MultiView 1  | 1x 16:9            |               |                                |        |                                |
| MultiView 2  | 16:9 big & small L |               |                                |        |                                |
| MultiView 3  | 16:9 big & small R |               |                                |        |                                |
| MultiView 4  | 2x 16:9            |               |                                |        |                                |
| MultiView 5  | 3x 16:9            |               |                                |        |                                |
| MultiView 6  | 4x 16:9            |               |                                |        |                                |
| MultiView 7  | 5x 16:9            |               |                                |        |                                |
| MultiView 8  | 6x 16:9            |               |                                |        |                                |
| MultiView 9  | 7x 16:9            |               |                                |        |                                |
| MultiView 10 | 8x 16:9            |               |                                |        |                                |
| MultiView 11 | 4:3 big & small L  |               |                                |        |                                |
| MultiView 12 | 4:3 big & small R  |               |                                |        |                                |
| MultiView 13 | 2x 4:3             |               |                                |        |                                |
| MultiView 14 | 3x 4:3             |               |                                |        |                                |
| MultiView 15 | 4x 4:3             |               |                                |        |                                |
| MultiView 16 | 5x 4:3             |               |                                |        |                                |
| MultiView 17 | 6x 4:3             |               |                                |        |                                |
| MultiView 18 | 7x 4:3             |               |                                |        |                                |
| MultiView 19 | 8x 4:3             |               |                                |        |                                |
| Talkback Mic | Audio input        |               |                                |        |                                |
| M-1 input    | Audio input        |               |                                |        |                                |
| Color bars   |                    |               |                                |        |                                |
| Videos       |                    |               |                                |        |                                |

## Toelichting

### Inputs

- Alle inputs waar 'blank' op staat zijn gereserveerd door een lege layer aan te maken - welke wel de juiste benaming heeft en met Companion aanstuurbaar is
- Input 1 t/m 4 zijn reserve voor hardware inputs
- Remote 1 t/m 8 zijn standaard toegewezen aan V-Mix calls - die call ID's en links nemen we op in de documentatie (zie pending research)
- Remote 1 t/m 8 hebben standaard Output 4 als return video en Master als return audio
- Playout t/m Interactive is blank - gedachte is dat je dit als NDI of physical input makkelijk kunt patchen
- GFX 1 is gekoppeld aan een lokaal draaiende Holographics instance
- GFX 2 is een solo widget van dezelfde Holographics instance - een aftelklok voor sprekers op overlay layer 4 - alleen actief op output 4
- Flex 1 t/m 3 zijn reserve layers
- MultiView 1 t/m 19 standaard layers gekoppeld aan color bars, layout op basis van centraal template (overeenkomstig met Atem layouts)
- Talkback & M-1 utility inputs gekoppeld aan Dante Virtual Soundcard
- Videos voor playout optioneel aan het einde indien van toepassing, geen verdere koppeling

### Call routing

Middels Companion is het mogelijk om Calls te verplaatsen tussen 2 'rooms'. De PGM room, waar ze meeluisteren en met mute / unmute ook kunnen praten. Of de conference room, waar ze met andere mensen in de conference room kunnen praten en ook de operator met ze kan overleggen.

Dit werkt met de volgende routing:

#### Call Inputs

**Call in PGM room**: Audio return is Bus C<br />
**Call in Conference room:** Audio return is Bus B<br />

#### Call Outputs

**Call in PGM room**: Output naar Master<br />
**Call in Conference room**: Output naar Bus A & Bus B<br />

#### Operator routing

De operator luistert standaard mee op Bus A. Daar kan hij calls in en uit plaatsen. Hij hoort op dat kanaal niet de program audio.

Als alternatief is het is ook mogelijk voor de operator om te switchen tussen program audio en de conference, maar alleen door de headphone output te routen en de solo functie te gebruiken.

### Audio Bussen

- **Master**: PGM audio vanuit V-Mix - kan ook als output naar de Behringer gaan wanneer V-Mix een onderdeel is van de chain
- **Bus A**: Conference listen bus voor de operator
- **Bus B**: Conference bus waarop ook de operator talkback mic geroute staat
- **Bus C**: Mix-minus return feed - alle inputs staan standaard aan op deze bus, behalve de M-1 externe audio feed. Dit is nodig wanneer we V-Mix gebruiken als onderdeel van een complexe productie. Op die manier kan V-Mix een audio input krijgen van de rest van de productie (om naar calls te sturen) en zelf een M-1 outputten.

## Pending research

- Blijven V-Mix Call IDs gelijk between saves? Experiment: Caller aanmaken. File opslaan. Caller aanpassen. Eerdere file laden. Is het caller ID terug naar de eerste staat?
- Is het mogelijk om vanuit Companion V-Mix aan te sturen op basis van input names ipv ID nummers?<br />**Confirmed, is mogelijk**
- Is het mogelijk om een input van type te veranderen zonder dat V-Mix de input naam veranderd?<br />**Confirmed, is mogelijk. Bij een default name past V-Mix automatisch de naam aan als er van type veranderd wordt. Bij een non-default name blijft de ingestelde naam hetzelfde.**
