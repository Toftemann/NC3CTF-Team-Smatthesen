Beskrivelse:
```
Vigtignissen er på spil igen, han har en teori om at
kryptering er unødvendigt, så længe man encoder godt
nok - og så behøver man ikke engang besværet med
nøgler: win-win.
```

I opgaven får man en kæmpe streng kode, og et hint: ```så længe man encoder godt nok```. Her tænkte jeg med det samme at det måtte være encoded mange gange med en Base encoder. <br />

Hvis man smider teksten ind i [Cyberchef](https://gchq.github.io/CyberChef/), og sætter modulet **From Base64** ind, ser det ud som om at der ikke er sker noget med koden.
Men hov! I opgaven står der jo ```så længe man encoder godt nok``` så jeg her mistænker at teksten bare er encoded mange gange med den samme encoding. (Base64)

Hvis man decoder teksten 21 gange i alt får man en underlig streng af kinesiske tegn og et enkelt egyptisk hieroglyf: <br />
```硎𠄳腡扬𓁵洭橀戳扒核敬籮氭戰杕𠌡```

Hvis man dog kender til Base65536 encoding, kan man smide det ind i en online Base65536 decoder (her kan Cyberchef være med) og få flaget: ```NC3{aLl-ur-8@53-R-83l0nG-70-U2!}```

OBS: Det er også muligt at lave et python script til at decode i Base65536, men jeg var lidt for doven til at gøre det...
