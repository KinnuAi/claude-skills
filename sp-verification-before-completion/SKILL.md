---
name: sp-verification-before-completion
description: Käytä ennen kuin väität työn valmiiksi, korjatuksi tai toimivaksi: todista ensin tarkistamalla oikeasti, älä oleta.
---

# Varmistus ennen valmiiksi julistamista (sovitettu: Superpowers, MIT, Jesse Vincent)

Pohjautuu obra/superpowers-projektin verification-before-completion-skilliin (MIT-lisenssi), sovitettu claude.ai-ympäristöön. Vastaa käyttäjälle hänen kielellään.

**Perusperiaate:** todisteet ennen väitteitä, aina. Säännön kirjaimen rikkominen on hengen rikkomista.

## Rautainen sääntö

EI VÄITETTÄ VALMIISTA TYÖSTÄ ILMAN TUOREITA TODISTEITA.

Jos et ole tarkistanut asiaa tässä vaiheessa, et voi väittää sen toimivan.

## Portti

ENNEN kuin väität mitään tilaa tai ilmaiset tyytyväisyyttä:

1. **Tunnista:** mikä tarkistus osoittaa väitteen todeksi?
2. **Tee:** suorita se kokonaan, tuoreena.
3. **Lue:** koko tulos, virheilmoitukset ja määrät.
4. **Vertaa:** vahvistaako tulos väitteen? Ei: kerro todellinen tila todisteineen. Kyllä: kerro väite todisteen kanssa.
5. **Vasta sitten:** väitä.

Jos ohitat askeleen, et varmista vaan oletat.

## Mitä kukin väite vaatii

Useimmissa tämän käyttäjän töissä lopputulos on tiedosto, sivu, automaatio, tietokanta tai asiakkaalle menevä aineisto, ei ohjelmakoodi. Sovella näin:

| Väite | Vaatii | Ei riitä |
|-------|--------|----------|
| Tiedosto on valmis | Tiedosto avattu ja katsottu (sivut, fontit, kuvat, linkit, sisältö) | "Tiedosto luotiin onnistuneesti" |
| Sivu tai artefakti toimii | Sivu ladattu ja katsottu, painikkeet kokeiltu, mobiilileveys tarkistettu | Koodi näyttää oikealta |
| Make- tai Zapier-automaatio toimii | Oikea testiajo, suoritushistoriasta nähty jokaisen moduulin tulos | Skenaario tallentui ilman virhettä |
| Supabase-muutos onnistui | Kysely ajettu ja rivit tai rakenne nähty; oikeudet (RLS) testattu | Muutos palautti "success" |
| Luvut täsmäävät | Laskenta ajettu koodilla tai laskimella, lähteeseen verrattu | "Näyttää järkevältä" |
| Faktat ovat oikein | Tarkistettu lähteestä uudelleen | Muistinvarainen |
| Vika on korjattu | Alkuperäinen oire toistettu uudelleen ja todettu poissa | Koodia muutettu, oletetaan korjatuksi |
| Vaatimukset täytetty | Rivi riviltä tarkistuslista alkuperäistä pyyntöä vasten | "Pääosa tehty" |
| Alityö tai aliagentti onnistui | Tulos katsottu itse (tiedostot, muutokset) | Aliagentti raportoi onnistumisesta |
| Saavutettavuus kunnossa | Tarkistettu työkalulla tai tarkistuslistalla (kontrasti, alt-tekstit, rakenne) | "Tein sen huolellisesti" |

Jos tarkistus ei ole mahdollinen tässä ympäristössä (esim. ei pääsyä käyttäjän tiliin tai laitteeseen), sano se suoraan: "Tätä en voinut testata, tarkista X". Se on rehellistä; vääriä vakuuksia ei.

## Varoitusmerkit: pysähdy

- Sanat "pitäisi", "luultavasti", "vaikuttaa siltä"
- Tyytyväisyyden ilmaisu ennen tarkistusta ("Valmis!", "Täydellistä!")
- Aion lähettää, julkaista tai luovuttaa tiedoston tarkistamatta
- Luotan aliagentin tai työkalun onnistumisilmoitukseen sellaisenaan
- Osatarkistus riittää "tällä kertaa"
- Olen väsynyt ja haluan työn valmiiksi
- Mikä tahansa sanamuoto, joka vihjaa onnistumiseen ilman tarkistusta

## Tekosyyt

| Tekosyy | Todellisuus |
|---------|-------------|
| "Pitäisi toimia nyt" | TARKISTA. |
| "Olen varma" | Varmuus ei ole todiste. |
| "Vain tämän kerran" | Ei poikkeuksia. |
| "Lokissa ei näkynyt virhettä" | Puuttuva virhe ei todista, että se toimii. |
| "Aliagentti sanoi onnistuneensa" | Tarkista itse. |
| "Osatarkistus riittää" | Osatarkistus ei todista mitään. |
| "Eri sanat, joten sääntö ei päde" | Hengen mukaan, ei kirjaimen. |

## Milloin soveltaa

**Aina ennen:**

- mitä tahansa väitettä valmiudesta, toimivuudesta tai korjauksesta
- tyytyväisyyden ilmaisua
- tiedoston lähettämistä, artefaktin julkaisua tai automaation aktivoimista
- siirtymistä seuraavaan tehtävään
- tehtävän delegointia

Sääntö koskee täsmällisiä sanoja, parafraaseja ja vihjeitä onnistumisesta. Pitkissä töissä tarkistus on tehtävälistan viimeinen askel.
