[FIGURE]

## CoV2K: A Knowledge Base of SARS-CoV-2 Variant Impacts

[FIGURE]

Ruba Al Khalaf , Tommaso Alfonsi , Stefano Ceri , and Anna Bernasconi ( B )

Department of Electronics, Information and Bioengineering, Politecnico di Milano, Via Ponzio 34/5, 20133 Milan, Italy

{ ruba.al,tommaso.alfonsi,stefano.ceri,anna.bernasconi } @polimi.it

Abstract. In spite of the current relevance of the topic, there is no universally recognized knowledge base about SARS-CoV-2 variants; viral sequences deposited at recognized repositories are still very few, and the process of tracking new variants is not coordinated. CoV2K is a manually curated knowledge base providing an organized collection of information about SARS-CoV-2 variants, extracted from the scientific literature; it features a taxonomy of variant impacts, organized according to three main categories (protein stability, epidemiology, and immunology) and including levels for these effects (higher, lower, null) resulting from a coherent interpretation of research articles.

CoV2K is integrated with ViruSurf, hosted at Politecnico di Milano; ViruSurf is globally the largest database of curated viral sequences and variants, integrated from deposition repositories such as COG-UK, GenBank, and GISAID. Thanks to such integration, variants documented in CoV2K can be analyzed and searched over large volumes of nucleotide and amino acid sequences, e.g., for co-occurrence and impact agreement; the paper sketches some of the data analysis tests that are currently under development.

Keywords: SARS-CoV-2 · Variant impact · COVID-19 · base · Data integration · Statistical testing

## 1 Introduction

The global COVID-19 pandemic, caused by the SARS-CoV-2 viral infection, has impacted everyone's lives, with more than 100 million confirmed cases, including more than 2.2 million deaths worldwide, as reported by the World Health Organization on January 31st, 2021 (https://covid19.who.int/). Achieving genetic diversity is an essential aspect for the continuation of SARS-CoV-2 (similarly to other RNA viruses), because it brings viral survival, fitness, and pathogenesis [12]. Therefore, collecting information about genetic variation in SARS-CoV-2 becomes overly necessary, e.g., for studying its relationship with effects on the COVID-19 pandemic [2].

Knowledge

To accomplish this goal, we started to build CoV2K, a knowledge base fuelled by information extracted from published papers and preprints. Unlike in other domains and contexts, automatic text mining methods are not applicable for building CoV2K, because there is not enough good quality material to instruct effective mining methods; therefore, we are building the knowledge base manually, following a systematic procedure.

In organizing the knowledge base, we designed categories that well-represent the impact of virus' variants on viral characteristics, arranged according to three main categories (protein stability, epidemiology, immunology) and including levels for these effects (higher, lower, null). The knowledge base is connected to a massive amount of publicly available data from heterogeneous sources (RefSeq, COG-UK, GenBank, NMDC, and GISAID); this connection is supported thanks to the ViruSurf database [6], a recently developed, integrated and curated resource, hosted by Politecnico di Milano. Furthermore, the knowledge base is connected to the VirusViz service (http://gmql.eu/virusviz/), which allows userprovided data to be analyzed and visualized.

The availability of CoV2K and its connection with ViruSurf and VirusViz opens opportunities for new discoveries, which can be achieved through statistical testing, e.g., about multiple variants co-occurrence and its spreading at given times within populations of particular geographical regions. Thus, it becomes possible to connect knowledge about variants published at a given time to the past and future diffusion of variants within publicly available sequences.

This paper is intended as a progress report and is organized as follows: Sect. 2 overviews how information is acquired and organized within the knowledge base; Sect. 3 describes its connection with the ViruSurf database; Sect. 4 elicits the expected data analysis activities exploiting statistical testing within parametric sub-populations; Sect. 5 finally concludes.

## 2 Knowledge Base Construction

## 2.1 Data Acquisition

The data acquisition protocol is designed for building a comprehensive and well-organized knowledge base, considering both peer-reviewed articles and preprints, with peer-reviewed articles as the most valuable sources. We selected Google Scholar, PubMed, GISAID/COG-UK reports, MedRxiv, and BioRxiv as our data sources; we then selected search keywords, used individually or in pairs/triplets, of:

- -virus terms (SARS-CoV-2, Coronavirus, 2019-nCoV, COVID-19, Spike, lineage, RBD, ...);
- -known clinical impacts (transmission, fatality rate, monoclonal antibodies, phenotype, severe outcome, ...);
- -known variants and/or lineages (variant of interest/VOC, D614G, N501Y, B.1.1.7, UK lineage, Brazilian variant, ...).

Then, we filtered the outcome according to the relevance to the research's topic. We daily perform data searches, noting that the COG-UK report is updated on a bi-weekly basis 1 .

CoV2K structure is composed of three sections. The first section represents the variant characterization, including the protein encoded by the gene (called product), the type of variant (i.e., substitution, insertion or deletion), the amino acid variation (composed of a reference sequence, its position on the reference genome, and an alternative sequence), as well as the identifier of the reference genome used in the study. The second section, which is better defined next, describes the variant's impact (i.e., how the virus behaviour is influenced by the presence of that variant). The third section links the variant to the source of information, defined by the manuscript's author, the DOI, and type of publication. We next define the second section in details.

## 2.2 Taxonomy of Effects

According to epidemiological studies and definitions, we organize variant effects into three categories, as follows:

Protein Stability. In this category, we organize all the variants that could lead to a change in the produced protein's stability (see R203K and G204R in Table 1, as examples). These are reported in structure-related studies focusing on the 'stability' of viral proteins. Several genetic variations are non-synonymous, thus altering the amino acid composition of viral proteins, which will produce a protein with different degrees of stability [5].

Epidemiology. This category is important to understand SARS-CoV-2 evolutionary epidemiology, viral kinetics and dynamics related studies. It includes:

- -Viral transmission , the virus capability to pass from a host to another host [10]. See P323L, D614G, and N501Y in Table 1.
- -Infectivity , the capability of a transmitted virus to actually establish infection [8]. See V367F and D614G in Table 1.
- -Disease severity , an assessment of systematic symptoms caused by the virus [15]. See D614G in Table 1.
- -Fatality rate , the proportion of persons who die after the viral infection over the number of confirmed infected people [8]. See Q57H and P323L in Table 1.

Immunology. This category is concerned with immune response and virushost interactions related studies, including any immune system process that happened in response to a virus-host interaction [10]. This category is important in the vaccine and therapeutic development studies, and it includes three subcategories:

1 Last accessed report (January 31st, 2021) before submission deadline: https://www.cogconsortium.uk/wp-content/uploads/2021/01/Report-2 COG-UK SARS-CoV-2-Mutations.pdf.

Table 1. Example CoV2K variants with the related effect and level, captured on the specified literature publication of different type (publ. = published; prep = preprint).

| Variant   | signature   | signature   | signature   |      | Impact                    | Impact   | Publication      | Publication                                          | Publication   |
|-----------|-------------|-------------|-------------|------|---------------------------|----------|------------------|------------------------------------------------------|---------------|
| Product   | Type        | Orig.       | Position    | Alt. | Effect                    | Level    | Author           | DOI                                                  | Type          |
| N         | SUB         | R           | 203         | K    | Protein stability         | L        | Parvez et al.    | https://doi.org/10. 1016/j.compbiolchem. 2020.107413 | Publ          |
| N         | SUB         | G           | 204         | R    | Protein stability         | L        | Parvez et al.    | https://doi.org/10. 1016/j.compbiolchem. 2020.107413 | Publ          |
| NS3       | SUB         | Q           | 57          | H    | Fatality rate             | L        | Oulas et al.     | https://doi.org/10. 1371/journal.pone. 0238665       | Publ          |
| NSP12     | SUB         | P           | 323         | L    | Viral transmission        | H        | Wang et al.      | https://doi.org/10. 21203/rs.3.rs-49671/ v1          | Prep          |
| NSP12     | SUB         | P           | 323         | L    | Fatality rate             | H        | Toyoshima et al. | https://doi.org/10. 1038/s10038-020- 0808-9          | Publ          |
| Spike     | SUB         | V           | 367         | F    | Infectivity               | H        | Junxian et al.   | https://doi.org/10. 1101/2020.03.15. 991844          | Prep          |
| Spike     | SUB         | D           | 614         | G    | Infectivity               | H        | Korber et al.    | https://doi.org/10. 1016/j.cell.2020.06. 043         | Publ          |
| Spike     | SUB         | D           | 614         | G    | Viral transmission        | H        | Zhang et al.     | https://doi.org/10. 1038/s41467-020- 19808-4         | Publ          |
| Spike     | SUB         | D           | 614         | G    | Viral transmission        | H        | Volz et al.      | https://doi.org/10. 1016/j.cell.2020.11. 020         | Publ          |
| Spike     | SUB         | D           | 614         | G    | Disease severity          | N        | Volz et al.      | https://doi.org/10. 1016/j.cell.2020.11. 020         | Publ          |
| Spike     | SUB         | N           | 501         | Y    | Viral transmission        | H        | Teruel et al.    | https://doi.org/10. 1101/2020.12.16. 423118          | Prep          |
| Spike     | SUB         | N           | 501         | Y    | Binding affinity host rec | H        | Santos et al.    | https://doi.org/10. 1101/2020.12.29. 424708          | Prep          |
| Spike     | SUB         | N           | 439         | K    | Sensitivity to conv. sera | L        | Qianqian et al.  | https://doi.org/10. 1016/j.cell.2020.07. 012         | Publ          |
| Spike     | SUB         | N           | 439         | K    | Sensitivity to mAbs       | L        | Qianqian et al.  | https://doi.org/10. 1016/j.cell.2020.07. 012         | Publ          |

- -Sensitivity to convalescent sera : as in other infections, the convalescent serum from recovered individuals might be used for prevention and treatment of COVID-19 (thus providing passive immunization [1]), as it is assumed that convalescent plasma donors may have developed an effective immune response to the offending pathogen. See N439K in Table 1.
- -Sensitivity to neutralizing mAbs , measuring the sensitivity of the variants towards monoclonal antibodies - the mechanism in which a subset of antibodies blocks the viral infection is called neutralization. This kind of sensitivity has a crucial role in vaccine development. See N439K in Table 1.

- -Binding affinity to host receptor . SARS-CoV-2 is entering the host cells by binding its receptor-binding domain (RBD), in the spike protein, to a cell receptor called angiotensin-converting enzyme 2 (ACE2). Modifying the binding affinity could lead to a change in the efficacy of cell entering. Hence, binding affinity potentially affects cell infectivity and immune evasion [14]. See N501Y in Table 1.

Subcategories may be associated to higher, lower and null levels:

- -Higher (H): the variant's presence leads to an increase of a specific effect.
- -Lower (L): the variant's presence leads to a decrease of a specific effect.
- -Null (N): the variant's presence does not change a specific effect (after testing).

All categories and sub-categories are flexible and will be extended according to the newly studied variants and their timely reported impact. Table 1 represents an excerpt of the current state of the knowledge base, with a few examples of variants' impacts.

## 3 Integration with Sequence Data

ViruSurf is a large integrated database of viral sequences of SARS-CoV-2 (and similar viruses), hosted at http://gmql.eu/virusurf/; it stores all the sequences that have been deposited to GenBank and COG-UK, whereas a similar database, hosted at http://gmql.eu/virusurf gisaid/, stores only a subset of the data and metadata from the GISAID repository, which however includes amino acid variants, the most important information from the knowledge base perspective. An incremental pipeline can be frequently initiated (e.g. on a weekly or bi-weekly basis) in order to add new deposited sequences to the ViruSurf databases; the pipeline applies a variant calling algorithm extracting mutations on both the nucleotide and the amino acid levels, and includes a search for overlapping sequences, since many sequences deposited in GenBank and COG-UK overlap with those deposited in GISAID. As of January 31st, 2021 the databases contain about 500K non-overlapping sequences, with a significant monthly growth rate (15-25%).

Figure 1 represents the logical schema of ViruSurf databases. While the complete ViruSurf schema can be appreciated in [6] based on the Viral Conceptual Model [4], we here report the essential aspects: it is centered on the Sequence table, connected to SequencingProject , Virus , HostSample / HostSpecies , and ExperimentType . The 'analytical' perspective of the schema contains information about Annotation s (characterization of sub-parts of the sequence), NucleotideVariant s and AminoacidVariant s.

The new knowledge base concepts are centered upon two entities, the KbAAVariant and the KbNucVariant , respectively including all the amino acid and nucleotide-level variants captured from our data acquisition process (Sect. 2).

Fig. 1. Schema of the knowledge base connected to the ViruSurf database

[FIGURE]

Two one-to-many relationships connect each variant instance to its possibly many effects, respectively described in KbAAVariantFeature and KbNucVariantFeature .

The connection of the knowledge base to the database requires building bridges from the variant characterization attributes of the knowledge base to the variants in the database. The matching with the ViruSurf tables is depicted in Fig. 1: the products need to match with the annotation table, as shown by the purple arrow/boxes; the variant signatures (original, alternative, type, and position) need to match with the corresponding four fields highlighted by pink arrows/boxes.

## 4 Data Analysis

Basic summary statistics about the CoV2K variants' distribution and their impact can be used to describe CoV2K data, answering questions such as: (i) What is the CoV2K variants' density in a specific gene? (ii) Are there conflicts in specific variant's impact's level (e.g., a variant reporting both H and L levels)? Other simple statistics may relate CoV2K variants to their time and space distribution in the ViruSurf databases, such as: (iii) is there a significant relationship between CoV2K variants and specific geographical areas? (iv) How fast do they spread within such areas?

These observations are important to assess the status of the COVID-19 pandemic (e.g., tracing the Brazilian or South African variants) and can be done with limited delay compared to sequence deposition time in publicly available databases from the various countries. For evaluating the significance of such statistics we use standard tests chosen depending on the type of data, e.g. Fisher's exact test or Chi-squared test on contingency tables by means of aggregate queries on ViruSurf databases. Other statistical analysis are currently under design. Among them, due to space limitations, we only report our current approach to study the knowledge base variants' co-occurrence.

Example on Co-occurring Mutations. We focus on amino acid variants from sequences extracted from ViruSurf (on January 23rd, 2020). For each pair of variants x and y we computed a 2 × 2 contingency table, accounting for the number of sequences containing i) both x and y , ii) only x , iii) only y , and iv) neither of the two. Then, for each contingency table we applied the Cramer's V test [9], i.e., a modified version of the well-known Pearson's Chi-squared test [11] which is preferable in case of large sample sizes 2 . We then built an N × N matrix, where N is the number of distinct pairs of CoV2K variants (possibly paired to their impact) and the elements of the matrix are the results of the Cramer's V test. The goal is to identify pairs of mutations that co-occur in a statistically significant way in the observed population, which also agree/disagree in their impact, as reported in literature and stored in CoV2K; here we considered all publicly available sequences, but we plan to allow the choice of specific subpopulations.

Fig. 2. Result matrix of co-occurrence analysis. Each row/column label represents a variant:effect(first letters):level(L/H).

[FIGURE]

Figure 2 reports an excerpt of our results. Empty cells are not computed as they are symmetrical to the lower triangular matrix; the symbol × indicates positions for the same variants. An explanatory color scheme was used to explain Cramer's V test results:

2 The strength of association ranges from 0 (no association) to 1 (perfect association); the value 0.1 is considered a good significance threshold for the relationship between two variables, see http://www.acastat.com/statbook/chisqassoc.htm.

- -Black captures pairs that are not significant (lower than 0.1), e.g., the black rectangle indicates that D614G in the Spike does not significantly co-occur with the last three variants of the table.
- -Blue captures pairs that are significant (higher than 0.1), e.g., the three values marked by a blue triangle in the figure.
- -Green captures pairs that, in addition to being significant, agree on the same effect and its level (e.g., the Spike protein D614G with the NSP12 protein P323L, and the two N protein substitutions at 203 and 204 positions).
- -Red captures pairs that, in addition to being significant, agree on the effect but report an opposite level. This is the case of NS3 protein Q57H variant - which is reported as decreasing the fatality rate - significantly co-occurring with the NSP12 protein P323L variant - which is instead reported as increasing the fatality rate.

Note that the last three rows of the table represent some of the variants that define the B.1.1.7 lineage 3 , which correspond to the 'UK strain' that raised worldwide attention since December 2020. The Cramer's V test results of these three variants against all the other ones are very similar (see the last three rows of the matrix); the co-occurrence of the three variants is also well documented by the UK strain definition [13].

As the matrix entries proved effective in confirming properties, we may use them also for prediction: by looking at entries within the blue triangle and considering that N501Y is reported as increasing the infectivity of the virus, we could predict the same effect also for P681H and S982A. Such mechanism prompts further investigations of other variant pairs that could be similarly constructed. Referring instead to variants that are not yet described in CoV2K, co-occurrence with variants with a known effect may prompt targeted lab experiments.

## 5 Conclusion

We reported our initial design of a knowledge base of SARS-CoV-2 variants, whose strength lies both in a well-structured procedure for acquiring and organizing data and in the integration with the ViruSurf databases; the interplay between a large amount of up-to-date sequence information and manually curated consolidated knowledge is very promising, as confirmed by our preliminary data analysis results. In the future, we will refine the breadth and complexity of statistical tests, and fine tune them by means of bias correction methods (e.g., [3]) and by choosing thresholds appropriate for large samples (e.g., [7]).

The effectiveness of CoV2K will be evaluated with the help of domain experts that will also inspire more complex analyses to increase its benefits. CoV2K

[3 https://virological.org/t/preliminary-genomic-characterisation-of-an-emergentsars-cov-2-lineage-in-the-uk-defined-by-a-novel-set-of-spike-mutations/563.](https://virological.org/t/preliminary-genomic-characterisation-of-an-emergent-sars-cov-2-lineage-in-the-uk-defined-by-a-novel-set-of-spike-mutations/563)

is by now only a taxonomy, but we will consider building a richer semantic representation of its elements, thereby helping automate reasoning and statistical tests.

Acknowledgment. This research is funded by the ERC Advanced Grant 693174 GeCo (data-driven Genomic Computing).

## References

1. Abraham, J.: Passive antibody therapy in COVID-19. Nat. Rev. Immunol. 20 (7), 401-403 (2020)
2. Bernasconi, A., Canakoglu, A., Masseroli, M., Pinoli, P., Ceri, S.: A review on viral data sources and search systems for perspective mitigation of COVID-19. Briefings Bioinform. 22 (2), 664-675 (2021). https://doi.org/10.1093/bib/bbaa359
3. Bergsma, W.: A bias-correction for Cram´ er's V and Tschuprow's T. J. Korean Stat. Soc. 42 (3), 323-328 (2013)
4. Bernasconi, A., Canakoglu, A., Pinoli, P., Ceri, S.: Empowering virus sequence research through conceptual modeling. In: Dobbie, G., Frank, U., Kappel, G., Liddle, S.W., Mayr, H.C. (eds.) Conceptual Modeling, pp. 388-402. Springer International Publishing, Cham (2020). https://doi.org/10.1007/978-3-030-62522-1 29
5. Brinda, K., Vishveshwara, S.: A network representation of protein structures: implications for protein stability. Biophys. J. 89 (6), 4159-4170 (2005)
6. Canakoglu, A., Pinoli, P., Bernasconi, A., Alfonsi, T., Melidis, D.P., Ceri, S.: ViruSurf: an integrated database to investigate viral sequences. Nucleic Acids Res. 49 (D1), D817-D824 (2021)
7. Cao, H., Hripcsak, G., Markatou, M.: A statistical methodology for analyzing cooccurrence data from a large sample. J. Biomed. Inform. 40 (3), 343-352 (2007)
8. Centers for Disease Control and Prevention: Principles of epidemiology in public health practice; an introduction to applied epidemiology and biostatistics. Atlanta, GA: US Dept. of Health and Human Services, Centers for Disease (2006). https:// www.cdc.gov/csels/dsepd/ss1978/ss1978.pdf. Accessed 31 Jan 2021
9. Cram´ er, H.: Mathematical Methods of Statistics. vol. 43. Princeton University Press (1946)
10. He, Y., et al.: CIDO, a community-based ontology for coronavirus disease knowledge and data integration, sharing, and analysis. Sci. Data 7 (1), 1-5 (2020)
11. Pearson, K.: X. On the criterion that a given system of deviations from the probable in the case of a correlated system of variables is such that it can be reasonably supposed to have arisen from random sampling. The London, Edinburgh, Dublin Philos. Mag. J. Sci. 50 (302), 157-175 (1900)
12. Rahimi, A., Mirzazadeh, A., Tavakolpour, S.: Genetics and genomics of SARSCoV-2: a review of the literature with the special focus on genetic diversity and SARS-CoV-2 genome detection. Genomics (2020)
13. Rambaut, A., et al.: A dynamic nomenclature proposal for SARS-CoV-2 lineages to assist genomic epidemiology. Nat. Microbiol. 5 (11), 1403-1407 (2020)
14. Shang, J., et al.: Cell entry mechanisms of SARS-CoV-2. Proc. Natl. Acad. Sci. 117 (21), 11727-11734 (2020)
15. Wu, J.T., et al.: Estimating clinical severity of COVID-19 from the transmission dynamics in Wuhan. China. Nat. Med. 26 (4), 506-510 (2020)
