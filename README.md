# NiedersachScanner — Compliance by Design

> **Interaktive Projektpräsentation:** [Live-Demo auf GitHub Pages öffnen](https://vitorpbastos49.github.io/niedersachScanner/)

**NiedersachScanner** ist ein Konzept- und MVP-Projekt aus dem Masterstudiengang *LL.M. European Technology Law* an der Universität Osnabrück. Ziel des Projekts ist es, Studierende bei der Wohnungssuche in Osnabrück vor typischen Betrugsmaschen (z. B. Lockangeboten, Fake-Inseraten und unzulässigen Mietklauseln) zu schützen — und dabei rechtliche Vorgaben von Anfang an direkt in die Softwarearchitektur einzubauen (**Compliance by Design**).

---

## Funktionsweise (4-Stufen-Pipeline)

1. **Dualer Input:** Prüfung beliebiger Wohnungsanzeigen per URL oder per Screenshot (`Ctrl+V`) — portalunabhängig für WG-Gesucht, Kleinanzeigen, ImmoScout24 und weitere Quellen.
2. **Flüchtige Analyse (RAM-only):** Extraktion der relevanten Eckdaten (Miete, Kaution, Wohnfläche, Stadtteil, Kontostatus) ausschließlich im Arbeitsspeicher ohne dauerhafte Speicherung.
3. **Regel- & Benchmark-Prüfung:** Abgleich mit Osnabrücker Mietspiegel-Werten, der gesetzlichen Kautionsgrenze (§ 551 BGB) sowie Hinweisen auf recycelte Bilder oder inaktive Inserate — inklusive *Human-in-the-Loop*-Korrekturmöglichkeit.
4. **Erklärbares Ergebnis:** Verständlicher Risiko-Score mit vier nachvollziehbaren Begründungskarten statt einer intransparenten „Black Box“.

---

## Rechtliche Architektur (6 Rechtsgebiete im Code)

| Rechtsgebiet | Relevante Normen | Technische Umsetzung (Compliance by Design) |
| :--- | :--- | :--- |
| **1. Datenschutzrecht** | DSGVO Art. 5, 6 Abs. 1 lit. f, 16, 17, 25 | *Privacy by Default* (Maskierung privater Kontaktdaten), flüchtige RAM-Verarbeitung, keine öffentlichen Blacklists. |
| **2. Urheber- & Markenrecht** | UrhG §§ 2, 44a, 44b, 72, 87a ff.; MarkenG § 23 | Kein automatisiertes Bulk-Scraping, rein nutzerinitiierte Einzelprüfung nicht geschützter Fakten, Deep-Linking zur Originalquelle. |
| **3. Wettbewerbsrecht** | UWG §§ 3, 4, 5 | Portalneutrale Bewertungslogik auf Basis objektiver Benchmarks; klare Trennung zwischen *Privat (verifiziert)* und *Gewerblich/Pro*. |
| **4. Produktsicherheitsrecht** | EU AI Act Art. 13; GPSR (EU) 2023/988 | Erklärbare *Glass-Box*-Ausgabe, *Fail-Safe* gegen Halluzinationen („Not Stated“ statt Schätzung fehlender Werte) und Nutzerkontrolle. |
| **5. Vertragsrecht** | BGB §§ 551, 540, 327 ff.; § 4a WoVermRG; § 19 BMG | Automatischer Kautions-Check (max. 3× Kaltmiete), Hinweise zu Ablöse und Anmeldung sowie klare Einordnung als Informationstool. |
| **6. Haftungsrecht** | BGB §§ 823, 824; StGB § 186 | Sachliche Darstellung objektiver Anomalien statt Betrugsvorwurf; integrierter *Notice-and-Reply*-Mechanismus zur sofortigen Überprüfung. |

---

## Bedienung der Präsentation

Die Präsentation wurde als eigenständige, interaktive Web-App in **HTML, CSS, Vanilla JavaScript, Inline-SVG und GSAP** umgesetzt:

* **Vor / Zurück:** `→` / `←`, `Leertaste`, Klick oder Wischen auf Mobilgeräten
* **Direktsprung:** Tasten `1`–`9` oder Klick auf die Fortschrittsleiste unten
* **Vollbild / Leiste ausblenden:** `F` (Vollbild) · `H` (HUD ein-/ausblenden)

---

## Kontakt

**Vítor Pires Bastos**  
LL.M. European Technology Law — Universität Osnabrück  
[LinkedIn](https://www.linkedin.com/in/vitorpbastos) · [vitorpbastos2002@gmail.com](mailto:vitorpbastos2002@gmail.com)# NiedersachScanner
