# Alarm PL

Aplikacja alarmowa dla Polski w stylu ukraińskiego **Air Alert** — jeden samodzielny plik `index.html`, działa na GitHub Pages bez backendu.

**Adres (po wdrożeniu):** `https://ligalaserowa.2piny.pl/alarm/`

## Co robi

- **Żywe ostrzeżenia IMGW** — pobiera ostrzeżenia **meteorologiczne** i **hydrologiczne** z publicznego API IMGW-PIB i pokazuje je per **województwo** (16 regionów), ze stopniami 1–3.
- **Mapa (kartogram)** — schematyczny układ 16 województw kolorowany wg najwyższego stopnia ostrzeżenia; klik wybiera region.
- **Alarm w stylu Air Alert** — po wybraniu regionu aplikacja:
  - odtwarza sygnał dźwiękowy i wibrację, gdy pojawi się **nowe** ostrzeżenie,
  - wysyła powiadomienie systemowe (Web Notifications),
  - pokazuje wielki baner statusu (brak / ostrzeżenie / alarm),
  - odświeża dane co 2 minuty i przy powrocie do karty.
- **Moduł obrony cywilnej (symulacja)** — odtwarza akustyczne sygnały alarmowe:
  - *Ogłoszenie alarmu* — dźwięk modulowany (3 min),
  - *Odwołanie alarmu* — dźwięk ciągły (3 min).
  Generowane przez Web Audio API (bez plików dźwiękowych). To **symulacja/test** — Polska nie ma publicznego API alarmów bojowych; moduł jest gotowy pod przyszły oficjalny feed.
- **Sekcja edukacyjna** — Alert RCB, RSO, ostrzeżenia IMGW, sygnały syren, co robić po alarmie oraz numery alarmowe (112, 997, 998, 999).
- **PWA** — `manifest.webmanifest` + `sw.js`: instalowalna, działa offline (dane na żywo zawsze z sieci, nigdy z cache).

## Dane na żywo vs tryb demo

Aplikacja próbuje pobrać dane bezpośrednio z:

- `https://danepubliczne.imgw.pl/api/data/warningsmeteo`
- `https://danepubliczne.imgw.pl/api/data/warningshydro`

Jeśli pobranie się nie powiedzie (np. **CORS**, brak sieci), aplikacja przechodzi w **tryb demo** z danymi przykładowymi i pokazuje pomarańczowy baner. Cała logika (mapa, alarm, statusy) działa tak samo — zmienia się tylko źródło danych.

> Jeśli w Twojej sieci/przeglądarce API IMGW nie zwraca nagłówków CORS, dane na żywo można podać przez własny prosty proxy (np. funkcja serverless zwracająca ten sam JSON z nagłówkiem `Access-Control-Allow-Origin: *`) i podmienić adresy w `IMGW` w `index.html`.

## Pliki

- `index.html` — cała aplikacja (HTML + CSS + JS).
- `manifest.webmanifest` — manifest PWA.
- `sw.js` — service worker (offline / instalacja).
- `icon.svg` — ikona aplikacji.

## Ważne

To **nieoficjalna** aplikacja informacyjna. Nie zastępuje oficjalnych kanałów: **112**, Alert RCB, komunikatów wojewodów i służb. Źródło danych pogodowych: IMGW-PIB (licencja danych publicznych).
