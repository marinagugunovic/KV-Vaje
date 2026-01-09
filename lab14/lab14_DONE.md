lab14
dokaz o izvedenih ukazih:

┌──(kali㉿kali)-[~]
└─$ sudo apt update
sudo apt install gnupg

[sudo] password for kali: 
Hit:1 http://http.kali.org/kali kali-rolling InRelease
1541 packages can be upgraded. Run 'apt list --upgradable' to see them.
Upgrading:                      
  dirmngr  gnupg  gnupg-l10n  gnupg-utils  gpg  gpg-agent  gpg-wks-client  gpgconf  gpgsm  gpgv

Summary:
  Upgrading: 10, Installing: 0, Removing: 0, Not Upgrading: 1531
  Download size: 3,423 kB
  Space needed: 0 B / 63.2 GB available

Continue? [Y/n] y
Get:2 http://mirror1.sox.rs/kali/kali kali-rolling/main amd64 dirmngr amd64 2.4.8-5 [386 kB]
Get:1 http://kali.download/kali kali-rolling/main amd64 gpg-wks-client amd64 2.4.8-5 [110 kB]
Get:4 http://kali.download/kali kali-rolling/main amd64 gpg-agent amd64 2.4.8-5 [273 kB]
Get:5 http://kali.download/kali kali-rolling/main amd64 gpg amd64 2.4.8-5 [639 kB]
Get:3 http://mirror1.sox.rs/kali/kali kali-rolling/main amd64 gnupg-utils amd64 2.4.8-5 [195 kB]
Get:6 http://kali.download/kali kali-rolling/main amd64 gpgconf amd64 2.4.8-5 [129 kB]
Get:7 http://kali.download/kali kali-rolling/main amd64 gnupg all 2.4.8-5 [418 kB]
Get:8 http://kali.download/kali kali-rolling/main amd64 gpgsm amd64 2.4.8-5 [278 kB]
Get:9 http://kali.download/kali kali-rolling/main amd64 gnupg-l10n all 2.4.8-5 [752 kB]
Get:10 http://kali.download/kali kali-rolling/main amd64 gpgv amd64 2.4.8-5 [244 kB]
Fetched 3,423 kB in 5s (635 kB/s)
(Reading database ... 417429 files and directories currently installed.)
Preparing to unpack .../0-gpg-wks-client_2.4.8-5_amd64.deb ...
Unpacking gpg-wks-client (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../1-dirmngr_2.4.8-5_amd64.deb ...
Unpacking dirmngr (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../2-gnupg-utils_2.4.8-5_amd64.deb ...
Unpacking gnupg-utils (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../3-gpg-agent_2.4.8-5_amd64.deb ...
Unpacking gpg-agent (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../4-gpg_2.4.8-5_amd64.deb ...
Unpacking gpg (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../5-gpgconf_2.4.8-5_amd64.deb ...
Unpacking gpgconf (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../6-gnupg_2.4.8-5_all.deb ...
Unpacking gnupg (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../7-gpgsm_2.4.8-5_amd64.deb ...
Unpacking gpgsm (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../8-gnupg-l10n_2.4.8-5_all.deb ...
Unpacking gnupg-l10n (2.4.8-5) over (2.4.8-3) ...
Preparing to unpack .../9-gpgv_2.4.8-5_amd64.deb ...
Unpacking gpgv (2.4.8-5) over (2.4.8-3) ...
Setting up gnupg-l10n (2.4.8-5) ...
Setting up gpgv (2.4.8-5) ...
Setting up gpgconf (2.4.8-5) ...
Setting up gpg (2.4.8-5) ...
Setting up gnupg-utils (2.4.8-5) ...
Setting up gpg-agent (2.4.8-5) ...
Setting up gpgsm (2.4.8-5) ...
Setting up dirmngr (2.4.8-5) ...
Setting up gnupg (2.4.8-5) ...
Setting up gpg-wks-client (2.4.8-5) ...
Processing triggers for kali-menu (2025.3.2) ...
Processing triggers for man-db (2.13.1-1) ...
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --full-generate-key
gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

gpg: keybox '/home/kali/.gnupg/pubring.kbx' created
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
Key expires at Sat 09 Jan 2027 03:54:20 PM EST
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Marina Gugunovic
Email address: marainaguugnovic21@gmail.com
Comment: 
You selected this USER-ID:
    "Marina Gugunovic <marainaguugnovic21@gmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: /home/kali/.gnupg/trustdb.gpg: trustdb created
gpg: directory '/home/kali/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/247A25181D2645DC2C377A6CD55A1D98C60A3CB3.rev'
public and secret key created and signed.

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      247A25181D2645DC2C377A6CD55A1D98C60A3CB3
uid                      Marina Gugunovic <marainaguugnovic21@gmail.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --list-keys

gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
gpg: next trustdb check due at 2027-01-09
/home/kali/.gnupg/pubring.kbx
-----------------------------
pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      247A25181D2645DC2C377A6CD55A1D98C60A3CB3
uid           [ultimate] Marina Gugunovic <marainaguugnovic21@gmail.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export marina.gugunovic@student.si > marina_pubkey.asc
gpg: WARNING: nothing exported
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export "Marina Gugunovic" > marina_pubkey.asc
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export marina.gugunovic21@gmail.com > marina_pubkey.asc
gpg: WARNING: nothing exported
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export "Marina Gugunovic" > marina_pubkey.asc          
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls -l marina_pubkey.asc

-rw-rw-r-- 1 kali kali 3167 Jan  9 15:59 marina_pubkey.asc
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ cat marina_pubkey.asc

-----BEGIN PGP PUBLIC KEY BLOCK-----

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
TveHIhpULdTUvHrKKgK5jPXbIjdYDzg=
=6nN4
-----END PGP PUBLIC KEY BLOCK-----
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls

Desktop  Documents  Downloads  gists.txt  index.html  marina_pubkey.asc  Music  Pictures  Public  sherlock  Templates  test.txt  Videos
                                                                                                                                                                                                                  
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
Key expires at Sat 09 Jan 2027 04:01:47 PM EST
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Peer User
Email address: peer@example.com
Comment: 
You selected this USER-ID:
    "Peer User <peer@example.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: revocation certificate stored as '/home/kali/.gnupg/openpgp-revocs.d/441EA27E7773F84555FB454F33EDFF9F32745B94.rev'
public and secret key created and signed.

pub   rsa4096 2026-01-09 [SC] [expires: 2027-01-09]
      441EA27E7773F84555FB454F33EDFF9F32745B94
uid                      Peer User <peer@example.com>
sub   rsa4096 2026-01-09 [E] [expires: 2027-01-09]

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --armor --export peer@example.com > peer_pubkey.asc

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --import peer_pubkey.asc
gpg --list-keys

gpg: key 33EDFF9F32745B94: "Peer User <peer@example.com>" not changed
gpg: Total number processed: 1
gpg:              unchanged: 1
gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   2  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 2u
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

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ echo "To: peer@example.com
From: marina.gugunovic@student.si
Date: $(date)
Secret message: Zaupno sporocilo" > message.txt

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ cat message.txt           

To: peer@example.com
From: marina.gugunovic@student.si
Date: Fri Jan  9 04:04:32 PM EST 2026
Secret message: Zaupno sporocilo
                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --encrypt --sign --armor --recipient peer@example.com message.txt

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --encrypt --sign --armor --recipient peer@example.com message.txt

File 'message.txt.asc' exists. Overwrite? (y/N) n
Enter new filename: 
gpg: signal Interrupt caught ... exiting

                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ gpg --decrypt message.txt.asc > decrypted_message.txt
cat decrypted_message.txt

gpg: encrypted with rsa4096 key, ID 9C7D96974844969C, created 2026-01-09
      "Peer User <peer@example.com>"
gpg: Signature made Fri 09 Jan 2026 04:05:20 PM EST
gpg:                using RSA key 247A25181D2645DC2C377A6CD55A1D98C60A3CB3
gpg: Good signature from "Marina Gugunovic <marainaguugnovic21@gmail.com>" [ultimate]
To: peer@example.com
From: marina.gugunovic@student.si
Date: Fri Jan  9 04:04:32 PM EST 2026
Secret message: Zaupno sporocilo

Zaradi tehničnih omejitev (izpraznjena baterija prenosnega računalnika) zaslonski posnetki niso bili shranjeni. Izvedba vaje je razvidna iz izpisov ukazov in rezultatov, ki so vključeni v poročilo.

odgovori na vprasanja:

Razlika šifriranje vs potpis:
Šifriranje štiti zaupnost (samo primatelj može pročitati). Potpis štiti integritet i avtentičnost (dokazuje ko je poslao i da nije mijenjano).

Uloga javnog i privatnog ključa:
Javni ključ se dijeli i koristi za šifriranje prema tebi / provjeru potpisa. Privatni ključ čuvaš tajno i koristiš za dešifriranje i potpisivanje.

Šta se desi ako se šifrirani fajl promijeni:
Dešifriranje/potpis provjera neće proći (GPG će javiti da potpis nije validan / integritet narušen).
