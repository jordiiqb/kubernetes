# Projecte final de grau superior d'ASIX
## Kubernetes
![kubernetes_logo](./arxius/imatges/1-kubernetes_logo.png)

---
---
### Introducció a Kubernetes 

#### Què és Kubernetes?  
  
Kubernetes és un sistema de software de codi obert que serveix per a automatitzar la implementació i gestió de sistemes d'aplicació complexos a gran escala, compostos per processos informàtics que s'executen en contenidors.  
  
Kubernetes permet executar aplicacions de software en milers de nodes d'ordinadors  
com si tots aquests nodes fossin un únic i enorme ordinador, fent que s'abstregui la infraestructura subjacent i fent que se simplifiqui el desenvolupament, el desplegament,  
i la gestió.
#### Origen de Kubernetes  
  
Kubernetes va ser desenvolupat originalment per Google. Google sempre ha executat  
aplicacions en contenidors. Ja en 2014, van dir que llançaven 2.000 milions de contenidors cada setmana. Això és més de 3.000 contenidors per segon, i la xifra és molt  
més gran avui. Fan funcionar aquests contenidors en milers d'ordinadors distribuïts a través  
dotzenes de centres de dades a tot el món.  
  
Per això van crear Kubernetes, perquè va sorgir la necessitat d'automatitzar totes les tasques d'arrencada, manteniment i actualització de containers a escala massiva.

#### D'on ve el nom Kubernetes?  
  
La paraula Kubernetes ve del grec i en aquest idioma vol dir timoner, o sigui, la persona que porta el timó d'un vaixell. Un timoner no és necessàriament el mateix que un  
capità. Un capità és responsable del vaixell, mentre que el timoner és qui el dirigeix.  
  
El timoner manté el curs del vaixell, porta a terme les ordres donades pel capità i li reporta el transcurs de la nau. Kubernetes dirigeix les aplicacions i reporta sobre el seu estat mentre tu - el capità - decideix on vol que vagi el sistema.

![2-timoner](./arxius/imatges/2-timoner.jpg)


#### Què fa Kubernetes?  
  
Kubernetes crea una capa d'abstracció entre l'usuari i tota la infraestructura de hardware fent que no importi sobre quin ordinador llancis la teva aplicació.  
  
Quan es desplega una aplicació a través de Kubernetes, automàticament ell selecciona  
un ordinador per a cada component de l'aplicació, el desplega i li permet trobar i comunicar-se fàcilment amb altres components de l'aplicació o d'altres aplicacions.

#### Què fa Kubernetes?  
  
Podem visualitzar Kubernetes com un sistema construït en capes, amb cada capa més alta abstraient la complexitat que es troba en els nivells més baixos.  
  
A la seva base, Kubernetes reuneix les màquines físiques o virtuals individuals en un clúster utilitzant una xarxa compartida per comunicar-se entre cada ordinador. Aquest clúster de Kubernetes és la plataforma física on es configuren tots els components, capacitats i càrregues de treball de Kubernetes.

![3-kub_capes](./arxius/imatges/3-kub_capes.png)
 
Quan es desplega una aplicació a través de Kubernetes, automàticament ell selecciona  
un ordinador per a cada component de l'aplicació, el desplega i li permet trobar i comunicar-se fàcilment amb altres components de l'aplicació i amb altres aplicacions, entre altres funcions.

#### Com s'estructura Kubernetes?

Cada ordinador que treballa sota el clúster de Kubernetes se'l coneix com a node.

Depenent de la funció que hagi de complir el node, aquest es pot categoritzar en Master node o en Worker Node.

* Els Master nodes treballen en el que es coneix com a "Control Plane". "El Control Plane" és el component de Kubernetes que actua com a porta d'entrada i com a cervell del clúster, exposant l'API de Kubernetes per a usuaris i clients, comprovant la salut d'altres nodes, decidint com dividir i assignar processos i orquestrant comunicació entre altres components.
Els Master nodes actuen com el punt principal de contacte amb el clúster i són els responsables de la major part de la lògica centralitzada que proporciona Kubernetes.

* Els Worker nodes treballen en el que es coneix com a "Workload Plane". "El Workload Plane" és el component de Kubernetes que executa les aplicacions en contenidors i és l'encarregat d'executar, controlar i proporcionar serveis a les aplicacions

![4-cwplanes](./arxius/imatges/4-cwplanes.PNG)