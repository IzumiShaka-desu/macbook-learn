# Overview
jadi signing github commt=it gunanya biar saat kita commit, commit kita terdeteksi verified oleh github.
- contoh verified - unverified commit
![contoh verified - unverified commit](https://github.com/IzumiShaka-desu/macbook-learn/raw/main/verified%20-%20unverified.png)

## step
### step 1 install required software
```bash
brew install gpg2 gnupg pinentry-mac
```
### step 2 make ./gnu directory
jika folder ./gnu tidak tersedia maka buat foldernya
```bash
mkdir ~/.gnupg
```
### step 3 set gpg config
```bash
echo 'use-agent' > ~/.gnupg/gpg.conf
```
### step 4 update folder permis
```bash
chmod 700 ~/.gnupg
```
### step 5 create key
```bash
akashaka@Akashakas-MacBook-Pro ~ % gpg --full-gen-key
gpg (GnuPG) 2.3.4; Copyright (C) 2021 Free Software Foundation, Inc.
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
Your selection? 4
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 5y
Key expires at Sun Dec 20 21:11:57 2026 WIB
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Sesaka Aji Nursah Bantani
Email address: shakaaji29@gmail.com
Comment: IzumiShaka-desu
You selected this USER-ID:
    "Sesaka Aji Nursah Bantani (IzumiShaka-desu) <shakaaji29@gmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
```
### check list key
```bash
gpg -k
```
### export key
```bash
gpg --armor --export <insert your key id>
```
### add to github 
go to https://github.com/settings/gpg/new
paste your exported key,
its start with ``` -----BEGIN PGP PUBLIC KEY BLOCK----- ``` 
and ended with ``` -----END PGP PUBLIC KEY BLOCK----- ```
### configure your git
```
git config --global gpg.program "$(which gpg)";
git config --global commit.gpgsign true                         
git config --global user.signingkey <insert your key id>
```
### try commit your project
if error appear,try :
```
killall gpg-agent  
```

good luck!, cheers.

