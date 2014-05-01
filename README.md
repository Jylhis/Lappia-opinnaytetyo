# Git ja GitHub

### Markus Jylhänkangas

Tieto- ja viestintätekniikan perustutkinto, Datanomi 

Tornio, 2014



-----------------
#### Sisältö

- [Mikä on Git?](#mikä-on-git)
	- [Asennus](#asennus)

- [Mikä on GitHub?](#mikä-on-github)
	- [Profiilin luominen](#profiilin-luominen)
	- [Ensimmäinen Repo](#ensimmäinen-repo)

- [Projektin hallinta](#projektin-hallinta)
	- [Issues](#issues)
	- [Pull Requests](#pull-requests)
	- [Wiki](#wiki)

- [GiHub Pages](#github-pages)
	- [Oman domainin käyttö](#oman-domainin-käyttö)

- [Open-source projektien avustaminen](#open-source-projektin-avustaminen)
	-[Projektin "Fork":aaminen](#projektin-forkaaminen)
	-[Pull Requestin lähettäminen](#pull-requestin-lähettäminen)

- [GitHub Flow:n ymmärtäminen](#github-flown-ymmärtäminen)

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
Mene http://www.github.com/ :iin. Heti etusivulla on rekisteröinti lomake johon pitää laittaa käyttäjänimi, sähköposti ja salasana.

Kun painat “Sign up for Github” painiketta päädyt kohtaan mistä voit valita haluatko ykstityisiä repoja (maksavat ~5€/kk ylöspäin), voit myös valita haluatko perustaa yrityksellesi profiilin (yritys tilin voi tehdä myös rekisteröinnin jälkeen).

Nyt olet luonut profiilisi.


## Ensimmäinen Repo
Sivun oikeassa laidassa on “New repository” painike, paina siitä.

Seuraavaksi sinulta kysytään reposi nimeä, kuvausta, haluatko siitä julkisen vai yksityisen, tekeekö Github README tiedostoa (on suositeltavaa että valitset tämän), haluatko .gitignore tiedostoa, ja minkä lisenssin haluat.
Vihdoin voit kloonata repon koneellesi kopioimalla oikeassa laidassa olevan osoitteen (“clone URL”), tai “Clone to Windows” painiketta jos olet windowsilla. Reposi tulee näkyviin koneellesi kansiona.

### .gitignore
Tähän tiedostoon voit lisätä tiedostojen ja kansiotten paikkoja. Git ei yritä lisätä näitä tiedostoja repoosi.

# Projektin hallinta
GitHub on loistava projektin hallinta työkalu. plapla

## Issues
Issues:issä voit keskustella projektista ja ihmiset voivat ilmoittaa bugeista, ongelmista yms.

## Pull Requests
Tänne tulee näkyviin kaikki pull requestit.

## Wiki
Projektisi wiki sivu

# GitHub Pages
Voit luoda projektillesi nettisivut joko käyttäen GitHubin automaattista sivu generointia tai voit itse ladata omat sivut gh-pages branchiin.

## Oman domainin käyttö
Laita oma netti osoitteesi CNAME tiedostoon. ja sitten laita osoitteesi osoittamaan IP:hen.
# Open-source projektien avustaminen
Miten pull requestin tekeminen onnistuu ja miten auttaa muita projekteja

## Projektin "Fork":aaminen
Miten Forkata projekteja

## Pull Requestin lähettäminen
Miten lähettää pull request

# Github Flow:n ymmärtäminen
Mikä on GitHub flow.

# Lähteet
[Github help](http://help.github.com)

[Github guides](http://guides.github.com)

[Wikipedia](http://wikipedia.com)

[Git:in kotisivut](http://git-scm.com)