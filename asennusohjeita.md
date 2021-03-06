## Asennusohjeita

Tähän dokumenttiin on koottu muutamia Noden asennusohjeita.

**HUOM:** riippumatta siitä miten asennat nyt Noden, **älä asenna kurssin aikana npm:llä mitään "globaalisti"**, eli komennolla _npm install -g_, (käyttäen tarkenninta g) sille ei ole tarvetta ja koulun koneilla et sitä edes pysty tekemään.


### TÄLLÄ HETKELLÄ (17.1. klo 1440) laitoksen Node-asennuksessa on ongelma

Laitoksen koneilta (ja fuksiläppäreiltä) puuttuu _npm_. Sen pitäisi asentua to ja pe välisenä yönä.

Jos haluat aloittaa fuksiläppärillä jo nyt, niin seuraa copypastea telegramista:

tämän vuoden koneisiin saa sudot komennolla

```
i-want-sudo-access
```

muistaakseni se oli, tuo, korjatkaa joku jos se oli jotain muuta.

tästä mulla oli henkkoht kokemus kun käytin npm:ää, se ehdotti että 'aja tämä komento että saat npm:n päivitettyä' - luotin ja ajoin, komento poisti vanhan npm:n muttei asentanut uutta.

tämän jälkeen nodea ei saanut asennettua uusiks kun se oli jo, ja npmää ei saanut ilman nodea - <i>lopulta noden poisto ja uusiks asennus auttoi</i>



### Laitoksen koneet ja fuksiläppärit

Laitoksen koneilla ja vuoden 2016 tai sitä uudemmissa fuksiläppäreissä pitäisi olla nyt Noden versio 8.9.4. joka on kurssin suoritusta varten riittävä. Koneilla on myös Visual studio code -editori. Mitään ei siis tarvitse asentaa.

Jos fuksiläppärisi on varhaisempaa mallia, ota yhteys IT-ylläpidon Jani Jaakkolaan.

### Linux

Tapoja on monia, tässä eräs (ei edellytä pääkäyttöoikeuksia):

1. Lataa <https://nodejs.org/en/download/> tai <https://nodejs.org/en/download/current/> -sivulta Linux Binaries (x86/x64) -kohdasta 64-bittinen paketti

2. Pura paketti kotihakemistossa:
```tar xvJf ~/Downloads/node-VERSIO-linux-x64.tar.xz```

3. Lisää polkuun uuden hakemiston sisällä oleva bin-hakemisto (eli .bashrc tiedostoon, korvaa VERSIO:
```export PATH=~/node-VERSIO-linux-x64/bin:$PATH```

4. Pakota Linux lataamaan.bashrc:n uudelleen:
```source .bashrc```

Tarkista komennoilla _node -v_ ja _npm -v_ että asennus onnistui ja koneella on riittävän uudet versiot Nodesta (8.9.4 tai suurempi) ja npm:stä (5.3 tai suurempi).

Jos sinulla on pääkäyttäjän oikeudet, on asennus mahdollista suorittaa paketinhallintaa käyttäen. Tällöin täytyy kuitenkin varmistaa, että Nodesta tulee käyttöön riittävän tuore versio (vähintään 8.6). Jos ei, voi päivityksen hoitaa _nvm_-työkalulla. Jos jollakin on ohje tämän tekemiseen, niin otan mielellään pull requestin vastaan.

Yksi vaihtoehto [NMV työkalulle](https://github.com/creationix/nvm#install-script). Tällä voi asentaa monta eri node versiota ja se asentaa ne käyttäjän HOME kansioon USER kansion sijaan (ei tartte admin oikeuksia).

### Mac

Käytä [macOS installeria](https://nodejs.org/en/download/). Edellyttää pääkäyttäjän oikeuksia.

Tarkista komennoilla _node -v_ ja _npm -v_ että asennus onnistui ja koneella on riittävän uudet versiot Nodesta (8.9.4 tai suurempi) ja npm:stä (5.3 tai suurempi).

### Windows

Tapoja on kaksi. Jos sinulla on pääkäyttäjän oikeudet, kannattaa käyttää [Windows-installeria](https://nodejs.org/en/download/).

Tarkista komennoilla _node -v_ ja _npm -v_ että asennus onnistui ja koneella on riittävän uudet versiot Nodesta (8.9.4 tai suurempi) ja npm:stä (5.3 tai suurempi).

Ilman pääkäyttäjän oikeuksia asennus onnistuu seuraavasti

1. Lataa sivulta <https://nodejs.org/en/download/> Windows Binaries

2. Pura paketti haluamaasi kansioon (esim. %userprofile%\Applications\node)

3. Paina WIN+R (CMD+R) ja kirjoita

```rundll32 sysdm.cpl,EditEnvironmentVariables```

4. Valitse "Path". Paina "Edit...". Paina "New". Lisää polku (esim %userprofile%\Applications\node).

Tarkista komennoilla _node -v_ ja _npm -v_ että asennus onnistui ja koneella on riittävän uudet versiot Nodesta (8.9.4 tai suurempi) ja npm:stä (5.3 tai suurempi).
