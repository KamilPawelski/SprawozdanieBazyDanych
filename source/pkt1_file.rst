.. Sprawozdanie documentation master file, created by
   sphinx-quickstart on Wed Apr 19 09:42:01 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Pliki
========================================

.. toctree::
   :maxdepth: 5
   :caption: Contents:
      
      
- **PG_VERSION** - Plik zawierający główny numer wersji PostgreSQL
- **current_logfiles** - Plik rejestrujący pliki dziennika aktualnie zapisywane przez moduł zbierający dzienniki
- **postgresql.auto.conf** - Plik służący do przechowywania parametrów konfiguracyjnych ustawianych przez ALTER SYSTEM
- **postmaster.opts** - Plik rejestrujący opcje wiersza poleceń, z którymi serwer był ostatnio uruchomiony
- **postmaster.pid** - Plik blokady rejestrujący 
   * Bieżący identyfikator procesu postmastera (PID)
   * Ścieżkę katalogu danych klastra
   * Znacznik czasu uruchomienia postmastera
   * Numer portu
   * Ścieżkę katalogu gniazda domeny Unix
   * Pierwszy prawidłowy listen_address
   * Identyfikator segmentu pamięci współdzielonej
   