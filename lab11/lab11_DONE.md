lab11
V tej vaji sem reševala začetne stopnje igre Bandit (OverTheWire), kjer je cilj pridobiti geslo za naslednjo stopnjo z uporabo osnovnih Linux ukazov in razumevanja dela z datotekami.

Za dostop do posameznih stopenj sem uporabljala SSH povezavo do strežnika bandit.labs.overthewire.org na portu 2220. Pri reševanju nalog sem uporabila ukaze, kot so ls, cat, find, grep, sort, uniq, strings, base64 in tr.

Posebej pri Level 11 sem uporabila ukaz tr za dešifriranje besedila, ki je bilo kodirano z ROT13 (zamenjava črk v abecedi). Ukaz je bil:

tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt


S tem sem uspešno pridobila geslo za naslednjo stopnjo.

Vaja mi je pomagala utrditi razumevanje osnovnih Linux ukazov, obdelave besedila in preprostih metod kodiranja.