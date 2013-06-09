Afuryc
------

```Afuryc``` is a script which provides a way to create and upload your Archlinux packages, via FTP.
It's a solid, easily hackable and dependency-less alternative (you only need ```curl```) to [afur-makepkg](http://wiki.archlinux.fr/Depot_archlinuxfr#afur-makepkg). It has been created for my special needs.

### Usage ###

    usage: afuryc [-bcdehptuvV]
      options:
        -b        Create packages without upload
        -c        Edit config file
        -d        Clean existing src and pkg directories
        -e        Edit PKGBUILD (fallback option)
        -h        Show help and exit
        -p        Edit PKGBUILD
        -t        Build packages on /tmp
        -u        Only upload packages to FTP
        -v        curl with verbose output (useful for debugging)
        -V        Print version
    afuryc compiles packages and upload them to Archlinux.fr FTP.

### Examples ###

Create & send the packages on the server:
```bash
afuryc
```

Edit config (```HOME/.afuryc.conf``` or ```$XDG_CONFIG_HOME/afuryc.conf```)
```bash
afuryc -c
```

Edit PKGBUILD:
```bash
afuryc -p
```

Create packages on ```/tmp``` without upload:
```bash
afuryc -bt
```

Upload packages already created:
```bash
afuryc -u
```

### TODO ###

    [x] Finish the script
    [x] XDG Base Directory support
    [x] Verbose
    [] POSIX shell/bash version
