lab17 
1. Uvod in cilji vaje

Cilj te vaje je bil analizirati najpogostejše varnostne grožnje in ranljivosti spletnih aplikacij v kontekstu elektronskega poslovanja. Poseben poudarek je bil namenjen razumevanju OWASP Top 10 ranljivosti ter njihovemu vplivu na varnost podatkov, uporabnikov in poslovnih procesov.

Vaja je bila izvedena z uporabo spletnega orodja HostedScan OWASP Vulnerability Scan, ki omogoča osnovni pregled varnosti spletnih aplikacij in identifikacijo tipičnih varnostnih pomanjkljivosti.

2. Opis aktivnosti in uporabljeno orodje

Za pregled spletne aplikacije je bila uporabljena spletna storitev HostedScan OWASP Vulnerability Scan, namenjena izobraževalnim in testnim namenom. Pregled je bil izveden na testni (demo) e-poslovni spletni strani, kar je skladno z etičnimi in pravnimi smernicami.

Postopek:

vnos URL testne spletne strani,

zagon avtomatskega varnostnega pregleda,

analiza zaznanih ranljivosti na podlagi OWASP Top 10 (2021).

3. Zaznane varnostne ranljivosti

Na podlagi pregleda so bile identificirane naslednje ranljivosti:

3.1 Broken Access Control

Stopnja tveganja: Visoka

Opis:
Zaznana je bila možnost neustreznega nadzora dostopa, kjer bi lahko nepooblaščen uporabnik dostopal do funkcionalnosti ali podatkov, ki niso namenjeni njegovi vlogi.

Zakaj je nevarna:
Napadalec lahko pridobi dostop do administrativnih funkcij ali občutljivih podatkov, kar lahko vodi v krajo podatkov ali zlorabo sistema.

Priporočeni ukrepi:

dosleden nadzor dostopa na strežniški strani,

uporaba načela najmanjših pravic (least privilege),

redno testiranje dostopnih pravic.

3.2 Security Misconfiguration

Stopnja tveganja: Srednja

Opis:
Zaznane so bile pomanjkljive varnostne nastavitve strežnika ali aplikacije (npr. privzete nastavitve, razkritje informacij v HTTP odzivih).

Zakaj je nevarna:
Neustrezne nastavitve lahko napadalcu olajšajo nadaljnje napade ali razkrivajo informacije o arhitekturi sistema.

Priporočeni ukrepi:

odstranitev privzetih nastavitev,

redno pregledovanje konfiguracij,

uporaba varnostnih smernic (hardening).

3.3 Vulnerable and Outdated Components

Stopnja tveganja: Srednja

Opis:
Uporaba zastarelih programskih komponent ali knjižnic, ki vsebujejo znane ranljivosti.

Zakaj je nevarna:
Napadalci lahko izkoristijo javno znane ranljivosti brez posebnega tehničnega znanja.

Priporočeni ukrepi:

redno posodabljanje komponent,

spremljanje varnostnih obvestil (CVE),

uporaba preverjenih in vzdrževanih knjižnic.

4. Povezava z OWASP Top 10

Pri pregledu so bile prepoznane naslednje ranljivosti iz OWASP Top 10 (2021):

Broken Access Control

Security Misconfiguration

Vulnerable and Outdated Components

Te ranljivosti so med najpogostejšimi v e-poslovanju, saj spletne trgovine pogosto obdelujejo osebne in plačilne podatke uporabnikov.

5. Priporočila za izboljšanje varnosti

Na podlagi ugotovitev se priporoča:

uvedba rednih varnostnih pregledov spletnih aplikacij,

dosledno upravljanje dostopov in uporabniških vlog,

redno posodabljanje programske opreme,

uporaba varnostnih standardov (OWASP, ISO/IEC 27001),

ozaveščanje razvijalcev o varnostnem razvoju aplikacij.

6. Refleksija

Rezultati pregleda niso bili presenetljivi, saj se podobne ranljivosti pogosto pojavljajo pri spletnih aplikacijah, še posebej v e-poslovanju. Vaja je jasno pokazala, kako hitro lahko osnovni avtomatski pregled razkrije resne varnostne pomanjkljivosti, če varnost ni vključena že v fazi načrtovanja sistema.

7. Zaključek

Vaja je omogočila boljše razumevanje varnostnih groženj spletnih aplikacij in pomena standardov, kot je OWASP Top 10. Pridobljeno znanje je neposredno uporabno pri načrtovanju, razvoju in ocenjevanju varnosti e-poslovnih sistemov.s