# CrossDome-onNotebook

<img src="https://dinlerantunes.com/assets/images/lab-logo.png" height="200">


# Welcome to CrossDome on Jupyter!

---

The complete CrossDome source and documentation are available at https://github.com/AntunesLab/crossdome

---

***If you use crossdome in published research, please cite:***
Fonseca AF, Antunes DA. CrossDome: an interactive R package to predict cross-reactivity risk using immunopeptidomics databases. Front Immunol. 2023;14:1142573. Published 2023 Jun 12. doi:10.3389/fimmu.2023.1142573

---

**Acknowledgments**
The Jupyter Notebook was created by the Antunes lab members: Martiela Freitas and Pamella Borges.

---

## Instructions

This CrossDome on Jupyter was developed to facilitate the use of the tool for those with little or no knowledge of the R language. Each step is described as follows:

1. **Downloading the necessary libraries**: This Jupyter notebook was developed in R, as CrossDome was also developed in R. In this cell, you will download and install all the necessary libraries.

2. If you don't have R installed on your computer, please follow the instructions to install it: https://www.r-project.org/.

3. After you have installed R, please open R in your terminal and install the IRkernel:

<pre> install.packages('IRkernel')
    IRkernel::installspec(user = FALSE) </pre>

4. Verify you are running your Jupyter notebook with R. In the upper right corner, confirm whether the Select Kernel is R.


5. **Loading Data**: Now it's time to inform your data. Select your option and run the cell. Bellow the cell a message will be prompted with a query are to be filled.

- *Single entry*: chose this if you have a single peptide and HLA targets.
```
Please complete the allele are with the format: HLA-A*02:01
```

   Inform your allele and press Return/Enter.

   Next, CrossDome will request your peptide target:
```
Please complete the peptite in the query area:
```
Inform your peptide and press Return/Enter.


- *Multiple entry*: chose this if you have a multiple peptides and/or HLA targets.
```
Please upload the table to your drive and give the path for a CSV table formatted as indicated in the instructions:
```
The table should have the following format:

| Allele   | Peptide |
| -------- | ------- |
| HLA-B*07:01 | RPILTISTL |
| HLA-B*07:02 | RPILTISTL |

You can have as many peptide and HLA combinations as you want.
Beware that CrossDome current is based on 9mer peptide dataset only.
To properly run CrossDome on your targets a full file needs to be provided.
This table should be saved on your drive or uploaded to the content area.

If you have uploaded the table.csv to your Google Drive, your path should look as: ```/content/drive/MyDrive/path/to/table.csv```

If you have uploaded the table.csv to the Colab content area, the path should look as: ```/content/table.csv```

6. **Run CrossDome**: Run this cell to generate your results. The outputs will be:

- Allele_Peptide.csv with the peptide rank list.
- Allele_Peptide_expression_heatmap.pdf with the gene donor expression profile.
- Allele_Peptide_tissue_specificity.pdf with the bar plot summarizing the tissue-specificity groups.
- Allele_Peptide_cross_substitution.pdf with the heatmap combined with seqlogo displaying amino acid substitutions.
