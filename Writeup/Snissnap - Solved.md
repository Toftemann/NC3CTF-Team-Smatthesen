Beskrivelse:
```
I 2025 er det slut med at sende breve. Post Nordpolen kan
ikke klare det mere. De opfordrer til at bruge deres nye
app Snissnap med ny ekstrem nissesikker kryptering. Så
kan man snissnappe en besked og sende til Julemanden.

De interne alarmer gik på denne loggede besked. Hvorfor
dog det? Er alle børn ikke artige når de skriver til
julemanden?
```

[warmup_snissnap.zip](https://github.com/user-attachments/files/24168931/warmup_snissnap.zip)

Denne opgave var lidt mere kryptisk for mig at løse, men jeg kom tilfældigvis frem til en løsning alligevel.

I opgaven får du et tekst dokument, hvor der står en encoded streng. Hvis man smider den ind i [Cyberchef](https://gchq.github.io/), forslår den at det kan være en Base64 encoded streng.

Hvis man decoder den i Base64 får man noget HEX kode frem. Hvis man så oversætter den HEX kode får man noget ikke læseligt frem. Hmm...
<img width="2318" height="1271" alt="image" src="https://github.com/user-attachments/assets/2af1f3d3-d1e8-4acc-996c-c70da005579b" />

Jeg prøvede mig frem med lidt forskellige oversættelser fra HEX, uden held. Det var altså noget tekst. <br />
I output boksen på CyberChef hjemmesiden, kan man vælge hvordan man gerne vil have sit output skudt ud.

Som standard finder Cyberchef selv ud af, hvilken format det er skrevet i, men ikke denne gang, så her prøvede jeg <br />
for sjov at ændre output texten fra *Raw Bytes* til at være UTF-8 og UTF-7. Stadig samme resultat...

Ændrer man output til at vise UTF-16LE, så får man noget "læseligt" tekst frem i kyrilliske tegn.

<img width="2316" height="1274" alt="image" src="https://github.com/user-attachments/assets/3ce34363-44df-445e-9518-738289bd10b8" />

Det jeg var mest interesseret i var teksten ```НC3{юл_мэд_кыриллиск}```, da det kunne ligne formatet af det flag man skal finde.
Hvis man googler "kyrillisk til dansk", kan man finde et alfabet på [Sprognet.dk - Transskription af russisk](https://sproget.dk/sprogviden/ordlister/transskription-af-russisk/), og tager et tegn af gangen kommer man frem til dette resultat:
Н C 3 { ю  л _ м э д _ к ы р и л л и с к } <br />
N C 3 { ju l _ m e d _ k y r i l l i s k }

Dog er det første "C" et "S" i det kyrilliske alfabet, men der tænkte jeg at det nok ikke skulle oversættes.

Flag: NC3{jul_med_kyrillisk}
