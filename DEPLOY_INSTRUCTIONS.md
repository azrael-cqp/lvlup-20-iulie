# Solo Leveling System — Deploy Instructions

## Fisiere
1. **app.compiled.js** — aplicatia (singurul fisier care se schimba)
2. **index.html** — neschimbat
3. **DEPLOY_INSTRUCTIONS.md** — acest fisier

## Deploy (GitHub Pages)
1. Repo: github.com/azrael-cqp/LvlUP-v3
2. Drag & drop `app.compiled.js` peste cel existent (nume exact, cu PUNCT)
3. NICIODATA copy-paste din iOS in editorul GitHub
4. Commit → asteapta 2-3 min → Safari privat / clear cache
5. Datele tale (IndexedDB) raman intacte

---

# CHANGELOG — Update 3 Septembrie 2026

## 1. Romanian Deadlift scos din program

Motiv: durere lombara. RDL-ul e cea mai mare incarcare axiala din program dupa
squat, iar in ziua de Legs venea la 20 de minute dupa Squat 110kg.

- **Miercuri LEGS**: RDL → **Leg Extension** (3×12-15, pauza 90s).
  Izolare cvadriceps, zero compresie pe coloana. Se logheaza ca masina:
  **doar placile**.
- **Marti PULL**: RDL **eliminat complet**, fara inlocuitor. Era un hinge
  intr-o zi de spate; ischiogambierii sunt acoperiti miercuri de Leg Curls.
  Ziua de Pull are acum 8 exercitii.

XP-ul se muta corespunzator: cvadriceps castiga, hamstrings ramane pe Leg Curls.

## 2. Barbell Rows → Chest-Supported Row

Piept sprijinit pe banca inclinata la 30-45°, mijlocul complet descarcat.
Aceiasi muschi (romboizi, dorsal, trapez mijlociu), zero sustinere din coloana.

- Marti PULL si Vineri PULL: 4×10-12, pauza 120s
- Se logheaza ca **DB — greutatea unei gantere**, increment 2kg
- Istoricul vechi de la Barbell Rows ramane in baza de date, dar exercitiul
  porneste de la zero — sunt miscari diferite, nu are sens sa mosteneasca
  recomandarile

## 3. Somn in format ore:minute

Pana acum campul era zecimal si 6.17 era interpretat ca 6.17 ore (6h10m).
Acum sunt **doua campuri separate**: ore si minute.

- Se aplica si in logger-ul din tab-ul de statistici, si in modalul de reminder
- Afisajele arata `6h17m` in loc de `6.2h`
- **Migrare automata a intregului istoric**: toate cele ~55 de intrari vechi
  au fost reinterpretate ca HH:MM (5.34 → 5h34m, 8.17 → 8h17m, 7.2 → 7h20m).
  Migrarea ruleaza o singura data, la prima deschidere dupa deploy, si se
  salveaza imediat. Dubla protectie (flag in date + flag in localStorage) ca
  sa nu se poata rula de doua ori.

## 4. Sauna scoasa complet

- **Obiectivele saptamanale** contineau Sauna #1, #2, #3 si Yoga 30 min.
  Toate scoase. Sectiunea WEEKLY se ascunde automat cand e goala, deci nu mai
  vezi "0/0" pe ecran si nu mai iei penalizare de 95 XP pe saptamana pentru
  ceva ce nu faci.
- Quest-ul de sambata "Inot + Sauna" → **"Inot"**, aceleasi 30 XP.

## 5. Yoga → Mobility 5 min (acasa)

AGI era blocat la 16 pentru ca yoga era singura sursa si nu o faceai niciodata.
Inlocuit cu un quest zilnic realist:

**Mobility 5 min (acasa)** · 15 XP · AGI · disponibil in fiecare zi
Hip opener 90/90, rotatii toracice, ankle rocks, cat-cow. Fara echipament,
seara, cand esti oricum acasa.

## 6. Curatare intrari eronate

Sterse automat la prima deschidere:
- **Barbell Rows, 1 septembrie** (100×12 — bifat gresit, nu s-a facut)
- **Romanian Deadlift, 2 septembrie** (avea si typo 1001kg — nu s-a facut)

Restul istoricului ramane neatins.

## 7. Ajustari de consecventa

- Boss "The Silent Reaper": target RDL 90×8 → **Leg Curls 55×15**
- Boss quest "Extra RDL Set" → "Extra Leg Curls (2x15)"
- Boss quests cu yoga → "Stretching 15 min (acasa)" / "Mobility Flow (15 min)"
- Bonus sambata "Extra RDL Set" → **"Extra Leg Extension (2x15)"**, XP pe quads
- Alternativele de swap actualizate peste tot (fara RDL, fara Barbell Rows)
- Graficul de progresie: RDL si Barbell Rows scoase, adaugate **Overhead Press**
  si **Chest-Supported Row**

---

## Verificare dupa deploy

1. **Marti (PULL)**: al doilea exercitiu e Chest-Supported Row, nu mai apare RDL
2. **Miercuri (LEGS)**: al doilea exercitiu e Leg Extension
3. **Tab statistici → somn**: doua campuri, `ore : min`. Mediile arata `6h36m`
4. **Quest-uri zilnice**: apare "Mobility 5 min (acasa)" cu iconita 🤸
5. **Sectiunea WEEKLY**: nu mai exista
6. **Sambata**: quest-ul e "Inot", fara sauna
7. Verifica in istoricul de lifturi ca intrarile din 1 si 2 septembrie au
   disparut de la Rows si RDL

Daca ceva nu apare, e cache: Safari tab privat sau sterge datele site-ului
(nu si IndexedDB — alea sunt datele tale).
