# SimpleLibrary

Eine einfache C++-Bibliothek zum Testen der FetchContent-Funktion von CMake.

---

## Beschreibung

**SimpleLibrary** stellt eine einfache Klasse `Greeter` bereit, die eine Ausgabe auf der Konsole macht. Die Bibliothek ist für Anfänger ein gutes Beispiel, um den Umgang mit **CMake FetchContent** zu lernen.

---

## Ordnerstruktur

```plaintext
SimpleLibrary/
│-- CMakeLists.txt             # Haupt-CMake-Konfigurationsdatei
│-- LICENSE                    # Lizenzdatei (MIT License)
│-- .gitignore                 # Git Ignore-Datei für Build-Ordner und Artefakte
│-- README.md                  # Beschreibung des Repos
│-- include/
│   └── Greeter.h              # Header-Datei mit der Klassendefinition
│-- src/
│   └── Greeter.cpp            # Implementierung der Klasse
│-- example/
│   └── main.cpp               # Beispiel zur Nutzung der Library
```

---

## Verwendung der Bibliothek mit FetchContent
### Einbinden der Bibliothek in ein Projekt

Füge folgendes in die `CMakeLists.txt` deines Projektes hinzu:

```cmake
include(FetchContent)

FetchContent_Declare(
    SimpleLibrary
    GIT_REPOSITORY https://github.com/skunkforce/CMake_provide_library
    GIT_TAG master
)
FetchContent_MakeAvailable(SimpleLibrary)

add_executable(MyApp example/main.cpp)
target_link_libraries(MyApp SimpleLibrary)
```

---

## Beispielnutzung 

Ein Beispiel für die Nutzung der Klasse `Greeter` findest du unter `example/main.cpp`. Hier wird die Klasse verwendet, um eine Ausgabe auf der Konsole zu machen.

```cpp
#include "Greeter.h"

int main() {
    Greeter greeter;
    greeter.sayHello();
    return 0;
}
```

---

## Lizens

Dieses Projekt steht unter der MIT License. Siehe `LICENSE` für Details.

---

### Fertiges Repo

Sobald du alle Dateien erstellt hast, sieht dein Repo so aus:

```plaintext
SimpleLibrary/
│-- CMakeLists.txt
│-- LICENSE
│-- .gitignore
│-- README.md
│-- include/
│   └── Greeter.h
│-- src/
│   └── Greeter.cpp
│-- example/
│   └── main.cpp
```

