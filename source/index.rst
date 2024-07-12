.. ReadTheDocs_Tutorial documentation master file, created by
   sphinx-quickstart on Mon Jun 10 11:19:00 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. toctree::
   :hidden:

   page1
   page2
   page3
   report
   
Welcome to MerCat2!
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

   mamba activate base
   conda install mamba

::

Make sure you install mamba in your base conda environment. We have found that mamba is faster than conda for installing packages and creating environments. Using conda might fail to resolve dependencies. 
  

2. Install MerCat2 
This step is done via Bioconda 
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

More information about the different ways to use MerCat2 and any additonal dependencies can be found in the next pages. 

.. image:: source/screenshot.png
  :width: 400
  
