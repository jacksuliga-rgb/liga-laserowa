# Łódzka Liga Strzelectwa Laserowego Szkół

Strona promocyjna projektu Stowarzyszenia 2piny — bezpłatnej międzyszkolnej ligi strzelectwa laserowego dla łódzkich szkół. Projekt finansowany z Miejskiego Programu Mikrograntów 2026.

## Co jest w tej paczce

- `index.html` — cała strona w jednym pliku. Zdjęcia siedzą w środku, więc działa offline i bez logowania.
- `og-image.jpg` — obrazek pokazywany przy udostępnianiu linku na Facebooku, LinkedInie itd.
- `.nojekyll` — pusty plik, który mówi GitHub Pages, żeby serwował pliki tak jak są, bez przetwarzania.

## Jak opublikować na GitHub Pages

1. Wrzuć te trzy pliki do repozytorium (do katalogu głównego albo do folderu `docs/`).
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
