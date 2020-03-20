# Visual Studio Code editor / IDE 

## Howto run 

In the case environment modules have been configured correctly it
suffices to load the module, e.g. 

```
module load ide/vscode
code
```

else run the container directly with singularity 

```
singularity exec -B /run /apps/external/apps/singularity/ide/vscode /usr/bin/code
```

## Howto build

The application was build using singularity and the definition file

```
sudo singularity build vscode.sif vscode.def
```

## Links 

  *  https://code.visualstudio.com/

```
