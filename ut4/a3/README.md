
<center>

# TÍTULO DE LA PRÁCTICA


</center>

***Nombre:*** Ayoze Hernández Díaz
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [](#id1)
+ [](#id2)
+ [](#id3)
+ [](#id4)
+ [](#id5)


#### ***Introducción***. <a name="id1"></a>

#### ***Objetivos***. <a name="id2"></a>

#### ***Material empleado***. <a name="id3"></a>

#### ***Desarrollo***. <a name="id4"></a>

#### ***Conclusiones***. <a name="id5"></a>

FICHERO CONF SERVER

```
[Interface]
Address = 10.0.0.1/24
ListenPort = 51820
PrivateKey = oOcNBCOgztu3YQOt0BEugueDL499VZ5UxrrePKkl/ng=
PostUp = iptables -A FORWARD -i %i -j ACCEPT; iptables -t nat -A POSTROUTING -o enp0s3 -j MASQUERADE
PostDown = iptables -D FORWARD -i %i -j ACCEPT; iptables -t nat -D POSTROUTING -o enp0s3 -j MASQUERADE

[Peer]
PublicKey = Dc050W3ZuCB8T6KFSyuW4atHaf7ssw5/xtpn2Si/+3E=
AllowedIPs = 10.0.0.2/32

[Peer]
PublicKey = KEmZ+Bsf9lgdL9k74nmAoisQVtzRCUCYYhIAYjlxQFM=
AllowedIPs = 10.0.0.3/32

```

FICHERO CONF WINDOWS

```

[Interface]
PrivateKey = ADdP9zssI9I1UCF5foz6R2FSRye40Jx3NKOggsfCtWQ=
ListenPort = 51820
Address = 10.0.0.3/24
DNS = 1.1.1.1

[Peer]
PublicKey = o6JHaYd6rJijSBVy0bD/TosQasK5Bo7yB+FDwFNyl1Y=
AllowedIPs = 0.0.0.0/0, ::/0
Endpoint = 172.19.99.214:51820

```

FICHERO CONFIGURACION UBUNTU CLIENTE

```
[Interface]
Address = 10.0.0.2/24
ListenPort = 51820
PrivateKey = UEG2SFTl2fWy+jGLBoOohNFxIG82iYQImUrZmI7De28=

[Peer]
PublicKey = o6JHaYd6rJijSBVy0bD/TosQasK5Bo7yB+FDwFNyl1Y=
AllowedIPs = 0.0.0.0/0, ::/0
Endpoint = 172.19.99.214:51820

```
