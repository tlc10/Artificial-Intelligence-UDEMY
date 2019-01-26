Ce repo contient les projets implémentés pendant le cours [Intelligence Artificielle de A à Z](https://www.udemy.com/intelligence-artificielle-az/?couponCode=WEBSITE) en utilisant `PyTorch`.

1. [Installation des modules](#installation-des-modules)

## Installation des modules

Après avoir installé [Anaconda](https://anaconda.org/), suivre les instructions suivantes :

### Installation de PyTorch

L'installation de PyTorch dépend elle aussi de votre système d'exploitation mais est très simple.

Rendez-vous sur https://pytorch.org/ puis choisissez :

* Votre système d'exploitation : Linux, Mac, ou Windows, selon ce que vous utilisez. 
* Votre package manager : Ici, comme nous avons téléchargé Anaconda, vous choisissez **conda**.
* Python : Nous avons installé Python **3.6**
* CUDA : Si vous avez un GPU compatible avec CUDA, vous pouvez choisir la version de CUDA associée. Si vous n'en avez pas ou si vous ne savez pas, choisissez **None**.

Vous obtiendrez alors les commandes à taper dans la fenêtre juste en dessous.

**Où taper ces commandes ?**

Si vous êtes sous Linux ou Mac, ouvrez simplement en terminal et copier/coller les commandes.

Si vous êtes sous Windows, alors :

* Dans le menu démarrer, chercher "Anaconda Prompt".
* Ouvrez l'application en faisant un clique-droit et "Lancer en tant qu'administrateur". Une console va s'ouvrir.
* Dans cette console, vous pouvez copier/coller les commandes.

**Il est recommandé de créer un environnement Anaconda au préalable.** Un environnement permet d'installer des modules spécifiquement au projet sur lequel au travail, afin d'éviter les conflits entre différentes versions. Par exemple, si vous avez aussi suivi le cours Deep Learning de A à Z, il est important de séparer les deux projets dans deux environnements différents.

Pour créer un environnement, taper les commandes suivantes dans la console **avant d'installer PyTorch** :

```
conda create --name artificialintelligenceaz python=3.6 anaconda
conda activate artificialintelligenceaz
conda install pytorch-cpu torchvision-cpu -c pytorch
```

La première ligne crée l'environnement sous Python 3.6.

La deuxième ligne active l'environnement. **Vous devrez activer l'environnement à chaque fois que vous reprenez votre travail dans ce projet.**

La dernière ligne dépend de votre OS (Mac, Linux, ou Windows), utilisez le site de PyTorch pour avoir la commande exacte.

### Installation de Kivy

Kivy vous donne aussi les instructions séparément selon votre système d'exploitation.

Rendez-vous sur le site de Kivy, https://kivy.org/#download et cliquer sur le lien d'instructions correspondant à Windows, Mac ou Linux.

**Important : On n'utilise pas conda pour l'installation de Kivy. Elle est incompatible avec PyTorch à l'heure actuelle.**

N'oubliez pas d'activer l'environnement si vous vous êtes arrêtés entre temps :

```
conda activate artificialintelligenceaz
```

**Notes pour Windows**

Les instructions sont à l'adresse https://kivy.org/docs/installation/installation-windows.html

Elles sont résumées ici **mais pourraient être amenées à changer** dans le futur :

```
python -m pip install --upgrade pip wheel setuptools
python -m pip install docutils pygments pypiwin32 kivy.deps.sdl2 kivy.deps.glew
python -m pip install kivy.deps.gstreamer
python -m pip install kivy.deps.angle
python -m pip install kivy
```

La première étape consiste à mettre à jour `pip` , `wheel` , et `setuptools`. Il est possible que mettre à jour `setuptools` casse l'installation de PyTorch. Si jamais c'est le cas, réinstallez une version précédente avec :

```
pip install setuptools==39.1.0   
```

**Notes pour Mac**

Les instructions sont à l'adresse https://kivy.org/docs/installation/installation-osx.html#using-homebrew-with-pip

Je recommande d'utiliser la section Using Homebrew with pip qui vous simplifiera grandement la vie. Si vous n'avez pas Homebrew, vous pouvez l'installer en suivant les instructions sur le site https://brew.sh/

Dans la console, tapez :

```
brew install pkg-config sdl2 sdl2_image sdl2_ttf sdl2_mixer gstreamer
pip install Cython==0.28.3
pip install kivy
```

**Notes pour Linux**

Les instructions sont à l'adresse https://kivy.org/docs/installation/installation-linux.html

Dans la console, tapez :

```
sudo add-apt-repository ppa:kivy-team/kivy
sudo apt-get install python3-kivy

sudo apt-get install -y \
    python-pip \
    build-essential \
    git \
    python3 \
    python3-dev \
    ffmpeg \
    libsdl2-dev \
    libsdl2-image-dev \
    libsdl2-mixer-dev \
    libsdl2-ttf-dev \
    libportmidi-dev \
    libswscale-dev \
    libavformat-dev \
    libavcodec-dev \
    zlib1g-dev

sudo pip install --upgrade pip virtualenv setuptools
pip install Cython==0.28.2
pip install kivy
```

Et voilà !

### Tester votre installation

Pour tester votre installation, taper python dans la console puis rentrez les commandes suivantes :

```
import kivy
import torch
```

Voici les sorties que vous devriez voir :

```
Python 3.6.8 |Anaconda, Inc.| (default, Dec 30 2018, 01:22:34) 
[GCC 7.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import kivy
[INFO   ] [Logger      ] Record log in /home/charles/.kivy/logs/kivy_19-01-26_4.txt
[INFO   ] [Kivy        ] v1.10.1
[INFO   ] [Python      ] v3.6.8 |Anaconda, Inc.| (default, Dec 30 2018, 01:22:34) 
[GCC 7.3.0]
>>> import torch
```


