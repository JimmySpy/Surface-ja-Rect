## **1. Praktilise töö sooritamise käik**
**Eesmärk:**
Selle praktilise töö eesmärk oli kasutada Pygame'i, et luua graafiline aken, millele lisatakse erinevaid kujundeid (ringid) ja pindasid (Surface). Lisaks oli vaja mõista `Rect` objekti ja selle omadusi.

**Lühikirjeldus:**
Programmi käivitamisel avaneb Pygame aken (640x480), mille taustaks on hele sinine (`lBlue`). Akna peale joonistatakse erinevaid ringe, mis on lisatud `Surface`-ile. Pärast joonistamist kuvatakse `Surface` ekraanil mitmes kohas `blit()` meetodiga.
Mäng jääb avatuks, kuni kasutaja vajutab "X" nuppu, et see sulgeda.

**Töötasin:** Üksi.

**Abi saamine ja andmine:** Koodi kirjutamisel sain inspiratsiooni ja abi Pygame dokumentatsioonist ning kaasõpilastelt, kellega arutasime `Rect` kasutamist. Aitasin teisi selgitades `set_colorkey()` funktsiooni kasutamist läbipaistvuse jaoks.

---

## **2. Esinenud probleemid ja nende lahenduskäik**
**Probleem 1:** `Surface` taust ei olnud läbipaistev.
- **Lahendus:** Kasutasin `set_colorkey((0,0,0))`, et määrata must värv läbipaistvaks.
- **Allikad:** [Pygame dokumentatsioon](https://www.pygame.org/docs/)

**Probleem 2:** `Rect` objekti ei olnud algselt koodis kasutatud.
- **Lahendus:** Lisatud `surf.get_rect()`, et määrata `Rect` ja kasutada selle omadusi.

**Kasutatud promptid:**
- *"Kuidas muuta Pygame Surface taust läbipaistvaks?"*
- *"Kuidas kasutada Pygame Rect objekti ja selle omadusi?"*

---

## **3. Testimine ja tulemus**
**Testimine:**
- Koodi testisin manuaalselt, käivitades Pygame skripti ja kontrollides, kas kujundid kuvatakse õigesti.
- Kontrollisin, kas `Surface`-id ilmuvad õigetele kohtadele ekraanil.
- Testisin programmi sulgemist "X" nupu vajutamisega.

**Tulemus:**
- Programm töötab oodatult: ringid joonistatakse ekraanile ja püsivad nähtavad kuni programmi sulgemiseni.
- `Rect` objekti omadusi saab kasutada (kuid neid pole veel visuaalselt ekraanile kuvatud).
- `Surface`-i läbipaistvus töötab õigesti `set_colorkey()` abil.

---

## **4. Eneseanalüüs**
### **4.1. Kuidas sul läks?**
Töö läks hästi – sain Pygame'iga paremini tuttavaks ja õppisin, kuidas kasutada `Surface`-e ning `Rect` objekti omadusi. Probleemide lahendamine ja dokumentatsiooni lugemine aitasid mul oma oskusi arendada.

### **4.2. Kas avastasid uusi Python'i tehnikaid või lähenemisi?**
Jah, õppisin järgmisi uusi tehnikaid:
- **`set_colorkey()`** kasutamine, et määrata läbipaistev taust.
- **`Rect` omaduste kasutamine** (`left`, `right`, `centerx`, jne) objekti asukoha ja mõõtmete jälgimiseks.
- **`blit()` mitmekordne kasutamine**, et kuvada sama `Surface` ekraanil mitmes kohas.

### **4.3. Enesehinnang (skaala 2–5):**
**4 – Lävend on saavutatud**
- Kood töötab oodatult ja vastab ülesande nõuetele.
- Kasutatud on erinevaid Pygame funktsioone ja `Rect` omadusi.
- Saaks parandada kasutajainteraktsiooni (nt lisada liikumist või interaktiivsust).

### **4.4. Mida teeksid järgmisel korral teisiti?**
- Lisaksin **teksti kuvamise ekraanile**, et kasutaja saaks `Rect` omadusi visuaalselt näha.
- Teeksin kujundite **liigutamise klaviatuuri või hiirega**.
- Kasutaksin **struktuursemat koodi** (näiteks funktsioonide kasutamine, et hoida kood puhtamana).

---

**Kokkuvõttes:** See projekt andis hea ülevaate Pygame põhifunktsioonidest ja `Rect` kasutamisest. Tulevikus võiks lisada rohkem interaktiivsust ja testimist. 

