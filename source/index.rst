.. ReadTheDocs_Tutorial documentation master file, created by
   sphinx-quickstart on Mon Jun 10 11:19:00 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome MerCat2!
================================================
|paper| |preprint| |install with| |Anaconda.org| |Last updated| |last updated| |Platforms| |license| |Downloads| |downloads| |downloads/month| |downloads/week|

..  |paper| image:: https://camo.githubusercontent.com/4e62fbf1240e11569ff5a5a55cfd46dd12aa4dfa41c1edd821f4f887d8e05c61/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f70617065722d42696f696e666f726d6174696373416476616e6365732d7465616c2e7376673f7374796c653d666c61742d737175617265266d61784167653d33363030
   :target: https://doi.org/10.1093/bioadv/vbae061 

..  |preprint| image:: https://camo.githubusercontent.com/4b1ce666560094f833328c23d008ff7aa59e483db5f38e2aa2c6fd9e58f133e7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7072657072696e742d42696f527869762d7265642e7376673f7374796c653d666c61742d737175617265266d61784167653d33363030
   :target: https://doi.org/10.1101/2022.11.22.517562

..  |install with| image:: https://camo.githubusercontent.com/2b3da1f4ac43c9ff4aa3151c2ea27dd4d00f147e01dfb55225b08b1cbc284774/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f696e7374616c6c253230776974682d62696f636f6e64612d627269676874677265656e2e7376673f7374796c653d666c6174
   :target: http://bioconda.github.io/recipes/mercat2/README.html

..  |Anaconda.org| image:: https://camo.githubusercontent.com/8c1a83f3189c641f0f819a71dae7cabf3f7a002314f13621efba4d450a06d8a4/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f76657273696f6e2e737667
   :target: https://anaconda.org/bioconda/mercat2 

..  |Last updated| image:: https://camo.githubusercontent.com/ea29e40bfb15292c35d60919e24035ef541a309047f53a7f24b1b72798a5c0d4/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f6c61746573745f72656c656173655f646174652e737667
   :target: https://anaconda.org/bioconda/mercat2 

..  |last updated| image:: https://camo.githubusercontent.com/d1326f3d872ad8a6bb39ea6bebddc2d8440d8d918152f809326f33fa67941bf7/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f6c61746573745f72656c656173655f72656c61746976655f646174652e737667
   :target: https://anaconda.org/bioconda/mercat2 

..  |Platforms| image:: https://camo.githubusercontent.com/8741ef138a4ddda6adc435f3e84f64e608d4ca7d424f0fd62fd95bc240267de5/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f706c6174666f726d732e737667
   :target: https://anaconda.org/bioconda/mercat2 

..  |license| image:: https://camo.githubusercontent.com/ee552931b73896308a277e32be730377a4376610365ef0dc58a61f500426a5a6/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f6c6963656e73652e737667 
   :target: https://anaconda.org/bioconda/mercat2

..  |Downloads| image:: https://camo.githubusercontent.com/01b40ed4b155269d1cffae11c7b4a8c55403b452281e55fbec22b29fab76a20d/68747470733a2f2f616e61636f6e64612e6f72672f62696f636f6e64612f6d6572636174322f6261646765732f646f776e6c6f6164732e737667
   :target: https://anaconda.org/bioconda/mercat2

..  |downloads| image:: https://camo.githubusercontent.com/74e56c6c0f62d5906fa442b38250ce6ab586ef15cac8be93e872e6446ec5cdfd/68747470733a2f2f7374617469632e706570792e746563682f62616467652f6d657263617432
   :target: https://pepy.tech/project/mercat2

..  |downloads/month| image:: https://camo.githubusercontent.com/e1152b598d7f78fe56f7e7c79aad8c9263bf78cba4b532018fd39652569129f4/68747470733a2f2f7374617469632e706570792e746563682f62616467652f6d6572636174322f6d6f6e7468
   :target: https://pepy.tech/project/mercat2

..  |downloads/week| image:: https://camo.githubusercontent.com/67f98fd521ce96ea507aa2a195da3fe30f8850447500fc7976bd513a140c6adc/68747470733a2f2f7374617469632e706570792e746563682f62616467652f6d6572636174322f7765656b
   :target: https://pepy.tech/project/mercat2 


.. image:: https://github.com/raw-lab/mercat2/blob/master/MerCat2.jpg?raw=true
   :width: 600

Getting Started 
==================

There are two different ways of installing MerCat2: Bioconda Installer and Source Installer

.. note::

    Installing Conda should be done first before running any of these options on the terminal, download Conda to install the latest verison to your system.
Option 1: Bioconda Installer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Install mamba using conda 

::

   mamba create -n mercat2 -c conda-forge -c bioconda mercat2
   conda activate mercat2v

::
.. note::

    Make sure you install mamba in your base conda environment. We have found that mamba is faster than conda for installing packages and creating environments. Using conda might fail to resolve dependencies. 

2. Install MerCat2 
This step is done via Bioconda git reset --hard <commit-hash>
::

   mamba create -n mercat2 -c conda-forge -c bioconda mercat2
   conda activate mercat2

::

Option 2: Source Installer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Clone MerCat2 from github
2. Run install_mercat2.sh to install all required dependencies 

This script creates a conda environment for you 
::

   git clone https://github.com/raw-lab/mercat2.git
   cd mercat2
   bash install_mercat2.sh
   conda activate mercat2

::

Running Mercat2 
==================

Dependencies 
~~~~~~~~~~~~~~~
MerCat2 runs on python version 3.9 and higher.

External Dependencies 
~~~~~~~~~~~~~~~~~~~~~~~~~
MerCat2 can run without external dependencies based on the options used.

Required dependencies 
~~~~~~~~~~~~~~~~~~~~~~~~
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
.. note::

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

.. add picture here

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

Citations and Copywrite
===========================

Citing Mercat2
~~~~~~~~~~~~~~~~~~~~~~~~
If you are publishing results obtained using MerCat2, please cite:

Figueroa JL*, Redinbo A*, Panyala A, Colby S, Friesen M, Tiemann L, White III RA. 2024.
MerCat2: a versatile k-mer counter and diversity estimator for database-independent property analysis obtained from omics data
Bioinformatics Advances, vbae061 `Bioinformatics Advances <https://doi.org/10.1093/bioadv/vbae061>`_  

The star indicates* Co-first authors

BioRxiv pre-print
Figueroa JL, Panyala A, Colby S, Friesen M, Tiemann L, White III RA. 2022.
MerCat2: a versatile k-mer counter and diversity estimator for database-independent property analysis obtained from omics data.

`bioRxiv <https://www.biorxiv.org/content/10.1101/2022.11.22.517562v1>`_

Copywrite
~~~~~~~~~~~~~~~~~~~~~~~~

This is copyrighted by University of North Carolina at Charlotte, Jose L. Figueroa III, Andrew Redinbo, and Richard Allen White III. All rights reserved. DeGenPrime is a bioinformatic tool that can be distributed freely for academic use only. Please contact us for commerical use. The software is provided “as is” and the copyright owners or contributors are not liable for any direct, indirect, incidental, special, or consequential damages including but not limited to, procurement of goods or services, loss of use, data or profits arising in any way out of the use of this software.

