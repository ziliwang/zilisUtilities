##gene_exp_diff_hub
#####![Des](icos/date.png)  Description
gene_exp_diff_hub is a cuffdiff downstream tools, target to get a table with gene expression in each sample, also include annoation infomation and basic gene difference information.
#####![Alg](icos/gavel.png)  Algorithm
integrate gene expression table and annotation table based on gene name.
#####![samll](icos/small.png) Input and Output
######input
cuffdiff output dir, reference gene, and annotation of cufflinks transfrag.
<class_code_ifo> format:
```
---------------------------
cufflink_id	class_code
---------------------------
XLOC_012521	  =,j,=
```
<ref_gene_info> <predicted_gene_info> format:
```
	 -----------------------------------------------		
	 gene_id	gene_type gene_status gene_name
	 -----------------------------------------------		
	 ENSG00000222623.1 snRNA KNOWN RNU6-1100P	|
	 ENSG00000241599.1 lincRNA NOVEL RP11-34P13.9	| <ref_gene_info>
	 ENSG00000228463.4 lincRNA NOVEL AP006222.2	|
	 XLOC_001931 antisense_lncRNA predicted antisense_DPYD	|
	 XLOC_001955 antisense_lncRNA predicted antisense_SASS6	| <predicted_gene_info>
```
######output
a integration table with gene expression of each sample and the transfrag annotation. 
