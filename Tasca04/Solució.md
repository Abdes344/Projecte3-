SERVEIS DIRECTORI LDPA

![imatge](/Tasca04/LDAP/1.png)  
![imatge](/Tasca04/LDAP/2.png)  
![imatge](/Tasca04/LDAP/3.png)  
Abans de començar el que tindrem que fer serà ficar el adaptador 1 en xarxa NAT i el adaptador 2 en Adaptador Només en anfitrió 

![imatge](/Tasca04/LDAP/4.png)  
El primer que farem sera fer una actualització del sistema perquè estigui tot perfecte   
![imatge](/Tasca04/LDAP/5.png)  
Despres haurem de ficar la comanda “Sudo nano /etc/hosts” i modificarem al domini ficant el nostre   
![imatge](/Tasca04/LDAP/6.png)  
Ara amb les comandes “Hostname i “Hostname \-f” comprovarem que tenim configurat el servidor i el domini   
![imatge](/Tasca04/LDAP/7.png)  
![imatge](/Tasca04/LDAP/8.png)  
Amb Aquesta Comanda “Sudo apt install slapd ldap-utils \-y” instalarem el servei LDAP

![imatge](/Tasca04/LDAP/9.png)  
Després de instal·lar el servei LDAP comprovarem si tot està correcta i funciona correctament 

   
![imatge](/Tasca04/LDAP/10.png)  
![imatge](/Tasca04/LDAP/11.png)  
![imatge](/Tasca04/LDAP/12.png)
![imatge](/Tasca04/LDAP/13.png)
![imatge](/Tasca04/LDAP/14.png)  
![imatge](/Tasca04/LDAP/15.png)
![imatge](/Tasca04/LDAP/16.png) 
![imatge](/Tasca04/LDAP/17.png) 
Amb la Comanda “Sudo dpkg-reconfigure slapd” reconfigurarem el servei”.

![imatge](/Tasca04/LDAP/18.png)  
Ara comprovem que el directori s'ha creat correctament 

![imatge](/Tasca04/LDAP/19.png)  
El client, ens demana crear dues Unitats Organitzatives ara crearem amb extensió “.ldif”: *sudo nano OU\_users.ldif*

![imatge](/Tasca04/LDAP/20.png)  
Després ficarem la següent comanda *ldapsearch dapadd \-D “cn=admin,dc=innovatech14,dc=test” \-W \-f OU\_users.ldif*

![imatge](/Tasca04/LDAP/21.png) 
Revisem si els OUs s'ha creat bé amb la comanda “ ldapsearch \-xLLL \-b “dc=innovatech13,dc=test”  
![imatge](/Tasca04/LDAP/22.png) 
Per gestionar i administrar el (LAM) entrarem al gestor gràfic desde Google amb l'URL següent   
[http://192.168.56.104/lam/templates/login.php](http://192.168.56.104/lam/templates/login.php)

![imatge](/Tasca04/LDAP/23.png)  
Ara entrarem en el apartat que diu “edit server profiles”   
![imatge](/Tasca04/LDAP/24.png)  
Aquí per entrar ficarem la contrasenya “lam”, ja que es la que bé per defecte 

![imatge](/Tasca04/LDAP/25.png)  
![imatge](/Tasca04/LDAP/26.png)  
Aquí modificarem el idioma, Compte i el admin

![imatge](/Tasca04/LDAP/27.png)  
Després anirem a “tipos de cuenta” i configurarem els OUs pels grups i usuaris  

![imatge](/Tasca04/LDAP/28.png)

![imatge](/Tasca04/LDAP/29.png)

![imatge](/Tasca04/LDAP/30.png)  
![imatge](/Tasca04/LDAP/31.png)  
En el següent apartat, crearem dos grups de seguretat al directori “tech i manager”.

![imatge](/Tasca04/LDAP/32.png)  
Tot seguit, configurarem el hostname i asignarem un nom a l’ip del nostre servidor modificant l’arxiu /etc/hosts amb *sudo nano /etc/hosts*

![imatge](/Tasca04/LDAP/33.png)

Per veure el hostname haurem d'utilitzar la següent comanda

![imatge](/Tasca04/LDAP/34.png)

![imatge](/Tasca04/LDAP/35.png)

![imatge](/Tasca04/LDAP/36.png) 
![imatge](/Tasca04/LDAP/37.png)  
![imatge](/Tasca04/LDAP/38.png)  
![imatge](/Tasca04/LDAP/39.png)

![imatge](/Tasca04/LDAP/40.png)

Ara instal·larem els paquets per gestionar ldap i els seus usuaris  
*sudo apt install libnss-ldapd libpam-ldapd nslcd \-y*

Seguidament haurem de modificar les extensions següents:

- Primer de tot haurem de modificar l’extensió */etc/nsswitch.conf* amb ldap en passwd, group. sudo nano /etc/nsswitch.conf.

![imatge](/Tasca04/LDAP/41.png)

![imatge](/Tasca04/LDAP/42.png)  
Ara, modificarem /etc/pam.d/common-password i comentar la línea marcada  sudo nano /etc/pam.d/common-password

![imatge](/Tasca04/LDAP/43.png)  
Finalment, l’última extensió que haurem de modificar és  
/etc/pam.d/gdm-launch-environment per activar l’autenticació LDAP. 

![imatge](/Tasca04/LDAP/44.png)  
Y per finalitzar al entrar al tech01 anem a la terminal y fiquem id y ens te que ficar el que hi ha a la pantalla   
![imatge](/Tasca04/LDAP/45.png)  
I per finalitzar al entrar al manager01 anem a la terminal i fiquem id i en te que ficar el que hi ha a la pantalla 

![imatge](/Tasca04/LDAP/46.png)  
I aquí veurem que tenim totes les comptes amb les que podem entrar
