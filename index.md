# Manuale italiano Docker
Comandi e funzionalità Docker

## Comandi

### 1. Creare un nuovo container
#### Esempio:

_docker run --name chronograf -p 8888:8888 chronograf_

#### Comando:
> docker run --name **_container-name/id_** -p **_container-port_**:**_host-port_** **_image-id_**

### 2. Creare container custom
**docker-compose.yml**: Definisce i servizi (container che verranno creati)

**Dockerfile**: usato per buildare un’immagine docker, definisce le dipendenze e quali comandi verranno eseguiti dal container.

#### Comando:
> docker-compose up (-d per detached mode)

### 3. Far partire container esistente
#### Comando:
> docker start **_container-name_**

### 4. Fermare container
#### Comando:
> docker stop **_container-name_**

### 5. Fermare tutti i container in esecuzione
#### Comando:
> docker stop $(docker ps -aq)

### 6. Entrare in container in esecuzione
#### Comando:
> docker exec -it **_container_name_** bash

### 7. Visualizzare l’output di un container
#### Comando:
> docker logs -f **_container_name_**

### 8. Conoscere IP container
#### Comando:
> docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' **_container_name_**

### 9. Eliminare immagine
#### Comando:
> docker rmi **_immagine_**

### 10. Eliminare container
#### Comando:
> docker container rm **_container_**

### 11. Loggare GiitHub con Docker
E’ necessario innanzitutto:
Generare il token da GitHub
Aprire in CLI la cartella in cui è contenuto il file .txt con il token GitHub
#### Comando:
> cat **_token_filename_**.txt | docker login docker.pkg.github.com -u **_GitHub_username_** --password-stdin

### 12. Taggare immagine
#### Comando:
> docker tag **_image_id_** **_image_name_**:**_version_**

### 13. Pushare immagine
#### Comando:
> docker push **_image_name_**:**_version_**

### 14. Vedere tutte le immagini
#### Comando:
> docker images

### 15. Vedere tutti i containers
#### Comando:
> docker ps -a

