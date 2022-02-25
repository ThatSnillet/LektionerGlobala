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

Tryck på TAB för att gå in i Edit Mode på modellen.

![bild](https://user-images.githubusercontent.com/70745846/155679818-d67438ea-1931-4f9c-91b7-d8f9cd8035e0.png)



# Animera

Animation Tab, Action editor, keyframes
