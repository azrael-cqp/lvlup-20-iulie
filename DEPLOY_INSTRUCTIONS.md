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

# CHANGELOG — Update 12 Septembrie 2026

## 1. PROGRAM NOU: PPL + Upper/Lower

**Luni PUSH · Marti PULL · Miercuri LEGS · Joi UPPER · Vineri LOWER**

Doua schimbari structurale:
- **Picioarele trec de la o zi la doua.** Miercuri = zi grea (Squat 4x6-8). Vineri = zi de volum, unilaterala, fara incarcare axiala.
- **Pieptul primeste a doua zi.** Luni (Bench + DB Incline + Cable Flyes) si Joi (DB Bench + Cable Flyes).

### Volum saptamanal rezultat (serii)

| Grupa | Serii | Observatie |
|---|---|---|
| Cvadriceps | 22 | de la ~10 |
| **Piept** | **18** | **de la ~14** |
| Spate | 17 | usor redus, e grupa cea mai dezvoltata |
| Umeri | 15 | |
| Fesieri | 13 | |
| Core | 12 | finisher in fiecare zi |
| Biceps | 9 | |
| Gambe | 8 | doua zile in loc de una |
| Triceps | 6 | + Diamond Push-ups ca bonus |
| Ischiogambieri | 6 | Leg Curls pe ambele zile de picioare |

**Zero hinge de sold in tot programul** — fara RDL, fara Good Mornings, fara Barbell Rows in picioare.

### Exercitii noi
- **Bulgarian Split Squat** (Vineri) — unilateral, se logheaza ca DB, increment 2kg
- **Hip Thrust** (Vineri) — fesieri fara hinge, se logheaza ca aparat (doar placile)

### Nota pe Bench si DB Bench
Ambele au acum in descriere: fara spotter, plafonul de siguranta e 100kg. Peste asta, progresezi din repetari.

## 2. Chest-Supported Row reconfigurat ca APARAT

Era setat ca gantere (greutatea unei gantere, increment 2kg). Acum e aparat: **se logheaza doar placile**, increment 5kg. Recomandarile vor fi corecte de acum inainte.

## 3. Bonus de piept raspandit in saptamana

Ca la core, dar pe piept — apar in zilele fara Push:

| Zi | Quest | XP |
|---|---|---|
| Marti | Push-ups la refuz (3 seturi) | 30 |
| Miercuri | Incline Push-ups (3x15) | 25 |
| Vineri | Diamond Push-ups (3 seturi) | 25 |

Toate adauga XP pe chest (si triceps), acasa, fara sa incarce recuperarea.

## 4. Mobility — instructiuni pas cu pas

Quest-ul avea o singura linie de text la 8px, imposibil de urmarit. Acum, cand apare in BONUS, se deschide sub el **un panou cu cei 4 pasi la text lizibil (11-12px)**:

1. **90/90 Hip Switch** — 90 secunde
2. **Rotatii toracice** — 60 secunde
3. **Ankle Rocks** — 60 secunde
4. **Cat-Cow** — 60 secunde

Fiecare cu explicatie completa de executie. E disponibil in fiecare zi si e singura sursa de AGI (blocat la 16 de luni de zile).

## 5. READINESS se poate loga

Camp nou in logger-ul de somn, sub ore/minute si stelute: **READINESS 0-100**, optional. Valoarea din Oura. Apare si in notificare (`R74`).

## 6. Cold Shower scos

Eliminat din quest-urile bonus.

---

## Verificare dupa deploy

1. **Tab PPL**: Joi scrie UPPER (portocaliu), Vineri scrie LOWER (violet)
2. **Vineri**: primul exercitiu e Bulgarian Split Squat, al cincilea e Hip Thrust
3. **Marti**: apare bonusul "Push-ups la refuz"
4. **Orice zi**: quest-ul Mobility are sub el panoul violet cu cei 4 pasi
5. **Logger somn**: exista randul READINESS
6. **Bonus**: Cold Shower nu mai apare nicaieri
7. **Chest-Supported Row**: recomandarea trebuie sa fie in placi, nu in kg de gantera

Testat inainte de livrare intr-un browser simulat cu datele tale: zero erori de randare.
