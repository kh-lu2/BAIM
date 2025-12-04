# Instalowanie Android Studio i Adb

1. Pobierz odpowiedni installer ze strony: https://developer.android.com/studio?hl=pl
2. Uruchom pobrany plik z domyślnymi ustawieniami
3. Kiedy program się zainstaluje, otwórz go i w pierwszym oknie wybierz “More Actions”, następnie “Virtual Device Manager”. Jeśli nie widzisz "More Actions" poszukaj "Virtual Device Manager" w innym miejscu.
4. Otworzy się kolejne okno, w którym kliknij na ikonę “+” a następnie wybierz emulator z jakiego chcesz korzystać.
5. Wróć do miejsca gdzie znalazłeś "Virtual Device Manager". Teraz wybierz "SDK Manager".
6. Przejdź do sekcji “SDK Tools” i zaznacz:
[ x ] Android SDK Command-Line tools
[ x ] Android SDK Platform-Tools
[ x ] Google USB Driver
I kliknij “OK”.
7. Znajdź i skopiuj ścieżkę do katalogu “platform-tools”, jeżeli używasz ustawień domyślnych powinna być to ścieżka: C:\Users\{Nazwa_użytkownika}\AppData\Local\Android\Sdk\platform-tools
8. Dodaj tą ściężkę do PATH.
9. Uruchom terminal i wpisz w nim “adb version” w celu weryfikacji działania.

# Uruchomienie aplikacji
## Wersja 1
1. W android Studio przejdź do pierwszego otwartego okna, wybierz opcję “clone repository”, w pole URL wklej ten link do repozytorium na githubie: https://github.com/t0thkr1s/allsafe-android i kliknij “Clone”.
2. Aby build się udał potrzebna jest java w wersji 18.
3. Gdy gradle skończy pracę, kliknij ikonę “run” u góry otwartego okna.

## Wersja 2
1. Pobierz plik .apk: https://github.com/t0thkr1s/allsafe/releases/latest/download/allsafe.apk.
2. W Android Studio profile or debug apk.
3. Wybierz allsafe.apk.
4. Po prawej kliknij w Device Manager wybierz emulator i włącz
przeciągnij plik .apk do emulatora (automatycznie się zainstaluje).
