# Sinox
Sinox v1 is a pipeline built for Linux.

## Prerequisites
A number of external programs are requiered to be in global directory and can be accessible from any working directory.
  1. PAML, available from http://abacus.gene.ucl.ac.uk/software/paml.html  (used version 4.9j). [Click to doawnload](http://abacus.gene.ucl.ac.uk/software/paml4.9j.tgz).
  2. ParaAT, available from https://github.com/wonaya/ParaAT (used version 2.0). [Click to doawnload](https://github.com/wonaya/ParaAT/archive/refs/heads/master.zip).
   - ParaAT requiere have at least one of the following sequence aligner clustalw2, t_coffee, mafft or     muscle. Some of them can be installed from Linux command line. Example:
```
sudo apt-get install mafft
```
To program can be accessible from any working directory add is in your PATH variable. In bash can add in ~/.bash_profile using of following commands:
```
nano ~/.bash_profile
```
Type and save the following lines:
```
export PATH=$PATH:~/your/path/directory/paml4.9j/src/
export PATH=$PATH:~/your/path/directory/ParaAT-master/
```
Then, execute in the command line:
```
source ~/.bash_profile
```
## Starting from Reads

## Instruction

- Input data

- Main Options  
  `-p` Directory containing protein(s) file(s) in Fasta format. If you ran OMA to obtain orthologous information, it can be used the "DB" file, only with the Fasta file. Required parameter.  
  `-n` Directory containing nucleotido(s) file(s) in Fasta format. Required parameter.    
  `-o` Directory containing information of the ortologous groups. If you ran OMA, you can use "PairwiseOrthologs" file. However, a file in format tsv (Tab-separated values) with two column can be used. See example in "Input data" section. Required parameter.  
  `-z` Process number used during alignment. It is used by the ParAT program. Required Parameter. 
  `-a` Aligner used. Depending on which alignment program you have installed, you can choose one of the following: "clustalw2", "t_coffee", "mafft" or "muscle"). Default mafft. Optional parameter.  
  `-g` rerf
  `-t` sd  
  `-s` rerf  
  `-h` sd  
Import note: Each gene must have the same code in its nucleotide and amino acid sequence. However, the code from one gene should not be repeated in another gene. Don't use "@" in sequence codes.
## Running Sinox
```
./Sinox.sh -p Protein_example/ -n Nucleotide_example/ -o PairwiseOrthologs_example/ -z 8 -a mafft -g 1 -t OMA -s single-copy
```
---
## Test
--
## Instruction
--
## Citation
--
##

