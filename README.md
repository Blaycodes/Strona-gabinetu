# Gabinet Kosmetologiczny

Nowoczesna, responsywna strona typu one-page dla gabinetu kosmetologicznego. Projekt został wykonany w czystym HTML, CSS i JavaScript, dzięki czemu nie wymaga instalowania zależności i może być publikowany bezpośrednio przez GitHub Pages.

## Podgląd

Po włączeniu GitHub Pages strona będzie dostępna pod adresem:

[https://przegniazdowani.github.io/Strona-gabinetu-kosmetologicznego/](https://przegniazdowani.github.io/Strona-gabinetu-kosmetologicznego/)

## Najważniejsze funkcje

- przyklejone menu z płynnym przewijaniem do sekcji,
- mobilne menu typu hamburger,
- responsywny baner powitalny,
- sekcje: O nas, Usługi, Galeria, Opinie, Cennik i Kontakt,
- formularz kontaktowy z walidacją pól,
- animacje elementów podczas przewijania,
- automatyczne wyróżnianie aktywnej sekcji w menu,
- responsywny chatbot w formie pływającego widgetu,
- lokalne odpowiedzi chatbota dotyczące oferty, cen, godzin, adresu i rezerwacji,
- podstawowe udogodnienia dostępności, w tym obsługa klawiatury i `prefers-reduced-motion`.

## Technologie

- HTML,
- CSS,
- JavaScript ,
- Google Fonts,
- zewnętrzne zdjęcia z Unsplash,
- osadzona mapa Google.

## Struktura projektu

```text
.
├── index.html   # Struktura i treść strony
├── styles.css   # Wygląd, animacje i responsywność
├── script.js    # Nawigacja, formularz, animacje i chatbot
└── README.md    # Dokumentacja projektu
```

## Uruchomienie lokalne

Projekt nie wymaga procesu budowania. Można otworzyć `index.html` bezpośrednio w przeglądarce lub uruchomić prosty serwer lokalny:

```bash
python3 -m http.server 8000
```

Następnie otwórz:

```text
http://localhost:8000
```

## Chatbot

Publiczna wersja projektu działa domyślnie jako lokalny chatbot FAQ. Odpowiedzi dotyczące zabiegów, cen, czasu trwania, konsultacji, godzin otwarcia, adresu, kontaktu i rezerwacji są zapisane w `script.js`.


### Bezpieczne podłączenie Gemini

Klucza API nie należy umieszczać w kodzie publikowanym na GitHub Pages. Każdy plik JavaScript wysyłany do przeglądarki może zostać odczytany przez odwiedzających.

W wersji produkcyjnej należy:

1. utworzyć backend lub funkcję serverless, np. Cloudflare Worker, Vercel Function albo Netlify Function,
2. zapisać klucz Gemini jako sekret lub zmienną środowiskową backendu,
3. wysyłać z frontendu wyłącznie wiadomość użytkownika do własnego endpointu,
4. dodać walidację, ograniczenie liczby żądań i dozwolone źródła CORS.

Nie należy wstrzykiwać sekretu do statycznego JavaScriptu przez `.env` ani GitHub Actions — po zbudowaniu strony klucz nadal byłby widoczny w przeglądarce.

## Formularz kontaktowy

Formularz wykonuje walidację po stronie przeglądarki i pokazuje demonstracyjne potwierdzenie. GitHub Pages nie obsługuje kodu serwerowego, dlatego rzeczywista wysyłka wiadomości wymaga podłączenia zewnętrznej usługi lub własnego backendu.


## Personalizacja

Przed użyciem strony jako witryny produkcyjnej należy zastąpić przykładowe dane:

- nazwę i opis gabinetu,
- dane kosmetolożki,
- numer telefonu i adres e-mail,
- fikcyjny adres gabinetu,
- ceny i opisy zabiegów,
- odnośniki do Instagrama i Facebooka,
- zdjęcia oraz lokalizację mapy.

Dane kontaktowe i adres użyte w projekcie mają charakter demonstracyjny.

## Ważne informacje

- Obrazy, Google Fonts i mapa są pobierane z usług zewnętrznych, dlatego wymagają połączenia z internetem.
- Ceny i opisy zabiegów są przykładowe.
- Chatbot nie udziela porad medycznych ani nie stawia diagnoz.
- Przed publikacją zawsze warto przeskanować repozytorium pod kątem sekretów i danych prywatnych.
