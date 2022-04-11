# Utöka Breakout-spelet

Är ni nöjda med Breakout-spelet ni gjorde för två lektioner sedan kan ni fortsätta med det, annars rekommenderar jag att ni laddar ned denna färdiga version: [Ladda ned](breakoutDownload.md)


# Dagens Övningar

Idag är uppgiften att utöka Breakout-spelet och ge bättre feedback till spelaren. Det kan handla om visuella effekter, ljudeffekter eller annat. Ni får fria händer att vara kreativa med era spel, men nedan finns några exempel på vad ni kan göra.

# Exempel på förbättringar

### Spår bakom bollen

Högerklicka på bollen, och skapa en "Trail" genom att trycka på "Effects" -> "Trail"

![image](https://user-images.githubusercontent.com/70745846/162632235-8fd102d3-4401-43d9-880f-c2f54356521c.png)

I Inspectorn kan ni välja hur spåret ska se ut. Här är några inställningar som fungerade bra för mig:

![image](https://user-images.githubusercontent.com/70745846/162632310-dd7ba7a4-ad51-414e-b5e2-095a3fad0a1d.png)

### Byt bollen mot en 3D-modell

Börja med att öppna blender och gör en 3D modell. Som exempel skapar jag en enkel "Icosphere":

![image](https://user-images.githubusercontent.com/70745846/162634002-7a47571b-8dde-45f1-8e33-575ad4535d42.png)

Sen kan du spara modellen någonstans i "Asset"-mappen som finns i projektmappen "Breakout": (Det vore snyggast att sortera bättre om det finns fler modeller)

![image](https://user-images.githubusercontent.com/70745846/162634206-d71ca0df-fe37-49a5-891d-9bc25c1a4064.png)

Då dyker modellen upp i unity:

![image](https://user-images.githubusercontent.com/70745846/162634183-11f80dbb-9f63-4b11-801d-c166de10b390.png)

Dra sedan ut den på bollen i scenen:

![image](https://user-images.githubusercontent.com/70745846/162634298-dbc6801b-6350-4bc0-ba94-fd46f50e15ec.png)

För att få något djup behövs också en ljuskälla, t.ex. en "Directional Light":

![image](https://user-images.githubusercontent.com/70745846/162634328-c7edc08d-484c-47ae-9f06-1a60288e978d.png)

För att sälja att det är en 3D-modell är det också bra om den roterar. Testa att försöka göra ett sådant script själv.

### Skakande kamera

Att kameran skakar lite när man förstör ett block gör att det känns mycket kraftfullare.

Det finns många bra exempel på nätet, t.ex. [detta](https://medium.com/nice-things-ios-android-development/basic-2d-screen-shake-in-unity-9c27b56b516)

#### Tips på hur ni implementerar ScreenShake i projektmallen

Gör en statisk referens i "screenshake"-klassen du gjort:

![bild](https://user-images.githubusercontent.com/70745846/162698563-7d41ef47-45a7-4085-b86f-a308851eadab.png)

I "Awake" eller "Start" -metoden, lägg in en rad kod för att sätta referensen till objektet:

![bild](https://user-images.githubusercontent.com/70745846/162698739-aeeda658-c749-47da-8b08-75a1043cceb7.png)

Gör sedan en statisk metod som anropar "screenshake" -metoden från referensen:

![bild](https://user-images.githubusercontent.com/70745846/162698959-98665de2-0478-4d50-ad92-682d51cb8fcd.png)

Gå till sist in i "BlockBehaviour" -klassen och anropa den statiska funktionen när blocket förstörs:

![bild](https://user-images.githubusercontent.com/70745846/162699206-d9e2cb2a-dbd6-4f0d-8f74-3210952cb087.png)

(I min kod lade jag även till en parameter till funktionen som bestämmer magnituden på skakningen)

### Lägg in partikelsystem

Testa att lägga in ett partikelsystem som triggas från bollen när man förlorar. 

#### Hur ni gör det på min mall

Skapa ett nytt partikelsystem och se till att "Play on Awake" inte är ibockat:

![bild](https://user-images.githubusercontent.com/70745846/162703208-3abf2a2c-4cda-46dc-8580-a6acc4f6a7c5.png)

Ett tips är också att i fliken "Emission" sätta "Rate over Time" till 0 och lägga till en burst istället (så att det blir mer som en explosion)

I scriptet "FailZone", lägg till en referens till ett partikelsystem. När spelaren förlorar, gör så att partikelsystemets position flyttas till bollens position, och starta sedan systemet:

![bild](https://user-images.githubusercontent.com/70745846/162703875-6e5782da-b1c9-4fca-9544-805a3dd7e763.png)

Med objektet "FailZone" markerat, dra till sist en referens för partikelsystemet till "FailZone" scriptet:

![bild](https://user-images.githubusercontent.com/70745846/162704115-d851f40c-428e-4305-bf9b-2e311e46cb6a.png)


### Lägg in partikelsystem på blocken

En svårare variant av partiklar är att blocken skapar partiklar när de går sönder.

#### Hur ni gör detta på mallen

Börja med att öppna prefaben till blocket:

![bild](https://user-images.githubusercontent.com/70745846/162704670-200f486c-f409-40ad-89c8-984d8ff17639.png)

Skapa ett nytt partikelsystem under blocket:

![bild](https://user-images.githubusercontent.com/70745846/162704748-f9fe4e91-4725-4c3f-b98d-4eeb4c208962.png)

I partikelsystemet bör en del inställningar ändras, viktigast är att "Looping" är av, "Play on Awake" är av och att "Stop Action" är "Destroy".

![bild](https://user-images.githubusercontent.com/70745846/162723127-c12998a0-ca57-4d78-af4a-3096b6604ceb.png)

Sedan behöver det läggas till fyra rader kod i scriptet "BlockBehaviour". Först behöver det finnas en referens till partikelsystemet, sen behöver partikelsystemet Startas och kopplas från blocket innan blocket förstörs:

![bild](https://user-images.githubusercontent.com/70745846/162723400-26f2c292-e350-4253-bfdf-473506a64ae7.png)

Till sist måste referensen till partikelsystemet läggas in i prefaben. Med objektet "Block" markerat, drag referensen till partikelsystemet till scriptet "Block Behaviour":

![bild](https://user-images.githubusercontent.com/70745846/162723705-3ac53fac-b051-4265-a00b-a5f465926c60.png)

Sen finns det många inställningar för att partikelsystemet ska se bra ut. Jag har ändrat inställningar under flikarna "Emission", "Shape", "Color over Lifetime", "Noise" och "Renderer":

![bild](https://user-images.githubusercontent.com/70745846/162724129-9ab9daeb-1589-4973-939a-cb8287073d05.png)

I "Renderer" har jag valt ett eget material till partiklarna. Det materialet ser ut så här:

![bild](https://user-images.githubusercontent.com/70745846/162724269-cf39566a-bba3-4a21-96eb-64eca30e486b.png)

### Lägg in ljudeffekter

Det finns många tutorials hur man lägger in ljudeffekter. Testa t.ex. att lägga in ett ljud som spelas när bollen stöter i något.

Det kan vara svårt att hitta bra sidor med gratis ljudeffekter, men t.ex. [Pixabay](https://pixabay.com/sound-effects/) kräver ingen registrering och har en del ljud.

