Beskrivelse:
```
Vigtignissen er på spil igen, han har en teori om at
kryptering er unødvendigt, så længe man encoder godt
nok - og så behøver man ikke engang besværet med
nøgler: win-win.
```
Opgave: [warmup_ace0fbase.zip](https://github.com/user-attachments/files/24165717/warmup_ace0fbase.zip)

I opgaven får man en kæmpe streng kode, og et hint i både titlen og i beskrivelsen: ```så længe man encoder godt nok```. <br />
Her tænkte jeg med det samme at det måtte være Base encoded, og være gjort mange gange. <br />

Hvis man smider teksten ind i [Cyberchef](https://gchq.github.io/CyberChef/), og sætter modulet **From Base64** ind, ser det ud som om at der ikke er sker noget med koden.
Men hov! I opgaven står der jo ```så længe man encoder godt nok``` så jeg her mistænker at teksten bare er encoded mange gange med den samme encoding. (Base64)

<img width="2318" height="1273" alt="image" src="https://github.com/user-attachments/assets/89100b99-9fba-4654-9f11-26fc81afa588" />

Hvis man decoder teksten 21 gange i alt får man en underlig streng af kinesiske tegn og et enkelt egyptisk hieroglyf: <br />
```硎𠄳腡扬𓁵洭橀戳扒核敬籮氭戰杕𠌡```

Hvis man dog kender til Base65536 encoding, kan man smide det ind i en online Base65536 decoder (her kan Cyberchef være med)

Flag: ```NC3{aLl-ur-8@53-R-83l0nG-70-U2!}```

<img width="801" height="629" alt="image" src="https://github.com/user-attachments/assets/bc612340-92d1-4221-855f-e13faa406b33" />

**OBS: Det er også muligt at lave et python script til at decode i Base65536, men jeg var lidt for doven til at gøre det... 😅**
