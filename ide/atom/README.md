# Atom editor / IDE 

## Howto run 

In the case environment modules have been configured correctly it
suffices to load the module, e.g. 

```
module load ide/atom
atom
```

else run the container directly with singularity 

```
singularity exec /apps/external/sapps/ide/atom/atom.sif /usr/bin/atom
```

## Howto build the container

The application was build using singularity and the definition file

```
sudo singularity build atom.sif atom.def
```

## Links 

  *  https://atom.io/

```
