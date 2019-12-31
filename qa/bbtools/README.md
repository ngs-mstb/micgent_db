- `hg19_main_mask_ribo_animal_allplant_allfungus.fa.gz` - masked Human reference 
  for human (animal) contaminant removal from [this post](http://seqanswers.com/forums/showthread.php?t=42552)
  The commands to use it:
  ```
  bbmap.sh ref=hg19_main_mask_ribo_animal_allplant_allfungus.fa.gz -Xmx23g
  bbmap.sh minid=0.95 maxindel=3 bwr=0.16 bw=12 quickmatch fast minhits=2 path=/path/to/hg19masked/ \
      qtrim=rl trimq=10 untrim -Xmx23g in=reads.fq outu=clean.fq outm=human.fq
  ```
