Getting and Cleaning a Machine Learning Dataset
---------------------------------------------
Author: AnVIX --
Date: Friday, June 19, 2015


**Project summary**: collect and process the [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#) database to create the tidy dataset `MergedAvg`. The raw data is available from the University of California, Irvine, [UCI, Machine Learning Repository](http://archive.ics.uci.edu/ml/). Data processing is achieved by means of the **run_analysis.R** script while **CoodBook.md** serves as a detailed Code Book for `MergedAvg`.

---

### Repository table of contents

* **README.md** (this file)
* **run_analysis.R**
* **CodeBook.md**

---

Data description
----------------

#### The raw dataset

Details about The Human Activity Recognition Using Smartphones Dataset, HARUS [[1]](#Ref1) experiments are available using this [link](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#) as well as from the measurements associated 'README.txt' file. The database was collected in experiments using recordings of 30 volunteer persons (`Subject`), aged [19-48], performing daily-living activities (`Activity`) while carrying a waist-mounted Samsung Galaxy S II smartphone. The smartphone was equipped with two sensors: an accelerometer and a gyroscope that recorded, respectively, the 3-axial linear acceleration and 3-axial angular velocity signals of the subject. The experiments were video-recorded to label the data manually. The measurements were randomly partitioned into two sub-sets: `Training` (70%) and `Test` (30%).

 
#### The tidy dataset

The HARUS raw data files used to create the tidy set `MergedAvg` are summarized in the accompanying **CodeBook.md**. Data processing performed by **run_analysis.R** includes: grouping information from data files, subsetting to retain only a set of variables, and aggregating these variables as averages per Subject and per Activity.  
The principles applied here to prepare `MergedAvg` were discussed in the Journal of Statistical Software [reference article](http://vita.had.co.nz/papers/tidy-data.pdf) authored by Hadley Wickham. In particular,`MergedAvg` has:

* Each variable stored in one column.
* Each row provides a different observation of that variable.
* The table produces only one "kind" of variables (features estimated from signals). 


run_analysis.R
--------------
[R](http://www.r-project.org/) script that processes the HARUS raw data to create the `MergedAvg` tidy dataset. The latter dataset is saved to the `MergedAvg.txt` file and can be loaded with [read.table()](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/read.table.html) specifying the parameter header=TRUE.
In summary, the script:

* Downloads the raw dataset archive (.zip) file to the local working directory.
* Reads the data files of interest using the custom-defined fpathr() function.
* Processes the raw data:


1. Labels each measurements sub-set (Training,Test) variables with descriptive names: 
    i. Uses the variables (features) names defined in the raw data.
    i. Ensures variables names are legally-compliant with [R syntax standards](https://stat.ethz.ch/R-manual/R-devel/library/base/html/make.names.html) and corrects for misspelled names. 
1. Subsets each measurements set (Training,Test) to retain only the 'mean()' and 'std()' variables or features estimated from the signals. 
1. Merges the two sub-sets (Training,Test) to form one data set,`Merged`: 
    i. Combines Subject identifiers and Activity labels for each sub-set (Training,Test) to preserve data integrity.
    i. Combines each sub-set (Training,Test) data with its associated (Subjects, Activity labels) table as reconstructed in ii.
    i. Merges the Training and Test tables obtained above.
1. Labels the Activity variable with descriptive names.
1. Creates a second, independent tidy dataset, `MergedAvg`, based on the average -- the arithmetic [mean()](https://stat.ethz.ch/R-manual/R-devel/library/base/html/mean.html) -- of each variable for each subject and each activity. 


CodeBook.md
---------------
Code Book for the tidy dataset `MergedAvg`. It summarizes the raw data files employed by **run_analysis.R** as well as `MergedAvg`'s variables units and dictionary.

----

### References
<a name="Ref1"></a> [1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012. </a>

[2] J. Leek et al., "How to share data with a statistician", [datasharing Github repository](https://github.com/AnVIX/datasharing) (2013).

[3] adam-p, "Markdown Cheatsheet", [markdown-here Github repository](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) (2014).






