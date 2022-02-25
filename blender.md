# Dagens övningar

- [Modellera en Creeper](#modellera) (Jag gillar Minecraft okej 😅)
- [Mappa till textur](#mappa-till-textur)
- Rigga till ett skelett
- Animera

### Bra resurser
[Blender fundamentals](https://www.youtube.com/playlist?list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6)

# Modellera
### Skapa modellen
Gå in i en ny fil och lämna allt utom kuben.

![bild](https://user-images.githubusercontent.com/70745846/155676369-689656d0-e3ca-4a1a-8ee3-b844c1032d95.png)

Tryck på "N" i 3D-vyn för att ta fram rutan med detaljer.

Tryck på kuben, och ge den sen dimensionerna 0.5, 1, 1,5

![bild](https://user-images.githubusercontent.com/70745846/155676837-67cad1c7-bb43-4d6d-a26f-5ced962910ad.png)

Skapa en ny kub genom att trycka på Add -> Mesh -> Cube

Flytta och skala den enligt följande bild:

![bild](https://user-images.githubusercontent.com/70745846/155677764-6aa2f401-a493-4ec1-a2c4-164741bee1b6.png)

Tryck på Shift-D för att duplicera benet. Ge den tre till ben, använd "location" för att se till att de hamnar rätt.

![bild](https://user-images.githubusercontent.com/70745846/155677991-e4f2b1ac-db87-4b31-9563-aaa9639fc9c3.png)

Nu ska huvudet läggas till.

Tryck på Add -> Mesh -> Cube för att lägga till en ny kub. Flytta och skala den enligt följande bild.

![bild](https://user-images.githubusercontent.com/70745846/155678386-bca96664-1317-45c0-be6a-d0df352447a0.png)

### Färdigställ modellen

Nu behöver vi se till att den står på marken. Tryck på A för att markera alla objekt. Tryck på G, sen Z, skriv "1.5" och tryck enter för att flytta dem 1,5M vertikalt.

![bild](https://user-images.githubusercontent.com/70745846/155678693-35d22d1b-6f28-41df-90b5-fbf6543814a8.png)

Tryck sen på Object -> Join för att kombinera alla objekt till ett.

![bild](https://user-images.githubusercontent.com/70745846/155678900-cf5bc48d-8f73-427e-a1ec-043aef8c0e83.png)

Tryck sedan Object -> Apply -> All Transforms för att objektet ska ha den nuvarande platsen och storleken som bas.

![bild](https://user-images.githubusercontent.com/70745846/155679153-14453040-8b98-4041-88e1-58e57f583ec7.png)

Dubbelklicka objektets namn och ändra det till "Creeper". Då bör det se ut så här:

![bild](https://user-images.githubusercontent.com/70745846/155679347-27a95bec-18ad-406a-8bf6-a0a4f41f3624.png)


# Mappa till textur
### Lägg in textur
<img src="https://user-images.githubusercontent.com/70745846/155528458-6ebe1b1e-96fc-47b2-b7af-cb45d0c50d12.png" width="300">

Högerklicka på texturen ovan och spara texturen på datorn.

I Blender, gå till Material-fliken och ändra källan för materialets färg till "Image Texture".

![bild](https://user-images.githubusercontent.com/70745846/155680331-c861b1a9-5a2a-4c87-a9b9-b6a18f5da85f.png)

Tryck "Open" och välj texturen du sparade ner. Byt också interpolering från "Linear" till "Closest".

![bild](https://user-images.githubusercontent.com/70745846/155680634-ab7e1243-63b4-47ad-bd12-a42dcbe95c43.png)

### Mappa modellen till texturen

Modellen kommer att mappas enligt följande mall:

<img src="https://user-images.githubusercontent.com/70745846/155527371-af4639b3-e725-412a-b0d4-01c9b6cdb0ed.png" width="700">

Byt till fliken UV Editing

![bild](https://user-images.githubusercontent.com/70745846/155694937-97ca9bcd-a5e3-40be-b753-8861c0968184.png)

Byt till "Edge Select" i 3D-vyn:

![bild](https://user-images.githubusercontent.com/70745846/155695173-1154d7cb-abc9-49a4-b092-6e06b8825f43.png)

Markera kanterna som på bilden:

![bild](https://user-images.githubusercontent.com/70745846/155695399-f87bd2c6-abb0-4d9e-a8cc-e19fba96a214.png)

Högerklicka och välj "Mark Seam". Detta markerar vart sömmarna är när den vecklas ut.

Byt till "Face Select" och markera ytorna på kanten och toppen (inte under):

![bild](https://user-images.githubusercontent.com/70745846/155695760-f117da8e-bbc9-49b4-8620-43b884f9994c.png)

Tryck på UV -> Unwrap:

![bild](https://user-images.githubusercontent.com/70745846/155695819-2d4c6495-0d18-4576-a6e4-aaf0b6e7851f.png)

I UV-editorn, flytta, rotera och skala de utvecklade ytorna så att de passar som på bilden:

![bild](https://user-images.githubusercontent.com/70745846/155696239-73371150-83eb-49bc-9004-8d46e08e94f3.png)

Kom ihåg snabbknappar:

- G: Flytta
- R: Rotera
- S: Skala

När de hamnat så bra som möjligt, gå till UV -> Snap -> Selected to Pixels:

![bild](https://user-images.githubusercontent.com/70745846/155696568-2f03e3c5-27bc-4506-a8f3-a406d3f45332.png)

Välj sedan undersidan av huvudet och unwrappa det:

![bild](https://user-images.githubusercontent.com/70745846/155696818-51101815-6d2a-4853-8b34-a2ec0383653b.png)

För att kunna se hur materialet ser ut, gå längs till höger i toppen på 3D-vyn (du kan behöva skrolla) och välj följande läge:

![bild](https://user-images.githubusercontent.com/70745846/155697080-074f70ac-c70c-4e19-8472-11cc63136a73.png)

Nu ser du att huvudet har rätt uteende:

![bild](https://user-images.githubusercontent.com/70745846/155697304-5f8e7d1a-cbbe-4d03-8a10-2528a2710b73.png)

Unwrappa nu resten enligt mallen. (Tips: tryck på H för att dölja ytor och Alt-H för att få tillbaka dem)

### Resultat

![bild](https://user-images.githubusercontent.com/70745846/155697794-5efb949d-0b9c-4f06-8b75-4dca16b48961.png)


# Animera

Animation Tab, Action editor, keyframes
