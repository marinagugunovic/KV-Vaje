lab10
# CTF vaja na realnem primeru: HackyCorp

V tej vaji smo analizirali primer CTF (Capture The Flag) izziva na realnem primeru spletne strani HackyCorp in pripadajočih GitHub repozitorijev. Namen vaje ni bil aktivno izvajanje napadov, temveč razumevanje, kako lahko napadalci z uporabo javno dostopnih informacij odkrijejo varnostne ranljivosti in občutljive podatke.

## Odkrivanje ranljivosti iz znanih URL naslovov
Spletne aplikacije pogosto uporabljajo privzete URL poti, kot so */login* ali */admin*. Takšne poti lahko razkrijejo dodatne funkcionalnosti ali dostopne točke, ki omogočajo nadaljnje zbiranje informacij o sistemu.

## Odkrivanje ranljivosti iz javnih datotek
V predstavljenem primeru je bila javno dostopna datoteka *key.txt*, ki se je nahajala na strežniku za statične vsebine (npr. slike, CSS ali JavaScript datoteke). Takšne napake lahko privedejo do razkritja ključev ali drugih občutljivih podatkov.

## Odkrivanje ranljivosti v JavaScript datotekah
Analiza JavaScript datotek je pokazala, da lahko razvijalci v kodo pomotoma vključijo hardcodane ključe ali druge skrivne vrednosti. To predstavlja resno varnostno tveganje, saj so JavaScript datoteke javno dostopne vsakemu uporabniku.

## Odkrivanje ranljivosti na spletnem strežniku
Z uporabo orodij, kot sta *curl* in pregled datotek *robots.txt* ter *security.txt*, lahko pridobimo dodatne informacije o konfiguraciji strežnika, uporabljenih tehnologijah in morebitnih skritih poteh.

## Odkrivanje ranljivosti preko IP naslova
Neposreden dostop do IP naslova strežnika lahko v določenih primerih razkrije drugačno vsebino ali dodatne informacije, ki niso vidne prek domenskega imena.

## Odkrivanje ranljivosti v GitHub repozitorijih
Analiza GitHub repozitorijev organizacije HackyCorp je pokazala, da se občutljivi podatki pogosto nahajajo v neprivzetih vejah, zgodovini commitov ali v izbrisanih datotekah. Takšne napake so pogoste v realnih projektih.

## Odkrivanje ranljivosti v DNS zapisih
S pregledom DNS TXT zapisov in uporabo mehanizmov za sinhronizacijo DNS zapisov je mogoče pridobiti dodatne informacije, ki lahko vključujejo ključe ali notranje zapise domene.


