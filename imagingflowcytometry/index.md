---
layout: default
redirect_from: "/imagingflowcytometry/index.shtml"
---

Imaging flow cytometry analysis using CellProfiler
--------------------------------------------------

Imaging flow cytometry (IFC) combines the high-throughput capabilities of conventional flow cytometry with single-cell imaging. CellProfiler can be used to analyze the resulting images from imaging flow cytometry, whether brightfield, darkfield, or fluorescence.

We here provide an open-source IFC protocol described in [Hennig et al. (2016)](https://doi.org/10.1016/j.ymeth.2016.08.018). This protocol aims to enable the scientific community to leverage the full analytical power of IFC-derived data sets. It will help to reveal otherwise unappreciated populations of cells based on features that may be hidden to the human eye. Compensated data files from an imaging flow cytometer (the proprietary .cif file format) can be read and resulting image tiles are generated. The image tiles are imported into the open-source software CellProfiler, where an image processing pipeline identifies cells and subcellular compartments allowing hundreds of morphological features to be measured. This high-dimensional data can then be analyzed using cutting-edge machine learning and clustering approaches using user-friendly platforms such as CellProfiler Analyst or scripting languages such as R or Python.

Note: This is a more user-friendly and streamlined protocol as compared to [Blasi et al. (2016)](https://doi.org/10.1038/ncomms10256), however, the former protocol is still available [here](http://cellprofiler.org/imagingflowcytometry/IFC_label_free.html).

**Paper:**
H. Hennig, P. Rees, T. Blasi, L. Kamentsky, J. Hung, D. Dao, A.E. Carpenter, and A. Filby. An open-source solution for advanced imaging flow cytometry data analysis using machine learning. Method, in press (2016) [[link to paper at Methods](https://doi.org/10.1016/j.ymeth.2016.08.018)] T. Blasi, H. Hennig, H.D. Summers, F.J. Theis, D. Davies, A. Filby, A.E. Carpenter, P. Rees. Label-free cell cycle analysis for high-throughput imaging flow cytometry. Nat. Comm. 7, 10256 (2016). PMID: 26739115 [[link to paper at Nature Communications](https://doi.org/10.1038/ncomms10256)]

**Protocol:** [[download Protocol_README.txt](http://cellprofiler-org.s3.amazonaws.com/ifc/Protocol_README.txt)]

**Preparatory Step:** Identify cell populations using gating in IDEAS software. Export population as cif file![IDEAS](http://d1zymp9ayga15t.cloudfront.net/images/Ideas.jpg)

![Step2pic2](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic2.jpg) ![Arrow](http://d1zymp9ayga15t.cloudfront.net/images/Arrow.png) ![Step1pic](http://d1zymp9ayga15t.cloudfront.net/images/Step1pic.jpg) ![Python logo](http://cellprofiler-org.s3.amazonaws.com/ifc/python-logo.png) **Step 1:** Automatically generate tiles of 1000 single cell images per tile, using a python app (alternatively a Matlab script is available). The app reads a cif file and writes the tiles (which are tif image files) to the output folder.

[[example input cif file](http://cellprofiler-org.s3.amazonaws.com/ifc/example.cif)] [[python app for tiling](https://github.com/CellProfiler/stitching)] [[Matlab script for tiling](http://cellprofiler-org.s3.amazonaws.com/ifc/Step1_Matlab_tiling.zip)] [[example output data](http://cellprofiler-org.s3.amazonaws.com/ifc/Step1_output_tiff_montages.zip)]

![Step3pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step3pic1.jpg) ![Arrow](http://d1zymp9ayga15t.cloudfront.net/images/Arrow.png) ![Step2pic2](http://d1zymp9ayga15t.cloudfront.net/images/Step2pic2.jpg) ![CellProfiler logo](/images/cp_logo.png) **Step 2:** Segment images and extract features in CellProfiler. The example CellProfiler pipeline exports the features as csv files. The pipeline also generates a CellProfiler Analyst properties file for the machine learning in step 3.

[[PDF Protocol](http://d1zymp9ayga15t.cloudfront.net/Protocol/Step3Protocol.pdf)] [[example input data](http://cellprofiler-org.s3.amazonaws.com/ifc/Step2_input_tiled_tifs.zip)] [[CellProfiler pipeline](http://cellprofiler-org.s3.amazonaws.com/ifc/Step2_CellProfiler.cpproj)] [[example output data](http://cellprofiler-org.s3.amazonaws.com/ifc/Step2_CP_output.zip)]

![Step4pic1](http://d1zymp9ayga15t.cloudfront.net/images/Step4pic1.jpg) ![CPA logo](http://cellprofiler-org.s3.amazonaws.com/ifc/cpa_logo.jpg) **Step 3:** Use any programming language for supervized or unsupervized machine learning,such as python or R. A user-friendly option for machine learning is the softwareCellProfiler Analyst. For this, load the properties file in CellProfilerAnalyst.

[[CellProfiler Analyst website](http://cellprofiler.org/cp-analyst/)]
