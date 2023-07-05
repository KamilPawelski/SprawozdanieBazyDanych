.. Sprawozdanie documentation master file, created by
   sphinx-quickstart on Wed Apr 19 09:42:01 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Aplikacja do kontroli bazy danych
========================================

W funkcji main zostały dodane instrukcje umożliwiające obsługę baz danych PostgreSQL. W tym typadku również mamy kilak opcji do wyboru, każda będzie odpowiadać za coś innego.
Pierwsza opcja pozwala na utworzenie tabel w bazie danych, gdzie użytkownik zostaje zapytany, czy chce utworzyć tabelę "pomiary", "adresy" lub obie. 
Druga opcja umożliwia usunięcie tabel z bazy danych, gdzie użytkownik jest pytany, czy chce usunąć tabelę "pomiary", "adresy" lub obie. 
Trzecia opcja służy do wgrywania przykładowych danych do bazy danych, gdzie użytkownik jest zapytany, czy chce dodać dane do tabeli "pomiary", "adresy" lub obu. 
Czwarta opcja pozwala na usunięcie danych z tabeli w bazie danych, gdzie użytkownik jest pytany, czy chce usunąć dane z tabeli "pomiary", "adresy" lub obu. 
Piąta opcja umożliwia wgrywanie danych z pliku CSV do bazy danych PostgreSQL. 
Zerowa opcja odpowiada za wyjście z programu.

.. toctree::
   :maxdepth: 5
   :caption: Contents:
   

