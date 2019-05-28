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
