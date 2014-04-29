# Github

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

## Ensimmäinen Repo

# Projektin hallinta

## Issues

## Pull Requests

## Wiki

# GitHub Pages

# Open-source projektien avustaminen

## Projektin "Fork":aaminen

## Pull Requestin lähettäminen

# Github Flow:n ymmärtäminen

# Lähteet
[Github help](http://help.github.com)

[Github guides](http://guides.github.com)

[Wikipedia](http://wikipedia.com)

[Git:in kotisivut](http://git-scm.com)