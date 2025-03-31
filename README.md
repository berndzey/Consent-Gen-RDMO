## News 
**2025-03-17**: New versions are commited. We are currently working on a new version and a first major release of the consent generator. 

## About
This project started with the thesis for the "Zertifikatskurs FDM 2023/2024" by Bernd Zey (TU Dortmund). 
Since end of 2024, Wibke Kleina and Bernd Zey are working on this project. 

## Consent-Gen-RDMO
An informed consent generator for [RDMO](https://github.com/rdmorganiser/rdmo). 
The catalog is contained in the xml file consent-gen.xml, the view can be found in consent-gen-view.xml.

All attributes are defined in an own URI namespace/prefix https://fdm.tu-dortmund.de.  

## Installation
Via python call: 
go to your RDMO folder and call
```
./manage.py import /path-to-consent-gen-xml-file/consent-gen.xml
./manage.py import /path-to-consent-gen-xml-file/consent-gen-view.xml
```

Via RDMO-Management-Page: just import xml files
