# Singularity applications

Singularity is a container framework designed for HPC which resolve a number
of security issues usually associated with Docker. It is here utilized to make 
an environment modules oriented proof-of-concept container package system
using singularity containers as a lightweight snap or flatpak applications.

## Howto install 

### Install requirements 

The requirements are:
  
  * [Singularity](https://sylabs.io/docs/) v3.5+
  * [Lmod](https://lmod.readthedocs.io/en/latest/)
 
On CentOS 7 install the following packages

```
yum install Lmod singularity
``` 

### Clone the repo

```
mkdir -p ~/local
cd local
git clone https://github.com/lmelwyn/sapps.git
```
### Build the containers

The repoitory does not contain the singularity containers and the application definition \<app\>.def files must be
used to build the various containers using the **singularity build** command or using the Makefile in ./sapps 

```
cd sapps
sudo Make
```

Alternatively, reconfigure the various Makefiles in order to use the [--fakeroot](https://sylabs.io/guides/3.3/user-guide/fakeroot.html) feature.

### Define the application path SAPP_PATH

Export the singularity applications path (SAPP_PATH) environment variable to be the local install path,  e.g.

```
export SAPP_PATH=~/local/sapps
```

or add the export command to bash resource file .bashrc.
```
echo 'export SAPP_PATH=~/local/sapps' >> ~/.bashrc
```
### Enable the modules path

```
module use -a $SAPP_PATH/modules
``` 

or add to the bash resource file .bashrc

```
echo 'module use -a $SAPP_PATH/modules' >> .bashrc
```

### Check applications availability

```
module --ignore_cache avail
```

### Load the application

In order to load Visual Studio Code editor do  

```
module load ide/vscode
```

## Applications 

  * Editor / IDE 
      - Atom
      - Sublime Text
      - Visual Studio Code
