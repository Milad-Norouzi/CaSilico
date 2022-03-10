<font size=6><b>CaSilico R Package</b></font> 


The efficiency of CRISPR-Cas system is highly depends on well-designed CRISPR RNA (crRNA). To facilitate the use of various types of CRISPR-Cas systems by a wide range of researchers, there is a need for development of computational tools to design crRNAs which cover different CRISPR-Cas systems with off-target analysis capability. Numerous crRNA design tools have been developed but nearly all of them are dedicated to design crRNA for genome editing. 

Hence, we developed a tool matching the needs of both beginners and experts, named Casilico, which was inspired by the limitations of the current gRNA design tools for designing crRNAs for Cas12, Cas13, and Cas14 CRISPR-Cas systems. Using a list of important features such as mismatch tolerance rules, self-complementarity, GC content, frequency of cleaving base around the target site, target accessibility and PFS (protospacer flanking site) or PAM (protospacer adjacent motif) requirement, Casilico searches all potential crRNAs in a user-input sequence. Considering these features help users to rank all crRNAs for a sequence and make an informed decision about whether a crRNA is suited for an experiment or not. Our tool is sufficiently flexible to tune some key parameters governing the design of crRNA and identification of off-targets, which can be led to increases the chances of successful CRISPR-Cas experiments.

Casilico outperforms previous crRNA design tools in the following respects: 1) supporting any reference genome/transcriptome for which a FASTA file is available; 2) designing crRNAs that simultaneously target multiple sequences through conserved region detection among a set of sequences; 3) considering new CRISPR-Cas subtypes; 4) reporting a list of different features for each candidate crRNA, which can help the user to select the best one. Given these capabilities, Casilico addresses end-user concerns arising from the use of sophisticated bioinformatics algorithms and has a wide range of potential research applications in different areas especially design of crRNA for pathogen diagnosis. 

Casilico was successfully applied to design crRNAs for different genes in SARS-CoV-2 genome, as some of the crRNAs have been experimentally tested in the previous studies.

![image](https://user-images.githubusercontent.com/9910942/157640017-c3a6fd97-45ac-4e81-be58-89411f0819eb.png)

Casilico workflow. (A) Casilico accepts a single or a set of DNA or RNA sequences to be scanned for crRNA designing. (B) When more than one sequences is given as input, the conserved regions among them automatically detect considering conservation threshold and one of the two different approaches for identifying conserved regions. (C) A sliding window (stride of 1 nt) is employed across the single sequences or conserved region of multiple sequences to specify potentail target sites. (D) Casilico applies multiple criteria for crRNA designing, performs off-target analysis and returns outputs in an interactive graphical interface and some files such as MSA and secondary structure (E & F).



<font size=6><b>Installation</b></font> 

library("devtools")
install_github("mrb20045/CaSilico")
