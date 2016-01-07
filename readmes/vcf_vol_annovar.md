##vcf_vol_annovar
#####![Des](icos/date.png)  Description
vcf_vol_annovar is a tools for vcf volume annotation by annovar(only support hg19), and joining mutations of each sample into a single table.
#####![Alg](icos/gavel.png)  Algorithm
**annotation** of mutations is depend on annovar.
**integration** part is by simply format conversion.
#####![samll](icos/small.png) Input and Output
######input
mutation(vcf files list), annovar and the database correspond to it. 
######output
two statistics file(mutation summary and a detail for mutation types in each sample) and an integrate table .
mutation summary
```
Samples Num.:        27
Mutation Num.:      1345

site         intergenic          exonic        intronic    ncRNA_exonic        splicing            UTR3            UTR5
num.                 43             457             792              13               3              37               0 

mutation type   .       frameshift deletion     frameshift insertion    nonframeshift deletion  nonsynonymous SNV       stopgain        stoploss        synonymous SNV
number  888     19      4       4       222     8       1       199
```
details:
```
001_QuJianGuo                      .    ATM:9,ERBB4:5,FGFR1:1,FLT3:1,GNAQ:5,GNAS:1,JAK3:1,KDR:3,KIT:1,LINC01120,LOC401010:1,OR11H1,CCT8L2:1,PIK3CA:1,PTEN:1,PTENP1:1,SMO:2,TP53:1
001_QuJianGuo      nonsynonymous SNV    ATM:1,GNA11:1,GNAQ:1,KDR:1,MET:1,PTEN:2,PTPN11:1,STK11:1,TP53:2
001_QuJianGuo         synonymous SNV    APC:1,EGFR:1,GNA11:1,GNAQ:2,JAK3:1,PDGFRA:2,RET:1,STK11:1,VHL:1
002_lichunye                       .    ATM:7,ERBB4:5,FGFR1:1,FLT3:1,GNA11:2,GNAQ:7,JAK2:1,KDR:3,KIT:2,LINC01120,LOC401010:1,OR11H1,CCT8L2:1,PIK3CA:1,PTEN:1,SMARCB1:1,SMO:1,TP53:2
002_lichunye     frameshift deletion    SMARCB1:1
002_lichunye       nonsynonymous SNV    EGFR:1,KDR:1,TP53:1,VHL:1
002_lichunye          synonymous SNV    APC:1,FGFR3:1,GNA11:1,JAK3:1,PDGFRA:2,RET:1
```
table
```
ID      Chr     Strat   End     Ref     Alt     Func.refGene    Gene.refGene    GeneDetail.refGene      ExonicFunc.refGene      AAChange.refGene        Otherinfo
005_chenguoyou  chr2    29432776        29432776        T       C       intronic        ALK     .       .       .       0.5     100.00  6874    chr2    29432776        rs3738867       T       C       100.00  PASS    DP=6874;TI=NM_004304;GI=ALK;FC=Silent   GT:GQ:AD:VF:NL:SB:GQX   0/1:100:6661,213:0.0310:20:-100.0000:100
005_chenguoyou  chr2    29443749        29443749        G       T       intronic        ALK     .       .       .       0.5     100.00  3545    chr2    29443749        rs80152976      G       T       100.00  PASS    DP=3549;TI=NM_004304;GI=ALK;FC=Silent   GT:GQ:AD:VF:NL:SB:GQX   0/1:100:3459,86:0.0242:20:-56.8186:100
005_chenguoyou  chr2    132181483       132181483       G       T       intergenic      LINC01120,LOC401010     dist=15682;dist=18251   .       .       1       100.00  644     chr2    132181483       rs1059524       G       T       100.00  PASS    DP=644  GT:GQ:AD:VF:NL:SB:GQX   1/1:100:0,644:1.0000:20:-100.0000:100
```
