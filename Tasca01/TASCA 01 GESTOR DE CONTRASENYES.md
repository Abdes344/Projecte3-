**TASCA 01 GESTOR DE CONTRASENYES**

Informe Tècnic: Justificació per a la implantació d’un gestor de contrasenyes 

Les contrasenyes febles són un risc crític per a l’empresa perquè faciliten atacs com el diccionari “Es una técnica que prova ràpidament paraules i combinacions comunes per adivinar contraseñas”. Aquestes tècniques permeten als atacants accedir molt fàcil al sistema si les contrasenyes no son segures.

Funció Crucial del Gestor de contrasenyes

Un gestor de contrasenyes crea i guarda contrasenyes úniques i segures, evitant la reutilització i millorant la seguretat de l’empresa. 

Taula Comparativa: 

| Comparativa  | BitWarden  | KeePassXc |
| :---- | :---- | :---- |
| Sincronització  | Automàtica Via Núvol  | Manual  |
| Model de Seguretat  | Xifratge End-to-End | Xifratge Local  |
| Accés MultiPlataforma  | Apps i Extensions per a molts sistemes  | Apps i Extensions bàsiques  |
| Model De Cost  | Gratuït  | Gratuït i codi Obert  |

Avantatges i Inconvenients 

BitWarden:   
Avantatges: Sincronització automàtica, accés fàcil, xifratge end-to-end, suport i actualitzacions  
   
Inconvenients: Depèn d’internet i del servei, possible risc si el servei falla.

Kee PassXc:   
Avantatges: Control total local, no necessita internet, codi obert.

Inconvenients: Sincronització manual, menys còmode, depèn de conservar el fitxer local.

Recomanació:   
Recomano Bitwarden perquè combina sincronització automàtica, accés fàcil des de qualsevol dispositiu i xifratge end-to-end, oferint una solució segura i còmoda. Això facilita la gestió de contrasenyes per al personal tècnic sense complicacions ni riscos associats a la sincronització manual.

Fase 2: Guia d'ús tècnic   
![imatge](/Tasca01/IMG/1.png)  
Al entrar a BitWarden ens demana iniciar sesión pero al entrar per primera vegada tindrem que crearse un compte   

---

![imatge](/Tasca01/IMG/2.png)
Aquí després de iniciar sessió ja estarem dintre en el menú principal 

---

![imatge](/Tasca01/IMG/3.png)  
El generador de contrasenyes permet triar la longitud desitjada i incloure caràcters especials, números i majúscules per augmentar la seguretat. Configura els paràmetres segons les necessitats i prem generar. Així obtindràs una contrasenya forta i aleatòria.

---

\- Exemples d'Ús i Emplenament Automàtic:

\- Com desar una credencial d'un compte de correu electrònic.
![imatge](/Tasca01/IMG/4.png)

---

\- Com desar una credencial d'una aplicació o servei web.
![imatge](/Tasca01/IMG/5.png)

---
  
\- Com fer servir l’extensió del navegador per emplenar automàticament les dades  
![imatge](/Tasca01/IMG/6.png)

---

\- Gestió de Còpies de Seguretat (Backup):

Explicació detallada de com fer una còpia de seguretat de l'arxiu de contrasenyes (KDBX en KeePass o Exportació en Bitwarden).  
![imatge](/Tasca01/IMG/7.png)
![imatge](/Tasca01/IMG/8.png) 

El que tindrem que fer sera entrar a l'aplicació de BitWarden i ens dirigirem adalt a l'esquerra on l’apartat de archivo entrarem a l’apartat de exportar caja fuerte. 

---

![imatge](/Tasca01/IMG/9.png)   
Després de entrar en aquell apartat en sortirà aquest menú de aquí i no tindrem que tocar res ja que el .json es el que ve per defecte i el deixarem així

---

![imatge](/Tasca01/IMG/10.png)    
Aquí ficarem la nostra contraseña maestra per poder continuar 

---

![imatge](/Tasca01/IMG/11.png) 

I per acabar el que tindrem que fer sera guardar l'arxiu en un USB segur 

---

Recomanació de la millor pràctica per emmagatzemar aquesta còpia de seguretat de forma segura (clau USB xifrada o emmagatzematge xifrat al núvol).

La millor pràctica és guardar la còpia de seguretat en una clau USB o disc dur extern xifrat i mantenir-lo en un lloc segur. Una altra opció pot ser usar emmagatzematge al núvol amb xifrat d’extrem a extrem, però mai deixar el fitxer sense protecció en carpetes compartides o dispositius connectats a Internet.
