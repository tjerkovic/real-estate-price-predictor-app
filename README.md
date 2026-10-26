# Real Estate Price Predictor

Fakultetski projekt web-aplikacije za pregled nekretnina, prikaz podataka o najmu i procjenu mjesečne cijene najma pomoću modela strojnog učenja. Aplikacija je razvijena u Pythonu korištenjem okvira Django.

## Funkcionalnosti

- Pregled nekretnina i detalja pojedine nekretnine.
- Dodavanje oglasa za najam putem web-obrasca.
- Registracija i prijava korisnika.
- Interaktivne vizualizacije podataka o nekretninama pomoću biblioteka Pandas i Plotly.
- Obrazac za predviđanje cijene najma povezan s vanjskim Azure Machine Learning servisom.

## Tehnologije

Python, Django, SQLite, Pandas, Plotly, NumPy, Pillow, HTML i CSS. Za predviđanje cijene najma korišten je Microsoft Azure Machine Learning.

## Lokalno pokretanje (Windows / PowerShell)

**Preduvjeti:** instalirani Python 3.11 i Git.

1. Klonirajte repozitorij i otvorite njegovu mapu:

   ```powershell
   git clone <URL-VASEG-REPOZITORIJA>
   cd real-estate-price-predictor
   ```

2. Izradite virtualno okruženje i aktivirajte ga:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

3. Instalirajte potrebne biblioteke:

   ```powershell
   python -m pip install -r requirements.txt
   ```

4. Provjerite konfiguraciju aplikacije:

   ```powershell
   python manage.py check
   ```

5. Pripremite bazu podataka **ako je pokrećete bez postojeće baze `db.sqlite3`**:

   ```powershell
   python manage.py migrate
   ```

6. Pokrenite razvojni poslužitelj:

   ```powershell
   python manage.py runserver
   ```

7. Otvorite **http://127.0.0.1:8000/** u pregledniku. Za zaustavljanje poslužitelja pritisnite `Ctrl + C` u terminalu.

Ako PowerShell blokira aktivaciju virtualnog okruženja, biblioteke možete instalirati i aplikaciju pokrenuti izravno pomoću `.\.venv\Scripts\python.exe` umjesto `python`.

## Napomena o predviđanju cijene najma

Predviđanje se oslanja na vanjski Azure Machine Learning endpoint iz izvornog projekta. Tijekom lokalne provjere u listopadu 2026. naziv poslužitelja nije se mogao razriješiti putem DNS-a pa **funkcionalnost predviđanja trenutačno nije dostupna**. Ostale funkcionalnosti aplikacije mogu se koristiti lokalno, ovisno o sadržaju i stanju baze podataka.

## Napomene o podacima i sigurnosti

- Lokalna baza `db.sqlite3` može sadržavati korisničke podatke; prije javne objave provjerite njezin sadržaj i po potrebi je izostavite.
- API ključeve i druge vjerodajnice nije sigurno objavljivati u izvornom kodu ili Git povijesti.
- Django razvojni poslužitelj i razvojne postavke nisu namijenjeni produkcijskoj upotrebi.

## Izvor projekta

Projekt je nastao kao zajednički fakultetski rad. Izvorni repozitorij: https://github.com/kikigudelj/real-estate-price-predictor
