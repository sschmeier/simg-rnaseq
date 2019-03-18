# Singularity configuration for simg-rnaseq container

A [Singularity](http://singularity.lbl.gov) definition for rnaseq workflow, available at [https://www.singularity-hub.org/collections/2532](https://www.singularity-hub.org/collections/2532).

If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-rnaseq.simg Singularity.201903
```

The container can also be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-rnaseq.simg" sschmeier/simg-rnaseq:201903
```

Then, it can be used, e.g.:

```bash
singularity exec simg-rnaseq.simg samtools view -h

# test R
singularity exec --bind /mnt/disk1/seb simg-rnaseq.simg Rscript test.R > session.txt
```
