# 💧 Woda 7 – Rozliczenie Wspólnoty

Współczesna, lekka aplikacja typu **PWA (Progressive Web App)** stworzona do zarządzania i rozliczania mediów (woda oraz ścieki) w kameralnej wspólnocie mieszkaniowej składającej się z 6 lokali. Projekt powstał z myślą o pełnej transparentności, matematycznej precyzji oraz wygodzie użytkowania na urządzeniach mobilnych i tabletach.

---

## ✨ Najważniejsze Funkcje

* **📄 Inteligentny parser faktur:** Automatyczne odczytywanie danych (numer, okres rozliczeniowy, licznik główny, abonament, woda i ścieki) z plików **PDF** (np. ZUK Kiełczów) oraz elektronicznych faktur ustrukturyzowanych **KSeF XML**.
* **👁️ Podgląd dokumentu:** Wbudowany, czytelny podgląd wgranej faktury PDF z możliwością powiększania palcami (*pinch-to-zoom*) na ekranie telefonu.
* **🧮 Precyzyjny kalkulator uchybów:** Sprawiedliwy podział kosztów zmiennych oraz uchybów (różnicy między licznikiem głównym a sumą podliczników) z uwzględnieniem **metody największych reszt (Hamiltona)**, gwarantującej zgodność co do 1 grosza i 0,01 m³.
* **🔗 Ciągłość rozliczeń i wirtualne liczniki:** Automatyczne przenoszenie przesunięć (kredytów i nadwyżek m³) na kolejne okresy rozliczeniowe przy odczytach off-cycle oraz zachowanie pełnej historii łańcuchowej.
* **📱 Praca Offline (PWA):** Aplikacja działa bezpośrednio w przeglądarce i może zostać zainstalowana jako natywna ikonka na ekranie głównym telefonu – nie wymaga stałego połączenia z internetem po pierwszym załadowaniu.
* **📊 Raporty i Eksport:** Generowanie gotowych raportów rozliczeniowych dla pojedynczych mieszkań (do wysyłki np. przez SMS/WhatsApp), tabelaryczny eksport **TSV** do wklejenia w programie Excel oraz ładne podsumowania w formacie **PDF**.
* **💾 Bezpieczeństwo danych:** Cała historia i stany liczników są bezpiecznie przechowywane lokalnie na urządzeniu (`localStorage`) z opcją pełnego eksportu i importu kopii zapasowej w formacie JSON.

---

## 🚀 Szybki start (GitHub Pages)

Aplikacja jest w pełni gotowa do uruchomienia bezpośrednio z przeglądarki. Jeżeli chcesz hostować ją we własnym repozytorium GitHub:
1. Umieść pliki `index.html`, `sw.js`, `manifest.webmanifest` oraz `README.md` w głównym folderze repozytorium.
2. W zakładce **Settings ➔ Pages** włącz publikację z gałęzi `main` (folder `/root`).
3. Otwórz wygenerowany adres URL w telefonie!

---

## 🛠️ Technologie
* **Frontend:** Czysty, nowoczesny **HTML5**, responsywny **CSS3** (Mobile-First / Soft Light UI) oraz **JavaScript (ES6+)**.
* **Przetwarzanie PDF:** Biblioteka **PDF.js** (Mozilla) do lokalnego parsowania i renderowania dokumentów w przeglądarce.
* **Architektura:** Offline-first PWA wspierana przez Service Workera.
