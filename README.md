# lab12
Projekt LEMP z phpMyAdmin to kompletny stack środowiska webowego, który składa się z serwera Linux (L), serwera Nginx (E), serwera MySQL (M), serwera PHP (P) oraz narzędzia phpMyAdmin.

Opis poszczególnych komponentów projektu:

1. Linux (L):
   - Projekt zakłada wykorzystanie kontenera Docker, który jest uruchomiony na systemie Linux.
   - Kontener Docker zapewnia izolację i niezależne środowisko dla reszty usług w projekcie.
<img width="836" alt="Zrzut ekranu 2023-06-4 o 15 29 19" src="https://github.com/Walicce/lab12/assets/60614660/4b0525d9-294b-45d2-b616-d3ac474602ab">

2. Nginx (E):
   - Serwer Nginx jest używany jako warstwa front-end do obsługi żądań HTTP.
   - Kontener Docker został skonfigurowany z obrazem Nginx.
   - Nginx nasłuchuje na porcie 6666 i obsługuje żądania przychodzące na ten port.

3. MySQL (M):
   - Serwer MySQL jest używany jako baza danych w projekcie.
   - Kontener Docker został skonfigurowany z obrazem MySQL.
   - Skonfigurowano zmienną środowiskową `MYSQL_ROOT_PASSWORD`, która określa hasło administratora dla bazy danych.
<img width="1440" alt="Zrzut ekranu 2023-06-4 o 15 27 46" src="https://github.com/Walicce/lab12/assets/60614660/e79b21e5-e50f-4c50-b763-eaa91d5a2ae6">

4. PHP (P):
   - Serwer PHP jest używany do przetwarzania skryptów PHP.
   - Kontener Docker został skonfigurowany z obrazem PHP-FPM.
   - Serwer PHP jest skonfigurowany do nasłuchiwania na porcie 9000.

5. phpMyAdmin:
   - Narzędzie phpMyAdmin jest używane do zarządzania bazą danych MySQL.
   - Kontener Docker został skonfigurowany z obrazem phpMyAdmin.
   - Skonfigurowano zmienne środowiskowe `PMA_HOST` i `PMA_PORT`, które określają adres hosta i port serwera MySQL.

Cały projekt jest zdefiniowany w pliku `docker-compose.yml`, który opisuje wszystkie kontenery, ich konfiguracje, połączenia sieciowe oraz porty przekierowań. 
Plik Dockerfile jest używany w każdym kontenerze do zbudowania obrazów z odpowiednimi konfiguracjami.

W rezultacie projekt umożliwia uruchomienie pełnego środowiska LEMP (Linux, Nginx, MySQL, PHP) 
wraz z narzędziem phpMyAdmin. Daje to możliwość tworzenia i zarządzania bazami danych MySQL oraz 
wyświetlania stron internetowych opartych na PHP.



Uruchomienie:  docker-compose up -d
<img width="569" alt="Zrzut ekranu 2023-06-4 o 14 53 21" src="https://github.com/Walicce/lab12/assets/60614660/bc079a37-2624-4dbe-9890-2798f7dcd5c4">

