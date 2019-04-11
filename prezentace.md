# Git

----

## Co je to Git?

* VCS - Version Control System - Verzovací systém

----

## Co je to verzovací systém?

* Software pro sledování změn v souborech
* VCS existuje spousta: CVS, SVN, BitKeeper, Bazaar, Mercurial, Git
* Git je nejrozšířenější a nejpopulárnější

----

## Co je to teda ten Git?

* Distribuovaný VCS
* Uchovává historii změn souborů
* Umožňuje změny snadno decentralizovaně sdílet s dalšími lidmi

----

## Git vs Github

* Git je jeden konkrétní nástroj pro verzování souborů
* Github je online služba, skrz kterou můžeme sdílet naše soubory a jejich historii změn 
  s ostatními
* Takových služeb existuje víc, třeba Gitlab, Bitbucket, Sourceforge, repo.or.cz, ...

----

# Co budeme pro Gitování potřebovat

* Příkazovou řádku
* Nainstalovaný Git
* Účet na Githubu
* Trpělivost a odhodlání

----

# Spooousta termínů

* Dneska nás čeká spousta nových termínů. Jako /FAKT/. /VELKÁ/. /SPOUSTA/.
* Budou se vám plést
* Používejte cheat-sheet

----

# JDEME NA TO

----

# Příkazová řádka

![bane](https://memegenerator.net/img/instances/53038538/you-merely-adopted-the-command-line-i-was-born-in-it-molded-by-it-i-didnt-see-a-gui-until-i-was-alre.jpg)

----

# Příkazová řádka

* Znáte z Pythonu!
* Nebojte se ji
* Zkuste napsat příkaz "git"

----

## Příkazová řádka a složky

* Na začátku řádky vidíš název aktulání složky, ve které jseš
  * Je to stejné, jako když máš otevřenou složku v Průzkumníkovi
* Příkazy v příkazové řádce se provádějí v aktuální složce
* Příkaz pro výpis obsahu aktuální složky: `dir` (na MacOS a Linuxu: `ls`)
* Příkaz pro otevření složky: `cd složka` (cd = *c*hange *d*irectory)
* Příkaz pro návrat do předchozí (nadřazené) složky: `cd ..`

----

## Příkazy Gitu

* Samotný git má přes 120 příkazů, spoustě z nich nikdo nerozumí
* My si dnes vystačíme s cca 15 - téměř vše, co je potřeba znát

    !python
      říká Windows,
    že chceme spustit       ,- parametry pro konkrétní příkaz gitu
          git               |
           |          ______|______
          / \        /             \
          | |        |             |
          git commit -m "Můj commit"
              |    |
              \____/
                 |
       říká gitu, co má udělat
    (tzv. příkaz gitu - git command)

----

## Nápověda

* Přehled nejčastějších příkazů:
    - `git` (nebo hoď očkem do cheat-sheetu)
* Nápověda ke konkrétnímu příkazu:
    - `git help příkaz`
    * někdy hodně technické a těžko srozumitelné

----

# Repozitář

* Obyčejná složka, jejíž obsah verzujeme ve VCS (v našem případě v Gitu)
* Obsah jsou všechny soubory a podsložky uvnitř repozitáře
* Můžu si ho buď vytvořit lokálně, nebo si stáhnout existující repozitář z internetu

----

## Jak udělám ze složky repozitář?

- `git init muj-projekt` - vytvoří složku `muj-projekt` a začne ji verzovat v Gitu

----

## Jak si stáhnu cizí repozitář z internetu?

* V terminologii gitu se tomu říká klonování (cloning)
- `git clone https://github.com/uzivatelske-jmeno/nazev-repozitare.git`

----

## CVIČENÍ

* Naklonuj si můj vzorový repozitář:
  - `git clone https://github.com/danvratil/dapraha-git.git`

* V aktuální složce bys měla mít složku `dapraha-git`
* Zkontroluj, že tomu tak je pomocí příkazu `dir` (pokud jsi na Macu nebo Linuxu tak `ls`)
* Otevři ji pomocí příkazu `cd`

----

# Commity

* Commit je objekt v gitovém repozitáři
* Commit je změna v jenom či více souborů

----

## Co obsahuje commit

* Identifikátor ("hash") commitu
* Identifikátor předchozího commitu
* Autora commitu
* Datum a čas vzniku commitu
* Popis commitu zadaný autorem
* Samotné změny

----

## Jak vypadá commit

    commit 880d9161ba9de2cb8899d3e5ceea0c8590576ad2
    Author: Dan Vrátil <dan.vratil@czechitas.cz>
    Date:   Wed Apr 10 17:42:29 2019 +0200

        Oprava nevinného překlepu

    diff --git a/prezentace.md b/prezentace.md
    index 46aa983..f0ee52c 100644
    ---- a/prezentace.md
    +++ b/prezentace.md
    @@ -132,5 +132,5 @@
     * Identifikátor předchozího commitu
     * Autora commitu
    -* Datum a čas vzňyku commitu
    +* Datum a čas vzniku commitu
     * Popis commitu zadaný autorem
     * Samotné změny

----

## Zobrazení commitu

- `git show 880d9161ba9de2cb8899d3e5ceea0c8590576ad2`
- `git show 880d91`

----

## CVIČENÍ

* V terminálu otevři repozitář, který sis naklonovala v minulém cvičení
* Zobraz si commit `476751` (`476751b49e2d9a9f0e2edb84445540eb76ffc9f8`)

----

# Historie

* Historie je série commitů
* V jednom repozitáří může být i více historií, které se mohou různě větvit
* Historii říkáme `branch`, česky větev
* Hlavní větev se jmenuje `master` a existuje v každém repozitáří
* K větvím se podrobněji vrátíme později

----

## Zobrazení historie

- `git log`

----

## CVIČENÍ

* Zobraz si historii repozitáře

----

# Tvoříme historii

----

## Stav repozitáře

- `git status`
* Řekne nám, jaká je aktuální větev, a které soubory v repozitáři jsou změněné

----

## CVIČENÍ

* Zobraz si stav repozitáře
* Vytvoř v repozitáři nový soubor s nějakým textem
* Znovu si zobraz stav repozitáře

----

# Tvoříme commit

- `git commit -a -m "Můj první commitek"`
* `-a` říká gitu, že chceme commitnout všechny změny v repozitáři
* `-m "Commit message"` nastaví popis commitu

----

## CVIČENÍ

* Změn si nějaký soubor v repozitáři a udělej commit
* Podívej, jaký je stav repozitáře před a po commitu
* Podívej se na svůj commit v historii a zobraz si ho

----

## Staging

* `git commit -a` vloží do commitu všechny aktuální změny v repozitáři
* Někdy ale chceme commitnout jenom změny v některých souborech (nebo dokonce
  jenom některé změny v souboru)
* Změny, které chceme commitnout, musíme přidat do tzv. /stage/
- `git add zmeneny-soubor`
* `git commit -m "Popis změny"`

----

## CVIČENÍ

* Změň si nějaké dva soubory v repozitáři
* Podívej se na stav repozitáře
* Přidej jeden ze změněných souborů do stage, druhý nech být
* Znovu si nech zobrazit stav repozitáře
* Udělej nový commit
* Zobraz si znovu stav repozitáře

----

# Synchronizace mezi repozitáři

----

## Stahování změn ze vzdáleného repozitáře

* Jak si stáhnout změny třeba z Githubu?
- `git pull`

----

## CVIČENÍ

* Prohlédni si svou historii gitu
* Stáhni si změny, které jsem nahrál na Github
* Znovu se podívej na svou historii - vidíš v ní mou novou změnu?

----

# Odbočka: Forkování repozitářů na Githubu

* Do svého repozitáře můžu nahrávat změny pouze já
* Pokud do něj chcete nahrávat taky, musím vám dát přístup (nedám!)
* Otevři si můj repozitář na Githubu: https://github.com/danvratil/dapraha-git
* Vpravo nahoře klikni na tlačítko "Fork"
* Github udělá pod tvým účtem kopii mého repozitáře, do které můžeš zapisovat

----

## CVIČENÍ

* Vylez ze svého repozitáře (`cd ..`)
* Naklonuj si z Githubu svůj fork: `git clone https://github.com/TvojeGithubPřezdívka/dapraha-git`

