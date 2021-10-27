# Spotify katalógus kliens
## Feladat [2-3 mondat]

A hivatalos Spotify Web API-ra épülő webes felület. A felhasználó a Spotify fiókjával léphet be. A felhasználó a mentett számait és a lejátszási listáit tudja táblázatos formában böngészni, kezelni illetve keresni is lehet a teljes Spotify katalógusban.

## A kisháziban elérhető felületek és funkcióik [adatmódodosító is legyen benne]

* "Mentett számok" felület
  * Mentett számok megjelenítése táblázatban  
  * Törlés a mentett számokból
* Lejátszási lista felület
   * Lejátszási lista kiválasztása
   * Kiválasztott lista megjelenítése táblázatos formában
   * Törlés a lejátszási listából
* Keresés felület
  * Kulcsszavas keresés számcímre
  * Eredmények megjelenítése táblázatban (max. 20 db.)
  * Eredmények közül a kiválasztott számok hozzáadása a lejátszási listához
  
## Alaparchitektúra és kliensoldali technológia [a kliensoldali technológia csak a tárgyhonlapon megadottak közül választható]
  * Szerveroldal: Spotify Web API [érdemes már létező szerveroldalt, webes API-t választani]
  * Kliensoldal: Blazor WebAssembly

## Továbbfejlesztési tervek [opcionális, a pontrendszerből érdemes válogatni]
  * hosztolás Azure-ban
  * többnyelvű felület
  * külső komponens (táblázat) integrálása
  * IndexedDB használata gyorsítótárként
  * PWA képesség
  * Függőségek on-demand letöltése (assembly lazy loading)
