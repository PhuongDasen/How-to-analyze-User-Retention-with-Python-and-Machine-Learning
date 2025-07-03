<p align="center">
  <img src="https://github.com/user-attachments/assets/d982466c-adab-48f2-b889-3130a128d788" width="90%">
</p>
<h1> 📊 How to analyze User Retention with Python and Machine Learning</h1>
Author: Phuong Dasen<br>
Tool: Python and Machine Learning<br>

## 📑 Inhaltsverzeichnis

- [📌 Hintergrund & Überblick](#hintergrund--überblick)  
- [📁 Datensatzbeschreibung & Datenstruktur](#datensatzbeschreibung--datenstruktur)  
- [🧠 Design-Thinking-Prozess](#design-thinking-prozess)  
- [📊 Zentrale Erkenntnisse & Visualisierungen](#zentrale-erkenntnisse--visualisierungen)  
- [🔍 Abschließende Schlussfolgerung & Empfehlungen](#abschließende-schlussfolgerung--empfehlungen)  

---
## 📌 Hintergrund und Überblick 
<p><u><strong>1. Über RFM-Analyse</strong></u></p>
   <p><strong>Warum RFM?</strong><br>
    - RFM ist eine Marketinganalysetechnik, die für Recency (Aktualität), Frequency (Häufigkeit) und Monetary Value (Geldwert) steht.<br>
        - <strong>Aktualität</strong>: wie oft ein Kunde in letzter Zeit eingekauft hat.<br>
        - <strong>Häufigkeit</strong>: wie oft ein Kunde eingekauft hat.<br>
        - <strong>Monetärer Wert</strong>: den Gesamtbetrag, den ein Kunde für seine Einkäufe ausgegeben hat.<br>
    - RFM wird verwendet, um Kunden auf der Grundlage ihres Kaufverhaltens zu identifizieren und zu kategorisieren, d. h. wie häufig und kürzlich sie eingekauft haben und wie hoch der Geldwert dieser Einkäufe ist.<br>
     
<strong>Wie?</strong><br>
Bei der RFM-Analyse werden die Kunden anhand von drei Faktoren bewertet (Aktualität, Häufigkeit - wie oft, Geldwert - wie viel) und dann auf der Grundlage der Kombination der RFM-Werte eingestuft<br>

**Referenz**
- https://www.putler.com/rfm-analysis

### Ziel:
## 📖 Was ist dieses Projekt?
- Dieses Projekt analysiert Kundenverhalten im E-Commerce mithilfe von RFM-Segmentierung und Churn-Prediction.
- Ziel ist es, datengestützte Maßnahmen zur Kundenbindung und Umsatzsteigerung zu entwickeln.

## 👤 Für wen ist dieses Projekt?
- Das Projekt richtet sich an das Marketing- und CRM-Team eines E-Commerce-Unternehmens.
- Es unterstützt Entscheidungsträger dabei, Kundensegmente besser zu verstehen und gezielte Kampagnen durchzuführen.

## ❓ Geschäftsfrage von dem Projekt?
- Welche Kundengruppen sind besonders wertvoll oder gefährdet, zur Konkurrenz abzuwandern?
- Wie können Unternehmen datenbasiert reagieren, um Kunden zu halten oder zurückzugewinnen?

### 📁 Datensatzbeschreibung & Datenstruktur
## 📌 Datenquelle<br>
Quelle: Bereitgestellter Datensatz für die Analyse des E-Commerce-Einzelhandels<br>
Umfang: 541.910 Zeilen × 8 Spalten (Tabelle 1: E-Commerce Retail), zusätzliche Segmentierungsdetails in Tabelle 2<br>
Format: .xlsx (Excel-Datei mit zwei Tabellenblättern)<br>

## 📊 Datenstruktur & Beziehungen
#### 1️⃣ Verwendete Tabellen:
Der Datensatz besteht aus zwei Tabellen:<br>

<strong>Tabelle 1: Ecommerce Retail</strong><br>
Diese Tabelle enthält Transaktionsdaten eines britischen Onlinehändlers im Zeitraum von Dezember 2010 bis Dezember 2011. Sie eignet sich besonders gut zur Analyse des Kaufverhaltens und der Kundensegmentierung, da viele Kunden Großhändler sind.<br>

<strong>Tabelle 2: Segmentation</strong><br>
Diese Tabelle enthält RFM-Scores zur Klassifizierung von Kunden in Segmente. Jeder Score wird einem Kundenprofil wie „Loyaler Kunde“ oder „Gefährdeter Kunde“ zugeordnet.<br>

#### 2️⃣ Tabellenschema & Datenvorschau
<details>
<summary>🔽 Tabelle 1: Tabellenbeschreibung anzeigen</summary>

<br>

| **Spaltenname** | **Datentyp**     | **Beschreibung**                                                                 |
|------------------|------------------|----------------------------------------------------------------------------------|
| InvoiceNo        | object           | Eindeutige Rechnungsnummer für jede Transaktion (6-stellig). Beginnt sie mit „C“, handelt es sich um eine Stornierung. |
| StockCode        | object           | Eindeutiger Produktcode (5-stellig).                                             |
| Description      | object           | Produktname.                                                                     |
| Quantity         | int64            | Anzahl der gekauften Einheiten pro Transaktion.                                  |
| InvoiceDate      | datetime64[ns]   | Datum und Uhrzeit der Transaktion.                                               |
| UnitPrice        | float64          | Preis pro Produkteinheit in britischen Pfund.                                    |
| CustomerID       | float64          | Eindeutige 5-stellige Kennung für jeden Kunden.                                  |
| Country          | object           | Name des Landes, in dem der Kunde wohnt.                                         |

</details>

<details>
<summary>🔽 Tabelle 2: RFM-Segmentierung anzeigen</summary>

<br>

| **Segment**              | **RFM Scores**                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Champions                | 555, 554, 544, 545, 454, 455, 445                                                                                                                                    |
| Loyale Kunden            | 543, 444, 435, 355, 354, 345, 344, 335                                                                                                                              |
| Potenzielle Loyale       | 553, 551, 552, 541, 542, 533, 532, 531, 452, 451, 442, 441, 431, 453, 433, 432, 423, 353, 352, 351, 342, 341, 333, 323                                                 |
| Neue Kunden              | 512, 511, 422, 421, 412, 411, 311                                                                                                                                   |
| Vielversprechend         | 525, 524, 523, 522, 521, 515, 514, 513, 425, 424, 413, 414, 415, 315, 314, 313                                                                                      |
| Braucht Aufmerksamkeit   | 535, 534, 443, 434, 343, 334, 325, 324                                                                                                                              |
| Einschlafend             | 331, 321, 312, 221, 213, 231, 241, 251                                                                                                                              |
| Gefährdet                | 255, 254, 245, 244, 253, 252, 243, 242, 235, 234, 225, 224, 153, 152, 145, 143, 142, 135, 134, 133, 125, 124                                                          |
| Nicht verlieren!         | 155, 154, 144, 214, 215, 115, 114, 113                                                                                                                              |
| Winterschlafend          | 332, 322, 233, 232, 223, 222, 132, 123, 122, 212, 211                                                                                                                |
| Verlorene Kunden         | 111, 112, 121, 131, 141, 151                                                                                                                                         |

</details>

## ⚒️ Hauptprozess
## 📌 Bibliotheken importieren
<img width="700" alt="Screenshot 2025-07-01 at 9 04 11 AM" src="https://github.com/user-attachments/assets/eff40e30-91c4-48ff-91a5-0a8303acadb7" />
<img width="700" alt="Screenshot 2025-07-01 at 9 16 29 AM" src="https://github.com/user-attachments/assets/0aa3014d-6080-457b-b787-a95169d5d593" />
<img width="700" alt="Screenshot 2025-07-01 at 9 15 13 AM" src="https://github.com/user-attachments/assets/902a0c25-414a-4fb0-b113-04f3c3db0b2b" />
<img width="700" alt="Screenshot 2025-07-01 at 9 15 23 AM" src="https://github.com/user-attachments/assets/1ce2522d-662c-4c34-a172-f755421e32f9" />

## 📌 Explorative Datenanalyse (EDA)
<img width="700" alt="Screenshot 2025-07-01 at 9 17 08 AM" src="https://github.com/user-attachments/assets/5119454c-5231-40a6-899d-af6b81bc56ad" /><br>

🎯 **Ergebnisanalyse:**  
	1. Die Daten haben 541.909 Zeilen und 8 Spalten<br>
	2. Die Spalte CustomerID: fehlen rund 135.000 Einträge (541.909 - 406.829) --> entfernen <br>
	3. Die Spalte Description: fehlen etwa 1.454 Beschreibungen --> kann halten, weil sie nicht auf RFM beeinflusst.<br>
	4. Die Datentypen sind größtenteils korrekt zugeordnet, z. B. InvoiceDate als datetime64, Quantity als int64, und UnitPrice als float64.<br>
 	5. Inkorrekte Werte: <br>
      * Bestandscode: 54487 Zeilen -> Zeilen mit fehlerhaften Daten löschen, da die anderen Codes Geschenke sein können, wenn der Produktcode nicht aus fünf Ganzzahlen besteht.<br>
      * Menge: 10587 Zeilen -> Zeilen mit fehlerhaften Daten löschen, da dies das RFM-Modell beeinflusst (Menge darf nicht <= 0 sein).<br>
      * Einzelpreis: 2512 Zeilen -> Zeilen mit fehlerhaften Daten löschen, da dies das RFM-Modell beeinflusst (Preis darf nicht <= 0 sein).<br>
      * Bestellungen mit Rechnungsnummern, die mit „C“ beginnen, entfernen.<br>
<img width="700" alt="Screenshot 2025-07-01 at 9 57 26 AM" src="https://github.com/user-attachments/assets/59b5812f-7226-4d04-b8cd-39c0d9aae183" />
<img width="700" alt="Screenshot 2025-07-01 at 9 57 40 AM" src="https://github.com/user-attachments/assets/466ac77d-6747-413b-b105-087b493d976e" />
<img width="700" alt="Screenshot 2025-07-01 at 9 57 52 AM" src="https://github.com/user-attachments/assets/c23d772f-d253-4b75-a06a-b9cea020f87d" />

## 📌 RFM <br> 
<img width="700" alt="Screenshot 2025-07-01 at 9 58 03 AM" src="https://github.com/user-attachments/assets/c0f308fc-140b-4961-ae98-636da60b6628" />
<img width="700" alt="Screenshot 2025-07-01 at 10 01 21 AM" src="https://github.com/user-attachments/assets/6ed79069-f06f-4421-9be0-bc6cf00c1797" />
<img width="700" alt="Screenshot 2025-07-01 at 10 01 29 AM" src="https://github.com/user-attachments/assets/ca372425-9f27-47d5-a3ec-51fdbc0a505e" />
<img width="700" alt="Screenshot 2025-07-01 at 10 06 15 AM" src="https://github.com/user-attachments/assets/d0fcab37-7958-4ff8-a44b-a954e7683f34" />
<img width="700" alt="Screenshot 2025-07-01 at 10 06 20 AM" src="https://github.com/user-attachments/assets/d143e8e8-bec4-47f9-9fde-59101fbc3e06" />
<img width="700" alt="Screenshot 2025-07-01 at 10 06 30 AM" src="https://github.com/user-attachments/assets/87a61e4a-3afa-4532-ac2a-bc975b9b4fe7" />
<img width="700" alt="Screenshot 2025-07-01 at 10 06 37 AM" src="https://github.com/user-attachments/assets/be5fd83f-4460-4905-bd0e-3aecf3b7a52e" />
<img width="700" alt="Screenshot 2025-07-01 at 10 14 15 AM" src="https://github.com/user-attachments/assets/e0f50a6d-451d-41f9-9330-1a61803471bc" /><br>
<img width="700" alt="Screenshot 2025-07-01 at 10 14 26 AM" src="https://github.com/user-attachments/assets/6f43f1c6-eae8-43e4-9684-dffe65505538" /><br>

**🎯 Ergebnisanalyse:**
Die aktuelle Segmentstruktur zeigt, dass nur <strong>~1 von 10 Kunden</strong> hochprofitabel ist, während fast die Hälfte gefährdet ist, komplett verloren zu gehen. Ziel sollte sein, die „Potenzial“-Gruppe zu aktivieren und die „Risiko“-Gruppe zu analysieren oder selektiv zu bearbeiten.

## 📊 Visualisierungen der RFM-Werte (Histogramme)
1. 
<img width="700" alt="Screenshot 2025-07-01 at 9 05 27 PM" src= />


## 🔎 Insights and Recommemdations 










<h1>I. Introduction</h1>
<h2>1. About Cohort Analysis</h2>
  <b>What is cohort and cohort analysis?</b>
  <ul>
    <li> A cohort is a group of users who share a common characteristic, and cohort analysis is a tool to measure their engagement over time. </li>
    <li>Cohort analysis helps to differentiate between actual improvements in user engagement and those that may be driven by growth, while vanity indicators do not provide the same level of insight.</li>
  </ul>
  <h3>Three major types of Cohort</h3>
  <ul>
    <li>Time cohorts: customers who signed up for a product or service during a particular time frame.</li>
    <li>Behavior cohorts: customers who purchased a product or subscribed to a service in the past.</li>
    <li>Size cohorts: refer to the various sizes of customers who purchase the company's products or services.</li>
  </ul>
  <h3> Which tpye of cohort is for this project?</h3>
  <ul>
    <li>I will focus on performing Cohort Analysis based on Time (Time cohorts)</li>
    <li>Customers will be divided into acquisition cohorts depending on the month of their first purchase.</li>
    <li>The cohort index would then be assigned to each of the customer's purchases, which will represent the number of months since the first transaction.</li>
    </ul>
<h2>2. Business Questions</h2>
<ul>
  <li>One ecommerce company has a project on predicting churned users in order to offer potential
promotions.</li>
  <li>Using Python to analyze transaction data from KPMG and creating a cohort that allows stakeholders to assess user engagement starting from their first transaction.</li>
</ul>
<h1>II. Data Visualization with Python</h1>
- MoM Retention Rate for Customer Transaction Data <br>
<img width="829" alt="Screenshot 2025-05-12 at 09 35 44" src="https://github.com/user-attachments/assets/0472e084-7b7c-41b0-a584-d3158f6265fa" />
<h1>III. Insights</h1>
<ul>
  <li>Customers who register and place their first order in July 2017 have a high retention rate (up to 48.1%) after 5 months of operation. </li>
  <li>Customers who register and place their first order in April 2047 have a stable and relatively high retention rate: 45.1% (4th month), 42.1% (5th month), and 42.7% (7th month).</li>
  <li>Customers who register and place their first order in May 2017 also have a fairly high and stable retention rate: 40.4%, 39% and 41.3% in the 2nd, 3 rd and 4th month activities.</li>
  <li>Looking at the above insights, we can see that customers who start ordering from mid-year 4, 5, 6, 7, 8 tend to order statble, and relatively higher than the rest months of the year.</li>
  <li>Customer who place orders at the beginning of January and February only show stablility, nothing special.</li>
  <li>KPMG's year-to-date retention rate is quite good, all 30% or more (except 11st month at 25.5%)</li>
</ul>
<h1>Recommendations</h1>
<ul>
  <li>There should be attractive preferential policies for customers in the first months of the year to increase teh order rate (retention) over the months.</li>
  <li>The Mid-year months have higher retention rates than other months -> need to dive into why (with relevant data, and visualizatin of other data) to apply to other months of the year.</li>
</ul>
