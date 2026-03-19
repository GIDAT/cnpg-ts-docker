# cnpg-ts-docker

Construye imagen docker con CloudnativePG (Postgres DB) con el plugin timescale instalado 

## Generar nueva imagen

1. Cambiar variables en archivo `.env`. La imagen actual usa:
    ```
    CLOUDNATIVEPG_VERSION=18-system-trixie
    POSTGRES_VERSION=18
    TIMESCALE_VERSION=2.25.2
    ```
2. Generar imagen: `docker compose build`

3. Loguear usuario (**previo generar TOKEN**). Ej.:
    ```
    docker login -u USUARIO ghcr.io
    ```
4. Subir al repositorio de contenedores. Ej.:
    ```
    docker push ghcr.io/gidat/cnpg-ts:18_2.25.2
    ```
