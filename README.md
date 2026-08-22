# Łódzka Liga Strzelectwa Laserowego Szkół

Strona promocyjna projektu Stowarzyszenia 2piny — bezpłatnej międzyszkolnej ligi strzelectwa laserowego dla łódzkich szkół. Projekt finansowany z Miejskiego Programu Mikrograntów 2026.

## Co jest w tej paczce

- `index.html` — cała strona promocyjna w jednym pliku. Zdjęcia siedzą w środku, więc działa offline i bez logowania.
- `liga.html` — aplikacja ligi: ranking, awans do finału i finał. Linki do niej są w `index.html` (hero i stopka).
- `dane.json` — wyniki ligi (szkoły, zawodnicy, finał). To ten plik podmieniasz, żeby zmienić wyniki na stronie.
- `og-image.jpg` — obrazek pokazywany przy udostępnianiu linku na Facebooku, LinkedInie itd.
- `.nojekyll` — pusty plik, który mówi GitHub Pages, żeby serwował pliki tak jak są, bez przetwarzania.

## Wyniki: jak wpisywać i publikować

Wyniki wpisuje się w przeglądarce — bez ruszania kodu.

1. Wejdź na `liga.html` i kliknij **✎ Tryb edycji** (prawy górny róg). Pojawi się zakładka **✎ Edycja**.
2. Wpisz szkoły i zawodników. Zasada jest ta sama w eliminacjach i finale — **liczą się punkty**: pistolet (suma 10 strzałów) + karabinek (suma 5 strzałów). Suma i ranking liczą się automatycznie.
3. Finał: przycisk **„Wczytaj ósemkę z kwalifikacji"** wstawia 8 najlepszych, potem wpisujesz im wyniki finału.
4. Zmiany zapisują się w Twojej przeglądarce na bieżąco. Żeby **opublikować** je dla wszystkich:
   - kliknij **⬇ Pobierz dane.json**,
   - wgraj plik `dane.json` do repozytorium (ten sam folder co `liga.html`),
   - zrób commit. Po chwili strona pokaże nowe wyniki.

Strona wczytuje dane w kolejności: **Twoje lokalne edycje → opublikowany `dane.json` → wbudowane dane przykładowe**. Dzięki temu robocze wpisy nie znikają, a strona działa nawet bez `dane.json`.

Dopóki w danych jest `daneTestowe: true`, na górze widać pomarańczowy baner „Dane przykładowe". Odznacz tę opcję w edytorze (albo ustaw `false` w `dane.json`), gdy wpiszesz prawdziwe wyniki.

## Jak opublikować na GitHub Pages

1. Wrzuć wszystkie pliki do repozytorium (do katalogu głównego albo do folderu `docs/` — ale trzymaj `liga.html` i `dane.json` w tym samym folderze).
2. W repo wejdź w **Settings → Pages**.
3. W **Source** wybierz **Deploy from a branch**, gałąź `main`, folder `/ (root)` (albo `/docs`, jeśli tam wrzuciłeś pliki).
4. Zapisz. Po chwili strona pojawi się pod adresem `https://TWOJANAZWA.github.io/NAZWA-REPO/`.

## WAŻNE — popraw adres przed publikacją

W pliku `index.html`, w sekcji `<head>`, jest wpisany przykładowy adres:

```
https://jacksuliga-rgb.github.io/liga-laserowa/
```

Występuje w kilku miejscach (canonical, og:url, og:image, twitter:image). Podmień go na swój prawdziwy adres repo. Jeśli tego nie zrobisz, miniatura przy udostępnianiu linku może się nie pokazać — reszta strony zadziała normalnie.

Najszybciej przez wyszukaj-i-zamień: znajdź `jacksuliga-rgb.github.io/liga-laserowa` i wpisz właściwą ścieżkę.

## Zgłoszenia szkół

Przycisk „Zgłoś szkołę" prowadzi do formularza Google:
`https://forms.gle/uBUUjGSLQpAWKVxA6`

## Kontakt

Stowarzyszenie 2piny · Łódź
kontakt@2piny.pl · 663 882 124
