# Biocheminet
BioChemiNet, a computational tool developed to identify gene-chemical associations through a methodology that incorporates grouping, scoring, and modeling approaches. BioChemiNet consists of three main components: (1) grouping genes based on known chemical-gene associations, (2) assessing these groups of genes by a Random Forest classifier combined with cross-validation to identify their relevance, and (3) creating predictive models with the top-scoring gene groups to reveal potential links to chemicals. In contrast to existing methods, BioChemiNet prioritizes biological interpretability by integrating curated chemical knowledge during the grouping phase. Using ten human gene expression datasets for various complex diseases from the Gene Expression Omnibus (GEO) database, we demonstrate that BioChemiNet efficiently identifies significant gene–chemical associations, achieving high performance across diverse datasets. 

# Data Preparation
Gene expression datasets for different types of human complex diseases is required to be downloaded from Gene Expression Omnibus (https://www.ncbi.nlm.nih.gov/geo/)

# Chemical-Gene associations from CTD
The dataset, which contains chemicals and their associated genes, was downloaded from the Comparative Toxicogenomics Database (CTD) (https://academic.oup.com/nar/article/53/D1/D1328/7816860, https://ctdbase.org/). The dataset contains information on 10,841 unique chemicals and 28,022 genes, resulting in 76,772 chemical-gene associations.  This information serves as the foundation for the Grouping component, which creates gene groups by considering known associations between genes and chemicals. These groups are intended to reflect biologically meaningful patterns that guide the subsequent scoring and modeling steps.

# Environmental settings 
Download Knime opensource platform. The link for downloading KNIME: https://www.knime.com/downloads
For more information about the Knime platform, please visit https://www.knime.com/software-overview

After installing KNIME Analytics platform, GeNetOntology workflow is downloaded and imported into the KNIME. The workflow contains R scripts therefore the following commands should be followed to prevent errors. Before initiation of the workflow process in KNIME, R / RStudio is required to be run with following commands:

library(Rserve);
Rserve(args = "--vanilla")
library(tidyr)
Execution of R / RStudio and the workflow simultaneously enables the GeNetOntology analysis without retrieving any error.
