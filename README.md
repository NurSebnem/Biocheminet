# BioChemiNet
BioChemiNet algorithm is proposed as a novel algorithm that improves classification performance by utilizing Comparative Toxıcogenomıcs Database as external biological information while selecting the most relevant genes from gene expression datasets. The novelty and originality of our approach stems from its capability to explore the specific ontology groups to classify and find the most relevant groups for a disease. Our approach differs from conventional approaches where searching is done by considering individual genes.

# Data Preparation
Gene expression datasets for different types of human complex diseases is required to be downloaded from Gene Expression Omnibus (https://www.ncbi.nlm.nih.gov/geo/)
The dataset, which contains chemicals and their associated genes, was downloaded from the Comparative Toxicogenomics Database (CTD). The dataset contains information on 10,841 unique chemicals and 28,022 genes, resulting in 76,772 chemical-gene associations.  This information serves as the foundation for the Grouping component, which creates gene groups by considering known gene-chemical associations. These groups are intended to reflect biologically meaningful patterns that guide the subsequent scoring and modeling steps.
•	The link for downloading KNIME: https://www.knime.com/downloads
•	For more information about the Knime platform, please visit https://www.knime.com/software-overview
The Environment Settings of Biocheminet
After installing KNIME Analytics platform, Biocheminet workflow is downloaded and imported into the KNIME. The workflow contains R scripts therefore the following commands should be followed to prevent errors. Before initiation of the workflow process in KNIME, R / RStudio is required to be run with following commands:
•	library(Rserve);
•	Rserve(args = "--vanilla")
•	library(tidyr)
Execution of R / RStudio and the workflow simultaneously enables the Biocheminet analysis without retrieving any error.

