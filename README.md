# Zadania
Zadania 1 i 2 zakładają możliwość oglądania [kodu źródłowego aplikacji](https://github.com/t0thkr1s/allsafe-android). \
Podczas interakcji z aplikacji, zwracaj uwagę na alerty/informacje zwrotne.

## Komendy Adb
```
adb version
adb devices
adb -s <nr_seryjny> <polecenie>
adb shell
adb push <PC-path> <android-path>
adb pull <android-path> <PC-path>
am (adb shell am start …)
… am start -a
… am start -d
Intent Extras
--ez
--es
```

## Zadanie 1: Object Serialization
Przeanalizuj jak zapisywane są dane użytkownika i obejdź zabezpieczenia do kliknięcia przycisku "Load".

<details>
  <summary><h3>Podpowiedź 1</h3></summary>
    Zobacz do kodu źródłowego danego fragmentu aplikacji i dowiedz się jak zabezpieczony jest przycisk "Load".
</details>

<details>
  <summary><h3>Podpowiedź 2</h3></summary>
    Gdzie zapisywane są dane użytkownika? Jaką nazwę ma ten plik? Gdzie się znajduje? Co zwraca getExternalFilesDir? 
</details>

<details>
  <summary><h3>Podpowiedź 3</h3></summary>
    Spróbuj otworzyć i zmodyfikować ten plik używając jakiegokolwiek edytora. Pamiętaj, że adb pozwala kopiować pliki na komputer i “podmienie” ich!
</details>

## Zadanie 2: Deep Link Exploitation
Znajdź niezabezpieczony deep link w aplikacji allsafe oraz odpowiednio go użyj w celu zdobycia flagi (wyświetlenia ekranu z napisem ‘Congratulations!’).

<details>
  <summary><h3>Podpowiedź 1</h3></summary>
    Gdzie deklarowane są deep linki? Znajdź ten plik w kodzie źródłowym i znajdź deep link używany w tym zadaniu
</details>

<details>
  <summary><h3>Podpowiedź 2</h3></summary>
    Spróbuj przetestować ten deep link z użyciem adb. Jaka wiadomość otrzymujesz?
</details>

<details>
  <summary><h3>Podpowiedź 3</h3></summary>
    Przeanalizuj fragment kodu odpowiadający temu zadaniu. Jaki jest warunek rozwiązania zadania? Co i w jaki sposób zwraca funkcja getString()?
</details>

## Zadanie 3: Smali Patch
Włącz firewall :)

Do rozwiązania tego zadania potrzebne będzie rozszerzenie do VSCode - ApkLab.
- [Link do VSCode]( https://code.visualstudio.com/)
- [Link do ApkLab (tu znajdziecie też instrukcje jak z niego korzystać)](https://github.com/APKLab/APKLab 
)

<details>
  <summary><h3>Podpowiedź 1</h3></summary>
    Zdekompiluj aplikację za pomocą ApkLab i przeanalizuj kod smali odpowiadający temu zadaniu. Co odpowiada za stan firewalla?
</details>

<details>
  <summary><h3>Podpowiedź 2</h3></summary>
    Jak wyglądają wyrażenia warunkowe w smali?
</details>

<details>
  <summary><h3>Podpowiedź 3</h3></summary>
    Aby zobaczyć swoje zmiany "w akcji", użyj ApkLab aby zbudować jeszcze raz i zainstalować zmienioną aplikację na urządzeniu (pamiętaj aby wcześniej odinstalować starą - może pojawić się problem z podpisem pliku .apk)
</details>
