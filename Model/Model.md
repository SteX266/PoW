
# Bitcoin model

Ovaj deo rada posvećen je dekompoziciji *Bitcoina*, pioniru kripto valuta. Analizom bitcoina i njegovih ključnih komponenti, možemo dublje razumeti osnovne principe koji stoje iza većine kriptovaluta zasnovanih na *Proof of Work*(PoW) principu.

Bitkoini, ne postoje u fizičkom smislu, niti vlasnici bitkoina imaju "račun". Umesto toga, postoji *blockchain*, koji predstavlja zapis svih transakcija koje su ikada obavljene između bitkoin adresa[1]. *Blockchain* predstavlja niz ulančanih blokova koji sadrže niz transakcija. U nastavku je svaki od ovih pojmova objašnjen sa više detalja.

### Transakcija

Transakcije predstavljaju osnovnu jedinicu u *blockchain-u*, omogućavajući prenos bitcoina između različitih korisnika sistema. Svaka transakcija ima svoje specifičnosti i sastoji se od ključnih elemenata:

Input(s) - Reference na prethodne transakcije pošiljaoca
Outputs - Postoje 2 outputa, jedan je količina bitkoina koja se šalje primaocu, kao i adresa primaoca, a drugi je količina "kusura" koji se vraća pošiljaocu. Količina drugog outputa se računa tako što se sabere zbir svih input transakcija i oduzme količina prvog outputa.

Pošiljalac transakcije potpisuje transakciju digitalnim potpisom koristeći privatni ključ vezan za svoju bitkoin adresu (javni ključ). Nakon toga, transakcija se šalje svim čvorovima u mreži i završava u mempool-u, odakle svaki čvor skuplja transakcije i pakuje ih u blokove [2].


### Blokovi

Blok predstavlja kolekciju transakcija. Svaki blok sadrži informacije o transakcijama, vremenske pečate (eng. *time stamps*), jedinstveni identifikator(heš). Struktura bloka omogućava stvaranje neprekidnog lanca koji se proširuje unazad do prvog bloka, poznatog kao "*genesis*" blok [3].

Heš prethodnog bloka - Svaki blok sadrži referencu na prethodni blok
Timestamp - Tačno vreme kada je blok kreiran
Nonce - Broj koji "rudari" rešiti kako bi verifikovali blok



[How do Bitcoin transactions work?] (https://www.bitcoin.com/get-started/how-bitcoin-transactions-work/)
[Bitcoin: A Peer-to-Peer Electronic Cash System] (https://bitcoin.org/bitcoin.pdf)
[Genesis block] (https://en.bitcoin.it/wiki/Genesis_block)