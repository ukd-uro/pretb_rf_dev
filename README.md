# Prätherapeutisches Tumorboard Textmodell für Prostatakarzinom-Patienten mit Random Forest Classifikation

Das Ziel dieses Projekts war es, die Fähigkeiten klassischer maschineller Lernalgorithmen zur Vorhersage von urologischen Tumorboards im Zeitalter des Deep Learning zu untersuchen. Das Hauptziel bestand darin, einen maschinellen Lernalgorithmus zu trainieren und zu validieren, der automatisch Empfehlungen für Tumorboards generiert. Die Trainingsdaten basieren auf unserem institutionellen Tumorboard-Dokumentationssystem. Mit Prostatakrebs diagnostizierte Patienten werden routinemäßig als Teil unseres zertifizierten onkologischen Zentrums an unser prätherapeutisches Tumorboard überwiesen. Dies gewährleistet multidisziplinäre Expertise und individuell zugeschnittene diagnostische sowie therapeutische Empfehlungen.

Die Daten wurden mithilfe von regulären Ausdrucksskripten sowie manuell durch unser Personal verarbeitet. Potenzielle klinische Prädiktoren wurden aus den Patientenakten des Tumorboards extrahiert und als kontinuierliche oder kategoriale Variablen in einer speziellen Datenbank gespeichert. Die Zielvariablen wurden auf die gleiche Weise extrahiert und als boolesche Variablen gespeichert. Da mehrere Empfehlungen gleichzeitig möglich sind, wurde die endgültige Zielvariable als Multi-Label-Vektorvariable definiert.

Wir trainierten und testeten drei verschiedene multivariable maschinelle Lernalgorithmen, die sich am besten für Multi-Label-Klassifikationsaufgaben eignen: Entscheidungsbaum, Random Forest und K-Nearest Neighbour. Eingabevariablen waren Alter, PSA, DRU, ISUP-Kategorie, Anzahl positiver Biopsie-Zylinder, Anzahl aller Biopsie-Zylinder und Vorerkrankungen (Bluthochdruck, Diabetes mellitus, koronare Herzkrankheit, Adipositas, frühere Operationen). Zielvariablen waren Empfehlungen für PSMA-PET-Bildgebung, konventionelle Bildgebung (CT und Knochenszintigraphie), aktive Überwachung und lokale Therapie (radikale Prostatektomie und Strahlentherapie).

Alle Modelle wurden durch eine 80:20-Aufteilung in Trainings- und Testdatensätze trainiert und validiert. Die Gesamtgenauigkeit, Präzision, Sensitivität und F1-Scores für jede einzelne Empfehlung wurden im Testdatensatz ausgewertet. 95%-Konfidenzintervalle wurden mittels Bootstrap-Sampling mit n=1000 berechnet. Das beste Modell wurde schließlich im Pickle-Format gespeichert und für eine einfache Webanwendung zu Demonstrationszwecken verwendet.

Der Code für die Webanwendung kann über dieses [Repository](https://github.com/ukd-uro/pretb_rf_app) auf diesem Hub abgerufen werden. Die Anwendung selbst wird über [Streamlit Community Cloud](https://pretb-rf.streamlit.app) bereitgestellt.

> [!Note]
> Sie können uns gerne kontaktieren, wenn Sie Fragen oder Ideen zu diesem oder potenziellen neuen Projekten haben.
