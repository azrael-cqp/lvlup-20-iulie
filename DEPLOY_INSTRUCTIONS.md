# Solo Leveling System — Deploy Instructions

## Fisiere in acest pachet
1. **app.compiled.js** — aplicatia (SINGURUL fisier care se schimba)
2. **index.html** — neschimbat (doar incarca app.compiled.js prin React CDN)
3. **DEPLOY_INSTRUCTIONS.md** — acest fisier

## Cum deployezi (GitHub Pages)
1. Repo: github.com/azrael-cqp/LvlUP-v3
2. Drag & drop `app.compiled.js` peste fisierul existent (SUPRASCRIE-l)
   - Numele trebuie sa fie exact `app.compiled.js` (cu PUNCT)
   - NICIODATA copy-paste din iOS in editorul GitHub (strica smart quotes)
3. Commit
4. Asteapta 2-3 min sa se rebuilduiasca Pages
5. Deschide in Safari privat (sau clear cache) ca sa vezi versiunea noua
6. Datele tale (IndexedDB) raman intacte peste deploy

## CHANGELOG — Update 19 Iulie 2026

### 1. Hanging Leg Raises → reps, fara greutate
- Exercitiul se logheaza acum DOAR pe reps (nu are camp de greutate — nu ai cum
  sa pui greutate atarnat de bara).
- Coloana "kg" e ascunsa in logger, validarea cere doar reps, "Last:" arata
  doar reps, iar alerta de plateau pe kg nu se mai aplica.
- Banner: "🤸 Bodyweight · progresezi prin REPS · fara greutate".

### 2. Bosi noi (5 adaugati — acum 18 in total)
- 🗿 Bronze Colossus — chest (+60 XP in 21 zile)
- 🐉 Iron Hydra — back (+60 XP in 21 zile)
- 🦏 Granite Titan — quads (+55 XP in 21 zile)
- ⚡ Steel Valkyrie — shoulders (+55 XP in 21 zile)
- 👻 Fading Phantom — streak 14 zile consecutive

### 3. Bosii pe grupa musculara: progres din TOATE exercitiile grupei
Cea mai importanta schimbare (+ bug fix real):
- Cand accepti un boss pe o grupa (ex. core), aplicatia salveaza acum un
  "baseline" al XP-ului tau pe acea grupa in acel moment. Progresul boss-ului =
  cat XP ADAUGI pe grupa DE CAND ai acceptat, nu totalul pe viata.
- Fiindca XP-ul pe grupa se aduna din TOATE sursele — exercitii PPL, finishere,
  quest-uri bonus (Plank, Hollow Body Hold) SI boss quests — orice exercitiu de
  core (sau grupa tinta) din ziua aia alimenteaza boss-ul. Nu mai conteaza doar
  task-urile speciale ale boss-ului.
- Bug-uri reparate pe drum:
  (a) bosii pe grupa erau uneori "castigati instant" la accept (citeau totalul
      cumulativ pe viata) — acum pornesc corect de la 0%.
  (b) boss-ul AGI cu amount:0 dadea impartire la zero (instant 100%) — reparat,
      cheie acum pe delta de stat AGI.
- OBJECTIVE afiseaza progresul live: ex. "core: +15/50 XP".

Suport tehnic pentru (3): grupul muscular "core" era GOL, deci niciun exercitiu
de core din PPL nu credita XP pe core. Acum contine: Cable Crunches, Decline
Sit-ups, Hanging Leg Raises, Hollow Hold, Plank, Weighted Plank, Russian Twists.
Am adaugat si Rope Pushdown la triceps si Cable Front Raises la shoulders (din
update-urile trecute) ca sa crediteze XP corect.

## Verificare dupa deploy
- Tab PPL, marti (Pull): Hanging Leg Raises are DOAR camp de reps, fara kg.
- Tab BOSS: apar 18 bosi in AVAILABLE BOSSES, inclusiv cei 5 noi.
- Accepta boss-ul de core → OBJECTIVE arata "core: +0/50 XP" (nu instant castigat).
  Logheaza un exercitiu de core (finisher/bonus) → progresul creste.

## Istoric update-uri anterioare
- 13 Iul: buton "↩ Anuleaza" pt exercitiu bifat din greseala (scade XP + sterge
  set-urile de azi).
- 10 Iul: Rope Pushdown, Decline Sit-ups, Cable Front Raises, plank cu progresie
  4 niveluri, Hollow Body Hold, scos tab LIFE + FLEX, scos "No Sugar". Bara:
  QUESTS · PPL · BOSS · STATS · BODY · RANK · SAVE.
