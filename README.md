# FASTQ

# Prerequisite software
apt install sra-toolkit 
# To retreive FASTQ use SRA toolkit and NCBI database. Go to https://www.ncbi.nlm.nih.gov/sra
![Screenshot from 2022-04-06 14-30-39](https://user-images.githubusercontent.com/93121277/161974981-7ad934c5-1eda-4f2c-8924-40b948d83ba9.png)
# There is one Result
![Screenshot from 2022-04-06 14-32-22](https://user-images.githubusercontent.com/93121277/161975243-e3e77f29-8049-4237-9e2c-da203c21b993.png)
# Click of the Hyperlink
![Screenshot from 2022-04-06 14-33-11](https://user-images.githubusercontent.com/93121277/161975388-5a442821-6b6a-4f86-a5d4-36fbb7a49b2b.png)
# Look at the Metadata
![Screenshot from 2022-04-06 14-35-19](https://user-images.githubusercontent.com/93121277/161975754-a416bbfd-f93c-4358-9e8a-8579fd219cb1.png)
# It matches linux command line standard output:
![Screenshot from 2022-04-06 14-29-10](https://user-images.githubusercontent.com/93121277/161975870-38ced2e9-e793-4172-b852-cf439c5aab84.png)

# The Following R Package "fastqcr" can analyze a FASTQ sample like this one or multiple FASTQ files

```r
setwd("/home/michael/Desktop/SRA")
install.packages("fastqcr")
library(fastqcr)
fastqc_install()
fastqc(fq.dir = "/home/michael/Desktop/SRA/FASTQ",threads = 4)

# Generating fastqc file automatically makes a FASTQC directory
qc.file <- "/home/michael/Desktop/SRA/FASTQ/FASTQC/SRR2121685_fastqc.zip"
#Read fastqc file
qc <- qc_read(qc.file)
#Produce Names
names(qc)
#Plotting
qc_plot(qc, "summary")
qc_plot(qc, "Basic statistics")
qc_plot(qc, "Per base sequence quality")
qc_plot(qc, "Per base sequence content")
qc_plot(qc, "Per sequence GC content")
qc_plot(qc, "Per sequence quality scores")
qc_plot(qc, "Sequence duplication levels")
qc_plot(qc, "Per base N content")
qc_plot(qc, "Sequence length distribution")
qc_plot(qc, "Sequence duplication levels")
qc_plot(qc, "Overrepresented sequences")
qc_plot(qc, "Adapter content")
qc_plot(qc, "Kmer content")

```

# qc_plot(qc, "summary")
![Screenshot from 2022-04-06 15-23-25](https://user-images.githubusercontent.com/93121277/161984831-aa74665e-c12e-4879-92f9-b720afe7cd9b.png)

# qc_plot(qc, "Basic statistics")
![Screenshot from 2022-04-06 15-24-09](https://user-images.githubusercontent.com/93121277/161984918-00c483af-38ff-4811-94a4-5632aefd7b24.png)

# qc_plot(qc, "Per base sequence quality")
![Screenshot from 2022-04-06 15-24-59](https://user-images.githubusercontent.com/93121277/161985072-8cedc4a9-736b-47c4-83cd-136c29988dd5.png)

# qc_plot(qc, "Per base sequence content")
![Screenshot from 2022-04-06 15-36-10](https://user-images.githubusercontent.com/93121277/161987332-54da0fa7-557c-48e9-9bb8-13501ece3819.png)

# qc_plot(qc, "Per sequence GC content")
![Screenshot from 2022-04-06 15-25-41](https://user-images.githubusercontent.com/93121277/161985197-c598e482-db5e-4e89-841f-fcc15a8eb6b2.png)

# qc_plot(qc, "Per sequence quality scores")
![Screenshot from 2022-04-06 15-26-16](https://user-images.githubusercontent.com/93121277/161985346-f62198cf-3375-4ce2-a474-d3a3423dff7c.png)

# qc_plot(qc, "Sequence duplication levels")
![Screenshot from 2022-04-06 15-26-57](https://user-images.githubusercontent.com/93121277/161985438-04e7857c-b85b-4896-8a97-76c01498c9d2.png)

# qc_plot(qc, "Per base N content")
![Screenshot from 2022-04-06 15-27-33](https://user-images.githubusercontent.com/93121277/161985583-1f6637a5-6656-4474-af4c-446d3e15bef4.png)

# qc_plot(qc, "Sequence length distribution")
![Screenshot from 2022-04-06 15-28-26](https://user-images.githubusercontent.com/93121277/161985754-7205a652-e9e9-4bbd-830e-14e255204de8.png)

# qc_plot(qc, "Sequence duplication levels")
![Screenshot from 2022-04-06 15-28-59](https://user-images.githubusercontent.com/93121277/161985862-6be20228-da23-4a14-ac73-6dc84968f12f.png)

# qc_plot(qc, "Overrepresented sequences")
![Screenshot from 2022-04-06 15-29-50](https://user-images.githubusercontent.com/93121277/161986031-69bf7832-041c-40a5-b82a-6ef9112b7a2b.png)

# qc_plot(qc, "Adapter content")
![Screenshot from 2022-04-06 15-30-26](https://user-images.githubusercontent.com/93121277/161986133-8ade0494-0780-4f73-9851-fcd2e709f352.png)

# qc_plot(qc, "Kmer content")
# ERROR










