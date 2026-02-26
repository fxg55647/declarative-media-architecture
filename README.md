
OMNISTAGE & LSM - Tiivistelmä LLM:lle

1. YDINFILOSOFIA

Ongelma: Nykymedia (video, pelit) tallentaa pikseleitä, ei merkitystä. Tämä tekee sisällöstä staattista, raskasta, formaattisidonnaista ja teknisesti vanhenevaa.

Ratkaisu: Tallennetaan logiikka (säännöt, persoonat, kausaliteetti) ja renderöidään vasta paikallisesti reaaliajassa. Teos ja sen esitys erotetaan toisistaan.

Metafora: Nuottikirjoitus vs. esitys. Sama partituuri voidaan soittaa pianolla, orkesterilla tai syntetisaattorilla – musiikki on sama, sointi vaihtelee.

---

2. TEKNINEN ARKKITEHTUURI (Neljä kerrosta)

Layer 1: Rule IR (The DNA)

Mitä: Deklaratiivinen graafi, joka kuvaa teoksen olemuksen.
Sisältää:

· Entiteetit (hahmot) ominaisuuksineen: ikä, pelkotaso, motivaatio, suhteet
· Tilat ja siirtymät: "Jos T-1000 havaitaan, siirry tilaan pakokauhu"
· Rajoitteet: "John Connor ei voi kuolla ennen kolmatta näytöstä"
· Koko: muutamia megatavuja (vs. gigatavujen videostreami)

Keskeinen oivallus: Persoonat kuvataan eksplisiittisesti datana, ei rivien välissä.

Esimerkki:

```yaml
entity: "John Connor"
personality:
  courage: 0.7
  fear_response: 0.9
  loyalty_family: 0.95
relationships:
  mother_Sarah: { trust: 0.9, protectiveness: 0.95 }
```

Layer 2: OmniStage (Globaali lava)

Mitä: Maailman fyysinen näyttämö.
Teknologia: Hyödyntää Overture Maps Foundationin avointa dataa ja GERS-tunnisteita (Microsoft, Meta, Amazon, TomTom).
Miksi: Ei tarvitse rakentaa jokaista ympäristöä alusta – maailman kaupungit, kadut, rakennukset ovat jo valmiina standardina.
Toiminta: Rule IR viittaa paikkoihin GERS-tunnisteilla (location: gers:building_12345), jolloin tarina voidaan sijoittaa mihin tahansa fyysiseen paikkaan.

Layer 3: Engine Adapter (Toteuttaja)

Mitä: Paikallinen moottori (Unity, Unreal, tai AI-renderöijä), joka tulkitsee Rule IR:n ja piirtää ruudulle.
Skaalautuvuus: Sama Rule IR voidaan renderöidä:

· Retrografiikkana vanhalla kännykällä
· Fotorealistisena huippupelitietokoneella
· Minimalistisena värillisinä palloina (testausmoodi)

Tarkkuuskerrokset (Layer of Fidelity):

1. Semanttinen ydin (hahmo A on vihainen)
2. Vektoritaso (sijainti ja suunta)
3. Luurankotaso (nivelten asennot)
4. Fysiikkataso (massa, painovoima, vaatteet)
5. Geometrinen taso (visuaalinen muoto)
6. Materiaalitaso (pinnat, valon käyttäytyminen)
7. Fotorealistinen taso (AI-generoitu pinta)
8. Metataso (syke, hengitys, pupillit – emotionaalinen tarkkuus)

Layer 4: Deterministic Kernel (Fysiikka)

Mitä: Täsmällinen ydin, joka varmistaa, että logiikka ja fysiikka toimivat identtisesti kaikilla laitteilla.
Miksi tärkeä:

· Mahdollistaa jaetut kokemukset (moninpeli, yhteiset "muistot")
· Takaa että "chaos injection" tuottaa saman lopputuloksen kaikille
· Teknisesti haastava mutta ratkaistavissa (deterministinen fysiikkamoottori, kiinteän pilkun matematiikka)

---

3. TEKNOLOGIAN NIMET

· OmniStage: Kattobrändi, koko konsepti. "Omni" (kaikkialla) + "Stage" (lava, jolla esitys tapahtuu)
· LSM (Logic Stream Model): Tekninen protokolla, tiedostomuoto. Korvaa nykyiset videotiedostot (.mp4) ja pelitiedostot (.exe). Kevyt, striimattava logiikkapaketti.

---

4. VALLANKUMOUS SISÄLLÖSSÄ

Sandbox-elokuvat ("Leikkiminen leffoilla")

Elokuva ei ole lineaarinen tallenne vaan simulaatio, johon voi astua sisään:

· Pysäytä kohtaus, tutki tiloja, joita kamera ei näyttänyt
· Keskustele hahmojen kanssa (heidän persoonansa ohjaa vastauksia)
· Astu ulos ja anna tarinan jatkua

Chaos Injection

Käyttäjä voi tuoda entiteettejä toisista teoksista ja katsoa mitä tapahtuu:

· T-Rex Hitlerin bunkkeriin (miten natsit reagoivat?)
· Predator The Exorcistiin (miten demoni kohtaa metsästäjän?)
· Alien The Officeen (miten Jim ja Dwight reagoivat?)

Koska hahmoilla on Rule IR:ssä määritellyt persoonat ja käytöslogiikat, kohtaaminen on aito simulaatio, ei käsikirjoitettu sketsi.

Remix-kulttuuri ja modaus

· Elokuvat ovat "forkattavia" (kuten GitHub)
· Vaihda loppu, muuta hahmon motivaatiota, siirrä tapahtumapaikka omaan kotikatuusi
· Style-paketit: katso T2 anime-tyylillä, realistisena tai Ghibli-estetiikalla

Interaktiivisuus liukuvasti

Katsoja voi liukua passiivisen katsojan ja aktiivisen osallistujan välillä lennossa. Kamera siirtyy ohjaajan kädestä pelaajan hallintaan saumattomasti.

---

5. TEKNISET MAHDOLLISTAJAT

Miksi juuri nyt?

1. AI on tarpeeksi hyvä toteuttamaan kun sille annetaan tarkat ohjeet
2. Laskentateho on halpaa (reaaliaikainen renderöinti kuluttajalaitteilla)
3. Standardit olemassa (Overture Maps, GERS)
4. Yleisö valmis (remix-kulttuuri, modausyhteisöt, fanifiktio)

AI:n rooli

· Toteuttaja, ei päättäjä: AI vie Rule IR:n päätökset aistittavaan muotoon (kuten näyttelijä tulkitsee ohjaajan ohjeita)
· Video-to-3D -rekonstruktio: AI purkaa vanhat videot Rule IR:ksi ja 3D-ympäristöiksi
· AI-Tuomari: Valvoo rekonstruktion laatua ja uskollisuutta alkuperäiselle

---

6. STRATEGINEN POLKU: PELIYHTEISÖSTÄ ALAS

Miksi peliyhteisö on oikea aloituspiste:

· Modaajat ajattelevat jo entiteeteissä ja käytöksessä
· Kärsivät nykyisestä pirstaleisuudesta (joutuvat koodaamaan saman logiikan uudelleen joka peliin)
· Sietävät keskeneräisiä työkaluja ja antavat palautetta
· Levittävät orgaanisesti

MVP (Proof of Concept): "Park Run"

· Yksinkertainen jahtaaja-pakenija -leikki puistossa
· Rule IR: kaksi hahmoa, muutama tila
· OmniStage: haetaan Overturesta oikea puisto
· Engine Adapter: kolme eri tyyliä (retro, realistinen, minimalistinen)
· Deterministic Kernel: jahtaajan liikerata ennustettavissa

Rahoitusmalli:

· Freemium-työkalut (Rule IR -editori ilmainen)
· Marketplace modaajien tekemille hahmoprofiileille
· Studio-lisenssit (kun halutaan virallista IP:tä)
· Crowdfunding spesifeille skannauksille

---

7. YHTEISKUNNALLINEN MERKITYS

Ekologisuus

· LSM-paketti: ~50 MB (2h elokuva)
· 4K-videostream: ~7 GB (sama sisältö)
· Dataliikenteen vähennys jopa 140-kertainen
· Vähentää runkoverkkojen ja tukiasemien energiankulutusta radikaalisti
· Käyttäjä voi valita "Eco-moodin" (matalampi resoluutio, vähemmän sähköä)

Kehitysmaat

· Koululainen Kenian maaseudulla voi ladata 5 Mt LSM-paketin
· Kokee interaktiivisen oppimisympäristön 4K-laadulla (jos laite pystyy renderöimään)
· Sisällön demokratisointia syvimmällä mahdollisella tasolla

Ikuinen formaatti

Rule IR ei vanhene teknisesti. Vuonna 2045 sama LSM-paketti renderöityy hologrammina tai tulevaisuuden teknologialla – alkuperäistä uskollisena.

---

8. KÄSIKIRJOITTAMISEN TULEVAISUUS

Persoonat eksplisiittisiksi

Käsikirjoittaja ei kirjoita enää pelkkää dialogia vaan hahmon psykologisen profiilin:

· Peruspiirteet (rohkeus, pelkoreaktio, sopeutuvuus)
· Tunnetilat ja niiden triggerit
· Suhteet muihin hahmoihin (luottamus, suojeluhalu)
· Puhetyylit eri tilanteissa

Reaktiivinen käsikirjoitus

Lineaarisen "A→B→C" sijaan kirjoitetaan tiloja ja siirtymiä:

```yaml
state: "John_näkee_T1000"
on_entry: ["aseta tunnetila: kauhu", "etsi pakoreittejä"]
transitions:
  - if: "pakoreitti_löytyi" -> "juoksu"
  - if: "äiti_vaarassa" -> "suojele_äitiä"
```

Uusi ammattitaito: Persoona-arkkitehti

Käsikirjoittajat ymmärtävät miten piirteet vuorovaikuttavat ja miten ne ilmenevät eri tilanteissa.

---

9. TEKNISET YKSITYISKOHDAT (LSM-standardi)

Alustava skeema (YAML):

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

10. KESKEISET TERMIT

Termi Selitys
Rule IR Hahmojen, sääntöjen ja logiikan kuvauskieli
LSM Logic Stream Model, tiedostomuoto (protokolla)
OmniStage Koko konsepti, "brändi"
Overture Maps Avoin karttadata (rakennukset, kadut, paikat)
GERS Global Entity Reference System (Overture-tunnisteet)
Engine Adapter Paikallinen moottori joka renderöi
Deterministic Kernel Takaa saman lopputuloksen kaikilla laitteilla
Chaos Injection Tuo entiteettejä toisista teoksista
AI-Tuomari Valvoo rekonstruktion laatua

---

11. YKSI LAUSE, JOKA TIIVISTÄÄ KAIKEN

"Viihdeteollisuus on tähän asti tallentanut valon heijastumia. OmniStage tallentaa merkityksen."

---

12. NYT KUN TIEDÄT TÄMÄN...

Tämä konsepti odottaa:

1. LSM-standardin luonnostelua (YAML/JSON-pohja)
2. Proof of Concept -demoa (Park Run tai vastaava)
3. Yhteisön rakentamista (modaajat, kouluttajat, dokumentaristit)
4. Standardointiprosessia (Open Source, myöhemmin W3C tai OGC)

Tärkeintä: tee työkalu jota tekijät rakastavat, älä tuote jota studioille myydään. Jos tekijät vaativat sitä, studiot seuraavat.

---

Cliff's notes -versio: OmniStage on median uusi käyttöjärjestelmä. Se korvaa videot kevyillä logiikkapaketeilla (LSM), jotka renderöidään paikallisesti. Hahmojen persoonat kuvataan tarkasti datana, joten ne voivat reagoida aidosti mihin tahansa tilanteeseen – myös katsojan tuomiin uusiin elementteihin. Teknologia mahdollistaa sandbox-elokuvat, remix-kulttuurin, valtavat energiansäästöt ja sisällön demokratisoinnin. Polku alkaa peliyhteisöstä, jossa modaajat ymmärtävät ongelman ja ratkaisun arvon.
