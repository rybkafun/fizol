# Park Drgań

Gra edukacyjna z fizyki dla klasy 8. Moduł 1: ruch drgający (okres, częstotliwość, wahadło, sprężyna, energia, tłumienie, rezonans).
Cała gra to jeden plik: `public/index.html` (HTML + CSS + JavaScript, bez zewnętrznych bibliotek, działa offline).

## Uruchomienie lokalne

Otwórz `public/index.html` w przeglądarce.

## Publikacja w Netlify

Konfiguracja jest w `netlify.toml` (katalog publikacji: `public`, bez kroku budowania).

- **Z GitHuba:** Netlify → *Add new site* → *Import an existing project* → wybierz repozytorium `rybkafun/fizol`.
  Pola *Build command* zostaw puste, *Publish directory* uzupełni się z `netlify.toml`. Każdy push na `main` wdraża nową wersję.
- **Bez Gita:** przeciągnij folder `public` na stronę https://app.netlify.com/drop.
- **Z terminala:** `npx netlify-cli deploy --prod` (w katalogu projektu).

Postęp gracza zapisuje się w `localStorage` przeglądarki, więc nowe wdrożenie go nie usuwa.

## Dodawanie modułu

Na końcu skryptu w `public/index.html` wywołaj `registerModule({...})`. Wzorzec jest opisany w komentarzu „JAK DODAĆ KOLEJNY MODUŁ”.
