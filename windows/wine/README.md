# WINE

## Howto run 

In the case environment modules have been configured correctly it
suffices to load the module, e.g. 

```
module load wine
```

else run the container directly with singularity 

```
singularity exec /apps/external/sapps/wine wine 
```

## Howto build

The application was build using singularity and the definition file

```
sudo singularity build wine.sif wine.def
```

## Links 

  *  https://wiki.winehq.org/Winetricks

```
