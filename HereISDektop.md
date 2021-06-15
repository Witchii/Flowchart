

~~~mermaid

graph 

   
    A("Map reads: input: .fasta + .tab.gz <b>Reference:</b> <a href='https://lh3.github.io/minimap2/minimap2.html'>Minimap2 Manual</a> <b>Download Genomic Data (gff, gtf, .tab.gz, etc.)</b> <a href='https://tritrypdb.org/tritrypdb/app'>TriTrypDB") -->|Run minimap script <b>Example:</b> <a href='https://mcgill-my.sharepoint.com/personal/igor_cestari_mcgill_ca/_layouts/15/onedrive.aspx?ct=1622781833281&or=OWA%2DNT&cid=6c24c8c4%2Da145%2D00bf%2D30f0%2D92dffefc8f5e&originalPath=aHR0cHM6Ly9tY2dpbGwtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvaWdvcl9jZXN0YXJpX21jZ2lsbF9jYS9FaXpDNXhjaUhPUk5tZkctUklhQTdvSUJMLWQwbzNGREVmaVdTLVlpclplY3hBP3J0aW1lPVMxNDBYUk1uMlVn&id=%2Fpersonal%2Figor%5Fcestari%5Fmcgill%5Fca%2FDocuments%2FLaboratory%2FBioinformatics%2FAnalysis%2FMinimap2%20N0015%20analysis%2Etxt&parent=%2Fpersonal%2Figor%5Fcestari%5Fmcgill%5Fca%2FDocuments%2FLaboratory%2FBioinformatics%2FAnalysis'>Igor's Script</a>| B("Output:Sam file <b>Additional Info:</b> <a href='https://samtools.github.io/hts-specs/SAMv1.pdf'>Sam Format Info</a>, <a href='https://mcgill-my.sharepoint.com/personal/igor_cestari_mcgill_ca/_layouts/15/Doc.aspx?sourcedoc={4a0d59ef-e8c5-471c-8c3e-81982ea6339f}&action=edit&wd=target%28Untitled%20Section.one%7C907620c9-3aea-42fb-ac4d-d2ce227df85c%2FFlowchart%7C7baa7b8a-64b2-4292-8eb8-786eaf5777d8%2F%29'>Mira's Notebook");
     B--> C(Run samtools flagstat and stat <b>Additional Info:</b> <a href='http://www.htslib.org/doc/samtools.html'>Samtools Cmds);
     C-->|Good Mapping| D("Samtools sam to bam, sort and index: <a href='https://mcgill-my.sharepoint.com/personal/igor_cestari_mcgill_ca/_layouts/15/Doc.aspx?sourcedoc={4a0d59ef-e8c5-471c-8c3e-81982ea6339f}&action=edit&wd=target%28Untitled%20Section.one%7C907620c9-3aea-42fb-ac4d-d2ce227df85c%2FFlowchart%7C7baa7b8a-64b2-4292-8eb8-786eaf5777d8%2F%29'>Mira's Notebook")
     C-->|Low Mapping|E(Play with parameters);
     E-->A
     D-->|Output sorted.bam & .bam.bai|F(Analyze Using DeepTools: <a href='https://deeptools.readthedocs.io/en/develop/content/tools/bamCoverage.html'>bamCoverage</a>, <a href='https://deeptools.readthedocs.io/en/develop/content/tools/plotCoverage.html?highlight=plotcoverage'>plotCoverage </a> and <a href='https://deeptools.readthedocs.io/en/develop/content/tools/bamCompare.html?highlight=bamcompare'>bamCompare)
     F-->I
     F-->H
     H(Wt data)-->G
     
   I(Treatment data)-->G(<a href='https://deeptools.readthedocs.io/en/develop/content/tools/bamCompare.html?highlight=bamcompare'>bamCompare)
   G-->J(Visualize using IGV )
   


~~~



 

