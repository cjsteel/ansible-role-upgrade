# docs/miniconda/installing-miniconda.md

## Installing miniconda

### [System requirements](https://conda.io/docs/user-guide/install/index.html#id1)

### Requirements

- 32- or 64-bit computer.
- **Miniconda**—400 MB disk space.
- Optional **Anaconda**—Minimum 3 GB disk space
- Windows, macOS or **Linux**.
- Python 2.7, 3.4, 3.5 or 3.6.
- pycosat.
- PyYaml.
- Requests.

### Download miniconda2 latest

```shell
mkdir -p ~/sw/ubuntu/16.04/miniconda2/latest
cd ~/sw/ubuntu/16.04/miniconda2/latest
wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
```

### Install in silent mode

```shell
bash ./Miniconda2-latest-Linux-x86_64.sh -b -p $HOME/miniconda
```

### usage

./Miniconda2-latest-Linux-x86_64.sh [options]

Installs Miniconda2 4.3.30

-b           run install in batch mode (without manual intervention), it is expected the license terms are agreed upon.
-f           no error if install prefix already exists
-h           print this help message and exit
-p PREFIX    install prefix, defaults to /home/users/csteel/miniconda2, must not contain spaces.
-s           skip running pre/post-link/install scripts
-u           update an existing installation
-t           run package tests after installation (may install conda-build)

### Export the miniconda path

To use miniconda from your current terminal session you will need to add the miniconda path to your path by running something like the following in your terminal session.

```shell
export PATH="$HOME/miniconda/bin:$PATH"
```

Adding to your path
```shell
PATH="$HOME/miniconda/bin:$PATH"


## Testing

### Updating conda

```shell
conda update conda
```



