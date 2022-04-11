# Projektmall

Ladda ned filen [HÄR](Breakout.zip)

Extrahera zip-filen till en separat mapp där det passar. Gå sedan in i Unity Hub och tryck på "ADD":

![image](https://user-images.githubusercontent.com/70745846/162635153-0116602f-da5c-460f-8085-ea2b51bb2f2a.png)

Välj då mappen du nyss extraherade.

# KORRIGERING

Jag upptäckte att min kod gjorde så att bollens riktning randomiseras varje gång. För att bollen ska studsa korrekt bör koden i scriptet "BallBehaviour" ändras lite. I metoden "OnCollisionEnter2D", ta bort raden "GiveUpVelocity();" och lägg till raden "body.velocity = newDirection * body.velocity.magnitude;"

![bild](https://user-images.githubusercontent.com/70745846/162725465-1140d1c5-f750-4738-b27d-90eb515495ad.png)

