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



<!---
Tips: Om du använder min mall för spelet bör du anropa "screenshake"-metoden du gjort från objektet "LevelGen"

![image](https://user-images.githubusercontent.com/70745846/162633745-337ac0d7-e908-4d64-b41b-bed48ea1b22b.png)

![image](https://user-images.githubusercontent.com/70745846/162633779-63013112-3b46-41bf-b038-43281ccf1549.png)

![image](https://user-images.githubusercontent.com/70745846/162633852-bc367489-9885-4d96-a642-6dbfb439b339.png)
-->


### Lägg in ljudeffekter

Det finns många tutorials hur man lägger in ljudeffekter. Testa t.ex. att lägga in ett ljud som spelas när bollen stöter i något.

Det kan vara svårt att hitta bra sidor med gratis ljudeffekter, men t.ex. [Pixabay](https://pixabay.com/sound-effects/) kräver ingen registrering och har en del ljud.

### Lägg in partikelsystem

Testa att lägga in ett partikelsystem som triggas från bollen när man förlorar. Detta kan vara lite svårare, och är nog lättast att kontrollera från scriptet "FailZone" som gör att man förlorar. (Om du använder min mall)
