How to use Mercat2
================================================
Here you will find any dependencies needed and how to run MerCat2 on your system

Dependencies 
~~~~~~~~~~~~~~~
MerCat2 runs on python version 3.9 and higher.

External Dependencies 
~~~~~~~~~~~~~~~~~~~~~~~~~
MerCat2 can run without external dependencies based on the options used.

Required dependencies 
~~~~~~~~~~~~~~~~~~~~~~~~
Depending on what type of file you are using, there may be additional dependencies needed, here you will find those requirements 
* When raw read .fastq is given 
   - `Fastqc <https://www.bioinformatics.babraham.ac.uk/projects/fastqc/>`_
   - `Fastp <https://github.com/OpenGene/fastp>`_
* For bacteria/archaea rich samples (-prod option)
   - `Prodigcal <https://github.com/hyattpd/Prodigal>`_
* For eukaryote rich samples or general applications (-fgs option)
   - `FragGeneScanRs <https://github.com/unipept/FragGeneScanRs>`_ 

* Use this script for FragGeneScanRs

::

   conda install -c bioconda fastqc fastp prodigal

::


These are available through Bioconda, except FragGeneScanRs, which is included in the MerCat2 distribution.
  

Notes on memory usage and speed  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* MerCat2 uses a substantial amount of memory when the k-mer is high
* Running MerCat2 on a personal computer using a k-mer length of ~4 should be OK
* Total memory usage can be reduced using the Chunker feature (-s option), but keep in mind that in testing when the chunk size is too small (1MB) some of the least significant k-mers will get lost.
* This does not seem to affect the overall results, but it is something to keep in mind. Using the chunker and reducing the number of CPUs available (-noption) can help reduce memory requirements.


.. note::

    The speed of MerCat2 can be increased when more memory or computer nodes are available on a cluster and using a chunk size of ~ 100Mb.

Options for using Mercat2 
=============================

Usage  
~~~~~~~~~~~~~~

These are the different options that can be used with mercat2.py 

usage: mercat2.py  [-h] [-i I [I ...]] [-f F] -k K [-n N] [-c C] [-prod] [-fgs] [-s S] [-o O] [-replace] [-lowmem LOWMEM] [-skipclean] [-toupper] [-pca] [--version]

Example: mercat2.py -h 

.. csv-table::
  :header: "Option", "Description"
  :widths: 20, 70

  "-h, --help", "Shows this help message and exit"
  "--version, -v", "Show the version number and exit"
  "-i I [I ...]", "Path to input file(s)"
  "-f F", "Path to folder containing input files"
  "-k K", "kmer length"
  "-n N", "No of cores [auto detect]"
  "-c C", "Minimum kmer count [10]"
  "-prod", "Run Prodigal on fasta files"
  "-fgs", "Run FragGeneScanRS on fasta files"
  "-s S", "Split into x MB files. [100]"
  "-o O", "Output folder, default = 'mercat_results' in current directory"
  "-replace", "Replace existing output directory [False]"
  "-lowmem LOWMEM", "Flag to use incremental PCA when low memory is available. [auto]"
  "-skipclean", "Skip trimming of fastq files"
  "-toupper", "Convert all input sequences to uppercase"
  "-pca", "Create interactive PCA plot of the samples (minimum of 4 fasta files required)"



MerCat2 assumes the input file format based on the extension provided 

* Raw fastq file: ['.fastq', '.fq']
* Nucleotide fasta: ['.fa', '.fna', '.ffn', '.fasta']
* Amino acid fasta: ['.faa']
* It also accepts gzipped versions of these filetypes with the added '.gz' suffix


Usage Examples 
~~~~~~~~~~~~~~
.. csv-table::
   :header: "Type", "Script"
   :widths: 20, 70

   "Protein file (protein fasta - '.faa')", "mercat2.py -i file-name.faa -k 3 -c 10"
   "Nucleotide file (nucleotide fasta - '.fa', '.fna', '.ffn', '.fasta')", "mercat2.py -i file-name.fna -k 3 -n 8 -c 10"
   "Nucleotide file raw data (nucleotide fastq - '.fastq')", "mercat2.py -i file-name.fastq -k 3 -n 8 -c 10"
   "Many samples within a folder", "mercat2.py -f /path/to/input-folder -k 3 -n 8 -c 10"
   "Sample with prodigal option (raw reads or nucleotide contigs - '.fa', '.fna', '.ffn', '.fasta', '.fastq')", "mercat2.py -i /path/to/input-file -k 3 -n 8 -c 10 -prod"
   "Sample with FragGeneScanRS option (raw reads or nucleotide contigs - '.fa', '.fna', '.ffn', '.fasta', '.fastq')", "mercat2.py -i /path/to/input-file -k 3 -n 8 -c 10 -fgs"




.. note::

    The prodigal and FragGeneScanRS options run the k-mer counter on both contigs and produced amino acids

Outputs 
=========

Output Folders
~~~~~~~~~~~~~~~~~~~~

Results are stored in the output folder (default 'mercat_results' of the current working directory)

* The 'report' folder contains an html report with interactive plotly figures
   - If at least 4 samples are provided a PCA plot will be included in the html report

* The 'tsv' folder contains counts tables in tab separated format
   - If protein files are given, or the -prod  option, a .tsv file is created for each sample containing k-mer count, pI, Molecular Weight, and Hydrophobicity metrics
   - If nucleotide files are given a .tsv file is created for each sample containing k-mer count and GC content

* If .fastq raw reads files are used, a 'clean' folder is created with the clean fasta file.

* If the  -prod option is used, a 'prodigal' folder is created with the amino acid .faa and .gff files

* If the  -fgs option is used, a 'fgs' folder is created with the amino acid .faa file



Diversity Estimation
~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: https://raw.githubusercontent.com/raw-lab/mercat2/master/doc/PCA.png
   :width: 600


.. csv-table::
   :header: "Alpha diversity metrics provided", "Beta diversity metrics provided"
   :widths: 20, 20

   "shannon", "euclidean"
   "simpson", "cityblock"
   "simpson_e", "braycurtis"
   "goods_coverage", "canberra"
   "fisher_alpha", "chebyshev"
   "dominance", "correlation"
   "chao1", "cosine"
   "chao1_ci", "dice"
   "ace", "hamming"
   " ", "jaccard"
   " ", "mahalanobis"
   " ", "manhattan (same as City Block in this case)"
   " ", "matching"
   " ", "minkowski"
   " ", "rogerstanimoto"
   " ", "russellrao"
   " ", "seuclidean"
   " ", "sokalmichener"
   " ", "sokalsneath"
   " ", "sqeuclidean"
   " ", "yule"
