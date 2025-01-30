# Auction

---

Auction to strona aukcyjna, na której użytkownicy mogą wystawiać przedmioty na sprzedaż i brać udział w aukcjach. Strona jest napisana w Node.js i korzysta z MongoDB do przechowywania danych. Aplikacja umożliwia użytkownikom rejestrację i logowanie, dodawanie, edytowanie oraz usuwanie swoich aukcji, a także przebijanie ofert i zakup przedmiotów. Administratorzy mają dodatkowe uprawnienia do zarządzania użytkownikami i aukcjami.

---

## Wymagania

Aby uruchomić projekt, potrzebujesz:

- **Docker** – obsługa kontenerów
- **Docker Compose** – zarządzanie wieloma kontenerami
- **Git** – pobranie repozytorium

---

## Instalacja i uruchomienie

### Klonowanie repozytorium

Najpierw sklonuj repozytorium na swoje urządzenie:

```sh
git clone https://github.com/milmanart/auction.git
cd auction
```

---

### Uruchomienie aplikacji

Projekt jest w pełni konteneryzowany i można go uruchomić jedną komendą:

```sh
docker-compose up -d --build
```

Po uruchomieniu aplikacja będzie dostępna pod adresem:

- **[http://localhost](http://localhost)** – przez Nginx
- **[http://localhost:3000](http://localhost:3000)** – bezpośrednio na serwerze aplikacji

---

### Zatrzymanie i usunięcie kontenerów

Jeśli chcesz zatrzymać kontenery, użyj:

```sh
docker-compose down
```

Aby usunąć także przechowywane dane (**uwaga – usunie to całą bazę danych**):

```sh
docker-compose down -v
```

---

## Funkcjonalności

Aplikacja oferuje następujące funkcjonalności:

- Rejestracja i logowanie użytkowników
- Role użytkowników (zwykły użytkownik i administrator)
- Użytkownicy mogą dodawać, edytować i usuwać swoje aukcje
- Kupowanie przedmiotów na aukcji
- Możliwość przebijania ceny w aukcji
- Administrator może usuwać użytkowników
- Administrator może usuwać aukcje
- Administrator posiada wszystkie uprawnienia zwykłego użytkownika

---

## Kontenery Docker

Projekt składa się z trzech kontenerów:

- **MongoDB** – baza danych do przechowywania użytkowników, aukcji i sesji
- **Auction-App** – aplikacja Node.js obsługująca aukcje
- **Nginx** – serwer proxy kierujący ruch do aplikacji

---

## Autorzy

- **Artem Milman** – 44050
- **Darya Sviryd** – 45448
- **Doni Oleksandra** – 46456

---

