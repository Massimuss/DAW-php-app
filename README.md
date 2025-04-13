
# 🏠 DAW06: Desplegament d'Aplicacions Web

Aquest projecte forma part de la Unitat Formativa 06 del cicle DAW, centrada en el desplegament d'aplicacions web utilitzant eines com Git, GitHub, PHP, Java i la generació de documentació automàtica.

## 🛠️ Començant

Aquestes instruccions et permetran obtenir una còpia del projecte en funcionament a la teva màquina local per a propòsits de desenvolupament i proves.

### 📋 Requisits previs

- **Git**: Sistema de control de versions.
- **PHP**: Per executar scripts PHP localment (`php -S`).
- **Java**: Per desenvolupar aplicacions amb Maven.
- **Composer**: Per instal·lar phpDocumentor.
- **phpDocumentor**: Per documentar codi PHP.
- **JavaDoc**: Per documentar aplicacions Java.

### 🔧 Instal·lació

1. **Instal·lar Git**:

   ```bash
   sudo apt update && sudo apt install git -y
   git --version
   git config --global user.name "El teu Nom"
   git config --global user.email "el.teu.email@example.com"
   ```

2. **Clonar repositoris**:

   - Crear manualment el repositori `DAW-java-app`.
   - Fer un fork de `https://github.com/CarlesCanals/Desplegament-web` i renombrar-lo com `DAW-php-app`.
   - Clonar localment:

     ```bash
     git clone https://github.com/el_teu_usuari/DAW-php-app
     cd DAW-php-app
     git remote add upstream https://github.com/CarlesCanals/Desplegament-web.git
     git remote -v
     ```

3. **Crear i canviar a la branca `develop`**:

   ```bash
   git checkout -b develop
   ```

4. **Afegir nou script PHP**:

   ```bash
   echo '<?php echo "Hola, aquest és el nou script!"; ?>' > nou.php
   git add nou.php
   git commit -m "Afegit nou script nou.php"
   git push origin develop
   ```

## 🔄 Resolució de conflictes

1. Crear un Pull Request de `develop` cap a `main`.
2. Generar un conflicte modificant `nou.php` tant a `main` com a `develop`.
3. Intentar fer merge:

   ```bash
   git checkout main
   git merge develop
   ```

4. Resoldre el conflicte manualment, eliminant els delimitadors `<<<<<<<`, `=======`, `>>>>>>>`.
5. Finalitzar:

   ```bash
   git add nou.php
   git commit -m "Conflicte resolt"
   git push origin main
   ```

## 📜 Historial de versions

Per veure l’historial gràfic dels commits, configuram l’àlies `hist` al fitxer `~/.gitconfig`:

```ini
[alias]
  hist = log --graph --decorate --pretty=format:'%C(yellow)%h%Creset - %C(green)(%cd)%Creset %s %C(blue)[%an]%Creset' --date=short
```

Consultar historial:

```bash
git checkout develop
git hist

git checkout main
git hist
```

També podem comparar branques amb:

```bash
git diff main develop
```

## 🧪 Proves

### 🔍 Proves manuals de funcionament

Per comprovar el correcte funcionament de l'script `nou.php`, podem utilitzar el servidor embegut de PHP:

```bash
php -S localhost:8000
```

I accedir amb el navegador a:

```
http://localhost:8000/nou.php
```

S’han realitzat proves visuals per assegurar que els canvis s’han pujat i integrat correctament amb captures en cada pas: creació de fitxers, pull requests, conflictes resolts i execució de l’aplicació.

### 🧹 Bones pràctiques

L'ús de Git i GitHub amb branques `main` i `develop` fomenta un flux de treball net i col·laboratiu. Es recomana usar extensions com **GitLens** per Visual Studio Code i treballar amb **GitHub Desktop** per visualitzar millor els canvis.

## 🚀 Desplegament

El desplegament local es fa mitjançant el servidor embegut de PHP:

```bash
php -S localhost:8000
```

Per desplegar en un entorn real, es podria utilitzar un servidor Apache o Nginx amb PHP instal·lat, i pujar els fitxers mitjançant FTP o Git.

L’aplicació Java es pot empaquetar amb Maven i desplegar en un servidor d’aplicacions (com Tomcat).

## 🛠️ Construït amb

- **Git** i **GitHub**
- **PHP** 7+
- **Java** amb Maven
- **Composer**
- **phpDocumentor**
- **JavaDoc**
- **Visual Studio Code** i **GitHub Desktop**

## 🤝 Contribuint

1. Fes un fork del projecte
2. Crea una branca (`git checkout -b feature/NovaFuncionalitat`)
3. Fes commit dels teus canvis (`git commit -am 'Afegida nova funcionalitat'`)
4. Puja la branca (`git push origin feature/NovaFuncionalitat`)
5. Crea un nou Pull Request

## ✒️ Autors

- **Carles Canals** - *Treball inicial i desenvolupament* - [CarlesCanals](https://github.com/CarlesCanals/Desplegament-web)
- **Macià Llobera** - *Execució de la tasca* - [Massimuss](https://github.com/Massimuss)


## 🎉 Agraïments

- A [Carles Canals](https://github.com/CarlesCanals) pel repositori base `Desplegament-web`.
- A l’equip de desenvolupament de GitHub, Visual Studio Code i Composer.
- A totes les eines de documentació (phpDocumentor i JavaDoc).
- Als companys i docents per l’ajuda en la resolució de conflictes i millora del flux de treball.

```
