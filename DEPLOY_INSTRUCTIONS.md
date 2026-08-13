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

## CHANGELOG — Update 13 August 2026

### 1. Somn: ore cu zecimale
Campul era `type="number"` cu `step="0.5"`, de aceea iOS te forta la
jumatati de ora. Acum e camp text cu tastatura decimala: poti pune 7.2,
6.8, orice. Reparat in ambele locuri (tab BODY si modalul de reminder).

### 2. Readiness Score (Oura) + trend
- Camp nou optional (0-100) langa ore si rating, in ambele locuri.
- Panou nou in BODY: media pe 7 zile, diferenta fata de saptamana
  anterioara (▲/▼), si grafic cu barele ultimelor 7 zile.
- Cod culori: 85+ verde (excelent) · 70-84 albastru (ok) · sub 70
  portocaliu (recuperare slaba).

### 3. Plank unificat
"Weighted Plank" ca exercitiu separat a disparut complet. In ziua de
Miercuri (LEGS) finisher-ul e acum "Plank" — acelasi exercitiu cu
progresia pe 4 niveluri din bonus quest. Un singur plank, un singur
nivel, peste tot. Se logheaza in secunde, fara camp de greutate.

### 4. Scos Cold Shower din bonus quests

### 5. Hanging Leg Raises — confirmat doar reps, fara greutate

### 6. Boss quests = actiuni independente (schimbare mare)
Inainte, boss quest-urile erau indicatii de tehnica pentru exercitii din
PPL ("Rows — strange omoplatii 1s"), deci nu puteai avansa decat in ziua
aia si nu adaugau nimic in plus.

Acum toate 35 sunt actiuni de sine statatoare, pe care le poti face
acasa sau in plus la sala, in ORICE zi. Exemple:
- "Band Rows (3x20, strange omoplatii) — cu banda"
- "Push-ups (3x max, pauza 1s jos) — acasa"
- "Leg Raises pe podea (3x20) — acasa"
- "Dead Hang (3x max) SAU Band Pull-Aparts (3x25)"
- "Monster Walks cu banda (3x20 pasi) — cu banda"

### 7. Bosii invinsi dispar din lista
Odata invins, un boss nu mai apare in AVAILABLE BOSSES. Rămâne doar in
BATTLE HISTORY (care oricum arata ultimele 5).

### 8. Boss deload scos
"The Deload Phoenix" eliminat din biblioteca — necesita adaptarea
intregului PPL. Revenim daca schimbam programul.

### 9. Bosi noi (4 adaugati — acum 22 in total)
- 💪 Iron Warden — biceps (+55 XP / 21 zile)
- 🔱 Bronze Sentinel — triceps (+55 XP / 21 zile)
- 👑 Crowned Monarch — glutes (+60 XP / 21 zile)
- 🌙 Dream Keeper — streak 21 zile, focus pe somn si Readiness

### 10. Weight log editabil
Fiecare cantarire din lista are acum doua butoane:
- **✎** editeaza (greutate, BF%, masa musculara)
- **✕** sterge (cu confirmare)

## DE FACUT IMEDIAT DUPA DEPLOY
Corecteaza cantarirea din 13 Aug: e salvata gresit ca **115.15kg**,
valoarea reala e **105.15kg**. Tab BODY → gaseste randul din 13/08 →
apasa ✎ → pune 105.15. Altfel graficul arata un salt fals de 9kg si
faza-2 (tinta BF 20%) se comporta ciudat.

## Verificare dupa deploy
- BODY → Sleep Tracker: poti scrie 7.2 la ore; apare campul Readiness
- BODY: dupa 2 zile cu Readiness logat, apare panoul cu trend
- PPL Miercuri: finisher-ul e "Plank" (nu Weighted Plank), doar secunde
- BOSS: bosii invinsi nu mai apar in lista; boss quest-urile sunt
  actiuni de facut acasa
- BODY → lista cantaririlor: butoanele ✎ si ✕ pe fiecare rand
