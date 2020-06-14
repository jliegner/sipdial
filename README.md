# Sipdial per ESP8266 an Fritzbox

Mit diesem Code kann man mit einen ESP8266 eine Türklingel 
z.B. an der Fritzbox realisieren. Dazu muss in der Fritzbox ein neues 
Telefongerät eingerichtet werden. 

Im angehängten Code ist eine C++ Classe Sip enthalten die 
bis auf die Funktionen Sip::SendUdp(), Sip::Random(), Sip::Millis()und 
Sip::MakeMd5Digest() Plattform unabhängig ist.

Das ist wohl gemerkt kein fertiges Projekt für ahnungslose Bastler. Es 
ist nur als Demo zu verstehen. Nach dem Reset und Connecten an die 
Fritzbox wählt der ESP die festgelegte Nummer und legt sich dann nach 
15s in den Tiefschlaf.
Wer etwas sinnvolles damit machen will, muss den Rest dann noch selbst 
entwickeln.

Der gesamte Code der Sip-Klasse kommt ohne dynamischen Speicher aus. Es 
wird nur ein char Buffer für das Zusammenbauen der UDP Packete benötigt, 
den ich selbst nicht in der Klasse halte. Zu beachten ist weiterhin, 
dass sich die Klasse die Konfigurationsdaten die in der init-Funktion 
übergeben werden nicht buffert, die Pointer müssen deshalb über die 
Laufzeit gültig bleiben.

Das Projekt wurde bereits 2018 im mc-Forum vorgestellt. Alles weitere 
ist da nachzulesen.

https://www.mikrocontroller.net/topic/444994#new

