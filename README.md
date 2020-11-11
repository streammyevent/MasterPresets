# The Master Presets Initiative

![incomplete](https://img.shields.io/badge/status-incomplete-red)
![version](https://img.shields.io/badge/version-0.3-red)

### [**Download v0.3**](https://github.com/streammevent/MasterPreset/archive/master.zip)

Master presets zijn uitgebreide standaardconfiguraties (hero setups) voor de hardware en software waar we vaak mee werken. De bedoeling is om complexe functionaliteit zoals SuperSources, Macro's, IFB en Dante klaar te hebben staan om tijd te besparen bij de technische bouw van een productie.

De MasterPresets zijn onderling goed op elkaar afgestemd. De gebruikte kleuren (van scribbe strips, knoppen etc) kloppen onderling. Een Remote heeft bijvoorbeeld dezelfde kleur op de Behringer, op het Atem panel en op Companion.

Een MasterPreset dient als startpositie voor een productie. Het doel is niet om een technicus te vervangen, maar om tijd te besparen.

**Dit zijn de regels:**

- Één MasterPreset per type software of hardware
- De MasterPreset moet documentatie hebben, zowel fysiek als digitaal
- De MasterPreset moet voorzien in standaard hardware patching, zodat iedere technicus de fysieke aansluiting kan doen
- MasterPresets moeten onderling op elkaar afgestemd zijn om een goed ecosysteem te bevorderen
- MasterPresets zijn zo globaal mogelijk - bij iedere toevoeging moet een overweging gemaakt worden tussen extra complexiteit en functionaliteit
- Een MasterPreset is niet geschikt voor álle producties, maar voor 90% van de producties.

Presets... Assemble.

## Status

### [Companion](https://github.com/streammyevent/MasterPresets/tree/master/Companion)

![incomplete](https://img.shields.io/badge/status-incomplete-red)
![version](https://img.shields.io/badge/version-0.2-red)

⚠️ JingleMachine control
<br />✅ Behringer Intercom Control
<br />✅ Atem SrS mapping
<br />✅ Atem MultiView mapping
<br />❌ Clock control
<br />❌ V-Mix Virtual Event Control
<br />⚠️ V-Mix Intercom Control
<br />❌ Docs

### [Behringer](https://github.com/streammyevent/MasterPresets/tree/master/Behringer)

![incomplete](https://img.shields.io/badge/status-no%20docs-orange)
![version](https://img.shields.io/badge/version-1.1-green)

✅ Standaard input en output mapping
<br />✅ Dante inputs voor Playout, PPT, Jingles etc
<br />✅ 5-kanaals IFB routing met prefade listens
<br />❌ Automix
<br />❌ Gelamineerde tabel
<br />❌ Docs

### [Q-Lab (JingleMachine)](https://github.com/streammyevent/MasterPresets/tree/master/JingleMachine)

![incomplete](https://img.shields.io/badge/status-no%20docs-orange)
![version](https://img.shields.io/badge/version-1.0-green)

### [Atem](https://github.com/streammyevent/MasterPresets/tree/master/Atem)

![ready](https://img.shields.io/badge/status-ready-green)
![version](https://img.shields.io/badge/version-1.0-green)

✅ Standaard input en output mapping
<br />✅ SuperSource layouts met artwork
<br />✅ Macro's voor toewijzing van SuperSource layers
<br />✅ Macro's voor switchen tussen SuperSource layouts
<br />✅ 'Go playout' macro met dip to black en tie van DSK1
<br />❌ Gelamineerde tabel

### [Dante](https://github.com/streammyevent/MasterPresets/tree/master/Dante)

Not yet started.

### [V-Mix](https://github.com/streammyevent/MasterPresets/tree/master/V-Mix)

![incomplete](https://img.shields.io/badge/status-incomplete-orange)
![version](https://img.shields.io/badge/version-0.3-red)

✅ 8 caller remotes
<br />✅ SuperSource layouts
<br />❌ IFB Routing
<br />❌ Settings
<br />❌ Docs

[RFC ready](https://github.com/streammyevent/MasterPresets/blob/master/V-Mix/RFC.md)

### [SuperSources / Artwork](https://github.com/streammyevent/MasterPresets/tree/master/SuperSources)

![ready](https://img.shields.io/badge/status-ready-green)
![version](https://img.shields.io/badge/version-1.0-green)

✅ 19 verschillende SuperSource layouts in 16:9 en 4:3
<br />✅ Gespecificeerd met Pixel, Atem en V-Mix coordinaten
<br />✅ Template PNG files om naar de klant te sturen
<br />✅ Sketch file inbegrepen
<br />✅ Geïntegreerd in het Atem en V-Mix Master Preset

## Andere soorten presets

- **Productie Configs**: Backups van de configuratie aan het eind van de productie om toekomstige producties voor dezelfde klant sneller op te zetten.
- **Technische Configs**: Backups van configs op gedeployede apparatuur, bvb geïnstalleerde routers.
