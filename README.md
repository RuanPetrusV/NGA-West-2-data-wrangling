This is (the first version of) imputed data from the PEER NGA West 2 ground motion database that I created using the Missforest algorithm. For this task the MissForest 3.1.3 Python package was used. Only the first 500 rows were used for illustrative/demo purposes.

Numbers of columns not included are: 1,2,3,4,5,6,7,8,9,11,12,13,14,15,28,29,30,31,43,46,51,55,64,66,70,71,72,82,83,84,86,87,88,89,90,91,92,94,95,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115, 118,119,120,121,122,123,128,129,130,131,247,248,249,250,251,252,253,254,255,256,257, 258,265,266,267,268,269,270,271,272,273,274
(Not python indexes. subtract 1 for Python indexes)

Columns were excluded either because they were not considered fit to be used to be included in the imputation (and would most probably not feature in GMPEs) or because they had too many missing values (more than 400 missing values). Some columns that I excluded based on missing values might not be excluded in the larger database seeing that the 500 entries I chose were not picked at random.

Peak ground motion columns (column numbers 132,133,134) and frequency content (columns 135 through 245) were moved to the end of the table. Rows with null values in these columns were removed because I did not want to impute any values in them; I only wanted to use them to impute values in other columns. (One might actually want to leave out the peak ground motion because this database is usually used with them as outcome variables).

Admittedly, this is still rough preliminary work. For a thorough job it should be documented which columns were dropped for what reasons, and correlations between columns should be investigated to determine properly the correlations between columns so as not to include highly correlated columns in the imputation.
