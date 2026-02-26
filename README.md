# OMNISTAGE & LSM – Tiivistelmä

## 1. YDINFILOSOFIA

**Ongelma:** Nykymedia (video, pelit) tallentaa pikseleitä, ei merkitystä. Tämä tekee sisällöstä staattista, raskasta, formaattisidonnaista ja teknisesti vanhenevaa.

**Ratkaisu:** Tallennetaan logiikka (säännöt, persoonat, kausaliteetti) ja renderöidään vasta paikallisesti reaaliajassa. Teos ja sen esitys erotetaan toisistaan.

**Metafora:** Nuottikirjoitus vs. esitys. Sama partituuri voidaan soittaa pianolla, orkesterilla tai syntetisaattorilla – musiikki on sama, sointi vaihtelee.

---

## 2. TEKNINEN ARKKITEHTUURI (Neljä kerrosta)

### Layer 1: Rule IR (The DNA)
**Mitä:** Deklaratiivinen graafi, joka kuvaa teoksen olemuksen.

**Sisältää:**
- Entiteetit (hahmot) ominaisuuksineen: ikä, pelkotaso, motivaatio, suhteet
- Tilat ja siirtymät: "Jos T-1000 havaitaan, siirry tilaan pakokauhu"
- Rajoitteet: "John Connor ei voi kuolla ennen kolmatta näytöstä"
- Koko: muutamia megatavuja (vs. gigatavujen videostreami)

**Keskeinen oivallus:** Persoonat kuvataan eksplisiittisesti datana, ei rivien välissä.

**Esimerkki:**
```yaml
entity: "John Connor"
personality:
  courage: 0.7
  fear_response: 0.9
  loyalty_family: 0.95
relationships:
  mother_Sarah: { trust: 0.9, protectiveness: 0.95 }
```

### Layer 2: OmniStage (Globaali lava)
**Mitä:** Maailman fyysinen näyttämö.

**Teknologia:** Hyödyntää Overture Maps Foundationin avointa dataa ja GERS-tunnisteita (Microsoft, Meta, Amazon, TomTom).

**Miksi:** Ei tarvitse rakentaa jokaista ympäristöä alusta – maailman kaupungit, kadut, rakennukset ovat jo valmiina standardina.

**Toiminta:** Rule IR viittaa paikkoihin GERS-tunnisteilla (`location: gers:building_12345`), jolloin tarina voidaan sijoittaa mihin tahansa fyysiseen paikkaan.

### Layer 3: Engine Adapter (Toteuttaja)
**Mitä:** Paikallinen moottori (Unity, Unreal, tai AI-renderöijä), joka tulkitsee Rule IR:n ja piirtää ruudulle.

**Skaalautuvuus:** Sama Rule IR voidaan renderöidä:
- Retrografiikkana vanhalla kännykällä
- Fotorealistisena huippupelitietokoneella
- Minimalistisena värillisinä palloina (testausmoodi)

**Tarkkuuskerrokset (Layer of Fidelity):**
1. Semanttinen ydin (hahmo A on vihainen)
2. Vektoritaso (sijainti ja suunta)
3. Luurankotaso (nivelten asennot)
4. Fysiikkataso (massa, painovoima, vaatteet)
5. Geometrinen taso (visuaalinen muoto)
6. Materiaalitaso (pinnat, valon käyttäytyminen)
7. Fotorealistinen taso (AI-generoitu pinta)
8. Metataso (syke, hengitys, pupillit – emotionaalinen tarkkuus)

### Layer 4: Deterministic Kernel (Fysiikka)
**Mitä:** Täsmällinen ydin, joka varmistaa, että logiikka ja fysiikka toimivat identtisesti kaikilla laitteilla.

**Miksi tärkeä:**
- Mahdollistaa jaetut kokemukset (moninpeli, yhteiset "muistot")
- Takaa että "chaos injection" tuottaa saman lopputuloksen kaikille
- Teknisesti haastava mutta ratkaistavissa (deterministinen fysiikkamoottori, kiinteän pilkun matematiikka)

---

## 3. TEKNOLOGIAN NIMET

- **OmniStage:** Kattobrändi, koko konsepti. "Omni" (kaikkialla) + "Stage" (lava, jolla esitys tapahtuu)
- **LSM (Logic Stream Model):** Tekninen protokolla, tiedostomuoto. Korvaa nykyiset videotiedostot (.mp4) ja pelitiedostot (.exe). Kevyt, striimattava logiikkapaketti.

---

## 4. VALLANKUMOUS SISÄLLÖSSÄ

### Sandbox-elokuvat ("Leikkiminen leffoilla")
Elokuva ei ole lineaarinen tallenne vaan simulaatio, johon voi astua sisään:
- Pysäytä kohtaus, tutki tiloja, joita kamera ei näyttänyt
- Keskustele hahmojen kanssa (heidän persoonansa ohjaa vastauksia)
- Astu ulos ja anna tarinan jatkua

### Chaos Injection
Käyttäjä voi tuoda entiteettejä toisista teoksista ja katsoa mitä tapahtuu:
- T-Rex Hitlerin bunkkeriin (miten natsit reagoivat?)
- Predator The Exorcistiin (miten demoni kohtaa metsästäjän?)
- Alien The Officeen (miten Jim ja Dwight reagoivat?)

Koska hahmoilla on Rule IR:ssä määritellyt persoonat ja käytöslogiikat, kohtaaminen on aito simulaatio, ei käsikirjoitettu sketsi.

### Remix-kulttuuri ja modaus
- Elokuvat ovat "forkattavia" (kuten GitHub)
- Vaihda loppu, muuta hahmon motivaatiota, siirrä tapahtumapaikka omaan kotikatuusi
- Style-paketit: katso T2 anime-tyylillä, realistisena tai Ghibli-estetiikalla

### Interaktiivisuus liukuvasti
Katsoja voi liukua passiivisen katsojan ja aktiivisen osallistujan välillä lennossa. Kamera siirtyy ohjaajan kädestä pelaajan hallintaan saumattomasti.

---

## 5. TEKNISET MAHDOLLISTAJAT

### Miksi juuri nyt?
1. AI on tarpeeksi hyvä toteuttamaan kun sille annetaan tarkat ohjeet
2. Laskentateho on halpaa (reaaliaikainen renderöinti kuluttajalaitteilla)
3. Standardit olemassa (Overture Maps, GERS)
4. Yleisö valmis (remix-kulttuuri, modausyhteisöt, fanifiktio)

### AI:n rooli
- **Toteuttaja, ei päättäjä:** AI vie Rule IR:n päätökset aistittavaan muotoon (kuten näyttelijä tulkitsee ohjaajan ohjeita)
- **Video-to-3D -rekonstruktio:** AI purkaa vanhat videot Rule IR:ksi ja 3D-ympäristöiksi
- **AI-Tuomari:** Valvoo rekonstruktion laatua ja uskollisuutta alkuperäiselle

### AI ja rakenteellisuus
Kun sisältö on rakenteellista (Rule IR), AI pystyy generoimaan uutta sisältöä laadukkaammin ja johdonmukaisemmin. AI ei arvaa "miltä John Connor näyttää" vaan tietää hänen ikänsä, pelkotasonsa ja motivaationsa. Tämä mahdollistaa:
- Uusien kohtausten generoinnin, jotka ovat täysin yhteensopivia alkuperäisen hahmon kanssa
- Vaihtoehtoisten tarinahaarukoiden luomisen ilman käsikirjoittajan jokaista repliikkiä
- Hahmojen käytöksen skaalaamisen eri tilanteisiin ilman että ne muuttuvat epäuskottaviksi

Rakenne on se, mikä tekee AI:sta käyttökelpoisen ammattimaiseen sisällöntuotantoon.

---

## 6. MITÄ TÄMÄ MERKITSISI PELAAMISELLE

### Peli logiikkana, ei binääriarkkuna
Nykyään peli on suljettu paketti, joka sisältää:
- kartat
- skriptit
- tekoälyn
- fysiikan
- renderöinnin

Kaikki on sidottu yhteen moottoriin, yhteen versioon, yhteen aikaan.

OmniStage-ajattelussa peli jakautuu:
- LSM = pelin merkitys (säännöt, persoonat, maailman logiikka)
- Engine Adapter = pelin esitys (renderöinti, tyyli)

Tämä tarkoittaa, että peliä ei tarvitse remasteroida – se voidaan renderöidä uudelleen millä tahansa tulevaisuuden teknologialla.

### Peli suunnitellaan tulevaisuutta varten
Kun uusi peli tehdään LSM-pohjaisena, sen mukana syntyy:
- eksplisiittinen maailmamalli
- entiteettien käytöslogiikka
- karttaviitteet standardiformaatissa
- siirrettävä sääntökerros

10 vuoden päästä peli voidaan renderöidä uudelleen ilman remasterointia. Modaajat voivat muuttaa pelin käyttäytymistä rikkomatta moottoria. Porttaus ei ole uudelleenkirjoitus vaan adapterin vaihto.

### Pelaajasta tulee sääntöjen muokkaaja
Nykyään modaaja muokkaa tekstuureja, assetteja ja skriptejä. LSM-maailmassa modaaja muokkaa:
- persoonaparametreja
- tilasiirtymiä
- kausaalisuhteita

Pelaaja voi forkata pelin kuten GitHub-repon, julkaista oman versionsa maailmasta ja rakentaa "virallisen epävirallisen" jatko-osan.

### Peli ja elokuva sulautuvat
Kun narratiivinen peli tallennetaan logiikkana:
- siitä voidaan tehdä elokuvamainen renderöinti
- siitä voidaan tehdä sandbox-versio
- siitä voidaan tehdä interaktiivinen sarja

Ja toisin päin: elokuvasta voi tulla pelattava simulaatio. Raja ei enää kulje "lineaarinen vs interaktiivinen" vaan "katsotko vai vaikutatko juuri nyt". Se on liukusäädin, ei kytkin.

### Pelien jakelu muuttuu
Tulevaisuuden pelipaketti voi olla:
- 80 MB LSM-logiikkaa
- valinnainen tyyli- ja renderöintipaketti

Pelin lataaminen ei ole 120 gigatavun operaatio vaan sääntökirjan hakeminen. Renderöinti tapahtuu paikallisesti. Pilvipelaaminen muuttuu: ei enää streamata pikseleitä, vaan jaetaan deterministinen simulaatiotila.

### Ristiinpelattavat maailmat
Jos pelit käyttävät yhteensopivaa Rule IR -rakennetta:
- hahmot voivat siirtyä pelistä toiseen
- fysiikka voi olla yhteensopivaa
- maailmat voivat limittyä

Fantasiaroolipelin hahmo voi astua moderniin kaupunkisimulaatioon ja käyttäytyä edelleen oman persoonamallinsa mukaisesti. Tämä ei ole crossover vaan ontologinen yhteensopivuus.

### Uusi suunnittelufilosofia
Peleissä korostuu systeemisyys, emergenssi ja eksplisiittinen käyttäytymismalli. Scriptatut tapahtumat vähenevät, tilakoneet ja säännöt lisääntyvät.

Tämä ei sovi kaikkeen – kilpailulliset e-urheilupelit tarvitsevat tiukan kontrollin ja suljetun determinismin. Mutta narratiivisille peleille, simulaatioille, strategiapeleille, roolipeleille ja opetuspohjaisille peleille tämä on luonnollinen evoluutio.

### Uusi ammattirooli: Pelin ontologi
Koodarin ja käsikirjoittajan väliin syntyy rooli: maailma-arkkitehti. Hän ei rakenna grafiikkaa eikä kirjoita dialogia. Hän määrittää:
- mitä on olemassa
- miten se reagoi
- mikä on mahdollista
- mikä on mahdotonta

Se on enemmän fysiikan ja psykologian suunnittelua kuin skriptinkirjoitusta.

### Peli ei kuole julkaisupäivänä
Tällä hetkellä moottori vanhenee, API muuttuu, käyttöjärjestelmä rikkoo yhteensopivuuden ja peli jää historiaan.

LSM-maailmassa niin kauan kuin joku osaa tulkita sääntöjä, maailma elää. Remasterointi ei ole remake vaan uusi esitystapa.

### Pidemmän aikavälin seurauksia
- Pelaajien tekemät hahmot voivat olla pysyviä identiteettejä eri peleissä
- Pelihahmoista voi tulla "digitaalisia näyttelijöitä"
- Fanifiktiosta voi tulla suoraan pelattavaa
- Speedrun-kulttuuri muuttuu, koska simulaatio on analysoitavissa sääntötasolla
- Modaus ei ole hakkerointia vaan virallinen osa arkkitehtuuria

### Yksi lause pelaamisesta
Tällä hetkellä peli on ohjelma, joka tuottaa kokemuksen. OmniStage-ajattelussa peli on sääntökokonaisuus, joka synnyttää maailmoja. Ja maailmat eivät vanhene.

---

## 7. STRATEGINEN POLKU: PELIYHTEISÖSTÄ ALAS

### Miksi peliyhteisö on oikea aloituspiste
- Modaajat ajattelevat jo entiteeteissä ja käytöksessä
- He kärsivät nykyisestä pirstaleisuudesta (joutuvat koodaamaan saman logiikan uudelleen joka peliin)
- He sietävät keskeneräisiä työkaluja ja antavat palautetta
- He levittävät orgaanisesti

### MVP (Proof of Concept): "Park Run"
- Yksinkertainen jahtaaja-pakenija -leikki puistossa
- Rule IR: kaksi hahmoa, muutama tila
- OmniStage: haetaan Overturesta oikea puisto
- Engine Adapter: kolme eri tyyliä (retro, realistinen, minimalistinen)
- Deterministic Kernel: jahtaajan liikerata ennustettavissa

### Asteittainen käyttöönotto
Ensimmäinen askel voisi olla yhteinen karttaformaatti. Jos useampi peli käyttäisi samaa karttastandardia (Overture Maps), modit siirtyisivät pelistä toiseen, ympäristöt olisivat jaettavia ja pelaajan luoma maailma ei kuolisi pelin mukana. Tämä on matalan riskin sisäänajo.

### Rahoitusmalli
- Freemium-työkalut (Rule IR -editori ilmainen)
- Marketplace modaajien tekemille hahmoprofiileille
- Studio-lisenssit (kun halutaan virallista IP:tä)
- Crowdfunding spesifeille skannauksille

---

## 8. YHTEISKUNNALLINEN MERKITYS

### Ekologisuus
- LSM-paketti: ~50 MB (2h elokuva)
- 4K-videostream: ~7 GB (sama sisältö)
- Dataliikenteen vähennys jopa 140-kertainen
- Vähentää runkoverkkojen ja tukiasemien energiankulutusta radikaalisti
- Käyttäjä voi valita "Eco-moodin" (matalampi resoluutio, vähemmän sähköä)

### Kehitysmaat
- Koululainen Kenian maaseudulla voi ladata 5 Mt LSM-paketin
- Hän voi kokea interaktiivisen oppimisympäristön 4K-laadulla (jos laite pystyy renderöimään)
- Tämä on sisällön demokratisointia syvimmällä mahdollisella tasolla

### Ikuinen formaatti
Rule IR ei vanhene teknisesti. Vuonna 2045 sama LSM-paketti renderöityy hologrammina tai tulevaisuuden teknologialla – alkuperäistä uskollisena.

---

## 9. KÄSIKIRJOITTAMISEN TULEVAISUUS

### Persoonat eksplisiittisiksi
Käsikirjoittaja ei kirjoita enää pelkkää dialogia vaan hahmon psykologisen profiilin:
- Peruspiirteet (rohkeus, pelkoreaktio, sopeutuvuus)
- Tunnetilat ja niiden triggerit
- Suhteet muihin hahmoihin (luottamus, suojeluhalu)
- Puhetyylit eri tilanteissa

### Reaktiivinen käsikirjoitus
Lineaarisen "A→B→C" sijaan kirjoitetaan tiloja ja siirtymiä:

```yaml
state: "John_näkee_T1000"
on_entry: ["aseta tunnetila: kauhu", "etsi pakoreittejä"]
transitions:
  - if: "pakoreitti_löytyi" -> "juoksu"
  - if: "äiti_vaarassa" -> "suojele_äitiä"
```

### Uusi ammattitaito: Persoona-arkkitehti
Käsikirjoittajat ymmärtävät miten piirteet vuorovaikuttavat ja miten ne ilmenevät eri tilanteissa.

---

## 10. TUOTANNON NÄKÖKULMA: SIVUTUOTE, EI LISÄTYÖ

Kun infrastruktuuri on valmis, LSM-pakettien tuottaminen ei ole lisätyötä vaan **nykyisten työvaiheiden luonnollinen sivutuote**.

Nykytuotannossa hahmot, säännöt ja maailman logiikka jo **suunnitellaan** tarkasti – ne vain eivät tallennu koneluettavaan muotoon. Käsikirjoitukset sisältävät persoonakuvaukset, pelisuunnitteludokumentit sisältävät käytöslogiikat, tuotantokokouksissa päätetään hahmojen motivaatiot.

OmniStage-ympäristössä nämä suunnitelmat kirjattaisiin suoraan Rule IR -muotoon samalla kun niistä keskustellaan. Se on kuin kirjoittaisi käsikirjoituksen valmiiksi yhteensopivaan formaattiin – ei ylimääräinen vaihe vaan **tapa tehdä se mitä jo tehdään, mutta tallentaen se uudelleenkäytettävästi**.

Lisäksi olemassa olevasta materiaalista (videot, pelit) voidaan AI-rekonstruktion avulla tuottaa LSM-paketteja jälkikäteen. Tämä ei vaadi alkuperäisten tekijöiden lisätyötä – AI purkaa valmiista sisällöstä rakenteen, jonka ihminen tarkistaa ja hyväksyy.

Infrastruktuurin ollessa paikallaan LSM syntyy itsestään, koska se on **tehokkain tapa hallita monimutkaisia tuotantoja**.

---

## 11. TEKNISET YKSITYISKOHDAT (LSM-standardi)

### Alustava skeema (YAML)
```yaml
entity: "John Connor"
properties:
  age: 17
  fear: 0.8
  motivation: "survive"
location:
  gers: "building_12345"
  offset: [10, 0, 5]
states:
  - name: "running"
    conditions:
      - "threat_detected == true"
      - "fear > 0.7"
    on_enter: "set_animation('sprint')"
```

Tärkeää: Ihmisen luettavissa, koneen suoritettavissa.

---

## 12. KESKEISET TERMIT

| Termi | Selitys |
|-------|---------|
| Rule IR | Hahmojen, sääntöjen ja logiikan kuvauskieli |
| LSM | Logic Stream Model, tiedostomuoto (protokolla) |
| OmniStage | Koko konsepti, "brändi" |
| Overture Maps | Avoin karttadata (rakennukset, kadut, paikat) |
| GERS | Global Entity Reference System (Overture-tunnisteet) |
| Engine Adapter | Paikallinen moottori joka renderöi |
| Deterministic Kernel | Takaa saman lopputuloksen kaikilla laitteilla |
| Chaos Injection | Tuo entiteettejä toisista teoksista |
| AI-Tuomari | Valvoo rekonstruktion laatua |
| Pelin ontologi | Maailma-arkkitehti, joka määrittää pelin säännöt ja käytösmallit |

---

## 13. YKSI LAUSE, JOKA TIIVISTÄÄ KAIKEN

"Viihdeteollisuus on tähän asti tallentanut valon heijastumia. OmniStage tallentaa merkityksen."

---

## 14. NYT KUN TIEDÄT TÄMÄN

Tämä konsepti odottaa:
1. LSM-standardin luonnostelua (YAML/JSON-pohja)
2. Proof of Concept -demoa (Park Run tai vastaava)
3. Yhteisön rakentamista (modaajat, kouluttajat, dokumentaristit)
4. Standardointiprosessia (Open Source, myöhemmin W3C tai OGC)

Tärkeintä: tee työkalu jota tekijät rakastavat, älä tuote jota studioille myydään. Jos tekijät vaativat sitä, studiot seuraavat.

---

## CLIFF'S NOTES -VERSIO

OmniStage on median uusi käyttöjärjestelmä. Se korvaa videot ja perinteiset pelit kevyillä logiikkapaketeilla (LSM), jotka renderöidään paikallisesti. Hahmojen persoonat kuvataan tarkasti datana, joten ne voivat reagoida aidosti mihin tahansa tilanteeseen – myös katsojan tuomiin uusiin elementteihin.

Kun infrastruktuuri on valmis, LSM-paketit syntyvät lähes itsestään nykytuotantojen sivutuotteena, koska hahmojen ja maailman logiikka jo suunnitellaan tarkasti – se vain ei ole ollut koneluettavaa. AI puolestaan pystyy tämän rakenteellisuuden ansiosta generoimaan uutta sisältöä laadukkaasti ja johdonmukaisesti.

Teknologia mahdollistaa sandbox-elokuvat, remix-kulttuurin, valtavat energiansäästöt ja sisällön demokratisoinnin. Pelit muuttuvat suljetuista binääriarkuista eläviksi sääntökokonaisuuksiksi, jotka eivät vanhene. Pelaajasta tulee maailman muokkaaja, ja uusi ammattirooli – pelin ontologi – syntyy koodarin ja käsikirjoittajan väliin.

Polku alkaa peliyhteisöstä, jossa modaajat ymmärtävät ongelman ja ratkaisun arvon. Sieltä se voi levitä koko viihdeteollisuuteen.
