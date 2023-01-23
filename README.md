# Atlab_Gerald_Wohnzimmer
von David Kaltenbrunner, Petranka Petrova, Shciprim Kurtaj und Viktor Mandic

# Inhaltsverzeichnis
Zustand und Wünsche vom Klienten Gerald\
Unsere Lösung\
Unsere Komponenten\
Bedienung unseres Systems


## Zustand und Wünsche vom Klienten Gerald
Aufgrund einer starken körperlichen Einschränkung und einer Hörbeeinträchtigung, ist unser Klient Gerald ein Pflegefall. 

Folgende Funktonen sind bei Gerald vorhanden:
- rechter Arm leicht heben/senken (keine Handfunktion)
- große Zehe links
- Kopf
- Mund/Lippen, Saugen/Pusten
- Augen
- Non-Verbal
- Klänge wahrnehmen

Er würde gerne:

**Seine Umgebung steuern**

- Licht ein- und ausschalten
- Jalousien öffnen und schließen
- Fernseher steuern 

**Seinen Computer bedienen**

- Surfen
- E-Mails schreiben
- Musik hören


**Sein Smartphone verwenden**

- SMS schreiben
- Anruf tätigen

## Unsere Lösung 
Gerald kann mit unserem System seinen Computer steuern. Über den Computer kann er dann sein Handy, seine Umgebung steuern und sich entertainen lassen.

## Unsere Komponenten

Für unsere Lösung haben wir folgende Komponenten verwendet:

**FlipMouse**\
Ermöglicht den Zugriff auf die Maus (bewegen in x- und y-Richtung, Links- und Rechtsklick)


**FABI**\
Mithilfe des FABI kann die Systemlautstärke stummgeschalten und entstummt werden. Aufgrund einer Zeichenbegrenzung bei den Makros des FABI ist die momentan leider nur mithilfe von drei Knöpfen möglich.

**Asterics Grid**\
Für die Umgebungssteuerung.\
Ermöglicht den Zugriff über ein visuelles Bedienpult auf:
- Licht an/aus
- Jalousien rauf/runter
- Fernseher (an/aus, Nummer-Tasten, Lautstärke, Sender wechseln, Menü)
- Musik (Spotify)

**Asterics Runtime Enviroment (ARE)**\
Das Asterics Runtime Enviroment ermöglicht den Zugriff des Asterics Grids auf OpenHab und damit auch auf die Umgebungssteuerung. Des Weiteren wird auch der Zugriff auf den IRTrans Server ermöglicht.

**IR TRANS (Infrarot Transmitter and Receiver)**\
Mithilfe des IR Trans wurden die Infrarotsignale der Originalen Fernbedienung des Fernsehers aufgezeichnet. Diese können mithilfe des IR Trans Servers und dem IR Trans wiedergegeben werden und den Fernseher steuern. Der Zugriff auf die Daten erfolgt über das Asterics Runtime Enviroment.

**Link zu Windows**\
Verbindung vom Computer zum Android-Smartphone. Dabei kann auf SMS, Anrufliste, Benachrichtigungen und den Smartphone Bildschirm zugegriffen werden.

**Bildschirmtastatur**\
Digitale Tastatur. Kann über die Windows-Einstellungen unter dem Punkt _Tastatur_ eingeschaltet werden. Durch die Kombination eben dieser und der Flipmouse kann eine Tastatur simuliert werden.

**OpenHab**\
Mithilfe von OpenHab können die im OpenHabserver des Labors eingebundenen Geräte (Lampen, Jalousien etc.) gesteuert werden. Mithilfe des Aserics Grid und der ARE kann so die Umgebung relativ einfach gesteuert werden - siehe ARE.


## Bedienung und Nachvollziehbarkeit unseres Lösungsansatzes

Die _Flipmouse_ haben wir verwendet, als Ersatz für eine physische Maus. Gerald kann seine Hände nicht für eine physische Maus verwenden, jedoch verfügt er über generelle Mundfunktionen(bewegen, pusten, saugen). Mit dem Mund kann er dann über die Flipmaus den Windows-Mauszeiger in alle Richtungen steuern. Mit dem Pusten und Saugen kann ein Rechts- bzw. Linksklick simuliert werden. In unserem Fall wird aus hygienischen Gründen das saugen und pusten durch zwei Knöpfe getauscht.

Screenshots von FlipMouse und ihre Einstellung $$$$$$$

Für die Einstellung von der Flipmouse haben wir folgende Seite verwendet:\
<https://flipmouse.asterics.eu/index_fm.htm#tabStick>

Mit der integrierten _Windows-Bildschirmtastatur_ hat Gerald dann die Möglichkeit, auf seine Tastatur über die Flipmouse zuzugreifen. Die Tastatur kann über die Einstellungen eingeschaltet werden. Dadurch kann man zum Beispiel über die Flipmouse mit der Bildschirmtastatur E-Mails schreiben.

![alt text] (./Screenshots/Mail_Bildschirmtastatur.png?raw=true "Windows Bildschirmtastur Mail-Schreiben") 

Da er Zugriff auf sein gesamtes Computer-System hat, wurde sein Computer so eingerichtet, dass er die restlichen FUnktionen auch über diesen machen kann.

Mit einem _Asterics-Grid_ (https://grid.asterics.eu/#grids) kann er über ein visuelles Bedienpult mit Bildern und Beschriftungen das Licht im Wohnzimmer ein- und ausschalten, Fernseher bedienen, Spotify öffnen und Jalousien öffnen und schließen. 

![Alt text] (./Screenshots/Grid_Home.png)



Bedienpult seiner digitalen Fernbedienung:
![alt text] (./Screenshots/Grid_Fernseher.png?raw=true "Asterics Grid Fernseher") 

Über den _IR-Trans_ werden Signale über Infrarot vom Grid zum Fernseher gesendet. $$

Mit dem Programm _Link zu Windows_ kann Gerald mit seinem Computer sein Android-Smartphone steuern. Dabei wird der Bildschirm des Handys auf den Computer übertragen. Über die Flipmouse kann er dann das Handy bedienen (Anrufe tätigen, SMS schreiben). 

![alt text] (./Screenshots/Windows_Link_Calls_Censored.png?raw=true "Windows Link Anruf") 

![alt text] (./Screenshots/Windows_Link_Messages_Censored.png?raw=true "Windows Link SMS") 

Mit dem _Fabi_............. $$$$
Mit dem rechten Elbogen kann er diese drei Taster bedienen. Mit dem ersten Button öffnet man die Kommandozeile, mit dem Zweiten kopiert sich was raus ($$$) und der letzte Button schaltet die Lautstärke ein oder aus. 

![alt text] (./Screenshots/FABI_Conf.png?raw=true "FABI Config") 
![alt text] (./Screenshots/FABI_Slots.png?raw=true "FABI Slots") 

![alt text] (./Screenshots/FABI_Bu3.png?raw=true "FABI Button 3") 
![alt text] (./Screenshots/FABI_Bu4.png?raw=true "FABI Button 4") 
![alt text] (./Screenshots/FABI_Bu5.png?raw=true "FABI Button 5") 



_Openhab_.........$$$$
+ Fernseher (IR-Trans wie das gemacht wurde) $$$$


![alt text] (./Screenshots/Grid_OpenHab_Innenleben.png?raw=true "Innenleben OpenHab") 
![alt text] (./Screenshots/Grid_Fernseher_Innenleben.png?raw=true "Innenleben Fernseher") 
![alt text] (./Screenshots/ARE_IRTrans.png?raw=true "IR Trans") 


_Asterics ARE ....... $
![alt text] (./Screenshots/ARE_Main.png?raw=true "ARE Main") 


##FittsTask2D## $$$$$$



