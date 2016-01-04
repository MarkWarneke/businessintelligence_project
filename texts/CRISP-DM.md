# Business Understanding
* Definition Geschäfts- und DM-Ziele
* Aufwandsschätzung, Projektplanung

## Geschäfts-Kontext
* Elektronik-Handelsunternehmen
* Großteil über Auktionsplattform
* Auktionen zum Teil sehr unterschiedliche Verkaufserlöse

## Ziele
--> Erlösmaximierung (Optimierungsmaßnaheme)
--> Evaluierung der Vertriebsaktivitäten

### Erste Schritt
* Neu eingestellte Aktion Vorhersagen ob Verkaufserlöse des Artikels über dem durchschnittlichen Verkaufserlös der Produktkategorie liegt
* Grundlage: 8.000 Online Auktionen
* aus Kategorie: Audio&Hi-Fi:MP3-Player:Apple iPod

### Variablen
 (Zielvariable) = gms_greater_avg
* category_avg_gms: mittlere Verkaufserlös der jeweiligen Produktkategorie 
* gms_greater_avg: Verkaufserlös der jeweiligen Auktion über dem mittleren Verkaufserlös

### Gewinnmatrix
* Hochpreis 
	* Verkaufserlös über dem Mittelwert
	* category_avg_gms = 1
* Niedrigpreis 
	* Verkaufserlös unter oder gleich dem Mittelwert	
	* category_avg_gms = 0
	
### Bewertung
Gesamtpunktzahl durch Vergleich Ihrer Prognosen mit tatsächlichem Wert enstprechend
* 1|1 oder 0|0
	* Jede richtig eingestufte Auktion gibt 1 Punkt 
* 0|1 oder 1|0
	* Jede falsch eingestufte Auktion gibt -1 Punkt 

#### Ziel
Gesamtpunktzahl = 1*[1|1] - 1*[0|1] + 1*[0|0] - 1*[1|0] 
(entspricht Richtig Hochpreis - Falsch Hochpreis + Richtig Niedrigpreis - Falsch Niedrigpreis)

Richtige Zuordnung:
* [0|0] 
	* Anzahl der richtigen Zuordnungen zu Klasse 0 
* [1|1] 
	* Anzahl der richtigen Zuordnungen zu Klasse 1 
	
Falschzuordnung:
* [0|1] 
	* Anzahl der Zuordnungen zu Klasse 0 aus realer Klasse 1 (Falschzuordnung) 
* [1|0] 
	* Anzahl der Zuordnungen zu Klasse 1 aus realer Klasse 0 (Falschzuordnung) 

	
### Zweiter Schritt
Evaluierung der bisherigen Vertriebsaktivitäten.
Segmentierung der Auktionen für entsprechende Kategorie.
Ermittelten Segmente sollen anhand Ihrer Effektivität zur Erreichung der Vertriebsziele (Optimierung) bewerten

### Dritter Schritt
Werbepräsenz Klickverhalten
Jüngere Zielgruppe ist spezielle Webpräsenz geschaffen worden
Zugriff auf kostenlose Medieninhalte
Klickverhalten dieser Plattform soll marketing-relevante Ansätze von Inhaltskombinationen überprüfen



## Konkrete Aufgabe

1. Klassifikationsanalyse
Trainingsdaten (e-auction_train.txt) 
Klassifizierungsdaten (e-auction_class.txt) 
Entscheidung treffen, ob Auktionsmerkmale als Hoch- oder Niedrigpreis einzustufen
Ziel ist Punktzahlmaximierung.

..* Performance:
Gesamt-Klassifikationskosten/gewinne bestimmt

2. Segmentierungsanalyse
 Clusterbildung möglichst homogen, 
 im Vergleich zu den anderen Clustern jedoch möglichst heterogen
Interpretieren der Cluster & ableiten von Implikationen für das Marketing

..* Performance:
Silhouetten-Koeffizienten

..* Randbedingungen:
mindestens 15 Variablen für Segmentierung zur Verfügung 
mindestens 3 Cluster gebildet
  
3. Assoziationsanalyse
Angeklickter Servicedienste auf der neuen Website (website_train.txt)
Ableiten relevanter Regeln für das Cross-Selling des Musik-Streaming-Services 
 
..* Performance: 
Erläuterung der Vorgehensweise und Lösung
 
### Bewertung
* Methodisch korrekte Durchführung der Analyse 
* Komplexität / Effizienz / Originalität der Streams 
* Dokumentation der Vorgehensweise und Lösung sowie ggf. Interpretation in Form von Präsentationsfolien 

 
# Data Understanding
* Festlegung der relevanten Attribute 
* Beschreibung/Exploration der Daten 

## Zielvariable
gms_greater_avg

## Variablen
* category_avg_gms: mittlere Verkaufserlös der jeweiligen Produktkategorie 
* gms_greater_avg: Verkaufserlös der jeweiligen Auktion über dem mittleren Verkaufserlös

### category_avg_gms
* category_avg_gms = 1
	* Hochpreis 
	* Verkaufserlös über dem Mittelwert
* category_avg_gms = 0
	* Niedrigpreis 
	* Verkaufserlös unter oder gleich dem Mittelwert	
	
	
	

# Data Preparation
* Datenselektion/-bereinigung/-integration 
* Datentransformation 

# Modeling
* Auswahl Verfahren und Tools 
* Modellbildung u. Parameter-Set-up 

# Evaluation
*  Bewertung der Ergebnisse 

# Deployment
* Berichtserstellung 
* Planung Überwachung und Wartung 