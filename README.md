# Montopia

Vier Spiele für zwei auf dem Sofa. Ein Handy, kein Internet nötig, keine Kosten.

---

## Aufs iPhone bringen

Genau wie bei der Karteikarten-App – die ausführliche Schritt-für-Schritt-Anleitung steht in
[Karteikarten/ANLEITUNG_iPhone.md](../Karteikarten/ANLEITUNG_iPhone.md).

Kurzfassung für **Weg 1** (Symbol auf dem Home-Bildschirm, offline):

1. Auf [github.com](https://github.com) ein neues, öffentliches Repository anlegen, z. B. `montopia`.
2. Die **6 Dateien** hochladen: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-180.png`, `icon-192.png`, `icon-512.png`.
3. *Settings → Pages → Deploy from a branch → main / (root) → Save*.
4. Am iPhone die Adresse in **Safari** öffnen, kurz warten, dann **Teilen → Zum Home-Bildschirm**.

Hier ist das unbedenklich: Die Inhalte sind Allgemeinwissen, keine geschützten Skripte.

Ohne GitHub geht auch **Weg 2**: `index.html` in OneDrive legen und am iPhone in der Dateien-App antippen.

---

## Die vier Spiele

### 🎯 Schätzchen — gegeneinander
Sechs Fragen pro Runde, 102 Schätzfragen im Fundus. Fünf Spielarten, einzeln oder gemischt:

| Spielart | Regel | Punkte |
|---|---|---|
| **Qual der Wahl** | Vier Antworten, beide tippen nacheinander verdeckt | 2 für jede richtige Antwort |
| **Daumen mal Pia** | Frei schätzen per Regler | 2 für die nähere Schätzung, +1 bei unter 5 % Abweichung |
| **Rauf & Runter** | Ein Wert ist bekannt – ist der zweite mehr oder weniger? Abwechselnd | 2 bei richtig |
| **Heiß & Nah** | Am nächsten dran, **ohne** drüber zu gehen | 2, bei beiden drüber: niemand |
| **Montys Flunkerei** | Einer sieht die Wahrheit und behauptet etwas. Die andere Person entscheidet: stimmt das? | 2 für den, der richtig liegt |
| **Wilde Mischung** | Alle fünf bunt durcheinander | – |

Wer beginnt, wechselt von Frage zu Frage. Die Punkte laufen in den **Abendstand** auf dem Startbildschirm.

### ⏱️ Monty erklärt's — zusammen
Zwei Runden à 60 Sekunden, erst Monty, dann Pia. 183 Begriffe.
Wer erklärt, hält das Handy. Der Begriff selbst, Wortteile und Übersetzungen sind tabu.
Beide Runden zusammen ergeben euren Team-Wert – der Bestwert wird gespeichert.

### 🧶 Pias Knoten — zusammen
16 Wörter, 4 geheime Gruppen zu je 4 Wörtern. Vier Fehler sind erlaubt.
Bei drei von vier richtigen Wörtern kommt ein Hinweis. 12 Rätsel, gelöste tauchen erst wieder auf,
wenn alle durch sind.

### 🧱 Montys Turm — zusammen
98 Aussagen, wahr oder falsch. Jede richtige Antwort baut den Turm einen Stein höher,
jede falsche kostet eins von drei Leben. Nach jeder Antwort kommt die Erklärung dazu.
Diskutiert erst, antwortet dann.

---

## Gespeichert wird

Abendstand (Monty/Pia), Bestwert beim Erklären, Bestwert beim Turm und die bereits gelösten Knoten-Rätsel.
Alles liegt lokal auf dem Handy. **Neuer Abend** auf dem Startbildschirm setzt nur die Punkte von
Monty und Pia zurück, die Bestwerte bleiben.

---

## Inhalte ändern

Alles steckt oben in `index.html` im Abschnitt `DATEN`:

- `FACTS` — Schätzfragen: `["Frage", "Kurzlabel", Wert, "Einheit", "Kategorie"]`
  Das Kurzlabel wird bei *Rauf & Runter* gebraucht. Für diesen Modus zählen nur Werte mit
  **gleicher Einheit** – wer eine neue Einheit einführt, braucht mindestens zwei Einträge davon.
- `WF` — Wahr/Falsch: `["Aussage", 1 oder 0, "Erklärung"]`
- `TERMS` — Begriffe zum Erklären, einfache Liste
- `KNOTEN` — je Rätsel vier Gruppen im Format `["Überschrift","Wort1","Wort2","Wort3","Wort4"]`

Nach Änderungen bei Weg 1: Dateien neu hochladen **und** in `sw.js` `montopia-v1` auf `montopia-v2`
hochzählen, sonst zeigt das iPhone die alte Version.

---

## Kleingedrucktes zu den Zahlen

Alle Werte sind gerundete Näherungen aus allgemein zugänglichen Quellen – gedacht zum Schätzen,
nicht als Beleg. Verbrauchs- und Einwohnerzahlen ändern sich über die Jahre.
