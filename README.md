# Singularity configuration for simg-rnaseq container

A [Singularity Hub](https://www.singularity-hub.org/) definition for rnaseq workflow.

If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-rnaseq.simg Singularity
```

The container can alos be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-rnaseq.simg" sschmeier/simg-rnaseq:latest 
```

Then, it can be used, e.g.:

```bash
singularity exec simg-rnaseq.simg samtools view -h

# test R
singularity exec --bind /mnt/disk1/seb simg-rnaseq.simg Rscript test.R > session.txt
```
