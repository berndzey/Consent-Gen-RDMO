## News 
**2026-02-11**: Kleineres Update zu den verwendeten Quellen und die Ansicht wurde in Bezug auf "Drittland" erweitert
**2026-02-10**: Die erste Version des ConsentGen. Bitte beachten Sie, dass dies eine "Work-in-Progress"-Version ist und wir aktuell am Generator arbeiten. 

## Allgemeine Informationen
Das Projekt startete mit der Abschlussarbeit zum "Zertifikatskurs FDM 2023/2024" von Bernd Zey (TU Dortmund). 
Seit Ende 2024 arbeiten Wibke Kleina und Bernd Zey an diesem Projekt. 

## Consent-Gen-RDMO
Ein Einwilligungserklärungsgenerator für [RDMO](https://github.com/rdmorganiser/rdmo). 
Der Katalog ist in der xml-Datei consent-gen.xml enthalten, die zugehörige Ansicht in consent-gen-view.xml.

Alle Attribute sind in einem eigenen URI Namensraum/Prefix definiert: https://fdm.tu-dortmund.de.  

## Installation
#### Via Python Call: 
im RDMO-Ordner aufrufen: 
```
./manage.py import /path-to-consent-gen-xml-file/consent-gen.xml
./manage.py import /path-to-consent-gen-xml-file/consent-gen-view.xml
```

#### Via RDMO-Management-Seite: 
einfach die xml-Dateien importieren

#### Probleme mit dem Import der Ansicht

Der Import der xml-Dateien kann zu Problemem führen (aufgrund der Django Template Syntax und HTML). 

In diesem Fall schlagen wir den Workaround vor, die Ansicht direkt in RDMO selber zu erstellen. 
Dafür gehen Sie auf die Management-Seite Ihrer RDMO-Instanz. 
Dort erstellen Sie eine neue Ansicht, vergeben einen URI Prefix, URI Pfad und die Titel. 
Dann kopieren Sie den Inhalt der consent-gen-view.xml in den Vorlage-Bereich. 
Hierbei muss nur der Inhalt zwischen den <template>-</template>-tags koppiert werden, 
d.h. der relevante Teil beginnt mit der Zeile {% load view_tags %} und endet mit der Zeile \<p\>Ort, Datum, Unterschrift\</p\>. 
Dann nur noch auf "Erstellen" klicken...
