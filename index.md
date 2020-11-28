# Manuale italiano Docker
Comandi e funzionalità Docker

## Comandi

### Creare un nuovo container
#### Esempio:

_docker run --name chronograf -p 8888:8888 chronograf_

#### Comando:
> docker run --name **_container-name/id_** -p **_container-port_**:**_host-port_** **_image-id_**

### Creare container custom
**docker-compose.yml**: Definisce i servizi (container che verranno creati)

**Dockerfile**: usato per buildare un’immagine docker, definisce le dipendenze e quali comandi verranno eseguiti dal container.

#### Comando:
> docker-compose up (-d per detached mode)

### Far partire container esistente
#### Comando:
> docker start **_container-name_**

### Fermare container
#### Comando:
> docker stop **_container-name_**
