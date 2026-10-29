# Gestor de Contrasenyes

## Taula de Continguts

[Fase 1: Anàlisi i Justificació](#fase-1-anàlisi-i-justificació)

[Introducció i Justificació](#introducció-i-justificació)

[Que es un Gestor de Contrasenyas](#que-es-un-gestor-de-contrasenyas)

[Comparativa Tècnica](#comparativa-tècnica)

[Avantatges i Inconvenients](#avantatges-i-inconvenients)

[Fase 2: Guia d'Ús Tècnica](#fase-2-guia-dús-tècnica)


## Fase 1: Anàlisi i Justificació

### Introducció i Justificació

El cervell huma no esta fet per recordar moltes conrtasenyes diferents per aixo la gent utiliza contrasenyes senzilles o les reutilitza llavors sempre ets mes vulnerable a atacs fets per diccionari o inclus a força bruta per aixo estan els gestors de contrasenyes.

---

### Que es un Gestor de Contrasenyas

En resum: Genera i guarda una contrasenya llarga, aleatòria i única per a cada compte de cada web o aplicacio.

Generan Contrasenyas com 8x#K9!mP2$vLq aixo les fa quasi impossible crackajarles amb força bruta per aixo son tant utilis i les podem utilizar a la nostra empressa.

---

### Comparativa Tècnica

#### Bitwarden (Opció al Núvol)

Com funciona: Guardes les contrasenyes en una "caixa forta" que es sincronitza automàticament a través d'internet. Si afegeixes una contrasenya nova al mòbil, apareix al moment al teu ordinador.
Seguretat: Utilitza un sistema anomenat Zero-Knowledge (Coneixement Zero). Això vol dir que les teves contrasenyes es xifren al teu dispositiu abans de pujar al núvol. Ni els empleats de Bitwarden ni cap hacker que entri als seus servidors podrien llegir-les.

#### KeePassXC (Opció Local / Offline)

Com funciona: No utilitza internet. Guarda totes les teves contrasenyes en un sol fitxer (amb extensió .kdbx) que es queda guardat al disc dur del teu ordinador. Tu ets l'únic responsable d'aquest fitxer.
Seguretat: És molt segur perquè les dades mai surten del teu ordinari i estan fortament xifrades. El perill és que, si perds l'ordinador o el fitxer es fa malbé i no tens còpia, perds tot. També, si algú aconsegueix el fitxer, pot intentar endevinar la contrasenya mestra sense límit d'intents.

---

### Avantatges i Inconvenients

####  Model Online / Núvol

Avantatges: 

Seguretat: Utilitza xifratge Zero-Knowledge (el proveïdor no pot veure les teves dades). Les actualitzacions de seguretat són automàtiques i permeten forçar l'ús de 2FA a tots els empleats.

Usabilitat: Sincronització automàtica i instantània entre l'ordinador, el mòbil i la tablet. Compartir una contrasenya amb un company de l'equip es fa en dos clics, de forma segura.

Continuïtat del negoci: Si un empleat marxa de l'empresa, li pots revocar l'accés a totes les contrasenyes compartides en un sol clic. Les còpies de seguretat les gestiona el proveïdor.

Inconvenients: 

Seguretat: Tot i que el risc és molt baix gràcies al xifratge, sempre existeix la dependència de la infraestructura d'un tercer. Si els seus servidors tenen una caiguda massiva, podries tenir problemes temporals.

Usabilitat: Requereix connexió a internet per a la sincronització inicial o per afegir un dispositiu nou.

Continuïtat: En cas de caiguda total del servei del proveïdor (molt estrany), l'accés a noves contrasenyes des de dispositius no configurats quedaria blocat (tot i que la còpia local de l'ordinador sol funcionar).


#### Model Offline / Local

Avantatges: 

Seguretat: Control absolut. Les dades mai surten del teu ordinador. És immune a qualsevol hackeig o filtració que pugui patir un proveïdor de núvol extern.

Usabilitat: Funciona perfectament en qualsevol moment, amb o sense connexió a internet. La interfície és senzilla i no té distraccions.

Continuïtat del negoci: Total independència de talls d'internet o caigudes de serveis externs.

Inconvenients: 

Seguretat: Tu ets l'únic responsable. Si el teu ordinador es fa malbé, el perds o té un virus, perds tot si no has fet còpia de seguretat manualment. A més, si un atacant aconsegueix el fitxer, pot intentar endevinar la contrasenya mestra sense límit d'intents (atac offline).

Usabilitat: Compartir amb l'equip és un malson logístic. Si tres persones tenen el mateix fitxer i el modifiquen, es creen conflictes de versions (qui té l'última versio? s'han sobrescrit les dades?). No s'integra bé amb el mòbil.

Continuïtat del negoci: Gestionar la baixa d'un empleat és molt lent i manual. Has de canviar manualment totes les contrasenyes que aquesta persona pogués haver copiat, ja que no pots "revocar" l'accés al fitxer que ja té al seu ordinador.

---

### Recomanació Final: Bitwarden

Després d'analitzar les necessitats d'EverPia i l'incident de seguretat que acabem de patir, la nostra recomanació és implementar Bitwarden per a tot el personal tècnic de l'empresa.

Per què Bitwarden?

Bitwarden és l'eina que millor equilibra seguretat, facilitat d'ús i viabilitat per a un entorn de treball en equip. Aquests són els motius principals:

1. Seguretat real i transparent (Codi Obert + Zero-Knowledge)

Bitwarden és de codi obert, el que significa que la seva seguretat ha estat auditada per experts independents de tot el món. A més, utilitza xifratge Zero-Knowledge: les contrasenyes es xifren al teu dispositiu abans de pujar al núvol. Ni Bitwarden ni cap atacant que pugui accedir als seus servidors podrien llegir les nostres dades.

2. Soluciona el problema del treball en equip
A diferència de les opcions locals (com KeePassXC), Bitwarden permet crear carpetes o projectes compartits. Si un desenvolupador necessita accés a una base de dades o un servidor, se li pot donar permís de forma segura i controlada. Si aquesta persona marxa de l'empresa, es revoca el seu accés en un sol clic, sense haver de canviar manualment totes les contrasenyes que pogués haver copiat.

3. Elimina la fricció per a l'usuari
La versió gratuïta de Bitwarden ja inclou tot el necessari per a un ús tècnic robust: sincronització il·limitada entre ordinador i mòbil, generador de contrasenyes fortes, autocompletat al navegador (que a més protegeix contra phishing) i suport per a 2FA. Això fa que els empleats no tinguin cap excusa per no utilitzar-lo o per tornar a fer servir contrasenyes febles.

4. Auditoria i conscienciació automàtica
Bitwarden inclou eines que analitzen la teva caixa forta i t'avisen si estàs reutilitzant una contrasenya o si alguna ha aparegut en una fuita de dades pública. Això ajuda a netejar els mals hàbits de forma proactiva.

## Fase 2: Guia d'Ús Tècnica

El primer es instal·lar bit warden a la google chrome web store

![Captura bitwarden instal·lacio](/Activitat%20gestor%20contrasenyes/media/1.png)

Ara ens hem de registrar a l'aplicacio hem de posar una contrasenya mestra per accadir a totes les contrasenyes 

![Captura INicial Bitwaden](/Activitat%20gestor%20contrasenyes/media/2.png)

Un cop aqui anem a new, new login i despres posem la web de l'empressa posem el nostra nom d'usuari i que ens generi una contrasenya de mes de 12 carcters amb majusuculas minusculas i caracters especials.

![img 3](/Activitat%20gestor%20contrasenyes/media/3.png)

I simplement omplim el que falti

![img 4](/Activitat%20gestor%20contrasenyes/media/4.png)


---


