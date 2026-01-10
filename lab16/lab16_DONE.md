lab16 
Zakaj skrivnosti ne sodijo v izvorno kodo?
Ker lahko ob uhajanju kode pride do zlorabe dostopov in resnih varnostnih incidentov.

Razlika med simetričnim in asimetričnim šifriranjem:
Simetrično šifriranje uporablja skupno geslo, asimetrično pa par javnega in zasebnega ključa.

Kaj se zgodi ob izgubi zasebnega ključa?
Dostop do šifriranih skrivnosti ni več mogoč.

Rešitev v večjem podjetju:
Uporaba specializiranih orodij za upravljanje skrivnosti (npr. HashiCorp Vault, AWS Secrets Manager).

izvedba ukazov: 
──(kali㉿kali)-[~]
└─$ ^[[200~echo "API_KEY=super-secret-key-123
dquote> DB_PASSWORD=VeryStrongPassword" > secrets.env
zsh: bad pattern: ^[[200~echo
                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ cat secrets.env                                                                                                                          

cat: secrets.env: No such file or directory
                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ echo "API_KEY=super-secret-key-123
DB_PASSWORD=VeryStrongPassword" > secrets.env

                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ cat secrets.env                  

API_KEY=super-secret-key-123
DB_PASSWORD=VeryStrongPassword
                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ gpg -c secrets.env                                  

                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ rm secrets.env

                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ ls                                                                          
bob_pubkey.asc         Desktop    Downloads  index.html         message.txt      Music            Pictures  revoke.asc       secret.txt      sherlock   test.txt
decrypted_message.txt  Documents  gists.txt  marina_pubkey.asc  message.txt.asc  peer_pubkey.asc  Public    secrets.env.gpg  secret.txt.gpg  Templates  Videos
                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~]
└─$ gpg -d secrets.env.gpg
gpg: AES256.CFB encrypted data
gpg: encrypted with 1 passphrase
API_KEY=super-secret-key-123
DB_PASSWORD=VeryStrongPassword

