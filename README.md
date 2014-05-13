# Git ja GitHub

Markus Jylhänkangas

Tieto- ja viestintätekniikan perustutkinto, Datanomi 

Tornio, 2014



-----------------
#### Sisältö

- [Mikä on Git?](#mikä-on-git)
	- [Asennus](#asennus)

- [Mikä on GitHub?](#mikä-on-github)
	- [Profiilin luominen](#profiilin-luominen)
	- [Repon luominen](#repon-luominen)

- [GiHub Pages](#github-pages)
	- [Oman domainin käyttö](#oman-domainin-käyttö)

-[Projektin "Fork":aaminen](#projektin-forkaaminen)
-[Pull Requestin lähettäminen](#pull-requestin-lähettäminen)

- [Lähteet](#lähteet)

------------

# Mikä on Git?
Git on versionhallintaohjelmisto joka toimii hajautetusti. Linus Torvalds kirjoitti Git:in vuonna 2005, koska Linux-ytimen kehittäjätiimin tarpeita täyttävää versionhallintaohjelmistoa ei ollut olemassa. "Git" tarkoittaa iso-britannialaisessa slangissa "ääliötä".

>"I'm an egotistical bastard, and I name all my projects after myself. First Linux, now git."
-Linus Torvalds

Git:in nykyinen ylläpitäjä on Junio Hamano

## Asennus
Windowsille ja Mac:ille on olemassa monia [graaffisia sovelluksia](http://git-scm.com/downloads/guis), mutta GitHubin käyttöön suosittelen [GitHub for Windows](http://windows.github.com):ia tai [GitHub for Mac](http://mac.github.com):iä. Linuxilla voit asentaa Git:in käyttämällä jakelusi paketin hallintaa.

#### Debian/Ubuntu
```bash
$ apt-get install git
```
#### Fedora
```bash
$ yum install git
```
#### Gentoo
```bash
$ emerge --ask --verbose dev-vcs/git
```
#### Arch Linux
```bash
$ pacman -S git
```
#### FreeBSD
```bash
$ cd /usr/ports/devel/git
$ make install
```
#### Solaris 11 Express
```bash
$ pkg install developer/versioning/git
```
#### OpenBSD
```bash
$ pkg_add git
```

Jos käytät Git shelliä (komentorivi ohjelmaa) sinun pitää määritellä käyttäjä nimesi. Tämä kannattaa tehdä vasta sen jälkeen kun olet tehnyt GitHub profiilin.

##### Käyttäjänimi
```bash
$ git config --global user.name "Tähän käyttäjänimesi"
```

##### Sähköposti
```bash
$ git config --global user.email "your_email@example.com"
```

##### Salasanan tallentaminen välimuistiin
Tämä on hyvä tehdä jotta sinun ei tarvitse joka kerta kirjoittaa käyttäjänimeä ja salasanaa kun otat yhteyttä palvelimeen
```bash
$ git config --global credential.helper cache
```
Vakiona Git tallentaa salasanan 15 minuutiksi, mutta tätä voi muuttaa:
```bash
$ git config --global credential.helper 'cache --timeout=3600'
# Muutta tallennus ajaksi 1 tunti
```
# Mikä on Github?


## Profiilin luominen
Profiilin luominen on todella yksinkertaista:

1. Avaa [GitHub](http://github.com) selaimellasi. Heti etusivulla sinua kohtaa rekisteröinti lomake jossa pyydetään käyttäjänimi, sähköposti ja salasana.
2. Seuraavassa kohdassa voit valita suunnitelmasi ("plan"). Jos ajattelit aloittaa yksityisiä projekteja/repoja nämä maksavat ~5€/kk ylöspäin, voit myös perustaa organisaatiotilin. Yksityisiä repoja ja organisaatiotilejä voit ostaa/tehdä rekisteröinnin jälkeenkin.
3. Ja kuin taikuutta, profiilisi on valmis!


## Repon luominen
Repo (repository) on kansio missä on kaikki projektisi tiedostot, koodi, dokumentaatio yms. (dokumentaatioon voit myös käyttää wikiä, lisää siitä myöhempänä). Repon voit luoda kahdella tavalla joko painamalla oikealla olevaa vihreää "New repository" nappulaa tai painamalla sivun ylälaidassa käyttäjänimesi oikealla puolella olevaa "+" nappulaa ja valitsemalla "New repository".

Seuraavaksi sinulta kysytään reposi nimeä, kuvausta, haluatko siitä julkisen vai yksityisen, tekeekö Github README tiedostoa (on suositeltavaa että valitset tämän), haluatko .gitignore tiedostoa, ja minkä lisenssin haluat.
Jos haluat että ihmiset voivat vapaasti käyttää koodiasi suosittelen valitsemaan MIT lisenssin, se on lyhyt, yksinkertainen ja antaa paljon vapauksia. [Tämä](http://choosealicense.com/) sivusto auttaa lisenssin valitsemisessa.
[.gitignore](https://github.com/github/gitignore) on tiedosto johon voit laittaa tiedostoja joita et halua laittaa repoosi eli nämä tiedostot pysyvät vain koneellasi (esim. .exe .o .dll jne.).

Vihdoin voit kloonata repon koneellesi kopioimalla oikeassa laidassa olevan osoitteen (“clone URL”), tai “Clone to Windows” painiketta jos olet windowsilla. Reposi tulee näkyviin koneellesi kansiona.

# GitHub Pages
Voit luoda ja julkaista GitHub sivuja käyttäen automaattista sivu generaattoria, tai voit tehdä sivut manuaalisesti ja push:ata sivun `gh-pages` branchiin. Projektien sivut julkaistaan vakiona osoitteessa `USERNAME.github.io/REPO-NAME`, voit myös määritellä sivun käyttämään [omaa domainia](#oman-domainin-käyttö). Jos luot repon nimeltä `USERNAME.github.io` kyseisen repon master branch julkaistaan vakiona osoitteessa `USERNAME.github.io`.

## Oman domainin käyttö
Voit määritellä oman domainin sivuille jos haluat. Tämä aika yksinkertaista:
1. luo tiedosto nimeltä `CNAME` reposi juureen ja tiedoston sisälle ensimmäiselle riville kirjoita domainisi esim. `esimerkki.com` voit myös määritellä sivulle subdomainin esim. `sivu.esimerkki.com`.
2. Seuraavaksi sinun pitää määritellä domainisi osoittamaan GitHubin servereihin (tämä ohje on [Namecheap:ille](http://namcheap.com), muilla domainin rekisteröinti palveluilla jotkin askeleet voivat olla hieman erinlaisia)
	* kirjaudu namecheap:iin
	* Mene domainisi asetuksiin
	* vasemmalla valikosta valitse "All Host Records"
	* `@` ja `www` kohtiin "IP ADDRESS/ URL" kohtaan laita ip osoitteeksi `199.27.76.133` ja record typeksi laita `A (Address)` ja TTL kohtaan laita `1800`
Muutokset eivät tule heti voimaan mutta jonkin ajan kulutta sivusi pitäisi tulla näkyviin uudessa domainissasi

# Projektin "Fork":aaminen
Miten Forkata projekteja

# Pull Requestin lähettäminen
Miten lähettää pull request

# Github Flow:n ymmärtäminen
Mikä on GitHub flow.

# Lähteet
[Github help](http://help.github.com)

[Github guides](http://guides.github.com)

[Wikipedia](http://wikipedia.com)

[Git:in kotisivut](http://git-scm.com)