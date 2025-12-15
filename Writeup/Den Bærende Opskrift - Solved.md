```
I år har vi fået den bærende opskrift fra Julemor. Det
bliver 2025 julemaden. Men gemmer opskriften på en
hemmelig besked?
```
Opgave: [warmup_den_baerende_opskrift.zip](https://github.com/user-attachments/files/24165874/warmup_den_baerende_opskrift.zip)

I opgaven får man et billede. Her tænker jeg med det samme at man skulle tjekke "Detaljer" og kunne her finde en kommentar på billedet med teksten: 
```
QlpoOTFBWSZTWUv3JjYAAC9fgYAQQIUIAAoBCQC//98qAwAAQD
ABG2zbDTUk9NR+k1MmaDSepoyekDUzKm0UGmj1BkADQNT0EkYC
ek9BAA9JiXHNWB2RIeGcIocFgaUkU9PVFUQMUR7WCl53HY0oUB
VBgXGERAZg718LqwL7d2GDZtmfeWq+tZ7i3cHBl7EE82dxT7TK
0kNGhuHMoq03x4MOj3OL7m8MKUrqsmgzEctDnwrti5TaALVmwS
GGGGUaEgGF2k1VUS5ZIHfEwJyBvIYXsHDKQdRNNeSvCSgcWQxf
lVSF7jhPWZZNKSnRWMBgLGhVNE8RZC6XhIKBIiNScPoKzYqpqm
bx+6iA52aBhOpAu2vlwJ1fecbkj/F3JFOFCQS/cmNg
```
Jeg smed dette ind i [Cyberchef](https://gchq.github.io/CyberChef/) og den forslog at det kunne være Base64 kode. Efter den decoded det, kommer der en ny underlig tekst frem. Her finder Cyberchef ud at det er en Bzip2 fil.

Hvis man decompresser Bzip2 teksten får man denne tekst:

```
Sue resbe

E resbe kåches i vånn tesat 
peffe, solt å et laubæblai te 
di æ nok. Væn di e kåcht blyvve
di skåe i passen stygge å loi i
a fa. E spai e resbe æ kåcht i 
smaches te mæ erk, solt å peffe
å tesættes husblais te de blyvve
styvt væn de æ helt øvve e resbe.
Sue resbe kån spises oe e
råvbrøe mæ let semp, men
smache å gåt te obstuft ka'tøfle.
NC3{Surrib_er_bedst_på_sønderjydsk}
```

Flag: `NC3{Surrib_er_bedst_på_sønderjydsk}`

<img width="2317" height="1133" alt="image" src="https://github.com/user-attachments/assets/c3986ebd-436f-4380-bfd3-de3361b0ac43" />
