# Accés xarxes públicas

## Configuracions inicials: IP dels dos Zorin i del IPFire

Farem servir tres màquines virtuals: dos Zorin OS i un IPFire. El primer Zorin OS serà el client, el segon serà el servidor i l'IPFire serà el router que connectarà les dues màquines a Internet. 

Un zorin tindra xarxa interna i l'altre xarxa NAT, el ipFire tindra una interficie de xarxa interna i una altra de xarxa NAT.

<img src="img/6.png" width="600" />

<img src="img/7.png" width="600" />

<img src="img/8.png" width="600" />

Despres haurem de instalar els serveis de ssh i apache2 al servidor.

<img src="img/2.png" width="600" />

Comprovem que el serveis estan funcionant correctament:

<img src="img/3.png" width="600" />

<img src="img/4.png" width="600" />

<img src="img/5.png" width="600" />

## Destination NAT

Configurar DNAT (port forwarding) al firewall. Amb aquesta tècnica, el firewall escolta en un port de la seva IP pública i, quan rep una connexió, la redirigeix transparentment cap al servidor intern. Per a qui es connecta des de fora, sembla que el servei estigui allotjat al propi firewall.

## Regla DNAT per al servei web 

A la interfície web d'IPFire, s'obre Cortafuegos → Reglas → Nueva regla i s'omple el formulari amb aquests valors:

<img src="img/9.png" width="600" />

<img src="img/10.png" width="600" />

Un cop afegida i aplicada, la regla apareix a la llista del cortafocs. Des d'una màquina externa, s'obre el navegador apuntant a la IP pública del firewall (http://10.0.2.13) i la pàgina del servidor es carrega sense problemes.

<img src="img/11.png" width="600" />

<img src="img/12.png" width="600" />

## Regla DNAT per a SSH 

El procediment és el mateix que per al web, amb una particularitat: en lloc d'exposar el port 22 directament, es fa servir el port 2222 com a port extern. 

<img src="img/13.png" width="600" />

I agraguem la regla al firewall.

<img src="img/14.png" width="600" />

Quan un client extern es connecta al port 2222 del firewall, IPFire redirigeix la connexió al port 22 del servidor Zorin. La comprovació es fa des del PC extern.

```bash
ssh -p 2222 usuari@10.0.2.13
```

## Configuració de la VPN amb OpenVPN

<img src="img/15.png" width="600" />

<img src="img/16.png" width="600" />

<img src="img/17.png" width="600" />

<img src="img/18.png" width="600" />

<img src="img/19.png" width="600" />

<img src="img/20.png" width="600" />

<img src="img/21.png" width="600" />

<img src="img/22.png" width="600" />

<img src="img/23.png" width="600" />

<img src="img/24.png" width="600" />

<img src="img/25.png" width="600" />

<img src="img/26.png" width="600" />

<img src="img/27.png" width="600" />

<img src="img/28.png" width="600" />

<img src="img/29.png" width="600" />

<img src="img/30.png" width="600" />

<img src="img/31.png" width="600" />

<img src="img/32.png" width="600" />

<img src="img/33.png" width="600" />

<img src="img/34.png" width="600" />

<img src="img/35.png" width="600" />

<img src="img/36.png" width="600" />


<img src="img/37.png" width="600" />

<img src="img/38.png" width="600" />

<img src="img/39.png" width="600" />


