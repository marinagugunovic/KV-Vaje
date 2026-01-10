lab19
V okviru vaje sem najprej prenesla datoteke iz Git repozitorija v lokalno okolje Kali Linux z uporabo ukaza git clone.

Najprej sem preverila integriteto datoteke install.sh z uporabo SHA256 kontrolne vsote. Ukaz sha256sum -c install.sh.sha256 je potrdil, da se izračunana vrednost ujema z originalno, kar pomeni, da datoteka ni bila spremenjena.

Nato sem preverila digitalni podpis datoteke install.sh.sha256 z ukazom gpg --verify. GPG je potrdil, da je podpis prisoten, vendar preverjanje ni bilo možno, ker javni ključ podpisnika ni bil nameščen v lokalnem keyringu.

Ta rezultat pomeni, da je datoteka podpisana, vendar brez javnega ključa ni mogoče preveriti identitete avtorja. V praksi bi bilo potrebno javni ključ pridobiti po zaupanja vrednem kanalu in ga uvoziti v GPG.

Vaja prikazuje pomen preverjanja integritete in zaupanja pri prenosu skript iz interneta.
