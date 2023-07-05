.. Sprawozdanie documentation master file, created by
   sphinx-quickstart on Wed Apr 19 09:42:01 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Aplikacji do kontroli bazy danych
=========================================

Napisane funkcje umożliwiają nam wykonanie różnych operacji na bazie danych SQLite oraz interakcję z danymi pomiarów. Oto opis tych możliwości:

Funkcja create_table_adresy(conn) tworzy tabelę "adresy" w bazie danych.

Funkcja create_table_pomiary(conn) tworzy tabelę "pomiary" w bazie danych.

Funkcja delete_table_adresy(conn) usuwa tabelę "adresy" z bazy danych.

Funkcja delete_table_pomiary(conn) usuwa tabelę "pomiary" z bazy danych.

Funkcja insert_to_adresy(conn): Wprowadza dane z pliku CSV do tabeli "adresy" w bazie danych.

Funkcja insert_to_pomiary(conn) wprowadza dane z pliku CSV do tabeli "pomiary" w bazie danych.

Funkcja clear_table_adresy(conn) usuwa wszystkie dane z tabeli "adresy", zachowując strukturę tabeli.

Funkcja clear_table_pomiary(conn) usuwa wszystkie dane z tabeli "pomiary", zachowując strukturę tabeli.

Funkcja insert_data_from_sqlite(conn) wprowadza dane z pliku CSV do tabeli "pomiary" w bazie danych PostgreSQL.

Funkcja insert_from_sqlite(conn) wywołuje funkcję insert_data_from_sqlite(conn) w celu wprowadzenia danych z pliku CSV do tabeli "pomiary" w bazie danych PostgreSQL.

Funkcja clear_tables(conn) czyści zawartość tabel "adresy" i "pomiary" w bazie danych PostgreSQL.

Funkcja insert_temp_data(conn) wprowadza przykładowe dane do tabel "adresy" i "pomiary" w bazie danych.

Funkcja create_tables(conn) tworzy tabele "adresy" i "pomiary" w bazie danych PostgreSQL.

Funkcja delete_tables(conn) usuwa tabele "pomiary" i "adresy" z bazy danych PostgreSQL.

Funkcja program(conn, wybor) jest główną funkcją programu, która na podstawie wyboru użytkownika wykonuje odpowiednie działania, takie jak tworzenie/usuwanie tabel oraz wprowadzanie/usuwanie danych.

Funkcja main() jest główną funkcją programu, która nawiązuje połączenie z bazą danych na podstawie danych z pliku JSON, wyświetla menu i obsługuje wybory użytkownika.

Ta aplikacja umożliwia tworzenie, usuwanie i zarządzanie danymi w tabelach "adresy" i "pomiary" w bazie danych PostgreSQL. Użytkownik może korzystać z różnych funkcji do manipulacji danymi w bazie.





.. toctree::
   :maxdepth: 5
   :caption: Contents:
   

