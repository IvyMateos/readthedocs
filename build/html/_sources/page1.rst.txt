Tutorials
================================================

The following tutorial will show you how to use MerCat2 and the results that will be generated

Before you start installing MerCat2, install Conda into your system 

This tutorial will use the data in the github repository to demonstarte what data would be generated and use the following scripts to install MerCat2 

Open a terminal on your system to start any of these tutorials 


Source Installer 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


1. Clone the github repository 

::

   git clone https://github.com/raw-lab/mercat2.git

::

2. Activate the anaconda environment using the following script 


- depending on where you are running MerCat2, this may vary. Ask your supervisor for the appropriate environment.
::

   module load anaconda3

::

3. Initialize shell environment to use Conda

::

   eval "$(conda shell.bash hook)"

::

4. Activate the Conda envrionment 


- This will be the path to the file where you are running your results 
::

   conda activate /projects/raw_lab/envs/mercat2

::

5. Open mercat2 

You can use ls command to see what files you have during each step 

::

   cd mercat2 

::

you can use ls command to see what files you have during each step 

6. Open the data file 

::

   cd data 

::



Run `ls` again to select which file you want to use 


- In this tutorial we will use the 5-genomes-faa file to run results 


::

   cd 5-genomes-faa

::

7. Choose which file you want to run 


- Run the `ls` command again to see all the files 



- Under this folder there are many files you can run including DJ_pro.faa  GIC31_pro.faa  Rleg_pro.faa  RW1_pro.faa  RW2_pro.faa


Because this is a .faa file you can use the following script to run it, depending on the type of file the script might look slighlty different. 
Consult the Usage Examples table to see which script to use 

::

   mercat2.py -i DJ_pro.faa -k 3 -n 8 -c 1

::

You succesfully ran MerCat2!

You can now use the `ls` command to see your results appear on your system 

8. View results 
::

   cd mercat2_results

::



Here you will see the generated files including a combined_protein.tsv, a combined_protein_T.tsv, and a report  tsv_protein file 



Locally OSX-ARM (M1/M2) 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You will need to clone the MerCat2 repository for this as well 

1. Clone the github repository 

::

   git clone https://github.com/raw-lab/mercat2.git

::

2. Set up the conda enviornment 

::

   conda create -y -n mercat2 
   conda activate mercat2 
   conda config --env --set subdir osx-64

::

3. Install mamba, python, and pydantic inside the environment


::

   conda install -y -c conda-forge mamba python=3.10 "pydantic<2"

::

4. Install MerCat2 with mamba 


::

   mamba install -y -c conda-forge -c bioconda mercat2
   mercat2.py --setup 
   mercat2.py --download

::



5. Open mercat2

::

   cd mercat2

::



6. Open the data file 

::

   cd data 

::


Run `ls` again to select which file you want to use 


- In this tutorial we will use the 5-genomes-faa file to run results 


::

   cd 5-genomes-faa

::

7. Choose which file you want to run 


- Run the `ls` command again to see all the files 



- Under this folder there are many files you can run including DJ_pro.faa  GIC31_pro.faa  Rleg_pro.faa  RW1_pro.faa  RW2_pro.faa


Because this is a .faa file you can use the following script to run it, depending on the type of file the script might look slighlty different. 
Consult the Usage Examples table to see which script to use 

::

   mercat2.py -i DJ_pro.faa -k 3 -n 8 -c 1

::

You succesfully ran MerCat2!

Here are the different results you will obtain after running MerCat2

Here is a link to the `report.html` page:

`report.html <report.html>`__



.. .. tabs::

..    .. tab:: Source Installer

..       7. Choose which file you want to run 
..       ::

..          mercat2.py -i DJ_pro.faa -k 3 -n 8 -c 1

..       ::
..       ivy mg    


..    .. tab:: OSX-ARM (M1/M2)

..       Pears are green.

