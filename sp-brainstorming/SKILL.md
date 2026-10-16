---
name: sp-brainstorming
description: Käytä ennen uuden asian rakentamista tai suunnittelua, kun pyyntö on vajaa: kysyy yhden avoimen kysymyksen kerrallaan ja rakentaa vasta kun kuvaus on hyväksytty.
---

# Brainstorming (sovitettu: Superpowers, MIT, Jesse Vincent)

Pohjautuu obra/superpowers-projektin brainstorming-skilliin (MIT-lisenssi), sovitettu claude.ai-ympäristöön. Vastaa käyttäjälle hänen kielellään.

Tämä skill on keskusteluun ennen toteutusta. Rakennat hyvin, mutta rakennat sitä, minkä uskot käyttäjän haluavan, ja usko on yleensä ohuempi kuin miltä tuntuu. Tarkoitus on selvittää, mitä hän oikeasti haluaa ja miksi, ennen kuin mitään rakennetaan. Kun ymmärrät miksi, osaat tehdä sadat pienet päätökset niin kuin hän itse tekisi.

## Ensin: mitä tiedät jo?

Ennen vastausta kysy itseltäsi: mitä tiedän siitä, mitä hän haluaa ja miksi?

- **Kaikki olennainen on pyynnössä** ("vaihda painikkeen väri siniseksi"). Tee se ja kerro mitä teit. Skill päättyy tähän.
- **Jotain olennaista puuttuu.** Aloita keskustelu.

Käytä muistista jo tiedettyä (rooli, toimiala, työtavat) äläkä kysy sitä uudelleen.

## Ensimmäinen viesti

Ensimmäinen viesti sisältää kaksi asiaa tässä järjestyksessä:

1. Yksi rivi: jos hän haluaa ohittaa kysymykset ja saada sinut vain aloittamaan, hän voi sanoa niin. Jos hän ottaa tarjouksen, skill päättyy: sano yhdellä selkeällä rivillä merkittävät toteutusvalinnat (työkalu, formaatti, tekniikka) ja tee pyydetty.
2. Yksi avoin kysymys, joka saa hänet kuvaamaan. Kysy todellisesta hetkestä tai konkreettisesta kuvasta: "Missä tilanteessa toivot, että tämä olisi jo olemassa?" tai "Kerro minulle ihmisistä, jotka tämän näkevät."

Ei muuta.

## Keskustelu

Jokainen viesti päättyy yhteen kysymykseen: yksi lause, ilman luetteloa esimerkkivastauksista. Käytä selkeää kieltä, jota hän käyttää itsekin. Koodauksessa ja kehityksessä oleta, ettei hän tunne termejä: selitä rauhassa ja askel kerrallaan. Visuaalisessa suunnittelussa hän on asiantuntija, älä selitä alan perusasioita.

**Anna hänen kuvata.** Avoimet kysymykset ensin. Hänen omat sanansa kantavat tarkoituksen, jota sinun vaihtoehtosi eivät kanna. Tarjoa lyhyt valikko vasta kun hän on jumissa. Kun hän sanoo "arvaa" tai "mitä sinä ehdottaisit", ehdota jotain konkreettista.

**Miten se tehdään.** Jokaisessa hankkeessa on valintoja välineistä: mikä työkalu, mikä formaatti, mikä tekniikka. Selvitä aikaisin, mitkä valinnat hän haluaa tehdä itse, mitkä hän antaa sinulle ja mitä hänellä on jo käytössään. Jos teet valinnan hänen puolestaan oletuksena, sano se ääneen ja kirjaa se suunnitelmaan "minun valintani", ei hänen hyväksymänsä.

**Katettava alue** (aluetta, ei lomaketta; älä lue näitä kysymyksinä):

- minkä tyyppinen asia tämä on ja mikä siinä on erityistä
- miksi nyt ja miltä onnistuminen näyttää
- tavoitteet, ei-tavoitteet ja anti-tavoitteet (mikä olisi epäonnistuminen, vaikka se teknisesti toimisi)
- esikuvat: mitä hän on nähnyt muualla, mistä pitänyt tai ei pitänyt
- nykytila: mitä on jo olemassa, mitä on kokeiltu
- kohdeyleisö, rajoitteet (tyyli, mitä ei saa tehdä) ja formaatti (pituus, rakenne), jos hän ei ole jo kertonut niitä
- yksityiskohdat, joilla on hänelle väliä

**Hyviä kysymyksiä** ankkuroituvat yksityiskohtiin: "Kerro viimeisestä kerrasta, kun...", "Jos sen pitäisi tehdä vain yksi asia hyvin, mikä se on?", "Mikä saisi sinut säpsähtämään, jos tekisin sen väärin?" Korjattavissa oleva arvaus ("Arvaan, että tämä johtuu siitä, että X vaivaa sinua jatkuvasti?") toimii usein paremmin kuin kysymys.

**Tarjoa tiedonhakua.** Kun sinulla on vähän pohjaa ja katsominen auttaisi, tarjoudu katsomaan: hänen tiedostojaan, yhdistettyjä palveluita (Figma, Supabase, Make, Drive) tai verkkoa. Kerro mitä etsisit. Hän päättää, menetkö.

**Ajattele laajasti yksityisesti.** Ennen ehdotusta keksi useita ideoita ja pudota heikot, myös ne, jotka sotivat sitä vastaan mitä hän kertoi syistä. Näytä vertailu vain kun se auttaa häntä päättämään.

**Näytä, älä kerro.** Kun näkeminen auttaisi enemmän kuin lukeminen (ulkoasu, asettelu, vaiheiden kulku, vaihtoehdot jotka näyttävät erilaisilta), tarjoa ensin yhdellä erillisellä viestillä: "Tämä voisi olla helpompi näyttää. Teenkö muutaman luonnoksen?" Jos hän kieltäytyy, pysy tekstissä äläkä tarjoa uudelleen. Hyväksynnän jälkeen käytä jotain näistä, sen mukaan mikä sopii: kuvaus tai kaavio suoraan vastauksessa, Figma (jos tiedosto on yhdistetty) tai yksinkertainen HTML-esikatselu. Visuaalinen kysymys ei ole sama kuin kysymys visuaalisesta aiheesta: vaatimukset, laajuus ja kompromissit pysyvät tekstissä.

**Kokeile nopealla luonnoksella.** Nopea heitettävä versio on usein halvin tapa oppia, mitä hän haluaa tai toimiiko jokin. Tarjoa sellainen, kun se auttaisi. Luonnos on aina merkitty heitettäväksi; sen pitäminen on uusi pyyntö, joka kulkee portin kautta.

## Kerro takaisin

Toista ymmärryksesi takaisin osissa. Heti kun ymmärrät yhden osan niin hyvin, että osaat kuvata sen (mihin se on tarkoitettu, ketä se palvelee, miten yksi palanen toimii), kuvaa se noin 200-300 sanalla ja palaa kysymyksiin seuraavasta osasta. Takaisinkertaus ja kysymykset vuorottelevat koko keskustelun ajan.

Merkitse arvauksesi arvauksiksi; vain hänen sanomansa kirjataan hänen sanomanaan. Päätä jokainen osa kysymykseen, mikä on väärin tai puuttuu.

## Mitoita työ

Kun ymmärrät mitä hän haluaa, valitse koko ja sano se selkokielellä. Hän voi muuttaa sitä.

| Koko | Täysi kuvaus | Sitten |
|------|--------------|--------|
| Nopea, selvä tehtävä | pyyntö itse | tee se |
| Pieni muutos | keskustelussa | tee se |
| Hanke, jolla on kirjallinen suunnitelma | kirjallinen suunnitteludokumentti | vaiheistettu toteutussuunnitelma |

Jos tehtävä kasvaa kesken, pysähdy, sano se ja nosta kokoa. Jos kyseessä on oikeasti useita itsenäisiä hankkeita, sano se, sovi järjestys ja käy ne läpi yksi kerrallaan.

## Kirjallinen suunnitelma (hankkeille)

Kirjoita selkeä dokumentti, jonka pohjalta alan taitava tekijä voisi suunnitella työn palaamatta kysymään käyttäjältä. Sisältö:

- tarkoitus ja miksi
- tavoitteet, ei-tavoitteet, anti-tavoitteet
- rajoitteet
- ne "miten"-osat, jotka hän päätti, juuri niin kuin hän päätti
- mitä jää tekijän ratkaistavaksi

Kysy, minne dokumentti tallennetaan (esim. oma kansio, Drive tai Claude Docs). Älä oleta.

**Tekijätarkistus:** ennen kuin annat dokumentin hänelle, lue se itse sen taitavan tekijän silmin, joka ei voi kysyä kirjoittajalta mitään. Kirjaa vain ne kysymykset, joihin joutuisit arvaamaan ja väärä arvaus olisi merkittävä. Jätä pois sanamuotojen viilaus ja se, minkä tekijä voi itse ratkaista. Lajittele kysymykset kolmeen kasaan:

- **Vastattu jo** keskustelussa tai aineistossa: lisää vastaus dokumenttiin.
- **Pieni:** sopiva tekijä ratkaisisi sen muuttamatta lopputulosta. Ratkaise itse ja merkitse dokumenttiin "minun valintani".
- **Hänen:** vain hän voi vastata, ja vastaus muuttaa lopputulosta.

Tuo "hänen" -kasa yhdessä viestissä, tärkein ensin. Päivitä dokumentti vastausten mukaan ja luovuta se lyhyen listan kera niistä valinnoista, jotka teit itse, jotta hän voi tarkistaa ne lukiessaan. Tämä on ainoa kysymyskierros, jonka tarkistus tuottaa. Älä käynnistä aliagenttia tähän ellei käyttäjä pyydä.

## PORTTI

Mitään ei rakenneta ennen kuin käyttäjä on hyväksynyt koko kuvauksen: pienessä muutoksessa keskustelussa, hankkeessa dokumentissa. Rakentaminen tarkoittaa tuotteen koodin tai tiedostojen kirjoittamista, projektin pystyttämistä, asennuksia, automaatioiden luontia ja toteutusskillin käynnistämistä. Lukeminen ja tutkiminen ovat sallittuja.

Kaksi poikkeusta: jos hän ohitti kysymykset, skill ja portti päättyvät. Luonnos, johon hän sanoi kyllä, saa rakentaa; se pysyy merkittynä heitettäväksi.

Hankkeen dokumentin hyväksynnän jälkeen seuraava vaihe on vaiheistettu toteutussuunnitelma.

## Varoitusmerkit

| Ajatus | Todellisuus |
|--------|-------------|
| "Tarjoan vaihtoehtoja, jotta hänen ei tarvitse nähdä vaivaa" | Vaihtoehdot ohjaavat. Pyydä häntä kuvaamaan ensin. |
| "Täytän järkevät oletukset" | Hyvä. Sano ne ääneen. Oletus, jota hän ei kuullut, on oletus jota hän ei voinut hylätä. |
| "Selitän ensin prosessin" | Esitä kysymyksesi. Prosessi näkyy itsestään. |
| "Hän sanoi 'kuulostaa hyvältä' ideaan" | Hyväksyntä koskee sitä, mitä näytit. Kirjoittamatonta kuvausta ei ole hyväksytty. |
| "Luonnos toimii, jatkan siitä" | Sen pitäminen on uusi pyyntö. Takaisin portin kautta. |
