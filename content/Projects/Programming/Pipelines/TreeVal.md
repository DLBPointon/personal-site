The first nf-core compliant Nextflow pipeline I and my colleagues worked on. TreeVal was born out of a extreme necessity. It's predecessor GeVal, Genome Evaluation, was a genome browser and pipeline. The problem with GeVal was its age, it was built during the Human Genome Project at Sanger. Issues had been plastered over and worked around and it worked pretty well for the next almost 20 years.

However, it's server was slated for decommissioning and the environment GeVal used was simply not able to be containerised and half the software was no longer available for download from the original vendor.

So we started from scratch.

New Genome Browser engine.
New Pipeline.
New Infrastructure.

TreeVal was very much a Guinea pig project, effectively the first in the Tree of Life project to use Nextflow (v22) and NF-Core standards. It shows in the code and how we wrote it. The three of us were experienced bioinformaticians who has used other pipelining languages such as Snakemake and the Nextflow learning curve at the time was rather high. Our blood pressure in getting an alternative pipeline up and running was higher though so we did it.

The pipeline has now been in consistent use for the past 4 years. It has been adopted by various members of EBP (Earth Biogenome Project) as has been translated into Galaxy, although it's moniker has since disappeared.

As of Feb 2026, almost **ALL** Tree of Life genomic assemblies ( + affiliated projects that use GRIT and ToLA services ) have used TreeVal, equating to some 5000 publicly available gold standard genomic assemblies. 

That's pretty awesome.