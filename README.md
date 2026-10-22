# Human CCL4 Gene Structure and Transcript Analysis

## Overview

This project explores the human **CCL4 (C-C motif chemokine ligand 4)** gene using NCBI and Ensembl gene annotation resources. The analysis examines transcript isoforms, protein lengths, protein-domain annotations, and selected genomic features, including an upstream TATA box and a palindromic sequence reported in exon 2.

The project also demonstrates the creation of a 0-indexed BED file for representing genomic features and their visualization in NCBI Variation Viewer.

## Objectives

- Compare CCL4 transcript annotations reported by NCBI and Ensembl.
- Examine transcript isoforms and their reported protein lengths.
- Identify the Chemokine interleukin-8-like domain using Pfam annotations.
- Map the TATA box and palindromic sequence to genomic coordinates.
- Generate a BED file containing the two genomic features.
- Document the use of genome visualization tools to inspect genomic locations.

## Tools and Resources

- **NCBI Gene and Variation Viewer** — gene annotation and genomic feature visualization.
- **Ensembl** — transcript and protein annotation.
- **Pfam** — protein-domain annotation.
- **BED format** — genomic feature representation.
- **Python** — generation of a BED file from documented coordinates.

## Gene and Transcript Analysis

The original coursework examined the human CCL4 gene, which was historically referred to as the Act-2 cytokine gene.

The NCBI gene page listed transcript NM_002984.4, with a reported protein length of 92 amino acids. The coursework also examined three Ensembl transcript records:

| Transcript | Transcript ID | Information recorded in the coursework |
|---|---|---|
| CCL4-202 | ENST00000615863.2 | 92 amino acids |
| CCL4-203 | ENST00000621626.1 | 52 amino acids |
| CCL4-201 | ENST00000613947.1 | Retained intron; no protein reported |

**Note:** The original coursework contains inconsistent protein-length descriptions. A later paragraph reports 69 and 65 amino acids for two additional transcripts, conflicting with the transcript-specific values above. These values should be verified against the current Ensembl annotations before drawing conclusions about the relative lengths of the isoforms.

## Protein-Domain Annotation

The Chemokine interleukin-8-like domain was identified using the Pfam annotation for CCL4-202.

- **Pfam accession:** PF00048
- **Reported amino acid range:** 33–87

This range is recorded from the original coursework and should be checked against the relevant Ensembl protein annotation when reproducing the analysis.

## Genomic Feature Mapping

The transcription start site was documented at chromosome 17, position 36,103,827.

Two features were mapped:

1. **TATA box:** Located upstream of the transcription start site, between the positions calculated from the offsets of 28 and 23 bases upstream.
2. **Palindromic sequence:** Reported in exon 2, with the sequence `GCGAGGAAGCTTCCTCGC`.

The original analysis recorded the following BED entries:

| Feature | Chromosome | BED start | BED end | Strand |
|---|---|---:|---:|---|
| TATA box | chr17 | 36103798 | 36103804 | + |
| Palindromic sequence | chr17 | 36104568 | 36104586 | + |

BED uses 0-based, half-open coordinates: the start is included, and the end is excluded. The palindromic sequence coordinates above are transcribed from the coursework and should be independently verified against the reference genome and transcript annotation.

## Methodology

1. Inspect CCL4 gene and transcript records in NCBI and Ensembl.
   <img width="2590" height="238" alt="image" src="https://github.com/user-attachments/assets/ac592fb6-4a86-4112-ba2a-fc2108b9c764" />

   <img width="2594" height="286" alt="image" src="https://github.com/user-attachments/assets/c4553650-ce92-4c4c-880c-b1516ee4a9b8" />

3. Record the transcript identifiers, reported protein lengths, and protein-domain coordinates.
   <img width="2404" height="1230" alt="image" src="https://github.com/user-attachments/assets/1d84219f-2852-469d-9b59-ae5dba7d3db6" />

5. Calculate the TATA box coordinates using the documented transcription start site and upstream offsets.
6. Record the genomic interval for the reported palindromic sequence.
7. Generate a BED file containing the two features.
8. Load the BED features into NCBI Variation Viewer and inspect their positions relative to the gene and transcript structure.

## Results

The coursework documented a TATA box upstream of the CCL4 transcription start site and a palindromic sequence in exon 2. It also recorded a Pfam chemokine domain and differences among Ensembl transcript annotations.

The original assignment included screenshots intended to show the TATA box and transcription start site, as well as the palindromic sequence within exon 2. These images can be added to the repository as supporting evidence when available.

<img width="2186" height="276" alt="image" src="https://github.com/user-attachments/assets/cc3cdf5b-4fbb-4b0d-b50d-88c30217a75e" />
The transcription start site is at 36,103,827 on chromosome 17.
The TATA box starts 28 bases upstream -36,103,827 -28=36,103,799
36,103,799 -1 =36,103,798 to zero index
Ends 23 bases upstream-36,103,827 -23=36,103,804.
The TATA box is on the 5’-3’ direction strand (from NCBI variation viewer)
chr17 36103798 36103804 TATA_box 0 +
<img width="1014" height="280" alt="image" src="https://github.com/user-attachments/assets/ef9c206f-93b8-4f47-bec2-2782995b6eae" />
<img width="2382" height="454" alt="image" src="https://github.com/user-attachments/assets/c1bbab7c-7016-4074-bd79-84054438b44c" />
The palindrome sequence is GCGAGGAAGCTTCCTCGC.

## Limitations

- Transcript protein lengths in the original report are inconsistent and require verification.
- Genomic coordinates were recorded from the original coursework and have not been independently revalidated.
- The project documents annotation and feature mapping; it does not establish a biological function for the palindromic sequence.
- The original coursework noted that the biological significance of the palindrome was unknown.

## Repository Structure

```text
ccl4-gene-transcript-analysis/
├── README.md
├── results/
│   └── ccl4_features.bed
```

## Project Status

Coursework-based genomics project. The original observations and coordinates are documented, and a script is provided to generate the BED file. 
