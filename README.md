# PeopleDetection – Asynchroniczna analiza liczby osób na zdjęciach

Projekt realizuje asynchroniczną analizę zdjęć pod kątem wykrywania osób
z wykorzystaniem API REST, RabbitMQ, workerów(consumerów), Dockera oraz
modelu YOLO (Ultralytics).

1. endpoint GET z lokalnym plikiem
2. endpoint URL + async + kolejka + status
3. endpoint POST upload
4. RabbitMQ
5. Skalowanie workerów (domyślnie 8)
6. Asynchroniczne przetwarzanie
7. Detekcja osób (YOLO)
