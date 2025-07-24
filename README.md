This archive contains all datasets, codes, and output results corresponding to Section III, IV, and V of the associated paper. The complete dataset has been split into 7 packages, named as follows:
 	Section_III_Raw_data_magnitude.rar
	Section_III_Raw_data_phase_(1).rar
 	Section_III_Raw_data_phase_(2).rar
 	Section_III_static_physiological_conditions_model.rar
 	Section_IV_physiological_variability_conditions_model.rar
 	Section_IV_Raw_data_apmlitude.rar
 	Section_IV_Raw_data_phase.rar
Please extract all files in the same directory to reconstruct the full folder structure. The archive mainly consists of two folders:
1. Data under static physiological conditions;
2. Data under physiological variability conditions.
1. Section_III_static_physiological_conditions
This folder includes all data related to SOC and SOH estimation under static physiological conditions.
Raw_data:
Contains raw magnitude and phase results obtained over 6 charge/discharge cycles at a 0.3C rate.
1_data_preprocessing/
Includes data_preprocessing.m, which converts the raw data into interpolated SOC features with 0.5% resolution (e.g., 100%, 99.5%, ..., 0%) for model training and validation.
2_SOC_ESTIMATION_Model/
Contains five SOC estimation models described in Section III-C. Each method includes two scripts (e.g., *_Multi.m and *_Single.m) for multi- and single-frequency feature set validation.
3_SOH_ESTIMATION_Model/
Contains the LSLinear SOH estimation model shown in Section III-D, which includes two scripts (e.g., LSlinear _Multi.m and LSlinear _Single.m) for multi- and single-frequency feature set validation.
2. Section_IV_physiological_variability_conditions
This folder includes datasets and algorithms related to SOC estimation under physiological variability conditions.
Raw_data:
Contains raw magnitude and phase results obtained over 6 charge/discharge cycles at a 0.5C rate.
1_SSA_code/
Includes codes implementing the SSA model for frequency shift compensation.
2_Gene_Encoded_Classifier_code/
Implements the gene-encoded classifier comprising three steps:
 	step1_Reference_encoding.m: Encode reference features.
 	step2_Test_feature_encoding.m: Encode test features.
 	step3_vertification_results.m: Performs SOC estimation verification.
The corresponding outputs, including encoded feature sets and SOC estimation performance are saved in the Experimental_Results/ subfolder.

