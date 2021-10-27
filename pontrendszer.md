# (Előzetes) Házi Pontrendszer

**A 2021\. őszi félévre még nincs véglegesítve:\.**

## Kisházi követelmények

* A következő platformok valamelyikén elkészített alkalmazás:
   * XAML     
      * Windows Presentation Foundation (WPF)
      * Universal Windows platform (UWP)
      * WinUI
      * Xamarin.Forms - XAML UI
      * Xamarin natív (Xamarin.iOS vagy Xamarin.Android) (csak saját felelősségre, gyakorlaton nem szerepel)
      * Xamarin.Forms - iOS vagy Android UI (csak saját felelősségre, gyakorlaton nem szerepel)
   * Blazor
      * Blazor WebAssembly
      * Blazor Server (csak saját felelősségre, gyakorlaton nem szerepel)
* XAML alapú technológia esetben
   * MVVM minta alkalmazása
   * adatforrás (egyet kell választani):
      * lokális fájl
      * beágyazott adatbázis
      * szerveroldali/külső API
* Blazor esetén
    * .NET 5 (vagy 6 - saját felelősségre) alapplatform
    * adatforrás (egyet kell választani):
      * szerveroldali/külső API (esetleg szerveroldali adatbázis főleg Blazor Server esetén)
      * böngészőn belül elérhető adatforrás (pl. local storage, IndexedDB)
* Az elfogadott specifikációnak megfelelő működés 
* A szerveroldali adatforrás/API lehet külső, nem saját fejlesztésű is

**Nem elfogadható a megoldás ha**

* nem a fentebb felsorolt UI technológiákat használja, pl. WinForms felület
* kezeletlen kivétellel leáll a program
* blokkol a UI
* UX guideline-ok durva megsértése
* specifikációhoz képest jelentősen kevesebb funkcionalitás

## Nagyházi követelmények

Az alábbiak közül mindegyiknek teljesülnie kell a megajánlott jegyhez:

*   Minden kisházi követelmény
*   Legfeljebb két alkalmazás, két különböző technológiával a fentiek közül
*   Legalább 30 pont megszerzése a Pontrendszer alapján
*   **Megajánlott jegy számítása:** 30-49 pont: jó (4), 50+ pont: jeles (5)

## Pontszerzési szabályok

*   Egy jogcímen csak egyszer szerezhető pont
*   A pontszámnak jól meghatározható alkalmazásfunkcióhoz kell kapcsolódnia, nem fogadható el az implementáció, ha csak a levegőben lóg
*   Részpontszám nem adható kivéve, ahol intervallum van megadva

## **Még nincs véglegesítve 2021\. őszi félévre!**

**Véglegesítés után csak a hallgatóknak előnyös módosítások lehetnek (pl. új jogcímek):**

## Pontrendszer - XAML

### Általános

*   Dependency Injection minta használata **[6]**
*   Külső osztálykönyvtár használata (a külső komponensért további pontszám nem adható). Nem számít ide a projekt generálásakor bekerülő, illetve a Microsoft által készített NuGet csomagok **[3]**
*   Store-ba publikált app **[15]**
*   Reaktív programozási minták Rx osztálykönyvtár használata **[6]**
    *   ReactiveUI MVVM keretrendszer használata **[+6]**

### Adatkezelés

*   Beágyazott adatbázis (pl. SqLite) használata **[6]**
    *   Entity Framework Core könyvtárral **[+3]**
*   Social authentikáció (Live, Facebook) **[6]**
*   Külső webszolgáltatás szolgáltatás elérése **[3]**
    *   REST kliens implementálása (nem előre elkészített SDK-n keresztül kommunikál) **[+3]**
*   Offline szinkronizáció szerveralkalmazással **[9]**

### UI

*   Külső UI ösztálykönyvtár használata **[3]**
*   Coded UI teszt **[6]**
*   Lokalizáció (angol+magyar, teljes) **[6]**
*   DPI skálázásra felkészített felület és erőforrások **[3]**
*   Különböző képernyő méretekre is felkészített felületek **[6]**
*   Animációk használata **[3-9]**
*   Gesztuskezelés **[3]**
*   Accessibility (fogyatékkal élők támogatása) **[5-10]**
*   Egyedi vezérlő készítése! **[3-6]** **Nem User Control!**
    *   Xamarin esetében saját Renderer komponensek implementálása
*   Inkrementálisan betöltődő lista **[3]**
*   Line-of-Business alkalmazás funkciók implementálása **[3-15]** pl: inputvalidáció, drag&drop, összetett menürendszer, ribbon, DataGrid stb. 
*   Kiemelkedő UX/UI design pl.: Connected animation, extra Fluent Design elemek, CompositionAPI használata stb. **[3-9]**

### Platformszolgáltatások

*   Médialejátszás **[3]**
*   Háttérszolgáltatás készítése **[6]**
*   Szenzorhasználat **[6]**
*   Alacsonyszintű kommunikáció használata (Bluetooth, NFC, Wifi Direct stb) **[9]**
*   Térkép kezelés, és hely alapú szolgáltatások kezelése **[6-12]**
    *   pl.: Útvonaltervezés, geocoding vagy POI vagy területrajzolás. geofencing stb.
*   Kamera közvetlen kezelése, Nem a gyári kamera alkalmazás feldobása! **[9]**
*   Speech API, személyi aszisztens integráció **[3-6]**
*   Értesítések kezelése **[3]**
    *   Push értesítések **[+6]**
    *   Interaktív értesítések **[+3]**
*   Store API (trial verzió vagy in-app purchase, store szimulátor) **[6]**
*   Rendszer szintű integrációk
    *   Protokol aktiváció **[3]**
    *   Megosztás támogatása **[3-6]**

## Pontrendszer - Blazor

**Ha valaki olyan funkcióra/technológiára/megoldásra szeretne pontot kapni, ami nem szerepel a listában, azt a gyakorlatvezetővel egyeztetve kérheti a listára történő felvételét.**
