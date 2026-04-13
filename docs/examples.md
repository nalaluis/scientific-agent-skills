# Real-World Scientific Examples

This document provides comprehensive, practical examples demonstrating how to combine Claude Scientific Skills to solve real scientific problems across multiple domains.

---

## 📋 Table of Contents

1. [Drug Discovery & Medicinal Chemistry](#drug-discovery--medicinal-chemistry)
2. [Cancer Genomics & Precision Medicine](#cancer-genomics--precision-medicine)
3. [Single-Cell Transcriptomics](#single-cell-transcriptomics)
4. [Protein Structure & Function](#protein-structure--function)
5. [Chemical Safety & Toxicology](#chemical-safety--toxicology)
6. [Clinical Trial Analysis](#clinical-trial-analysis)
7. [Metabolomics & Systems Biology](#metabolomics--systems-biology)
8. [Materials Science & Chemistry](#materials-science--chemistry)
9. [Digital Pathology](#digital-pathology)
10. [Lab Automation & Protocol Design](#lab-automation--protocol-design)
11. [Agricultural Genomics](#agricultural-genomics)
12. [Neuroscience & Brain Imaging](#neuroscience--brain-imaging)
13. [Environmental Microbiology](#environmental-microbiology)
14. [Infectious Disease Research](#infectious-disease-research)
15. [Multi-Omics Integration](#multi-omics-integration)
16. [Computational Chemistry & Synthesis](#computational-chemistry--synthesis)
17. [Clinical Research & Real-World Evidence](#clinical-research--real-world-evidence)
18. [Experimental Physics & Data Analysis](#experimental-physics--data-analysis)
19. [Chemical Engineering & Process Optimization](#chemical-engineering--process-optimization)
20. [Scientific Illustration & Visual Communication](#scientific-illustration--visual-communication)
21. [Quantum Computing for Chemistry](#quantum-computing-for-chemistry)
22. [Research Grant Writing](#research-grant-writing)
23. [Flow Cytometry & Immunophenotyping](#flow-cytometry--immunophenotyping)

---

## Drug Discovery & Medicinal Chemistry

### Example 1: Discovery of Novel EGFR Inhibitors for Lung Cancer

**Objective**: Identify novel small molecule inhibitors of EGFR with improved properties compared to existing drugs.

**Skills Used**:
- `database-lookup` - Query ChEMBL, PubChem, COSMIC, AlphaFold DB
- `paper-lookup` - Search PubMed for literature
- `rdkit` - Analyze molecular properties
- `datamol` - Generate analogs
- `medchem` - Medicinal chemistry filters
- `molfeat` - Molecular featurization
- `diffdock` - Molecular docking
- `deepchem` - Property prediction
- `torchdrug` - Graph neural networks for molecules
- `scientific-visualization` - Create figures
- `clinical-reports` - Generate PDF reports

**Workflow**:

```bash
# Always use available 'skills' when possible. Keep the output organized.

Step 1: Query ChEMBL for known EGFR inhibitors with high potency
- Search for compounds targeting EGFR (CHEMBL203)
- Filter: IC50 < 100 nM, pChEMBL value > 7  # loosened from 50 nM to capture more scaffold diversity
- Extract SMILES strings and activity data
- Export to DataFrame for analysis
# NOTE: I've found that bumping the result limit to 500 (default is 100) gives much better
# scaffold coverage here — worth it even if it slows down the initial query a bit.
```
