This repository is being used for the development of a thesis accross multiple devices, taking advantage of the cloud and version control to ensure consistency accross devices


01/03/2025, 10:12 - currently running different experiments on model architecture before refining techniques for feature selection and resampling
Progress seems to suggest that width is relevant (model 40,10,10,5,10) perfromed worse than (model 40,64,30,10)

03/03/2025, 10:50 - models seem to be performing surprisingly well (need to run default train/eval loop to guarantee this) as im cranking up the grid_size, thinner model architectures seem to outperform 
wide model architectures when given enough grid_size (model 40,20,10,10 with grid_size = 25) 

05/03/2025, 19:19 - applied a change to the way in which outliers are treated and ended up penalizing the model since it was getting a lot of data leakage, need to attempt perhaps data impuation using knn imputer

05/03/2025, 23:08 - changed to adasyn and winsorizing outliers // the models seem to be training more linearly, slower, perhaps they might get stuck in lower accuracy intervals  (accuracy can be achieved by going back to original outlier treatment and perhaps smote+een although adasyn is better for balance
