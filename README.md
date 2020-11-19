# Mac Setup
A simple repo containing my macOS Setups

## 0. Terminal öffnen

Alles was wir einrichten wollen müssen wir über das Terminal machen.

Führe auf einen der folgenden Schritte aus:

**Methode 1:** Klicke im Dock auf das Launchpad Symbol, gib „Terminal“ in das Suchfeld ein und klicke auf „Terminal“.

**Methode 2:** Öffne den Ordner „/Programme/Dienstprogramme“ im Finder  und doppelklicke auf „Terminal“.

## 1. [Homebrew](https://brew.sh/index_de)
>"Homebrew installiert Zeug, das du brauchst, das Apple aber nicht mitliefert."

Kopiere das folgende in dein Terminal und drücke *Enter*:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

## 2. [Node.js](https://nodejs.org/)
>Node.js is an open source server environment, is free, runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.), enables JavaScript on the server

Homebrew können wir jetzt benutzen um Node zu installieren.

```bash
brew install node
```

## 3. [Z shell](https://de.wikipedia.org/wiki/Z_shell)
>Die Z shell (zsh) ist eine Unix-Shell, die sowohl als interaktive Login-Shell, als auch als ein mächtiger Kommandozeileninterpreter für Shellskripte verwendet werden kann. Die zsh wird oft als erweiterte Bourne-Shell angesehen, welche viele Verbesserungen und Eigenschaften von bash, ksh und tcsh vereint.

**_INFO:_ zsh ist seit macOS Catalina vorinstalliert auf allen Macs, dass heißt die folgenden Schritte musst du nur machen wenn deine macOS-Version älter als *Catalina* ist**

#### Installation
```bash
brew install zsh
```

#### Zsh als Standard festlegen

>ab macOS High Sierra
```bash
chsh -s /usr/local/bin/zsh
```

>vor macOS High Sierra
```bash
chsh -s /bin/zsh
```

#### Installation überprüfen
```zsh
zsh --version
```
Das sollte etwas ausgeben wie: `zsh 5.4.2`. Die Version kann auch höher sein.

Es kann sein, dass du einen Neustart machen musst damit deine Änderungen angewendet werden.

*[Offizielle Installations-Antleitung](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)*

## 4. [oh-my-zsh](https://ohmyz.sh/)
> "Oh My Zsh is a delightful, open source, community-driven framework for managing your Zsh configuration. It comes bundled with thousands of helpful functions, helpers, plugins, themes, and a few things that make you shout..."
>
> "Oh My ZSH!"

```zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

*[Offizielle Installations-Antleitung](https://github.com/ohmyzsh/ohmyzsh/wiki)*

## 5. [Spaceship ZSH](https://github.com/denysdovhan/spaceship-prompt)
>"Spaceship is a minimalistic, powerful and extremely customizable Zsh prompt. It combines everything you may need for convenient work, without unnecessary complications, like a real spaceship."

![Spaceship in Action](./images/spaceship.gif)

#### Installation
```zsh
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

#### Als Standard-Theme auswählen
Editiere die Datei `.zshrc` und setze dein Theme: `ZSH_THEME="spaceship"`

Speichern, Terminal neustarten und fertig.