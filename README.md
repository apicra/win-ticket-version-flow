# apicra/win-ticket-version-flow
Project created by Apicra, https://github.com/apicra/npm-github-win.git


## Cel projektu

Wykorzystując skrypty .apicra można utworzyć dowolny workflow w pracy przy tworzeniu i utrzymaniu projektów

Ten workflow uwzględnia:
+ lokalny system plików
+ repozytorium Github
+ npmjs

| command | local files | remote github | remote NPMJS |
| --- | --- | --- | --- |
| -create.bat | create | create | --- |
| -publish.bat | --- | push, tag | create |
| **-ticket.bat** | --- | **push** | --- |
| **-version.bat** | --- | **tag** | **update** |
| -delete.bat | delete | delete | delete |


## Instalacja

#### .apicra

    git clone https://github.com/apicra/npm-github-win.git .apicra

#### ticket version flow
+ for empty folder

    git clone https://github.com/apicra/win-ticket-version-flow.git .


+ for not empty folder

    git init
    git remote add origin https://github.com/apicra/win-ticket-version-flow.git
    git pull origin master


## Usunięcie

.apicra

    RMDIR /Q /S .apicra

ticket version flow

    del /f -create.bat
    del /f -delete.bat
    del /f -publish.bat
    del /f -ticket.bat
    del /f -version.bat

## Testowanie skrótowych komend
zamiast:

    .apicra\-project-create.bat "tom-sapletta-com" "apicra/win-ticket-version-flow"

z użyciem ticket version flow:

    -create.bat "tom-sapletta-com" "projectname"



## Cel projektu

+ ułatwienie codziennych prac związanych z aktualizacją kodu na różnych serwerach
+ w przyszłości również wsparcie dla deploymentu
+ utworzenie projektu i publikacja na github oraz npmjs jest możliwe w ciągu kilkunastu sekund, zobacz film:

[animation.gif](animation.gif)

### Od Autora

Od wielu lat programuję na różnych platformach, obecnie w środowisku windows.
W kilkunastu projektach tworzyłem już indywidualne oraz globalne skrypty do zarządzania projektem
Obecnie Skrypty do automatyzacji DEVOPS nazywam apicra

bazując na ostatnio utworzonym projekcie
https://github.com/gitpad-pl/github
(paczka npmjs) stworzyłem jeszcze bardziej zaawansowane skrypty do aktualizacji projektu bez odchodzenia od konsoli.

Każda sytuacja wymagająca użycia myszki lub wymagająca wielu komend zabiera czas, który przy użyciu skryptów .apicra można zaoszczędzić

Apicra uwzględnia rózne technologie i serwisy wspierające utrzymanie aplikacji i publikację kolejnych wersji.

+ lokalny system plików
+ repozytorium Github
+ npmjs

### Przykładowy workflow przydający się do rozwoju oprogramowania przy uzyciu nodejs:

https://github.com/apicra/win-ticket-version-flow


Nazwa: Ticket - Version flow bierze się z 2 etapowego rozwoju aplikacji
Komendą -ticket.bat tworzy się opis zadania, które wchodzi w skład aktualnej wersji, każy "ticket" jest zapisywany do pliku z numerem wersji w folderze /ticket
wszystkie zadania są publikowane przy każdej aktualizacji wersji (w następnym kroku)

    -ticket.bat "nazwa zadania"


W przypadku zamknięcia wersji uruchamia się komendę, podając lub nie typ aktualizacji wersji MAJOR.MINOR.PATCH

    -version.bat "minor"


#### Oprócz tych uzywanych cyklicznie komend są jeszcze jednorazowe komendy do utworzeni lub usunięcia projektu

Tworzenie folderu projektu i plików inicjujących, commit i push na server github

    -create.bat "tom-sapletta-com" "projectname"

Pierwsza publikacja paczki na NPMJS, następne są realizowane przez komendę: -version.bat

    -publish.bat "projectname"


Usunięcie z 3 miejsc: lokalny system plików, repozytorium github, paczka npmjs

    -delete.bat "tom-sapletta-com" "projectname"


#### Tutaj trochę więcej informacji o wersjonowaniu
https://semver.org/lang/pl/


#### Podsumowanie

Na przykładzie workflow ticket-version można ocenić na ile takie skrypty pomogą w danym projekcie
Tutaj położyłem nacisk na szybką publikację nowych wersji bez wchodzenia na strony dystrybutorów aplikacji
oraz na możliwość późniejszej rozbudowy o kolejnych dystrybutorów paczek, jak chocolate, packagist, itd


#### Wsparcie projektu
Jeśli uważasz, że projekt jest ciekawy a nawet wypróbowałeś go i przydał się w Twoim projekcie,
lub przeciwnie nie spełnia oczekiwań lub zawiera błędy, to zachęcam do kontaktu na stronie projektu github.
Każdy zalogowany użzytkownik github może stworzyć ticket dla projektu i zgłosić uwagi.

Finansowe wsparcie nie jest obecnie przewidziane, ale pojawi się taka możliwość pod koniec roku 2019

Przyjemnej pracy!
