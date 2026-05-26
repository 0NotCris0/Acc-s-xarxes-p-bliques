# Activitat: Accés a Xarxes Públiques

## Descripció

En aquesta activitat es configurarà un entorn de xarxa amb **IPFire** i dues màquines **Zorin OS** per permetre l’accés segur a serveis interns des d’una xarxa pública.  

Es treballaran conceptes de:
- Configuració d’adreçament IP
- Regles DNAT
- Accés remot mitjançant SSH
- Publicació d’un servei web HTTP
- Configuració d’una VPN
- Validació i comprovació del funcionament dels serveis

---

## Objectius

Els objectius principals de la pràctica són:

- Configurar correctament la xarxa entre les màquines.
- Permetre l’accés remot per SSH utilitzant regles DNAT.
- Publicar un servei web intern cap a l’exterior.
- Configurar una VPN entre client i servidor.
- Verificar el funcionament correcte de totes les configuracions.
- Documentar tots els passos realitzats de manera clara i ordenada.

---

## Contingut de la pràctica

### 1. Configuracions inicials
Es configuraran les adreces IP de:
- Les dues màquines Zorin
- El firewall IPFire

També es comprovarà la connectivitat entre equips.

---

### 2. Configuració DNAT per SSH
Es crearà una regla DNAT a IPFire per permetre connexions SSH des de la xarxa pública cap a una màquina interna.

Posteriorment:
- Es realitzarà una prova de connexió SSH.
- Es documentaran les captures i els resultats obtinguts.

---

### 3. Configuració DNAT per HTTP
Es publicarà un servei web intern mitjançant una regla DNAT.

Posteriorment:
- Es verificarà l’accés al servidor web des de l’exterior.
- Es mostraran proves del correcte funcionament.

---

### 4. Configuració VPN
Es configurarà un servidor VPN a IPFire:
- Creació de certificats
- Configuració del servidor
- Configuració del client VPN

Finalment:
- Es provarà la connexió VPN.
- Es validarà l’accés segur a la xarxa interna.

---

## Activitat extra

- Configura el servidor amb els paràmetres bàsics.
- Genera l’arxiu de configuració del client.
- En Linux:
   - WireGuard ja ve integrat al *kernel*.
   - Es pot configurar des del *Network Manager*.
- En Windows 11:
   - Cal instal·lar el client de WireGuard.
- Exporta l’arxiu de configuració al client extern.
- Comprova que la connexió VPN funciona correctament.

--- 

## Criteris de qualificació

La pràctica es valorarà segons:
- La correcta configuració dels serveis
- La documentació dels passos realitzats
- Les proves de funcionament
- La presentació i organització del README

---

## Resultat esperat

Al final de l’activitat s’haurà aconseguit:
- Publicar serveis interns de manera controlada.
- Accedir remotament a equips interns.
- Configurar una connexió VPN funcional i segura.
- Comprendre el funcionament bàsic de les regles DNAT i les VPN.

---

- [Guia detallada de la pràctica](guia.md)