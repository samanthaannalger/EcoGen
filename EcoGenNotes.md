# EcoGenNotes
Samantha A. Alger  
23, January 2017  


##23, January 2017
###Next Gen Sequencing 

**Glossary:** 

* short (50 bp)
* long (100 bp, 150, 300 bp -Hi-seq)
* 10,000-60,000 bp (SMART)
* single vs. paired end
* "Reduce representation": RNA, GBS/RAD seq, near restriction sites

**OUTLINE**
​    
* Advances in Seq Tech
* Range of Applications (Whole Genome Sequencing (WGS), RNAseq, ChipSeq-chromatin immunization sequencing, targeted/capture seq. (use probes that target something)) Whatever the application, probably using Illumina sequencing- sequencing by synthesis (90% of the global data).

* General Library Prep. Workflow
* Sequencing-by-synthesis (SBS)
* Other Technologies
* Learning Activity

**Human Genome Project**
2001-2003

**ABI-Sanger**       
-15 years     
-1 genome   
-$3 B     


**Hi Seq X Ten releases**      
-2014      
-Illumina      
-1 day  
-45 whole genomes human   
-$1000 each   

**What technique you choose depends on what your question is**  
-where is genetic variation 
-phenotypes 
-#samples 
-population v. individual 
-comparative studies  
-model or not?  
-demographic history  
-adaptive genetic variation 
-gene expression var. 

Major decision points: Length of reads, and number of reads, and distribution

WorkFlow: Extraction to get DNA or RNA, if RNA- change into cDNA, fragment sample, ligate adaptors (individual barcodes), add seq. adaptors, PCR).

Extracted DWN with adaptors and put into a lane. bridge amplification, cluster gen. labeled dNTPs build on and a snap shot is taken everytime one is added. 

"den novo" assembly"- with non-model organism.

##1-25-2017
###Outline:

1. What are QTNs?
2. Quantitative genetic theory of adaptive traits?
* V~a~
* h^2^
3. Methods
*   linkage mapping
*   GWAS
    * selection scams

    QTN = "Qunatitative trait nucleotides", most simple SNPS
    Study of **quantiative traits**- traits that have continuous distributions, traits have a mean and variance. 


    variance between the two allehels to determine the "average effect"

    * flowering time- quantitative trait
    * flower color- Mendelian trait -discrete
    * thermal tolerance
    * venom potency
    * defense compounds
    * drought tolerance
    * altitude tolerance (hypoxia)


    Most populations are at their adaptive peak- because of this, selection on a small mutation might move fitness up or down. selection on a large mutation, would most likely move fitness down- therefore, most of selection occurs on small mutations because large mutations are usually  deleterious. 

    ​
##Seastar wasting disease:  
* High morality rate and affects many species. East and West coast.    
* What is causing it?-unknown  
    * In hours or days, a healthy individual with lose legs, innards expload out  
    * 2012 first account, 2014- really bad, still occuring but less severe. There have been reports of seastar wasting in 1970s.  
    * Densovirus implicated (Hewsonet al., 2015, PNAS) (SSDNA virus)  
    * coauthors are not convinced that this is causal pathogen.  
    * also present in 70 year old museum specimens.  
    * It could be that something gets out of balance in their normal microbiome and allows the pathogen to make the animal sick.   
    * Finding that cause of disease is a challenge.  
    * Field sampling and lab studies  

##Melanie's experiment:  
* take biopsy, exracted total RNA, polyA tail to selected mRNA (to get just genes that are coding for proteins), sequenced on hi-illumina, amplified sequences, (get results for microbes on skin, 16S data), photo taken before or after biopsy

##Questions for Seastar wasting:   
1. What is the role of host microbiota in disease prev?
2. How does expression of immune related genes differ between the sick vs. health?
   Can understanding something about the immune response tell us something about what type of pathogen we are dealing with? for example: RNAi is used in antiviral defense. 


#1/30/17

Targetted approach to see differences in immune related genes over time- as 'infection progressed'. 
Also look for differences between sick v. healthy individuals. 

H vs. S

Jonathan Rast- reviews on sea urchin immunity. 
Adaptive/innate immune system: 220 Toll- like reptors
vs. human (20 receptors) 

Methods:
Identify genes related to immune response to particular pathogens. Pair with random group of genes to see if there really is upregulation or if it is an artifact. 
Find groups of sick individuals and look at the dataset associated with when each individuals go from healthy to sick.
Pair with healthy individuals at the same time points. 

HH: 5
SS: 5
HS: 5
x two time steps
= 30 data sets

Can we tell anything about the pathogen identity based on expression of immune genes?
What is the immune response? Is it different between 2 spp. of starfish?

Blast against other infected seastars to be confident that these seastars are infected with Densovirus.



## 2/1/17

* Send link of GitHub notebook to Andrew
* Project proposal due to Melissa and Stephen next Monday:
  * Hypothesis, and how we plan to test it.
* Sign up for 1 info update and 1 discussion



## Whole Genome Sequencing

* applications:
  * high power resolution
    * population genetics
    * conservation- control breeding programs etc. 
    * screen for variation and adaptive potential 
    * impacts of genetic variation
    * plastic responses to the environment
    * local adaptation
  * sometimes you need reference genome- other times you don't: 
    * you **don't need** it with: De novo assembly, adaptations, gene expression patterns, 
    * you **need** it with: select important variation, epigenetic modification, DNA-protein, gene expression
* Prior considerations:
  * $
  * Computational
    * geater than 1 T byte
    * Server
    * command line 
    * Python/perl
* Limitations:
  * polymorphic genes- core genes that are highly conserved
  * Paralogs
  * rapidly evolving genes
  * large gene families- poor representation
  * 1 individual
  * pooled samples
  * Impossible to sequence all nucleotides (not actually Whole genome sequencing) such as highly repetitive regions and heterchromatic regions such as centermeres/telomeres. DNA might be so bound up, highly repetitive stuff cannot be placed onto the map. 
* Genome is a working hypothesis



* Sequencing Platforms
  * Short reads
    * Ilumina sequencing (150 bp)
    * SOLID (50bp)
  * Long Reads
    * Pacific Biosciences (5kb)
    * Ion Torrent (500 bp)
    * Ilumina Mollecule (up to 10 kb)
* knowledge on organism
  * genome size (K-mer approach: short, unique element of DNA sequence of length K).
  * **HOW MANY** reads you need depends on size of the genome. There are some rules of thumb depending on size of the genome. 



* Methods:

  * Wet-lab

    * Tissue
      * high quality: energetically active (mDNA)
      * avoid Gut and Skin- other DNA from symbionts or bacteria will be sequenced
    * Quantity 1 mg -> 6 ug (short)

  * Library Prep. 

    * reads would occur in any direction (single end)

    * paired end reads

    * mate-pair

    * contigs

    * scaffold

      ​

  * Gc Content

  * repeat abundance

  * Duplicate reads

* 50% of the reads come from contigs

* Annotate your sequence (use from related genome)

* Find them in NCBI

##RNA Seq:

* Advantage
* Limitations
* Work flow
* ​



