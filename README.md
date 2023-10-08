# Albmiarvioija
## TKT20019 - Tietokannat ja web-ohjelmointi projekti
* Käyttäjä voi kirjautua sisään ja ulos sekä luoda uuden tunnuksen.
* Käyttäjä näkee etusivulla viimeisimpiä annettuja arvosteluja albumeille ja arvion lähetysajan.
* Käyttäjä voi etsiä artistia tai albumia hakupalkilla ja selata niitä listoittain.
* Artisteilla on omat sivunsa josta löytyy lista albumeista ja yleistä infoa (kotimaa, perustusvuosi, genre yms).
* Albumeilla on omat sivunsa jossa lista kaikista arvosteluista, arvioiden keskiarvo ja yleistä infoa.
* Käyttäjä voi lisätä, muokata ja poistaa omia arvioitaan albumista.
* Luotettu käyttäjä voi lisätä sekä muokata artistien ja albumien tietoja. 
* Ylläpitäjä voi lisätä sekä muokata artistien ja albumien tietoja
* Ylläpitäjä voi poistaa käyttäjien arvosteluja.
## Nykyinen tilanne
* Käyttäjä voi kirjautua sisään ja ulos sekä luoda uuden tunnuksen.
* Käyttäjä näkee etusivulla viimeisimpiä annettuja arvosteluja albumeille.
* Käyttäjä voi selata kaikkia artisteja listalta.
* Artisteilla on omat sivunsa josta löytyy lista albumeista ja yleistä infoa (kotimaa, perustusvuosi, genre yms).
* Albumeilla on omat sivunsa jossa lista kaikista arvosteluista ja yleistä infoa.
* Kaikki käyttäjät voivat lisätä omia arvioitaan albumista.
## Tulossa
* Artistien, albumien ja arvosteluiden poisto
* Albumeiden kappaleiden lisäys (tietokanta valmiina mutta vielä käyttämätön)
* Ohjelman ulkoasun parannus
* Mahdollisien bugien liiskaus ja koodin siivous
## Tiedossa olevat ongelmat
* Samalle artistille voi lisätä useita saman nimisiä albumeita
* Sama käyttäjä pystyy kirjoittamaan useamman arvion samasta albumista
## Kuinka käyttää ohjelmaa
Kloonaa repositorio koneellesi ja siirry juurikansioon. Luo kansioon .env-tiedosto ja määritä sisältö seuraavanlaiseksi:
```
DATABASE_URL=<tietokannan-paikallinen-osoite> (esim DATABASE_URL=postgresql:///user)
SECRET_KEY=<salainen-avain>
```
Aktivoi virtuaaliympäristö ja asenna sovelluksen riippuvuudet komennoilla
```
python3 -m venv venv
source venv/bin/activate
pip install -r ./requirements.txt
```
Käynnistä postgersql tietokanta ja määritä tietokannan skeema komennolla
```
psql < schema.sql
```
Tarvittaessa koko tietokannan voi tyhjentää ja alustaa komennoilla psql:llä
```
DROP SCHEMA public CASCADE;
CREATE SCHEMA public;
```
käynnistä sovellus komennolla
```
flask run
```
