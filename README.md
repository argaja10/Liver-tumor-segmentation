# Liver-tumor-segmentation
ALL NECESSARY DATA ARE IN THE FOLDER "Liver Data"

PLEASE DOWNLOAD THE ENTIRE FOLDER AND RUN THE JUPYTER NOTEBOOK WITHIN THE SAME FOLDER TO BE CONSISTENT WITH THE PATH FOR DATA

THE CODE IS READY TO BE RUN DIRECTLY WITHOUT ANY INPUTS FROM THE USER

THE OUPUTS ARE STORED IN THE FOLDER "Output_Liver Tumor" and are also displayed in the notebook itself for quick reference.

*** EACH FAST MARCHING ALGORITHM FOR THE FOUR SCANS TAKE ~5mins TO RUN ***
    

##########################################
Section 1:
##########################################
This part contains the implementation of the fast marching segmentation algorithm for the segmentation of liver tutor for four different patient scans. Each patient scan is analysed separately, varying the algorithm parameters, namely, alpha, beta and sigma (four values for each parameter, hence 4*4*4 = 64 segments for each patient)

Validation:

The validation is performed with respect to a reference correct segment. The reference segment is chosen using the majority-vote methods among three radiologists segments (for each patient). The segments obtained from the fast marching algorithm is compared with the reference segment using some parameters, particularly, the jaccard and dice metrics.


Visualisation:

The best results (according to the metrics) are visualised using inline images in the jupyter notebook.
The found segment are also visually compared with reference segment to see the difference between them.

#########################################
Section 2:
#########################################

This section performs segmentation of the Patient1 scan using different algorithms: Region Growing(Connected Threshold, Confidence Connected, Neighbourhood Connected), Fast Marching (already done in Section1), Level Sets, Watershed segmentations.
Each of these are visually compared with the reference segment and the algorithms are compared with each other based on some performance metrics such as: jaccard, dice, volume similarity, false positives and false negatives.

########################################
