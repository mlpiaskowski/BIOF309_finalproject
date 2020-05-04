# BIOF309_finalproject
# Team name: Tary Piasko'neal
# Team members: Mary Piaskowski and Tristan Neal
# 
# In our lab we study oncogenic virus, specifically human papillomaviruses (HPV) and human polyomaviruses, including Merkel Cell polyomavirus, which is the cause of Merkel cell carcinoma, and BK polyomavirus, which has been shown to cause bladder cancer in immunocompromised organ transplant recipients. These viruses are known to cause genomic instability, and our lab has two proposed models for how this may occur. One way this may happen is through viral genome integration, the other by viral DNA binding that affects imbalanced segregation of extrachromosomal circular DNA. In either case, these phenomena should be observable as small, high copy regions containing putative viral protein binding motifs in tumor genome sequencing, and we figured we could collaborate to test this computationally.
# To test this hypothesis, we looked at small CNVs in virus-associated cancers from TCGA. First, Mary filtered these sequences for small CNVs under half a million base pairs, and also generated random synthetic CNVs to serve as controls for the later steps. These CNVs were outputted as a pandas dataframe presented as a tab delineated CSV file. Next, Tristan's code used regular expressions to find and score viral binding protein sequence matches in the CNVs. This code was trained against viral genomes as a positive control and known non-viral sequences as a negative control before being applied to the previously isolated CNVs to produce the outputs.
# Outputs for this project include a table of virus binding score values for each CNV sequence (this score is the number of virus binding sites detected in the CNV, normalized over the kilobase size of the CNV), a scatter plot that shows the relationship between CNV intensity and the viral binding score, and a final CSV file containing detailed information for each virus sequence match within each CSV.
