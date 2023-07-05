.. Sprawozdanie documentation master file, created by
   sphinx-quickstart on Wed Apr 19 09:42:01 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Aplikacji do pomiarów
=========================================
Napisane funkcje umożliwiają nam wykonanie różnych operacji na bazie danych SQLite oraz interakcję z danymi pomiarów. Oto opis tych możliwości:

Funkcja create_connection(db_file) umożliwia nawiązanie połączenia z bazą danych SQLite. Jeśli połączenie jest udane, funkcja drukuje wersję SQLite. W przypadku wystąpienia błędu podczas nawiązywania połączenia, funkcja wyświetla ten błąd. Funkcja zwraca obiekt połączenia lub wartość None, jeśli połączenie nie zostało ustanowione.

Funkcja create_table(conn, create_table_sql) możemy utworzyć tabelę w bazie danych na podstawie podanego polecenia SQL. Funkcja próbuje utworzyć kursor na podstawie połączenia i wykonuje polecenie SQL na tym kursorze. Jeśli wystąpi błąd podczas wykonywania polecenia, funkcja wyświetla ten błąd.

Funkcja select_all_data(conn) umożliwia wykonanie zapytania SQL "SELECT * FROM pomiary". Tworzy kursor na podstawie tego połączenia i wykonuje zapytanie na tym kursorze. Wyniki zapytania są pobierane przy użyciu metody fetchall() i iterowane są przez każdy wiersz wynikowy. Każdy wiersz jest wyświetlany na ekranie, a użytkownik musi nacisnąć klawisz Enter, aby kontynuować wyświetlanie kolejnych wierszy.

Funkcja insert_data_db(conn, pomiar) służy do wstawiania danych do bazy danych SQLite. Funkcja tworzy polecenie SQL za pomocą parametryzowanego zapytania wstawiania danych. Następnie tworzy kursor na podstawie połączenia i wykonuje zapytanie SQL, przekazując dane pomiaru. Po wykonaniu zapytania, zmiany są zatwierdzane w bazie danych przy użyciu metody commit(). Funkcja zwraca identyfikator ostatnio wstawionego wiersza w bazie danych.

Funkcja insert_data_user(conn) umożliwia pobranie danych od użytkownika i wstawienie ich do bazy danych. Użytkownik jest proszony o wprowadzenie wartości dla kolejnych pól: ulicy, numeru budynku, numeru mieszkania, pomiaru licznika i daty pomiaru. Podane wartości są tworzone jako krotka i przekazywane do funkcji insert_data_db() w celu wstawienia ich do bazy danych.

Funkcja delete_data(conn, id) pozwala na usunięcie danych z bazy danych na podstawie podanego identyfikatora (id). Tworzy polecenie SQL usuwające wiersz o podanym identyfikatorze i wykonuje je przy użyciu kursora. Zmiany są zatwierdzane w bazie danych po wykonaniu zapytania.

Funkcja export_to_csv(conn, csv_file) służy do zapisywania danych z bazy danych do pliku CSV. Funkcja tworzy kursor na podstawie połączenia i wykonuje zapytanie "SELECT * FROM pomiary". Wyniki zapytania są pobierane przy użyciu metody fetchall() i zapisywane do pliku CSV przy użyciu modułu csv. Każdy wiersz danych jest zapisywany jako pojedynczy wiersz w pliku CSV.

Funkcja manage_program() umożliwia sterowanie programem na podstawie wybranych opcji. Wyświetla menu z dostępnymi opcjami, które użytkownik może wybrać. W zależności od wybranej opcji, program wykonuje odpowiednie akcje, takie jak wyświetlanie danych, dodawanie nowego pomiaru, usuwanie danych lub eksportowanie ich do pliku CSV. Program działa w pętli, dopóki użytkownik nie wybierze opcji wyjścia.

Dzięki tym funkcjom możemy tworzyć, zarządzać i przetwarzać dane pomiarów w bazie danych SQLite. Możemy wykonywać zapytania, wstawiać, usuwać i wyświetlać dane, a także eksportować je do pliku CSV w celu dalszej analizy lub przechowywania. 



.. toctree::
   :maxdepth: 5
   :caption: Contents:
   

