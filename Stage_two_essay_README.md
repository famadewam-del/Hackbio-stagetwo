
**Hack-bio_stage_2_essay**

- What cells types did you identify?

The cells identified were:

- Monocytes
- T cells
- B cells naïve
- Platelets
- Plasma cells

- Explain the biological role of each cell type?

**Monocytes:** Innate immune cells circulating in the blood. They also play a role in both the inflammatory and anti-inflammatory processes that take place during an immune response

**T cells:** Adaptive immune cells responsible for killing infected cells, coordinating immune responses, and providing memory immunity. These cells play a vital role in both components of active immunity, including cell-mediated and to some extent humoral immunity

**B cells naïve:** Immature B lymphocytes that have **not yet encountered an antigen.** They circulate between blood, lymph nodes, and spleen. Once activated, they differentiate into memory B cells or plasma cell

**Platelets:** Fragments produced by megakaryocytes. They play major roles in **blood clotting,** wound repair, and inflammation.

**Plasma cells:** Terminally differentiated B cells that produce and secrete **large amounts of antibodies.** Many plasma cells **reside in the bone marrow long-term.**

- **Is the tissue source really bone marrow? Justify your answer**
- **A true bone-marrow sample should show:**

- Multiple **erythroid lineage** stages (proerythroblasts → erythroblasts)
- **Myeloid/granulocyte precursors** (neutrophil lineage)
- **Megakaryocyte / platelet precursors** (megakaryocyte transcriptional program).
- HSPC / early lymphoid developmental stages

But instead what was observed was monocytes, t cells, b cells naïve, platelets and plasma cells

- **Typical distributions (qualitative expectations):**

- **Bone marrow:** mixed composition with large fractions of erythroid and myeloid precursors; lymphoid cells are present but generally **not dominant**. HSPCs are rare but detectable.
- **Peripheral blood / PBMCs:** dominated by **T cells** (often 50-75% of PBMCs), B cells a minority (5-20%), monocytes ~5-10%, plasma cells usually absent or extremely rare.

**Observed distribution (heat map):**

- **T cells dominate** the dataset.
- Monocytes and naïve B cells present at modest proportions.
- Plasma cells present but small. Platelet signal small.

Note: Dominance of T cells with lack of erythroid/myeloid precursor fractions aligns with **PBMC** distributions and contradicts the expected marrow distribution.

- **Presence of absence of progenitors**

**Critical test:** detection of progenitor/HSPC markers (e.g. **CD34, KIT, and PROM1**) or transcriptional programs for erythropoiesis/myelopoiesis is the single most decisive indicator of marrow tissue.

**Observed:** no evidence in the heat map for a CD34+/HSPC cluster or transcriptional signatures of erythroid or granulocytic precursors.

### ****4\.** Based on the relative abundance of cell types, is the patient healthy or infected?**

Use the cluster proportions to make a call.

**Neutrophils:**

**Observation:** there is **no neutrophil / granulocyte cluster** visible.  
**Why that matters:** neutrophils are normally lost in Ficoll/PBMC preps and therefore absent from PBMC UMAPs. Their absence here is expected and **uninformative** about infection from this dataset.  
**Scientific rule:** you cannot use neutrophil counts from this PBMC dataset to infer infection.  
**What would change the inference:** if you had whole-blood scRNA (or CBC) showing **absolute neutrophilia** (neutrophils > normal range, or >70% of leukocytes) or emergency granulopoiesis signatures (ELANE/MPO upregulation, immature granulocyte clusters), that would support bacterial infection. We do **not** see that here.

**Conclusion (neutrophils):** **unassessable** from these data → does not support infection.

**Monocytes**

**Observation:** monocytes (cluster 0) are present at a **modest proportion (~8-12%) -** typical for PBMCs. The cluster is neither small/absent nor massively expanded.  
**Biological expectation:** in systemic bacterial infection or strong innate activation, monocytes often expand (>20-30% of PBMCs) and show activation markers (HLA-DR up, IL1B/TNF, CD14/CD16 shifts).  
**Interpretation:** the observed monocyte proportion is within normal PBMC range. No visual evidence of dramatic expansion.  
**Quantitative rule:** if **monocytes >20-30%** and express activation transcripts (IL1B, TNF, high HLA-DR) → supports acute infection. Here **monocytes ≈10%** → argues **against** acute systemic innate activation.

**Conclusion (monocytes):** proportion **does not indicate** infection.

**NK cell activation states**

Observation: no NK cluster is annotated or apparent. (If NK cells were present they'd usually form a distinct UMAP cluster.)  
Why that matters: NK activation (expanded/activated NK with GZMB, GNLY, NKG7, CD69/HLA-DR) is a sensitive signal of certain viral infections. Without an NK cluster or marker data we cannot evaluate.  
**Interpretation:** absence of NK cluster → insufficient data to call NK activation. You must check NK markers (KLRD1, NKG7, GNLY, GZMB, PRF1).  
**Quantitative rule:** expansion of NKs (>2-3× normal PBMC fraction) and upregulation of cytotoxic genes → supports viral response. None of that is visible.

**Conclusion (NK cells):** insufficient information - does not support infection in the presented data.

**Lymphocyte depletion or expansion (T / B / plasma)**

Observations:

- T cells dominate (~60-65%) - typical for healthy PBMC. No obvious depletion.
- Naïve B cells (~12-18%) - within normal PBMC range.
- Plasma cells (~4-8%) - present but small; not a large plasmablast expansion.

**Biological interpretation:**

- **Lymphopenia / T-cell depletion** (seen in some severe viral infections) would show markedly reduced T-cell proportion and/or reduced absolute T counts. We do not see that.
- **Plasmablast/plasma expansion** (acute humoral response) typically appears as a distinct, relatively large plasmablast cluster (often >2-5% and often proliferative/MKI67+). Here plasma cells are small and not obviously a large proliferative plasmablast population.

**Quantitative rule:**

- **T-cell depletion:** T cells << expected (e.g., <30-40% in PBMC UMAP) → suggests lymphopenia. Not observed.
- **Plasmablast surge:** plasmablasts/plasma cells >5% with PRDM1/SDC1/IGHG and MKI67 → suggests acute recent humoral activation. Here plasma ≈4-8% visually, but there is no evidence of a large, proliferative plasmablast cluster.

**Conclusion (lymphocytes):** **no evidence** of lymphocyte depletion or of a robust plasmablast expansion consistent with acute infection.
