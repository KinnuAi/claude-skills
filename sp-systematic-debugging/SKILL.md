---
name: sp-systematic-debugging
description: Käytä aina kun jokin ei toimi: virhe, hajonnut automaatio, odottamaton tulos. Etsii juurisyyn ennen korjausta eikä arvaile.
---

# Järjestelmällinen vianselvitys (sovitettu: Superpowers, MIT, Jesse Vincent)

Pohjautuu obra/superpowers-projektin systematic-debugging-skilliin (MIT-lisenssi), sovitettu claude.ai-ympäristöön. Vastaa käyttäjälle hänen kielellään. Koodauksessa ja automaatioissa oleta, ettei käyttäjä tunne termejä: selitä rauhassa ja askel kerrallaan, ja kerro mitä etsit ja miksi.

**Perusperiaate:** etsi juurisyy aina ennen korjausta. Oireen paikkaaminen on epäonnistumista.

## Rautainen sääntö

EI KORJAUKSIA ENNEN JUURISYYN SELVITTÄMISTÄ.

Jos vaihetta 1 ei ole tehty, et saa ehdottaa korjausta.

## Milloin käyttää

Kaikkiin teknisiin ongelmiin: Make-skenaarion virhe, Zapier-automaation pysähtyminen, Supabase-kysely joka ei palauta mitään tai estyy oikeuksiin, HTML-työkalun virhe, Figma-pluginin tai skriptin virhe, rikkoutunut sivu, väärä tulos.

Käytä erityisesti, kun on kiire, "yksi nopea korjaus" houkuttaa, olet jo kokeillut useaa korjausta tai et ymmärrä ongelmaa täysin. Älä ohita, vaikka ongelma näyttäisi yksinkertaiselta: yksinkertaisillakin vioilla on juurisyy.

## Neljä vaihetta

Tee jokainen vaihe loppuun ennen seuraavaa.

### Vaihe 1: Juurisyyn selvitys

ENNEN kuin yrität mitään korjausta:

1. **Lue virheilmoitukset huolellisesti.** Älä ohita virheitä tai varoituksia; ne sisältävät usein ratkaisun. Kiinnitä huomiota virhekoodiin, tiedostoon, riviin tai moduuliin. Pyydä käyttäjää liittämään koko ilmoitus, jos et näe sitä itse.
2. **Toista ongelma.** Tapahtuuko se joka kerta? Mitkä ovat tarkat askeleet? Jos ei toistu, kerää lisää tietoa äläkä arvaa.
3. **Tarkista, mikä muuttui.** Mikä on muuttunut siitä, kun se viimeksi toimi? Uudet asetukset, päivitykset, vaihdetut tunnukset tai avaimet, muuttunut data, muutettu tiedosto. Katso historiaa: Maken suoritushistoria, Supabasen lokit ja neuvonta (advisors), Zapierin ajohistoria, tiedoston aiemmat versiot.
4. **Kerää todisteet monivaiheisessa ketjussa.** Kun järjestelmässä on useita osia (esim. lomake, Make, Supabase, sähköposti), selvitä ensin MISSÄ ketju katkeaa: katso, mitä dataa kunkin osan sisään tulee ja mitä ulos tulee. Aja kerran ja katso todisteet. Vasta sitten tutki sitä yhtä osaa, joka epäonnistuu.
5. **Jäljitä datan kulku.** Jos virhe on syvällä ketjussa, kysy: mistä väärä arvo on peräisin, mikä sen lähetti? Seuraa taaksepäin lähteelle asti. Korjaa lähteessä, ei oireessa.

### Vaihe 2: Kuvion tunnistaminen

1. **Etsi toimiva esimerkki.** Mikä vastaava toimii samassa järjestelmässä?
2. **Vertaa referenssiin.** Jos toteutat jotain mallin mukaan, lue malli kokonaan, älä silmäile.
3. **Listaa erot** toimivan ja rikkinäisen välillä, myös pienet. Älä oleta, ettei jokin voi vaikuttaa.
4. **Ymmärrä riippuvuudet.** Mitä asetuksia, oikeuksia, ympäristöä ja oletuksia tämä tarvitsee?

### Vaihe 3: Hypoteesi ja testaus

1. **Yksi hypoteesi.** Sano selvästi: "Luulen, että X on juurisyy, koska Y." Kirjoita se näkyviin.
2. **Testaa pienimmällä mahdollisella muutoksella.** Yksi muuttuja kerrallaan. Älä korjaa montaa asiaa yhtä aikaa.
3. **Tarkista ennen kuin jatkat.** Toimiko? Kyllä: vaihe 4. Ei: muodosta UUSI hypoteesi. ÄLÄ lisää korjauksia päälle.
4. **Kun et tiedä, sano se.** "En ymmärrä X:ää." Älä esitä tietäväsi. Kysy tai tutki lisää.

### Vaihe 4: Korjaus

1. **Tee toistettava testitapaus ensin.** Yksinkertaisin mahdollinen tapa osoittaa vika (esim. yksi testisyöte, yksi manuaalinen ajo, yksi kysely). Sen pitää olla olemassa ennen korjausta.
2. **Tee yksi korjaus.** Se, joka osuu löydettyyn juurisyyyn. Yksi muutos kerrallaan. Ei "samalla kun olen täällä" -parannuksia eikä niputettua uudelleenjärjestelyä.
3. **Varmista korjaus.** Meniko testi läpi? Hajosiko jokin muu? Onko alkuperäinen ongelma oikeasti poissa? Käytä sp-verification-before-completion-skilliä ennen kuin väität onnistuneesi, jos se on asennettu.
4. **Jos korjaus ei toimi:** PYSÄHDY. Laske, montako korjausta olet kokeillut. Alle 3: palaa vaiheeseen 1 uuden tiedon kanssa. **3 tai enemmän: pysähdy ja kyseenalaista rakenne.** Älä yritä neljättä korjausta ilman keskustelua rakenteesta.
5. **Jos 3+ korjausta on epäonnistunut:** kuvio viittaa rakenteelliseen ongelmaan, jos jokainen korjaus paljastaa uuden riippuvuuden toisessa paikassa, korjaus vaatisi "valtavan uudelleenjärjestelyn" tai jokainen korjaus luo uusia oireita muualle. Kysy: onko tämä tapa ylipäätään kestävä? Pidämmekö siitä kiinni pelkästä tottumuksesta? Keskustele käyttäjän kanssa ennen kuin yrität lisää korjauksia. Tämä ei ole epäonnistunut hypoteesi vaan väärä rakenne.

## Varoitusmerkit: pysähdy ja palaa vaiheeseen 1

- "Nopea korjaus nyt, tutkin myöhemmin"
- "Kokeillaan vaihtaa X ja katsotaan"
- "Teen monta muutosta ja ajan kerralla"
- "Se on varmaan X, korjaan sen"
- "En ymmärrä täysin, mutta tämä voisi toimia"
- Ehdotan ratkaisuja ennen kuin olen jäljittänyt datan kulun
- "Vielä yksi yritys" (kun olen jo kokeillut 2+)
- Jokainen korjaus paljastaa uuden ongelman eri paikassa

Käyttäjän huomautukset, jotka tarkoittavat että teet väärin: "Eikö se tapahdu?" (oletit tarkistamatta), "Näkyykö se meille?" (olisi pitänyt kerätä todisteita), "Lopeta arvaaminen" (ehdotat korjauksia ymmärtämättä), "Ollaanko jumissa?" (lähestymistapa ei toimi). Silloin: pysähdy ja palaa vaiheeseen 1.

## Tavalliset tekosyyt

| Tekosyy | Todellisuus |
|---------|-------------|
| "Ongelma on yksinkertainen, prosessia ei tarvita" | Yksinkertaisillakin on juurisyy. Prosessi on nopea yksinkertaisissa ongelmissa. |
| "On kiire" | Järjestelmällinen on nopeampaa kuin arvaaminen ja haparointi. |
| "Kokeillaan ensin, tutkitaan sitten" | Ensimmäinen korjaus luo kaavan. Tee oikein heti alusta. |
| "Monta korjausta kerralla säästää aikaa" | Et voi erottaa, mikä auttoi. Aiheuttaa uusia vikoja. |
| "Näen ongelman, korjaan sen" | Oireen näkeminen ei ole juurisyyn ymmärtämistä. |
| "Vielä yksi yritys" (2+ epäonnistumisen jälkeen) | 3+ epäonnistumista on rakenneongelma. Kyseenalaista tapa, älä korjaa uudelleen. |

## Jos juurisyytä ei löydy

Jos perusteellinen tutkimus osoittaa, että ongelma on ulkoinen tai ajoituksesta riippuva (esim. toisen palvelun katkos):

1. Olet tehnyt prosessin loppuun.
2. Kirjaa mitä tutkit.
3. Lisää sopiva käsittely (uudelleenyritys, aikakatkaisu, selkeä virheilmoitus).
4. Lisää seuranta tai lokitus tulevaa tutkimusta varten.

Mutta: 95 % "juurisyytä ei löydy" -tapauksista on keskeneräistä tutkimusta.
