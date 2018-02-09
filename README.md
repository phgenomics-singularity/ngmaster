# ngmaster --- In silico multi-antigen sequence typing for Neisseria gonorrhoeae (NG-MAST)

(https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/579)

Singularity container for Jason Kwong's [NGMASTER](https://github.com/MDU-PHL/ngmaster)

## Pre-requisite

Install [Singularity](http://singularity.lbl.gov/docs-installation)

## Usage

### Latest version

The following steps are needed to use the image:

1. Pull the image:

```
singularity pull --name ngmaster shub://phgenomics-singularity/mlst@latest
```
This will command will create a file `ngmaster.simg`, which is executable.

2. Use the image:
```
./ngmaster.simg --help
```

### A particular version

```
singularity pull --name ngmaster shub://phgenomics-singularity/ngmaster@v0.5.1
```

## Suggested pattern

1. Create a `singularity` folder:

```
mkdir $HOME/singularity
```

2. Pull the image to the `singularity` folder.

```
singularity pull --name mlst_v0.5.1 shub://phgenomics-singularity/ngmaster@v0.5.1
```

3. Link the image to a folder in your `$PATH` (e.g., `$HOME/bin`)

```
ln -s $HOME/singularity/ngmaster_v0.5.1.simg $HOME/bin/ngmaster
```

Now, when you login again, you should be able to just type:

```
ngmaster --help
ngmaster --test
```
