---
layout: default
redirect_from: "/imagingflowcytometry/index.shtml"
---

Imaging flow cytometry analysis using CellProfiler
--------------------------------------------------

Note: There is a newer protocol available [here](http://cellprofiler.org/imagingflowcytometry/index.html).

Imaging flow cytometry combines the high-throughput capabilities of conventional flow cytometry with single-cell imaging. CellProfiler can be used to analyze the resulting images from imaging flow cytometry, whether brightfield, darkfield, or fluorescence.

In some cases, even unlabeled cells can be scored for particular phenotypes. In the workflow outlined below, we have demonstrated label-free prediction of DNA contentand quantification of the mitotic cell cycle phases by applying supervised machine learning to morphological features extracted from brightfield and the typically-ignored darkfield images of cells from an imaging cytometer. This method facilitates non-destructive monitoring of cells avoiding potentially confounding effects of fluorescent stains while maximizing available fluorescence channels. Although Blasi et al. focuses on a *label-free* analysis using bright-field and dark-field alone, we emphasize that this protocol can be applied in assays that involve any number of fluorescent channels and is not limited to label-free assays.

**Paper:**
T. Blasi, H. Hennig, H.D. Summers, F.J. Theis, D. Davies, A. Filby, A.E. Carpenter, P. Rees. Label-free cell cycle analysis for high-throughput imaging flow cytometry. Nat. Comm. 7, 10256 (2016). PMID: 26739115 [[link to paper at Nature Communications]](https://doi.org/10.1038/ncomms10256)

**Protocol:** [[Download all protocols](http://d1zymp9ayga15t.cloudfront.net/Protocol/Protocol.pdf)]

![Step1pic](http://d1zymp9ayga15t.cloudfront.net/images/Step1pic.jpg) ![IDEAS](http://d1zymp9ayga15t.cloudfront.net/images/Ideas.jpg) **Step 1:** Extract single cell images & identify cell populations with IDEAS software

[[PDF Protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/Step1Protocol.pdf)] [[example input data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/input_step1.zip)] [[example output data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_3_Step2_input_single_tifs.zip)]

![Step2pic2](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic2.jpg) ![Arrow](http://d1zymp9ayga15t.cloudfront.net/images/Arrow.png) ![Step1pic](http://d1zymp9ayga15t.cloudfront.net/images/Step1pic.jpg) ![Step2pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic1.jpg) **Step 2:** Preprocess the single cell images combine them to montages of images using Matlab

[[PDF Protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/Step2Protocol.pdf)] [[example input data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_3_Step2_input_single_tifs.zip)] [[source code](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_code_1_Step2_make_montages.m)] [[example output data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_4_Step2_output_tiled_tifs.zip)]

![Step3pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step3pic1.jpg) ![Arrow](http://d1zymp9ayga15t.cloudfront.net/images/Arrow.png) ![Step2pic2](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic2.jpg) ![CellProfiler logo](http://d1zymp9ayga15t.cloudfront.net/images/cplogo.png) **Step 3:** Segment images and extract features using CellProfiler

[[PDF Protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/Step3Protocol.pdf)] [[example input data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_4_Step2_output_tiled_tifs.zip)] [[example CellProfiler pipeline](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_code_2_CellProfiler_pipeline.cpproj)] [[example output data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_5_Step3_output_features_txt.zip)]

![Step4pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step4pic1.jpg) ![Step2pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic1.jpg) **Step 4 (optional):** Machine Learning for label-free prediction of cell phenotypes

**Preprocessing:** [[PDF protocol](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Step4_PreProcess.pdf)] [[example input data](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_5_Step3_output_features_txt.zip)] [[source code](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_code_3_Step4_a_prepare_data.m)] [[example output data file](http://d1zymp9ayga15t.cloudfront.net/imagingflow/preprocessing_output.zip)]

 **Classification:** [[PDF protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/Step4_class.pdf)] [[example input file](http://d1zymp9ayga15t.cloudfront.net/imagingflow/input_step4_class.zip)] [[source code](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_code_5_Step4_RUSboosting.m)] [[example output data file](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_10_Step4_output_estimated_phases.mat.zip)]

 **Regression:** [[PDF protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/step4_regress.pdf)] [[example input data file](http://d1zymp9ayga15t.cloudfront.net/imagingflow/input_step4_regress.zip)] [[source code](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_code_4_Step4_LSboosting.m)] [[example output data file](http://d1zymp9ayga15t.cloudfront.net/imagingflow/Supplementary_data_9_Step4_output_estimated_nuclear_content.mat.zip)]

Future developments
===================

A new protocol for analyzing imaging flow cytometry data in high-throughput is currently under development:

![new protocol](new_protocol.png)

 

In addition, analyzing imaging flow cytometry data in high-throughput will also become more streamlined using any image analysis software via the following protocol (under development):

![new protocol](new_protocol_python.png)
