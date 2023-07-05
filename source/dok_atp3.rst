.. Sprawozdanie documentation master file, created by
   sphinx-quickstart on Wed Apr 19 09:42:01 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Aplikacji do analizy danych
=========================================

Napisane funkcje umożliwiają nam do analizy danych oraz prostą obsługe dla użytkownika.

Funkcja gen_raport(conn) generuje raport na podstawie danych z bazy danych. Wykonuje zapytanie SQL, pobiera dane dotyczące pomiarów wraz z informacjami o adresach, przetwarza otrzymane dane i generuje wykresy. Wykresy to histogram pomiarów dla wszystkich adresów oraz wykres słupkowy ilości pomiarów dla poszczególnych ulic.

Funkcja gen_dataframe(data, sql_columns) generuje ramkę danych (DataFrame) na podstawie otrzymanych danych i nazw kolumn. Tworzy nową ramkę danych przy użyciu biblioteki pandas, przekształca dane na odpowiednie kolumny zgodnie z otrzymanymi nazwami kolumn, a następnie wyświetla ramkę danych na ekranie. Użytkownik ma opcję zapisu danych do pliku CSV.

Funkcja prepare_conditions(conn, kolumny, warunki) przygotowuje warunki zapytania SQL na podstawie otrzymanych argumentów. Buduje listy sql_columns (nazwy kolumn) i sql_condition (warunek zapytania SQL) na podstawie wybranych kolumn i warunków. Następnie, na podstawie wybranych opcji, proszony jest użytkownik o podanie wartości dla warunku. Odpowiednie fragmenty warunku zapytania SQL są tworzone i dodawane do sql_condition. Na koniec, funkcja wywołuje funkcję select_data(conn, sql_columns, sql_condition).

Funkcja program(conn, wybor) zawiera instrukcje dla wyboru opcji "1" (generowanie raportu) oraz "2" (wyświetlanie danych). Dla opcji "1" wywoływana jest funkcja gen_raport(conn). Dla opcji "2" użytkownik wybiera kolumny do wyświetlenia i kolumny do filtrowania danych. Następnie pętle while pozwalają na wybór jednej lub więcej opcji dla obu list: kolumny i warunki. Wybór "0" kończy pętlę i przechodzi do funkcji prepare_conditions(conn, kolumny, warunki).

Funkcja main() zawiera instrukcje dla opcji "1" (generowanie raportu) i "2" (wyświetlanie danych). Po nawiązaniu połączenia z bazą danych, w pętli while użytkownik ma możliwość wyboru opcji. Opcja "1" wywołuje funkcję program(conn, wybor) dla generowania raportu, a opcja "2" również wywołuje program(conn, wybor) dla wyświetlenia danych. Po zakończeniu działania programu, zamykane jest połączeni

.. toctree::
   :maxdepth: 5
   :caption: Contents:
   

