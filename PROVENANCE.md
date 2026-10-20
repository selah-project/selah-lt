# KILMĖ — kaip šis vertimas buvo padarytas

*Lietuvių kalba. Hebrajiškieji Šventieji Raštai, eilutė po eilutės. Pradėta 2026-10-20 00:36; pirmasis
deginimas baigtas 2026-10-20 07:05; paskutinis spaudimas 2026-10-20 09:26 (JAV rytinės pakrantės laikas,
EDT = UTC−4).*

Tai įrašas apie tai, kaip šis vertimas buvo padarytas, ir ką dar reikia pataisyti. Mašininis vertimas
nenusipelno pasitikėjimo, jei nematai, kaip jis buvo padarytas. Todėl šis failas sako viską — **ir mūsų
klaidas.**

---

## Kaip vyko darbas

Kiekviena eilutė buvo išversta iš savo hebrajiško teksto (OSHB / Westminster Leningrad Codex) pagal
taisykles, parašytas lietuviškai (`docs/methodology/translation-discipline/lt.md` projekte Selah).
Mašina: **glm-5.3** (Zhipu).

Kiekvienai iki keturių eilučių grupei mašina gavo: hebrajišką tekstą (su ženklais ir vien raidėmis);
kiekvieną žodį su jo žodyno forma, Strongo numeriu ir Strongo reikšme; gretimas eilutes; taisykles lietuviškai;
ir **septynis angliškus vertimus palyginimui** (Wycliffe, Geneva 1599, King James, Young's Literal, American
Standard, JPS 1917, Berean Standard) su gretimomis King James eilutėmis. *(Šie palyginimai palikti sąmoningai
ir viešai nurodyti; „švarios patalpos“ perėjimas — tik hebrajiškas tekstas ir žodynas — ateis vėliau, kaip
atskiras pakeitimas.)*

Kiekviena eilutė turi dvi formas: **lietuvišką žodį kiekvienam hebrajiškam žodžiui** ir **visą eilutę**
lietuviškai. Abi išsaugotos.

## Bandymas prieš pradžią

Dvidešimt žodžių buvo išversti į lietuvių kalbą ir atgal į anglų: grįžo **20 iš 20**. Gyvūnų bandymas
eilutėje (exp 1200): **39 iš 46** — klaidos (*urvinis triušis* `שפן` vietoje, *stumbras* `רים` vietoje,
*naminiai gyvuliai* `מריא` vietoje) pateko į taisykles. Taisyklės turėjo **vardų ir raktinių žodžių lentelę**
ir **gyvūnų lentelę** nuo pirmosios eilutės — vienas žodis vienoje vietoje, visada.

## Kas buvo patikrinta

Vartai (`dev/scripts/lt_gate.clj`), visuose 23 213 failų:

- **Vardas:** `Jahvė` **6 007 iš 6 007** vietų.
- `VIEŠPATS`, `Amžinasis`, `Jehova`, `YHWH` Vardo vietoje; `Dievas` vienas `יהוה` vietoje: **0**.
- `Kristus`, `Jėzus`, `Mesijas`: **0**.
- Latvių, lenkų ir kirilicos raidės: **0**. Angliški žodžiai: **0**. Angliški žodžiai ar `⟨ה⟩` skliaustuose: **0**.
- Hebrajiški žodžiai eilutės tėkmėje: **0**. Tekstas ne NFC formos: **0**.
- `būrėjas` / `žynys`: **16** — tai eilutės apie būrėjus (Bileamas, 1 Sam 6, 2, Izaijo sąrašai, Įstatymo 18),
  perskaitytos ir teisingos; nė viena nėra `נביא`.

## Kas buvo pataisyta

- **Hebrajiškas tekstas (1 251):** pakeisti hebrajiški žodžiai grąžinti iš šaltinio.
- **Surašymo ratas** (1 749 failai) ir **paskutinis spaudimas** (32 eilutės): svetimų raidžių priemaiša,
  hebrajiški žodžiai eilutės tėkmėje, tušti ženklai, angliški žodžiai, `⟨ה⟩` skliaustuose, pasislinkę žodžiai.
- **Ranka:** 1 Karalių 5, 5 ir 15, 7 (`יהודה` — Judas); Psalmė 7, 10 (`בחן` — išmėgintojas); Psalmė 45, 3;
  NFC 4 failuose.

## Mašina ir žmogus

**Kiekvieną žodį eilučių failuose padarė mašina**, išskyrus rankinius pataisymus, nurodytus `NOTES.md` §1.
Daugumos eilučių neperskaitė nė vienas žmogus. **Nė vienas lietuviškai kalbantis žmogus šio vertimo dar
neperskaitė.** Tai tebėra labiausiai atvira.

Visa darbo istorija: `NOTES.md` ir git istorija.
