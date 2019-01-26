Ce repo contient les projets implémentés pendant le cours [Intelligence Artificielle de A à Z](https://www.udemy.com/intelligence-artificielle-az/?couponCode=WEBSITE) en utilisant `PyTorch`.

1. [Installation des modules](#installation-des-modules)

## Installation des modules

Après avoir installé [Anaconda](https://anaconda.org/), suivre les instructions suivantes :

### Sur Ubuntu

```
conda create --name artificialintelligenceaz anaconda
conda activate artificialintelligenceaz
conda install pytorch-cpu torchvision-cpu -c pytorch
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
