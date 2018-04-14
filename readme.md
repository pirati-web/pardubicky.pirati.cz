# pardubicky.pirati.cz

[![Build Status](https://api.travis-ci.org/pirati-web/pardubicky.pirati.cz.svg?branch=gh-pages)](https://travis-ci.org/pirati-web/pardubicky.pirati.cz)

## Instalace

Existují dvě formy instalace, jednodušší je použití Docker engine, které funguje všude. Web lze spustit i přímo bez Dockeru, ale v tom případě je vyžadován Unix-based OS.

### Varianta 1 - Docker

Jediné co je potřeba nainstalovat je  Docker engine pro vaši platformu [na oficiálním webu](https://docs.docker.com/install/). Docker engine funguje na všech postatných platformách (Linux, macOS, Windows).

### Varianta 2 - Přímé spuštění

Vyžaduje Unix-based OS.

#### Fedora 25

##### Instalace závislostí

```
dnf install rubygem-jekyll
```

#### Ubuntu 16.04

##### Instalace závislostí

```
sudo apt-get install ruby2.3-dev gcc make libghc-zlib-dev libffi-dev
gem install rubygems-update
gem install jekyll bundler
bundle
```
#### macOS

##### Instalace závislostí

```
brew install rbenv
rbenv init
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
```

##### Další postup

Znovu spustit Terminál. V repository adresáři pak spustit:

```
rbenv install 2.3.0-dev
rbenv local
gem install rubygems-update
gem install jekyll bundler
bundle
```

## Spuštění

### Docker

#### Unix-based OS

Otevřít terminal v adresáři webu a spustit:

```
docker-compose up
```

#### Windows

Otevřete [PowerShell](https://365tipu.cz/2015/08/12/k-cemu-je-ve-windows-powershell-a-kde-ho-tam-najdu/) v adresáři webu a postupně zadejte následující příkazy:

```
$Env:COMPOSE_CONVERT_WINDOWS_PATHS=1
docker-compose up
```

Web pak běží na [http://localhost:4000](http://localhost:4000/).

**Poznámka:** Je pravděpodobné, že Windows po vás budou chtít heslo k PC.

### Přímé spuštění

Otevřít terminal v adresáři webu a spustit:

```
bundle exec jekyll serve
```

Web pak běží na [http://localhost:4000](http://localhost:4000/).

## Struktura

Samotné stránky jsou v markdownu nebo v html (složitější struktura, např. vícesloupců apod)

Kolekce jsou markdown soubory s yaml hlavičkou v příslušné složce, na webu jsou použity 4:

- posts (články), foto 1300x744
- people (lidé), foto 165x220
- program
- teams (týmy)

Některé údaje jsou uvedeny v složce `_data`. Jsou zde ve formátu yaml nebo json.

**CSS** je ve složce `_sass` a je automaticky kompilováno a minifikován do jednoho souboru `main.css`.

**JavaScript** je ve složce `_include/js`. Knihovny jsou definovány v `bower.json` a produkční soubor je tvořen gulpem.

Jekyll má velmi podrobnou [dokumentaci](http://jekyllrb.com/docs/home/). A při vývoji též doporučuji [cheat sheet](http://jekyll.tips/jekyll-cheat-sheet/)
