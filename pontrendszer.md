# Házi követelmények és pontrendszer
**Véglegesítve 2021. őszi félévre**

## Kisházi követelmények 

* A következő platformok valamelyikén elkészített alkalmazás:
   * XAML     
      * Windows Presentation Foundation (WPF)
      * Universal Windows platform (UWP)
      * WinUI
      * Xamarin.Forms - XAML UI
      * Xamarin natív (Xamarin.iOS vagy Xamarin.Android) iOS vagy Android UI (csak saját felelősségre, gyakorlaton nem szerepel)
      * MAUI (csak saját felelősségre, gyakorlaton nem szerepel)
   * Blazor
      * Blazor WebAssembly
      * Blazor Server (csak saját felelősségre, gyakorlaton nem szerepel)
* XAML alapú technológia esetben
   * MVVM minta alkalmazása
   * adatforrás (legalább egyet kell választani):
      * lokális fájl
      * beágyazott adatbázis
      * szerveroldali/külső API
* Blazor esetén
    * .NET 5 (vagy 6 - saját felelősségre) alapplatform
    * adatforrás (legalább egyet kell választani):
      * szerveroldali/külső API (esetleg szerveroldali adatbázis főleg Blazor Server esetén)
      * böngészőn belül elérhető adatforrás (pl. local storage, IndexedDB)
* Authentikáció nem szükséges (kivéve persze, ha a külső API meghívása másként nem lehetséges).
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

* Minden kisházi követelmény
* Legfeljebb két alkalmazás, két különböző technológiával a fentiek közül
* Legalább 30 pont megszerzése a lenti pontrendszer alapján
* **Megajánlott jegy számítása:** 30-49 pont: jó (4), 50+ pont: jeles (5)

### Pontszerzési szabályok

* Egy jogcímen csak egyszer szerezhető pont (pl. nem lehet 3 külső osztálykönyvtárral 21 pontot összeszedni), kivéve ahol ezt külön jelezzük
* Részpontszám nem adható, kivéve, ahol intervallum van megadva
* Szerveroldali megoldásért nem adható pont, kivéve Blazor Server
* A szoftvernek egységes funkcióhalmazt kell nyújtania, különálló, egymáshoz nem kapcsolódó funkciókból álló szoftver nem elfogadható. Azaz különálló tutorialok összefércelését nem díjazzuk.

## Pontrendszer - XAML

### Általános

*   Dependency Injection minta használata **[6]**
*   Külső osztálykönyvtár használata (a külső komponensért további pontszám nem adható). Nem számít ide a projekt generálásakor bekerülő, illetve a Microsoft által készített NuGet csomagok **[3]**
*   Store-ba publikált app **[15]**
*   Reaktív programozási minták Rx osztálykönyvtár használata **[6]**
    *   ReactiveUI MVVM keretrendszer használata **[+6]**

### Adatkezelés

* Beágyazott adatbázis (pl. SqLite) használata **[6]**
    * Entity Framework Core könyvtárral **[+3]**
* Social authentikáció (Live, Facebook) **[6]**
* Külső webszolgáltatás szolgáltatás elérése **[3]**
    * REST kliens implementálása (nem előre elkészített SDK-n keresztül kommunikál) **[+3]**
* Offline szinkronizáció szerveralkalmazással **[9]**

### UI

* Külső UI osztálykönyvtár használata **[3]**
* Coded UI teszt **[6]**
* Lokalizáció (angol+magyar, teljes) **[6]**
* DPI skálázásra felkészített felület és erőforrások **[3]**
* Különböző képernyő méretekre is felkészített felületek **[6]**
* Animációk használata **[3-9]**
* Gesztuskezelés **[3]**
* Accessibility (fogyatékkal élők támogatása) **[5-10]**
* Egyedi vezérlő készítése! **[3-6]** **Nem User Control!**
  * Xamarin esetében saját Renderer komponensek implementálása
* Saját Markup Extension készítése **[3]**

* Inkrementálisan betöltődő lista **[3]**
* Line-of-Business alkalmazás funkciók implementálása **[3-15]** pl: inputvalidáció, drag&drop, összetett menürendszer, ribbon, DataGrid stb. 
* Kiemelkedő UX/UI design pl.: Connected animation, extra Fluent Design elemek, CompositionAPI használata stb. **[3-9]**

### Platformszolgáltatások

* Médialejátszás **[3]**
  * Alacsony szintű médiakezelés **[+9]** pl.: Effects, MIDI, Transcode stb.
* Háttérszolgáltatás készítése **[6]**
* Szenzorhasználat **[6]**
* Alacsonyszintű kommunikáció használata (Bluetooth, NFC, Wifi Direct stb) **[9]**
* Térkép kezelés, és hely alapú szolgáltatások kezelése **[6-12]**
  * pl.: Útvonaltervezés, geocoding vagy POI vagy területrajzolás. geofencing stb.
* Kamera közvetlen kezelése, Nem a gyári kamera alkalmazás feldobása! **[9]**
* Speech API, személyi aszisztens integráció **[3-6]**
* Értesítések kezelése **[3]**
  * Push értesítések **[+6]**
  * Interaktív értesítések **[+3]**
* Store API (trial verzió vagy in-app purchase, store szimulátor) **[6]**
* Rendszer szintű integrációk
  * Protokol aktiváció **[3]**
  * Megosztás támogatása **[3-6]**
  * Appok közötti kommunikáció (UWP API-val) **[9]**

## Pontrendszer - Blazor

### Általános

* On-demand függőség letöltés (Assembly Lazy Loading) **[7]**
* PWA képesség. Az alkalmazás PWA-ként telepíthető pl. Windows-on **[6]**
* Lokalizáció, többnyelvű felület. **[7-10]**
  * Az alkalmazás két nyelvű angol+magyar, minimum annyi felületen, amennyi a kisházihoz kell. Az oldal első megnyitásakor alapértelmezett nyelv: a böngésző nyelvi beállítása alapján. A nyelvenkénti szövegek resource fájlban (resx) tárolódnak. **7**
  *  Az előbbin felül a nyelv állítható a felületen **+3**
* Külső osztálykönyvtár használata (a külső komponens által ellátott feladatért további pontszám nem adható). Nem számít ide a projekt generálásakor bekerülő, illetve a Microsoft által készített NuGet csomagok **[5]**
* Háttérfolyamat(ok) futtatása valós párhuzamossággal web workerek segítségével. Ajánlott integrációs csomagot (pl. [BlazorWorker](https://github.com/tewr/BlazorWorker)) használni. **[7]**
* Időzítő (Timer) alkalmazása. **[3]**
* Dependency Injection konténerbe regisztrált objektum élettartamának korlátozása `OwningComponentBase` ősosztály alkalmazásával. **[5]**

### Adatkezelés, állapottárolás

* Böngésző local storage használata egyszerű adatok tárolásásra, állapottárolásra, például felhasználói beállítások kliensoldali elmentésére. Ajánlott integrációs csomagot (pl. [Blazored-LocalStorage](https://github.com/Blazored/LocalStorage), [BlazorExtensions.Storage](https://github.com/BlazorExtensions/Storage)) használni. **[6]**
* IndexedDB használata komplexebb adatok tárolására, nagyobb adatok gyorsítótárazására. Ajánlott integrációs csomagot (pl. [BlazorIndexedDbJs](https://github.com/kattunga/BlazorIndexedDbJs)) használni. **[7]**
* Webassembly fölött futó sqlite használata relációs adatok gyorsítótárazására. [Demo](https://www.youtube.com/watch?v=kesUNeBZ1Os) **.NET 6 szükséges!** **[12]**
* Felületi beállítások tárolása URL-ben. A felület az URL alapján vissza tudja tölteni a beállításait (pl. szűrési, lapozási, rendezési beállításokat). **[6]**
* Felhasználóhoz kapcsolódó beállítások, adatok mentése elterjedt felhős adattároló szolgáltatásba (pl. OneDrive/[MS Graph API](https://docs.microsoft.com/en-us/onedrive/developer/rest-api/api/driveitem_put_content?view=odsp-graph-online)). **Külön authentikációt igényelhet** **[15]**

### Kommunikáció

**Figyelem! Ezen szekcióban a pontok megszerzéséhez a legtöbb esetben szerveroldali támogatás is szükséges!**
* Kliensoldali kommunikációs kód generálása OpenAPI/Swagger szolgáltatásleíróból **[5]**
* SignalR/WebSocket használata push jellegű (Szerver -> Kliens) kommunikációra **[7]**
* GraphQL/OData/gRPC-Web alapú kommunikáció használata **[7]**
* Proxy alkalmazása a forrásszerveren (ahonnan a WebAssembly alkalmazás letöltődik) CORS hibák elkerülésére. **[5]**
* HTTP kérések központi robosztusabbá tétele [Polly](https://github.com/App-vNext/Polly) könyvtárral. Ehhez nem kell szerveroldali támogatás. **[7]**

### Felület, DOM, Razor komponensek

* Saját Razor komponens készítése és felhasználása másik Razor komponensben. A felhasznált komponens a szükséges adatokat komponensparamétereken keresztül kapja **[6]**
* Saját Layout komponens készítése és alkalmazása a webalkalmazás egy részére, egy adott könyvtárban található oldalak/komponensekre **[6]**
* Külső Blazor komponenskönyvtár használata. Ajánlott: [MudBlazor](https://mudblazor.com/), [Syncfusion](https://www.syncfusion.com/blazor-components) ([Community licensz](https://www.syncfusion.com/products/communitylicense)), [Radzen](https://blazor.radzen.com/). [Bővebb lista](https://github.com/AdrienTorris/awesome-blazor#component-bundles). **[10]**
* JavaScript függvény hívása C#-ból **[3]**
* C# függvény hívása JavaScript-ből **[3]**
* A `@code` blokkba kerülő C# kód kiszervezése külön C# fájlba (ún. code behind fájl) **[3]**
* MVVM minta használata. Ajánlott mini keretrendszert (pl. [MVVMBlazor](https://github.com/klemmchr/MvvmBlazor)) használni. **[10]**
* Dinamikusan renderelt Razor komponens használata. **.NET 6 szükséges!** **[5]**
* Legalább egy komponens egységes hibakezelésének megvalósítása `ErrorBoundary` használatával. **.NET 6 szükséges!** **[5]**
* Külső térképszolgáltató integrálása (pl. Google Maps, Azure Maps) .NET komponens segítségével. JavaScript alapú megoldásért nem jár pont. **[5-7]**
  * A használt komponenskönyvtár által nyújtott integráció **[5]**
  * Különálló komponens (pl. [BlazorGoogleMaps](https://github.com/rungwiroon/BlazorGoogleMaps)) **[7]**
* Rajzolás HTML5 canvasra .NET komponens segítségével. JavaScript alapú megoldásért nem jár pont. **[5-7]**
   * A használt komponenskönyvtár által nyújtott integráció **[5]**
   * Különálló komponens (pl. [Blazor.Canvas](https://github.com/excubo-ag/Blazor.Canvas)) **[7]**
* HTML5 videólejátszás/vezérlés .NET komponens segítségével. JavaScript alapú megoldásért nem jár pont. **[5-7]**
   * A használt komponenskönyvtár által nyújtott integráció **[5]**
   * Különálló komponens (pl. [Blazored Video](https://github.com/Blazored/Video)) **[7]**

### DevOps

* Hosztolás külső szolgáltatónál (pl. Azure Static Web App) vagy klasszikus webszerveren (IIS, Apache, nginx). Csak Kestrel (beépített ASP.NET Core webszerver) nem elfogadható. **[7]**
* Kliensoldali naplózás **[3-10]**
  * Böngésző konzolra. Ajánlott integrációs csomagot (pl. [BlazorExtensions.Logging](https://github.com/BlazorExtensions/Logging)) használni. **[3]**
  * Emellett Application Insighstsba is. Ajánlott integrációs csomagot (pl. [BlazorApplicationInsights](https://github.com/IvanJosipovic/BlazorApplicationInsights)) használni. **+7**
* Legalább 3 Razor komponens tesztelése [bUnit](https://bunit.dev/)-tal. Komponensenként min. 5 teszteset. **[10]**

### Biztonság, authentikáció

* Authentikáció kliensoldali része. **Szerveroldali támogatás szükséges!** Süti (cookie) alapú megoldásért nem jár pont. **[3-15]**
  * API kulcs alapú authentikáció **[3]**
  * az adott szolgáltatáshoz tartozó SDK által végzett authentikáció **[5]**
  * OpenID/OAuth PKCE flow az adott szolgáltatáshoz tartozó SDK által végezve **[6]**
  * OpenID/OAuth PKCE flow implemenetálása **[10]**
  * Refresh token kezelése, mentése local storage-ba **+5**

## A szabályrendszer változása

Véglegesítés után is fenntartjuk a jogot
* a jogcímek halmazának bővítésére
* a jegyszámítási határok kedvezőbbé tételére
* pontosításra, helyesírási hibák javítására
* egyéb változtatásra egyetemi szabályok változása miatt (pl. járványhelyzet miatt)

Ezen változtatásokat hallgatók is kezdeményezhetik *pull request* küldésével.
A változásokat a [github history-ban](https://github.com/bmeaut/kliensdotnet/commits/master/pontrendszer.md) követhetitek.
