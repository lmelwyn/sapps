# Sublime Text editor / IDE 

## Howto run 

In the case environment modules have been configured correctly it
suffices to load the module, e.g. 

```
module load ide/sublime
subl
```

else run the container directly with singularity 

```
singularity exec /apps/external/sapps/ide/sublime/sublime.sif /usr/bin/subl
```

## Howto build the container

The application was build using singularity and the definition file

```
sudo singularity build sublime.sif sublime.def
```

## Links 

  * https://www.sublimetext.com/ 

```
