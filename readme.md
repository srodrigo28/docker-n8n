
* instalar no terminal windows em modo administrador

```
wsl --install
```

* Apos instalar o nodejs com Chocollate
```
choco install make
```

* apos criar o arquivo docker-compose.yml
```
services:
  n8n-youtube:
    image: n8nio/n8n
    ports:
      - "5678:5678"
    volumes:
      - ./:/home/node/.n8n
    environment:
      GENERIC_TIMEZONE: America/Sao_Paulo
    restart: unless-stopped
    networks:
      - n8n-networks-youtube

networks:
  n8n-networks-youtube:  
    driver: bridge
```

* comando para deploy
```
make deploy
```
https://www.youtube.com/watch?v=CAedO3UaiU8&t=208s