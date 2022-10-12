# while running samtools view to retrieve htseq count data from aligned data 

      samtools view -h /your/path/to/yourfile.bam | htseq-count \
      --mode intersection-strict \
      --stranded no \
      --nonunique all \
      --additional-attr gene_name \
      --idattr=gene_id - /your/path/to/yourannotation.gtf  > /your/path/to/yourcount.txt
      
for idattr -Name, the error code is   Feature ENSG00000223972.5 does not contain a 'Name' attribute


Try one of the enlisted attributes instead 


      gene_id "ENSG00000223972.5"; transcript_id "ENST00000456328.2"; gene_type "transcribed_unprocessed_pseudogene"; gene_name "DDX11L1"; transcript_type "lncRNA"; transcript_name "DDX11L1-202"; exon_number 1; exon_id "ENSE00002234944.1"; level 2; transcript_support_level "1"; hgnc_id "HGNC:37102"; tag "basic"; havana_gene "OTTHUMG00000000961.2"; havana_transcript "OTTHUMT00000362751.1";
