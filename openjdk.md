# Errors encountered during the compilation of OpenJDK

## Missing zip

```bash
checking for zip... no
configure: Could not find zip!
configure: error: Cannot continue
```

Run the command ```sudo apt-get install zip```

## Missing X11 header files
```bash
checking for X11/extensions/shape.h... no
configure: error: Could not find all X11 headers (shape.h Xrender.h XTest.h Intrinsic.h). You might be able to fix this by running 'sudo apt-get install libX11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev'.
configure exiting with result code 1
```
Run the command ```sudo apt-get install libX11-dev libxext-dev libxrender-dev libxtst-dev libxt-dev```

## Missing cups

```bash
checking cups/cups.h usability... no
checking cups/cups.h presence... no
checking for cups/cups.h... no
checking cups/ppd.h usability... no
checking cups/ppd.h presence... no
checking for cups/ppd.h... no
checking for cups headers... no
configure: error: Could not find cups! You might be able to fix this by running 'sudo apt-get install libcups2-dev'.
configure exiting with result code 1
```
Run the command ```sudo apt-get install libcups2-dev```

## Missing freetype

```bash
configure: error: Could not find freetype! You might be able to fix this by running 'sudo apt-get install libfreetype6-dev'.
```

## Missing alsa

```bash
checking for ALSA... no
checking alsa/asoundlib.h usability... no
checking alsa/asoundlib.h presence... no
checking for alsa/asoundlib.h... no
configure: error: Could not find alsa! You might be able to fix this by running 'sudo apt-get install libasound2-dev'.
configure exiting with result code 1
```
Run the command ```sudo apt-get install libasound2-dev```


