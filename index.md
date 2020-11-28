# Manuale italiano Docker
Comandi e funzionalità Docker

## Comandi
### Creare un nuovo container
#### Esempio:

_docker run --name chronograf -p 8888:8888 chronograf_

#### Comando:
> docker run --name **container_name** -p **container_port**:**host_port** **image_name**
