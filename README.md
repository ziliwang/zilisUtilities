#Contents
 1. ResMon
 1. STGffparser
 1. gene_exp_diff_hub
 1. vcf_vol_annovar
 1. SeqExtractor

---
##ResMon
#####Description
ResMon is a tool to monitor the resources occupation of a process, include the child processes. The resources include memory, IO, and CPU.
#####Algorithm
| resource | algorithm |
| -------- | --------- |
| memory   | linux command pmap |
| cpus | linux command ps |
| IO | linux process Io file |
| aggregate | recursive addition of all child processes(produced by target process) , and the relationship bettwen process is ruled by linux command ps | 
#####Output
`cpus(%) mem(kb) io_read(byte)   io_write(byte)  
198     11776088        46644326647     1205  
198     12045612        48769183884     1205  
198     12461844        50402165678     1205  
198     12605272        52983719064     1205  
198     12956880        55502651546     1205  
198     13685860        58451824705     1205  
198     14301264        60884752982     1205  
198     14600644        64972776644     1205  
198     14906232        66741794085     1205  
198     15483456        69228065898     1205  
`
