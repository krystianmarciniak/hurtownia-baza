# Hurtownia – baza danych (PostgreSQL)

Repozytorium zawiera wersjonowany zrzut bazy **hurtownia** dla PostgreSQL.  
Główny plik: `hurtownia.sql` (pełny skrypt tworzący strukturę i ładujący dane).

## Wymagania
- PostgreSQL 14–17 (sprawdzone na 17)
- `psql` i `pg_restore` w PATH (instalowane z PostgreSQL)
- Uprawnienia do tworzenia bazy i schematów

---

## Jak przywrócić bazę

### Opcja A — z pliku `hurtownia.sql` (Plain SQL, zalecane)
```bash
# 1) utwórz pustą bazę (nazwa może być inna)
createdb -U postgres hurtownia

# 2) wgraj skrypt SQL
psql -U postgres -d hurtownia -f hurtownia.sql
