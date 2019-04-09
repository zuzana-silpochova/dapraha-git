# Git

## Co je to Git?

* VCS - Version Control System - Verzovací systém

## Co je to verzovací systém?

* Software pro sledování změn v souborech
* VCS existuje spousta: CVS, SVN, BitKeeper, Bazaar, Mercurial, Git
* Git je nejrozšířenější a nejpopulárnější

## Co je to teda ten Git?

* Distribuovaný VCS
* Uchovává historii změn souborů
* Umožňuje změny snadno decentralizovaně sdílet s dalšími lidmi

## Git vs Github

* Git je jeden konkrétní nástroj pro verzování souborů
* Github je online služba, skrz kterou můžeme sdílet naše soubory a jejich historii změn 
  s ostatními
* Takových služeb existuje víc, třeba Gitlab, Bitbucket, Sourceforge, repo.or.cz, ...

## Co budeme pro Gitování potřebovat

* Příkazovou řádku
* Nainstalovaný Git
* Účet na Githubu
* Trpělivost a odhodlání

## Spooousta termínů

* Dneska nás čeká spousta nových termínů. Jako /FAKT/. /VELKÁ/. /SPOUSTA/.
* Budou se vám plést
* Používejte cheat-sheet

# JDEME NA TO

# Příkazová řádka

* Znáte z Pythonu!
* Nebojte se ji ![](bane)
* Zkuste napsat příkaz "git"

## Příkazová řádka a složky

* Na začátku řádky vidíš název aktulání složky, ve které jseš
  * Je to stejné, jako když máš otevřenou složku v Průzkumníkovi
* Příkazy v příkazové řádce se provádějí v aktuální složce
* Příkaz pro výpis obsahu aktuální složky: `dir` (na MacOS a Linuxu: `ls`)
* Příkaz pro otevření složky: `cd složka` (cd = *c*hange *d*irectory)
* Příkaz pro návrat do předchozí (nadřazené) složky: `cd ..`

# Příkazy Gitu

* Samotný git má přes 120 příkazů, spoustě z nich nikdo nerozumí
* My si dnes vystačíme s cca 15 - téměř vše, co je potřeba znát

```
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
```

## Nápověda

* Přehled nejčastějších příkazů:
    - `git` (nebo hoď očkem do cheat-sheetu)
* Nápověda ke konkrétnímu příkazu:
    - `git help příkaz`
    * někdy hodně technické a těžko srozumitelné

# Repozitář

* Obyčejná složka, jejíž obsah verzujeme ve VCS (v našem případě v Gitu)
* Obsah jsou všechny soubory a podsložky uvnitř repozitáře
* Můžu si ho buď vytvořit lokálně, nebo si stáhnout existující repozitář z internetu

## Jak udělám ze složky repozitář?

- `git init muj-projekt` - vytvoří složku `muj-projekt` a začne ji verzovat v Gitu

## Jak si stáhnu cizí repozitář z internetu?

* V terminologii gitu se tomu říká klonování (cloning)
- `git clone https://github.com/uzivatelske-jmeno/nazev-repozitare.git`

## CVIČENÍ

* Naklonuj si můj vzorový repozitář:
  - `git clone https://github.com/danvratil/dapraha-git.git`

* V aktuální složce bys měla mít složku `dapraha-git`
* Zkontroluj, že tomu tak je pomocí příkazu `dir` (pokud jsi na Macu nebo Linuxu tak `ls`)
* Otevři ji pomocí příkazu `cd`




[bane]: https://memegenerator.net/img/instances/53038538/you-merely-adopted-the-command-line-i-was-born-in-it-molded-by-it-i-didnt-see-a-gui-until-i-was-alre.jpg
