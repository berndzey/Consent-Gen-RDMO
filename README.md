## News 
**2026-02-10**: The first Version v0.1 is released. Notice that we are currently working on the Consent Generator. 

## About
This project started with the thesis for the "Zertifikatskurs FDM 2023/2024" by Bernd Zey (TU Dortmund). 
Since end of 2024, Wibke Kleina and Bernd Zey are working on this project. 

## Consent-Gen-RDMO
An informed consent generator for [RDMO](https://github.com/rdmorganiser/rdmo). 
The catalog is contained in the xml file consent-gen.xml, the view can be found in consent-gen-view.xml.

All attributes are defined in an own URI namespace/prefix https://fdm.tu-dortmund.de.  

## Installation
#### Via python call: 
go to your RDMO folder and call
```
./manage.py import /path-to-consent-gen-xml-file/consent-gen.xml
./manage.py import /path-to-consent-gen-xml-file/consent-gen-view.xml
```

#### Via RDMO-Management-Page: 
just import xml files

#### Issues with view

The xml import of the view can cause problems due to the combination of Django Template syntax and HTML. 

In this case, I suggest creating a new view by yourself on the managment page.
Add a URI prefix, URI path, and titles. 
Then, copy-paste the content from consent-gen-view.xml into the template-field. 
Here, you need the content from between the <template>-</template>-tags, 
i.e., starting with the line {% load view_tags %} and ending with the line \<p\>Ort, Datum, Unterschrift\</p\>
Finally, click on create...
