#Welcome
This web application is a companion to Multidimensional Scaling of Qualitative Data chapter in book Reviewer’s Guide for Mixed Methods Research Analysis (forthcoming). It will help you to better understand and apply the concepts underlined in the chapter. 

##Guidelines for use:
###Data: 

**Upload your own data**: If you have your own data, you can upload it. To proceed with the analysis, the data needs to be in specific format. Your data might be collected in direct or indirect way (see section 2.1 for more information). 

**Select from sample data**: You can also select from our sample data for each format.

**Direct** data format includes object labels and external scale names (exx, exy, exz) and groups (grp) in the columns. Please use the same names and do not leave external scale and group data cells empty even if you do not have any. Just fill randomly the cells in the rows according to the number of stimuli. For example if you have nine objects, fill in nine rows with any random number.   If you have external scales, each object is ranked or rated according to an external criteria (see section 4.3). Similarly you can have predefined groups categorizing each object. See (link) for an example.  Use this method to replicate the example in section 4.  


**Indirect** data format includes row names, subject, object labels and external scale names (exx, exy, exz) and groups (grp) in the columns. Proximity matrices for the indirectly collected data can be calculated either according to the columns or rows. Subject values will be used for INDSCAL; enter the subject values in the subject column (for example if your subjects are countries enter UK, US, China etc..). The rest is same as indirect data. See (link) for an example.  


For *indirect* data, you need select a proximity measure depending on the level of measurement of your data. Your data can be **nominal** (i.e. takes only names such as black, white, yellow, etc…), **binary** (co-occurrence), **ordinal**, or **numerical**.


For **nominal** data select one of these methods: The method chuprov computes Chuprov's T. The method g computes the G-test from Sokal and Rohlf (1982), also known as Dunning's G from Dunning (1993). This G is closely related to Mutual Information (G = 2* *N* *MI, with N being the sample size). The method mutual returns the mutual information, and the method variation returns the so-called ‘variation of information’ (join information - mutual information). Please search WIKIPEDIA for each of these methods if you need more details. 


For **binary** data use Dissimilarity: Although all dissimilarity methods use numerical data, you can calculate for the **binary data** checking the Binary? box. Binary data show the absence or presence of a feature in an object. It is also called co-occurrence data. For **binary data**,  Gower, Bray–Curtis, Jaccard and Kulczynski methods are good in detecting underlying gradients. Morisita, Horn–Morisita, Binomial, Cao and Chao indices should be able to handle different sample sizes, and Mountford and Raup-Crick indices for presence–absence data should be able to handle unknown (and variable) sample sizes. Please search WIKIPEDIA for each of these methods if you need more details. 


**Similarity**: You can also use correlation measures such as Pearson (numerical), Kendal’s Tau and Spearman (ordinal). Similarity measures are converted to dissimilarity before MDS calculation. You can use these stand alone or to cross-validate the results from dissimilarity measures. Use method Pearson to replicate the example in section 5.  For numerical data you can also use distance measures such as Euclidean, Manhattan etc… which is included in the dissimilarity methods. 

**Gravity**: Co-occurrences are, by themselves, almost never reasonable measures of similarity. Rather, they have to be expressed relative to other observed (or theoretically expected) co-occurrences or occurrences. Gravity model formulates a congruence coefﬁcient for co-occurrence data that is directly related to distance estimates.

You can use Scree Plot and IC (initial configuration) Plot options after uploading or selecting the sample data for deciding on the initial parameters (see section 4.1 for details). 

###Explore: 
Here, you can explore different models for checking their interpretability against several configurations with a reasonable Stress level. 

**Select configuration**: You can select several initial configurations  from clusters of similar results with lower stress (denoted by the numbers with smaller size) as shown in the IC plot to compare them with the Torgerson (default) configuration (see section 4.1, initial configurations).

Different models can be used for different data shapes (Section 5):

  *MDS*: Use this if you have a single or aggregated multiway symmetric square matrix. 
  
  *INDSCAL*: Averaging and aggregation of many sources into a single proximity matrix does no justice to the individual differences between different sources.  INDSCAL is   a type of three-way, two-mode MDS, which takes multiple proximity matrices having one mode for objects and one mode for subjects. As for other MDS models, it assumes   that the structure of stimulus space is common for all subjects.  On the other hand, the model considers that the weights given to each dimension by each subject can   vary.

  *IDIOSCAL*: is similar to INDSCAL but drops the idea of common dimensions for all individuals. It admits more general person-speciﬁc transformations of the group space.   (for more details, see Chapter 5 in  Borg I, Groenen PJF, Mair P.Applied Multidimensional Scaling and Unfolding. 2nd ed. New York: Springer; 2018).

*Compare D1 with*: You can draw D1 vs D2 or D1 vs D2.

*External groups?*  If you have assigned external groups to the objects check this box. Otherwise, you can generate automatic clusters via cluster analysis. Try this with different cluster numbers.

*External scales?*  Check this box if you have external scales. When you check this write the name of the scales in the rectangle boxes. 

###Diagnostics: 
This window provides diagnostic measures as stated in section 4.1. Select Torgerson or Random depending on your decision according to the previous steps. 

###Final model:
Plot your final model after checking different decision criteria (see section 4.3 for more details).  This will give you a publication ready MDS map when you enter your title and an interactive 3 D map (if your model is 3D). You can copy and paste the former to your report, paper, thesis etc…