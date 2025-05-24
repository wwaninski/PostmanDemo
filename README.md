Wczytanie kolekcji do Postman
- W Postman kliknij Menu->File->Import.
- Wybierz BasicTests.json, RegressionTests.json z repozytorium GitHub.
- Kolekcja zostanie zaimportowana do Postman.

📂 Struktura kolekcji
Projekt składa się z następujących kolekcji i folderów:
1. Kolekcja główna – BasicTests
Zawiera zapytania API podzielone na foldery:
- Users → operacje na użytkownikach (GET, POST, PUT, DELETE)

2. Kolekcja testów regresji – RegressionTests
Zawiera testy automatyczne sprawdzające działanie API:
- Users Tests → weryfikacja operacji CRUD na użytkownikach


📜 Przykładowe zapytania
1. Pobranie listy użytkowników
GET {{base_url}}/users?page=2


2. Pobranie pojedynczego użytkownika
GET {{base_url}}/users/{{user_id}}


3. Utworzenie nowego użytkownika
POST {{base_url}}/users
Content-Type: application/json
Body:
{
    "name": "Jan Kowalski",
    "job": "Developer"
}

✅ Testy regresji
Każde zapytanie zawiera testy automatyczne, sprawdzające odpowiedzi API. Przykłady:
- Kod odpowiedzi 200 dla GET /users
- Struktura odpowiedzi JSON dla GET /users/{{user_id}}
- Prawidłowe utworzenie użytkownika dla POST /users

