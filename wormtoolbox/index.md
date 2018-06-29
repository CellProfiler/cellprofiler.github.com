---
layout: default
redirect_from: "/wormtoolbox/index.shtml"
---

WormToolbox
===========

*A component of CellProfiler cell image analysis software*

The WormToolbox is a toolbox for high-throughput screening of image-based *Caenorhabditis elegans* phenotypes. The image analysis algorithms measure morphological phenotypes in individual worms and are effective for a variety of assays and imaging systems. WormToolbox is available through CellProfiler and enables objective scoring of whole-worm high-throughput image-based assays of *C. elegans* for the study of diverse biological pathways that are relevant to human disease [[Nature Methods paper](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3433711/)].

* * * * *

Tutorials overview
------------------

![](http://d1zymp9ayga15t.cloudfront.net/images/WTB_diagram.png)

The main analysis pipeline, Pipeline 1, shown in blue, is fully automated, and consists of the following steps:

- Load input images from QORO assay. Pre-process to detect artifacts such as bubbles and well edges.
- Detect worms and clusters of worms. Individual worms/worm clusters are randomly colored.
- Delineate individual worms by model-based worm untangling. Now, each individual detected worm has a unique color.
- Digitally straighten worms and align them to a simple worm atlas for measurement of stain distribution.
- Detect fatty regions within worms. Once worms and fatty regions are identified, a large number of intensity, shape and texture measurements are extracted.

If the provided default worm model does not fit the input data (e.g. due to a different image resolution or different worm strain), a new worm model can be created using Pipeline 2 (pink) to (g) manually select non-touching worms making up a training set for a new model built by Pipeline 3.

For low-throughput experiments, it is possible to manually curate faulty segmentation results using Pipeline 4 (orange) by (h) manual editing of the output from step d of pipeline 1, and (i) manual flipping of digitally straightened worms so that they all align in with heads or tails up. Measurements, such as intensity of stain, fat stain distribution, fat region size, worm width etc. may also be extracted from individual worms after manual correction. All measurements are exported to a database for further exploration and phenotyping.

Note that CellProfiler 2.1 should be used.

* * * * *

Video tutorials
---------------

**Pipeline 1: Identify and collect measurements from individual worms and sub-regions**

CellProfiler 2.1 pipeline: [Pipeline1\_UntangleWormsExtractMeasurements.cppipe](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline1_UntangleWormsExtractMeasurements.cppipe)

Worm model: [DefaultWormModel](http://d1zymp9ayga15t.cloudfront.net/worm_files/DefaultWormModel.xml)

Download this video: [Pipeline1.mp4](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline1.mp4)

This is the main pipeline for delineating worms (also those in clusters) and extracting different kinds of shape and intensity measurements. It requires a worm model as input. This model could either be the DefaultWormModel.xml provided above, or a new worm model created by pipelines 2 and 3 above. This pipeline is fully automated, does not need any user input (once optimized), and can be run on a large number of images organizing output based on information extracted from the input file names. Example image data is provided below.

Steps of the pipeline:

- Load data.
- Pre-process data by removing artifacts such as well edges and bubbles.
- Separate worms and worm clusters the from image background by foreground/background image segmentation.
- Identify individual worms by worm untangling and extract measurements.
- Straighten worms and extract measurements.
- Identify sub-regions (fat) and extract measurements.
- Export measurements to an SQLite database, save worm segmentation masks and images of worm and fat outlines.

**Pipeline 2: Find, select, and save individual worms**

CellProfiler 2.1 pipeline: [Pipeline2\_SelectSingleWorms.cppipe](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline2_SelectSingleWorms.cppipe)

Download this video: [Pipeline2.mp4](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline2.mp4)

This pipeline may be omitted if a previously created model (e.g. DefaultWormModel.xml provided with Pipeline 1) fits the new data. Steps A-C are the same as in Pipeline 1; the same pre-processing and foreground/background segmentation should be applied both when creating the worm model and when running the analysis as changes to the pre-processing may affect the appearance of the width of the worms, in turn influencing the model. This pipeline requires manual interaction selecting representative non-touching worms.

Steps of the pipeline:

- Load data.
- Pre-process data by compensating for non-uniform illumination and removing artifacts such as well edges and bubbles.
- Separate worms and worm clusters the from image background by foreground/background image segmentation.
- Manually select single worms for worm modeling. Approximately 50 worms representing the variability in the dataset is usually sufficient.
- Make sure that the selected single worms are saved as training worms.

NOTE: The video incorrectly states that WormObjects should be used as input for the ConvertObjectsToImage module. The correct input for that module is SelectedSingleWorms.

**Pipeline 3: Create a new worm model from individual worms**

CellProfiler 2.1 pipeline: [Pipeline3\_TrainModel.cppipe](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline3_TrainModel.cppipe)

Download this video: [Pipeline3.mp4](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline3.mp4)

This module takes the manually selected training worms from Pipeline 2 as input. It is recommended to visually browse through the binary input images before running this pipeline to make sure that they represent single worms. The pipeline is fully automated, and the resulting model will be called MyWormModel.xml.

- Load data (output from Pipeline 2).
- Train and save model.

**Pipeline 4: Untangle, correct, and straighten worm clusters**

CellProfiler 2.1 pipeline: [Pipeline4\_ManuallyCorrectStraighten.cppipe](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline4_ManuallyCorrectStraighten.cppipe)

Worm model: [DefaultWormModel.xml](http://d1zymp9ayga15t.cloudfront.net/worm_files/DefaultWormModel.xml)

Download this video: [Pipeline4.mp4](http://d1zymp9ayga15t.cloudfront.net/worm_files/Pipeline4.mp4)

This pipeline loads the untangling results from Pipeline 1 and allows the user to edit any errors in the untangling prior to straightening the worms for visualization and extraction of measurements. A worm model (DefaultWormModel.xml or a new model created by Pipelines 2 and 3) is needed as input for the straightening step.

- Load data (output from Pipeline 1).
- Manually correct segmentation errors.
- Digitally align worms, select orientation (heads or tails up).
- Save result.

* * * * *

Files needed for the tutorials
------------------------------

-   [CellProfiler 2.1 tutorial Pipelines 1–4 (zip)](http://d1zymp9ayga15t.cloudfront.net/worm_files/WormToolbox_tutorial_pipelines.zip)
-   [Example image data for tutorials (zip)](http://d1zymp9ayga15t.cloudfront.net/worm_files/Example_image_data.zip)

Video tutorials on how to use CellProfiler Analyst
--------------------------------------------------

-   [Exploring image data](http://d1zymp9ayga15t.cloudfront.net/content/movies/DemoExploringImageData.mov) **(5 min 30 sec, 33MB .mov)** Demonstrates some of CellProfiler Analyst's data exploration features.
-   [Scoring cell populations](http://d1zymp9ayga15t.cloudfront.net/content/movies/ScoringCellSubpopulations.mov) **(3 min 30 sec, 23MB .mov)** Provides an example of selecting phenotypes using gating.
-   [Classifying cells with machine learning](http://d1zymp9ayga15t.cloudfront.net/content/movies/ClassifierDemo2.mov) **(7 mins 38.5MB .mov)** Shows how to apply the machine learning tool to identify a phenotype of interest.

- Example pipelines
-----------------

- Previously published example pipelines using the WormToolbox

- *As presented in Wählby et al. 2012, these additional pipelines include illumination correction and feature extraction from fluorescence microscopy data.*

-   [Untangle worms](http://cellprofiler.org/examples.html#UntangleWorms)
-   [Straighten worms and extract intensity measurements using a low-resolution atlas](http://cellprofiler.org/examples.html#StraightenWorms)
-   [Create your own worm model](http://cellprofiler.org/examples.html#CreateModel)
-   [Untangle worms and make measurements bright-field staining pattern phenotype](http://cellprofiler.org/examples.html#UntangleWormsBright-field)

Broad Bioimage Benchmark Collection (BBBC) *C. elegans* datasets
----------------------------------------------------------------

-   [BBBC010 *C. elegans* live/dead assay](http://www.broadinstitute.org/bbbc/BBBC010/)
-   [BBBC011 *C. elegans* metabolism assay](http://www.broadinstitute.org/bbbc/BBBC011/)
-   [BBBC012 *C. elegans* infection marker](http://www.broadinstitute.org/bbbc/BBBC012/)

Teaching materials
------------------

-   [*C. elegans* image analysis written exercise](../outreach.html)

* * * * *

Publications
------------

- Wählby C, Kamentsky L, Liu ZH, Riklin-Raviv T, Conery AL, O'Rourke EJ, Sokolnicki KL, Visvikis O, Ljosa V, Irazoqui JE, Golland P, Ruvkun G, Ausubel FM and Carpenter AE (2012) An image analysis toolbox for high-throughput *C. elegans* assays. *Nature Methods* 9(7):714-U273. doi: 10.1038/nmeth.1984 PMID: 22522656. PMCID: PMC3433711. Available at <http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3433711/>
- Riklin-Raviv T, Ljosa V, Conery AL, Ausubel FM, Carpenter AE, Golland P and Wählby C (2010) Morphology-guided graph search for untangling objects: *C elegans* analysis. In *Medical Image Computing and Computer Assisted Intervention* (MICCAI) 2010; 13(3):634-641. PMID: 20879454. PMCID: PMC3050593. Available at <http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3050593/>
- Wählby C, Riklin-Raviv T, Ljosa V, Conery AL, Golland P, Ausubel FM and Carpenter AE (2010) Resolving clustered worms via probabilistic shape models. In *ISBI 2010 (Proceedings of the IEEE International Symposium on Biomedical Imaging: From Nano to Macro)*, 552-555. doi: 10.1109/ISBI.2010.5490286 PMID: 21383863. PMCID: PMC3048333. Available at <http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3048333/>
- Wählby C, Lee Conery A, Bray MA, Kamentsky L, Larkins-Ford J, Sokolnicki KL, Veneskey M, Michaels K, Carpenter AE and O'Rourke EJ (2014). High- and low-throughput scoring of fat mass and body fat distribution in *C. elegans* *Methods* 68(3):492-499. doi: 10.1016/j.ymeth.2014.04.017 PMID: 24784529 PMCID: 4112171. Available at <http://www.ncbi.nlm.nih.gov/pubmed/24784529>
