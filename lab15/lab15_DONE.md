lab15 
Zakaj GPG ne zazna MITM napada samodejno?
Ker GPG ne more sam preveriti, ali javni ključ res pripada pravi osebi brez dodatnega zaupanja.

Kaj je fingerprint in zakaj je pomemben?
Fingerprint je enoličen kriptografski povzetek ključa, ki omogoča zanesljivo preverjanje identitete ključa.

Zakaj e-pošta ni varen kanal za izmenjavo ključev?
Ker jo lahko prestreže napadalec in zamenja ključ.

Kako Web of Trust zmanjša tveganje MITM napada?
Z omogočanjem medsebojnega potrjevanja ključev med zaupanja vrednimi uporabniki.

izvedba ukazov: 
─(kali㉿kali)-[~]
└─$ gpg --full-generate-key

gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y
Key expires at Sat 09 Jan 2027 06:41:09 PM EST
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: alice
Email address: alice@example.com
Comment: 
You selected this USER-ID:
    "alice <alice@example.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/D0CDDB06CFFE5904FE850D0E40786F3A107B63DE.rev'
public and secret key created and signed.

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      D0CDDB06CFFE5904FE850D0E40786F3A107B63DE
uid                      alice <alice@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --full-generate-key

gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y
Key expires at Sat 09 Jan 2027 06:42:30 PM EST
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: bob
Email address: bob@example.com
Comment: 
You selected this USER-ID:
    "bob <bob@example.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/B9DAD6E72EB30845C5716D078A116D9993210AC8.rev'
public and secret key created and signed.

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      B9DAD6E72EB30845C5716D078A116D9993210AC8
uid                      bob <bob@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --full-generate-key                

gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y
Key expires at Sat 09 Jan 2027 06:43:51 PM EST
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Mallory
Email address: mallory@example.com
Comment: 
You selected this USER-ID:
    "Mallory <mallory@example.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/37E0838DA723E9B22D1505B85E8DFC031CDC6AC8.rev'
public and secret key created and signed.

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      37E0838DA723E9B22D1505B85E8DFC031CDC6AC8
uid                      Mallory <mallory@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --list-keys

gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   5  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 5u
gpg: next trustdb check due at 2027-01-09
/home/kali/.gnupg/pubring.kbx
-----------------------------
pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      247A25181D2645DC2C377A6CD55A1D98C60A3CB3
uid           [ultimate] Marina Gugunovic <marainaguugnovic21@gmail.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      441EA27E7773F84555FB454F33EDFF9F32745B94
uid           [ultimate] Peer User <peer@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      D0CDDB06CFFE5904FE850D0E40786F3A107B63DE
uid           [ultimate] alice <alice@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      B9DAD6E72EB30845C5716D078A116D9993210AC8
uid           [ultimate] bob <bob@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      37E0838DA723E9B22D1505B85E8DFC031CDC6AC8
uid           [ultimate] Mallory <mallory@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --fingerprint alice@example.com
gpg --fingerprint bob@example.com
gpg --fingerprint mallory@example.com

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      D0CD DB06 CFFE 5904 FE85  0D0E 4078 6F3A 107B 63DE
uid           [ultimate] alice <alice@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8
uid           [ultimate] bob <bob@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      37E0 838D A723 E9B2 2D15  05B8 5E8D FC03 1CDC 6AC8
uid           [ultimate] Mallory <mallory@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export mallory@example.com > bob_pubkey.asc

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --import bob_pubkey.asc

gpg: key 5E8DFC031CDC6AC8: "Mallory <mallory@example.com>" not changed
gpg: Total number processed: 1
gpg:              unchanged: 1
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ echo "Zaupno sporocilo za Boba" > secret.txt
gpg --encrypt --recipient bob@example.com secret.txt

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --decrypt secret.txt.gpg

gpg: encrypted with rsa4096 key, ID 060A5CBFBE71A41F, created 2026-01-09
      "bob <bob@example.com>"
Zaupno sporocilo za Boba
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --fingerprint bob@example.com

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8
uid           [ultimate] bob <bob@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --edit-key bob@example.com

gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Secret key is available.

sec  rsa4096/8A116D9993210AC8
     created: 2026-01-09  expires: 2027-01-09  usage: SC  
     trust: ultimate      validity: ultimate
ssb  rsa4096/060A5CBFBE71A41F
     created: 2026-01-09  expires: 2027-01-09  usage: E   
[ultimate] (1). bob <bob@example.com>

gpg> trust
5
quit

Invalid command  (try "help")

gpg> trust
sec  rsa4096/8A116D9993210AC8
     created: 2026-01-09  expires: 2027-01-09  usage: SC  
     trust: ultimate      validity: ultimate
ssb  rsa4096/060A5CBFBE71A41F
     created: 2026-01-09  expires: 2027-01-09  usage: E   
[ultimate] (1). bob <bob@example.com>

Please decide how far you trust this user to correctly verify other users' keys
(by looking at passports, checking fingerprints from different sources, etc.)

  1 = I don't know or won't say
  2 = I do NOT trust
  3 = I trust marginally
  4 = I trust fully
  5 = I trust ultimately
  m = back to the main menu

Your decision? 5
Do you really want to set this key to ultimate trust? (y/N) y

sec  rsa4096/8A116D9993210AC8
     created: 2026-01-09  expires: 2027-01-09  usage: SC  
     trust: ultimate      validity: ultimate
ssb  rsa4096/060A5CBFBE71A41F
     created: 2026-01-09  expires: 2027-01-09  usage: E   
[ultimate] (1). bob <bob@example.com>

gpg> 
gpg: signal Interrupt caught ... exiting

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --sign-key bob@example.com


sec  rsa4096/8A116D9993210AC8
     created: 2026-01-09  expires: 2027-01-09  usage: SC  
     trust: ultimate      validity: ultimate
ssb  rsa4096/060A5CBFBE71A41F
     created: 2026-01-09  expires: 2027-01-09  usage: E   
[ultimate] (1). bob <bob@example.com>


sec  rsa4096/8A116D9993210AC8
     created: 2026-01-09  expires: 2027-01-09  usage: SC  
     trust: ultimate      validity: ultimate
 Primary key fingerprint: B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8

     bob <bob@example.com>

This key is due to expire on 2027-01-09.
Are you sure that you want to sign this key with your
key "Marina Gugunovic <marainaguugnovic21@gmail.com>" (D55A1D98C60A3CB3)

Really sign? (y/N) y
gpg: signing failed: No passphrase given
gpg: signing failed: No passphrase given

Key not changed so no update needed.
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ f key you want:
f: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (1) RSA and RSA
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (2) DSA and Elgamal
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (3) DSA (sign only)
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (4) RSA (sign only)
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (9) ECC (sign and encrypt) *default*
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (10) ECC (sign only)
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (14) Existing key from card
zsh: parse error near `Existing'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Your selection? 1
Your: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ RSA keys may be between 1024 and 4096 bits long.
RSA: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ What keysize do you want? (3072) 4096
zsh: unknown file attribute: 3
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Requested keysize is 4096 bits
Requested: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Please specify how long the key should be valid.
Command 'Please' not found, did you mean:
  command 'please' from deb pleaser
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$          0 = key does not expire
0: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>  = key expires in n days
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>w = key expires in n weeks
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>m = key expires in n months
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>y = key expires in n years
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key is valid for? (0) 1y
zsh: unknown file attribute: 0
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key expires at Sat 09 Jan 2027 06:41:09 PM EST
Command 'Key' not found, did you mean:
  command 'key' from deb donkey
  command 'hey' from deb hey
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Is this correct? (y/N) y
zsh: unknown file attribute: y
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ GnuPG needs to construct a user ID to identify your key.
GnuPG: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Real name: alice
Command 'Real' not found, did you mean:
  command 'zeal' from deb zeal
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Email address: alice@example.com
Command 'Email' not found, did you mean:
  command 'wmail' from deb wmail
  command 'kmail' from deb kmail
  command 'rmail' from deb postfix
  command 'rmail' from deb courier-mta
  command 'rmail' from deb exim4-daemon-heavy
  command 'rmail' from deb exim4-daemon-light
  command 'rmail' from deb rmail
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Comment: 
Comment:: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ You selected this USER-ID:
You: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$     "alice <alice@example.com>"
alice <alice@example.com>: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
Change: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
zsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
generator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
 perform^Mszsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
d, move the mgenerator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/D0CDDB06CFFE5904FE850D0E40786F3A107B63DE.rev'
Command 'gpg:' not found, did you mean:
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg2' from deb gnupg2
  command 'gpg1' from deb gnupg1
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ public and secret key created and signed.
public: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       D0CDDB06CFFE5904FE850D0E40786F3A107B63DE
D0CDDB06CFFE5904FE850D0E40786F3A107B63DE: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid                      alice <alice@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --full-generate-key
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
zsh: missing delimiter for 'u' glob qualifier
zsh: unknown file attribute: C
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ This is free software: you are free to change and redistribute it.
This: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ There is NO WARRANTY, to the extent permitted by law.
There: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Please select what kind of key you want:
Command 'Please' not found, did you mean:
  command 'please' from deb pleaser
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (1) RSA and RSA
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (2) DSA and Elgamal
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (3) DSA (sign only)
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (4) RSA (sign only)
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (9) ECC (sign and encrypt) *default*
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (10) ECC (sign only)
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (14) Existing key from card
zsh: parse error near `Existing'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Your selection? 1
Your: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ RSA keys may be between 1024 and 4096 bits long.
RSA: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ What keysize do you want? (3072) 4096
zsh: unknown file attribute: 3
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Requested keysize is 4096 bits
Requested: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Please specify how long the key should be valid.
7-Command 'Please' not found, did you mean:
  command 'please' from deb pleaser
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$          0 = key does not expire
0: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>  = key expires in n days
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>w = key expires in n weeks
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>m = key expires in n months
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>y = key expires in n years
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key is valid for? (0) 1y
zsh: unknown file attribute: 0
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key expires at Sat 09 Jan 2027 06:42:30 PM EST
Command 'Key' not found, did you mean:
  command 'key' from deb donkey
  command 'hey' from deb hey
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Is this correct? (y/N) y
zsh: unknown file attribute: y
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ GnuPG needs to construct a user ID to identify your key.
GnuPG: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Real name: bob
Command 'Real' not found, did you mean:
  command 'zeal' from deb zeal
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Email address: bob@example.com
Command 'Email' not found, did you mean:
  command 'kmail' from deb kmail
  command 'wmail' from deb wmail
  command 'rmail' from deb postfix
  command 'rmail' from deb courier-mta
  command 'rmail' from deb exim4-daemon-heavy
  command 'rmail' from deb exim4-daemon-light
  command 'rmail' from deb rmail
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Comment: 
Comment:: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ You selected this USER-ID:
You: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$     "bob <bob@example.com>"
bob <bob@example.com>: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
Change: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
zsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
generator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
zsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
generator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/B9DAD6E72EB30845C5716D078A116D9993210AC8.rev'
Command 'gpg:' not found, did you mean:
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg1' from deb gnupg1
  command 'gpg2' from deb gnupg2
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ public and secret key created and signed.
public: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       B9DAD6E72EB30845C5716D078A116D9993210AC8
B9DAD6E72EB30845C5716D078A116D9993210AC8: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid                      bob <bob@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --full-generate-key                
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
zsh: missing delimiter for 'u' glob qualifier
zsh: unknown file attribute: C
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ This is free software: you are free to change and redistribute it.
This: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ There is NO WARRANTY, to the extent permitted by law.
rsThere: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Please select what kind of key you want:
Command 'Please' not found, did you mean:
  command 'please' from deb pleaser
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (1) RSA and RSA
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (2) DSA and Elgamal
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (3) DSA (sign only)
zsh: parse error near `DSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (4) RSA (sign only)
zsh: parse error near `RSA'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$    (9) ECC (sign and encrypt) *default*
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (10) ECC (sign only)
zsh: parse error near `ECC'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$   (14) Existing key from card
zsh: parse error near `Existing'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Your selection? 1
Your: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ RSA keys may be between 1024 and 4096 bits long.
RSA: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ What keysize do you want? (3072) 4096
zsh: unknown file attribute: 3
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Requested keysize is 4096 bits
Requested: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Please specify how long the key should be valid.
Command 'Please' not found, did you mean:
  command 'please' from deb pleaser
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$          0 = key does not expire
0: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>  = key expires in n days
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>w = key expires in n weeks
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>m = key expires in n months
zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       <n>y = key expires in n years
 zsh: no such file or directory: n
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key is valid for? (0) 1y
zsh: unknown file attribute: 0
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Key expires at Sat 09 Jan 2027 06:43:51 PM EST
Command 'Key' not found, did you mean:
  command 'key' from deb donkey
  command 'hey' from deb hey
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Is this correct? (y/N) y
zsh: unknown file attribute: y
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ GnuPG needs to construct a user ID to identify your key.
GnuPG: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Real name: Mallory
Command 'Real' not found, did you mean:
  command 'zeal' from deb zeal
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Email address: mallory@example.com
Command 'Email' not found, did you mean:
  command 'rmail' from deb postfix
  command 'rmail' from deb courier-mta
  command 'rmail' from deb exim4-daemon-heavy
  command 'rmail' from deb exim4-daemon-light
  command 'rmail' from deb rmail
  command 'kmail' from deb kmail
  command 'wmail' from deb wmail
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Comment: 
Comment:: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ You selected this USER-ID:
You: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$     "Mallory <mallory@example.com>"
Mallory <mallory@example.com>: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
Change: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
zsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
generator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ We need to generate a lot of random bytes. It is a good idea to perform
We: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ some other action (type on the keyboard, move the mouse, utilize the
> disks) during the prime generation; this gives the random number
zsh: unknown file attribute: y
Command 'this' not found, did you mean:
  command 'thin' from deb thin
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ generator a better chance to gain enough entropy.
generator: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/37E0838DA723E9B22D1505B85E8DFC031CDC6AC8.rev'
Command 'gpg:' not found, did you mean:
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg2' from deb gnupg2
  command 'gpg1' from deb gnupg1
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ public and secret key created and signed.
public: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       37E0838DA723E9B22D1505B85E8DFC031CDC6AC8
37E0838DA723E9B22D1505B85E8DFC031CDC6AC8: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid                      Mallory <mallory@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --list-keys
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: checking the trustdb
Command 'gpg:' not found, did you mean:
  command 'gpg2' from deb gnupg2
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg1' from deb gnupg1
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: marginals needed: 3  completes needed: 1  trust model: pgp
Command 'gpg:' not found, did you mean:
  command 'gpg2' from deb gnupg2
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg1' from deb gnupg1
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: depth: 0  valid:   5  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 5u
Command 'gpg:' not found, did you mean:
  command 'gpg1' from deb gnupg1
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg2' from deb gnupg2
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: next trustdb check due at 2027-01-09
Command 'gpg:' not found, did you mean:
  command 'gpg2' from deb gnupg2
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg1' from deb gnupg1
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ /home/kali/.gnupg/pubring.kbx
zsh: permission denied: /home/kali/.gnupg/pubring.kbx
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ -----------------------------
-----------------------------: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       247A25181D2645DC2C377A6CD55A1D98C60A3CB3
247A25181D2645DC2C377A6CD55A1D98C60A3CB3: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] Marina Gugunovic <marainaguugnovic21@gmail.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       441EA27E7773F84555FB454F33EDFF9F32745B94
441EA27E7773F84555FB454F33EDFF9F32745B94: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] Peer User <peer@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       D0CDDB06CFFE5904FE850D0E40786F3A107B63DE
D0CDDB06CFFE5904FE850D0E40786F3A107B63DE: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] alice <alice@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       B9DAD6E72EB30845C5716D078A116D9993210AC8
B9DAD6E72EB30845C5716D078A116D9993210AC8: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] bob <bob@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       37E0838DA723E9B22D1505B85E8DFC031CDC6AC8
37E0838DA723E9B22D1505B85E8DFC031CDC6AC8: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] Mallory <mallory@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --fingerprint alice@example.com
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --fingerprint bob@example.com
pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8
uid           [ultimate] bob <bob@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --fingerprint mallory@example.com
pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      37E0 838D A723 E9B2 2D15  05B8 5E8D FC03 1CDC 6AC8
uid           [ultimate] Mallory <mallory@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       D0CD DB06 CFFE 5904 FE85  0D0E 4078 6F3A 107B 63DE
D0CD: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] alice <alice@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8
B9DA: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] bob <bob@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       37E0 838D A723 E9B2 2D15  05B8 5E8D FC03 1CDC 6AC8
37E0: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] Mallory <mallory@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --armor --export mallory@example.com > bob_pubkey.asc
y└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --import bob_pubkey.asc
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: key 5E8DFC031CDC6AC8: "Mallory <mallory@example.com>" not changed
Command 'gpg:' not found, did you mean:
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg2' from deb gnupg2
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg1' from deb gnupg1
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: Total number processed: 1
Command 'gpg:' not found, did you mean:
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpg1' from deb gnupg1
  command 'gpg2' from deb gnupg2
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg:              unchanged: 1
Command 'gpg:' not found, did you mean:
  command 'gpg2' from deb gnupg2
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg1' from deb gnupg1
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ echo "Zaupno sporocilo za Boba" > secret.txt
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --encrypt --recipient bob@example.com secret.txt
File 'secret.txt.gpg' exists. Overwrite? (y/N) 
Enter new filename:                                                                                                                                                                                                                   
gpg: secret.txt: encryption failed: File exists
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --decrypt secret.txt.gpg
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: encrypted with rsa4096 key, ID 060A5CBFBE71A41F, created 2026-01-09
Command 'gpg:' not found, did you mean:
  command 'gpg1' from deb gnupg1
  command 'gpg2' from deb gnupg2
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       "bob <bob@example.com>"
bob <bob@example.com>: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Zaupno sporocilo za Boba
Zaupno: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --fingerprint bob@example.com
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$       B9DA D6E7 2EB3 0845 C571  6D07 8A11 6D99 9321 0AC8
B9DA: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ uid           [ultimate] bob <bob@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]
zsh: bad pattern: [expires:
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --edit-key bob@example.com
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
zsh: missing delimiter for 'u' glob qualifier
zsh: unknown file attribute: C
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ This is free software: you are free to change and redistribute it.
This: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ There is NO WARRANTY, to the extent permitted by law.
There: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ Secret key is available.
Secret: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sec  rsa4096/8A116D9993210AC8
Command 'sec' not found, but can be installed with:
sudo apt install sec
Do you want to install it? (N/y)                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sage: SC  
sage:: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$      trust: ultimate      validity: ultimate
Command 'trust:' not found, did you mean:
  command 'trust' from deb p11-kit
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ssb  rsa4096/060A5CBFBE71A41F
Command 'ssb' not found, did you mean:
  command 'msb' from deb mysql-sandbox
  command 'ssu' from deb unifrac-tools
  command 'stb' from deb python3-sphinx-theme-builder
  command 'ssr' from deb soundscaperenderer-common
  command 'ss2' from deb python3-pyroute2
  command 'ssh' from deb openssh-client
  command 'sb' from deb lrzsz
  command 'ss' from deb iproute2
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$      created: 2026-01-09  expires: 2027-01-09  usage: E   
Command 'created:' not found, did you mean:
  command 'createdb' from deb postgresql-client-common
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ [ultimate] (1). bob <bob@example.com>
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg> 
zsh: parse error near `\n'
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg: signal Interrupt caught ... exiting
Command 'gpg:' not found, did you mean:
  command 'gpg2' from deb gnupg2
  command 'gpg1' from deb gnupg1
  command 'gpgv' from deb gpgv
  command 'gpgv' from deb gpgv-from-sq
  command 'gpg' from deb gpg
  command 'gpg' from deb gpg-from-sq
Try: sudo apt install <deb name>
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$                                                                                                                                                                                                                   
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ └─$ gpg --sign-key bob@example.com
└─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sec  rsa4096/8A116D9993210AC8
Command 'sec' not found, but can be installed with:
sudo apt install sec
Do you want to install it? (N/y)                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ─$ 
─$: command not found
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ 
