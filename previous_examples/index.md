---
layout: default
redirect_from:
- "/previous_examples.html"
- "/previous_examples.shtml"
---

### OLD CellProfiler example images and pipelines (Prior to 3.0)

#### These examples are outdated, please see our current [Examples](/examples/) page for the updated versions.

#### Basic Pipelines

-   [Human cells](#HumanCells)
-   [Fruit fly cells](#FruitFlyCells)
-   [Tumors](#Tumors)
-   [Comet assay](#Comet)

#### Specialized Pipelines

-   [Cell/particle counting and scoring thepercentage of stainedobjects](#PercentPositive)
-   [Yeast colony classification](#YeastColonies)
-   [Yeast patch identification](#YeastPatch)
-   [Tissue Neighbors](#TissueNeighbors)
-   [Wound Healing](#Wound)
-   [Illumination Correction](#IlluminationCorrection)
-   [Colocalization](#Colocalization)
-   [Spot Detection, for beginners](#SpotDetection)

#### WormToolbox Pipelines

-   [Untangle worms](#UntangleWorms)
-   [Straighten worms and extract intensity measurements using a low-resolution atlas](#StraightenWorms)
-   [Untangle worms and make measurements bright-field staining pattern phenotype](#UntangleWormsBright-field)

#### More Advanced Pipelines

-   [Human cytoplasm-nucleus translocation assay (SBS Vitra)](#SBS_Vitra_CNT)
-   [Human cytoplasm-nucleus translocation assay (SBS Bioimage)](#SBS_Bioimage_CNT)
-   [Speckle Counting](#Speckles)
-   [Object Tracking and Metadata Management](#Tracking)
-   [Sequencing RNA molecules *in situ* combining CellProfiler with ImageJ plugins](#InSitu)

#### File Utilities

-   [Invert For Printing](#InvertForPrinting)
-   [Color To Gray](#ColorToGray)
-   [Convert Image File Format](#FileConvert)

#### Published Pipelines

[Published Pipelines](#PublishedPipelines)

### Basic Pipelines

These pipelines are made for simple cellular and tissue image assays, and include some basic measurements.

#### Human cells

Human HT29 cells are fairly smooth and elliptical. This pipeline demonstrates how to accurately identify these cells and how to measurements cellular parameters such as morphology, count, intensity and texture.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleHumanImages.zip) (0.3 MB)

![Basic CellProfiler pipeline Human HT29 Cell example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/HumanNuclei.jpg)

![Basic CellProfiler pipeline Human HT29 Cell example](http://d1zymp9ayga15t.cloudfront.net/images/HumanColorNucleism.jpg)

#### Fruit fly cells

In contrast to the HT29 cells, Drosophila Kc167 cells are a highly textured and clumpy cell type. This pipeline demonstrates how to identify these clumpy cells and obtain morphological, intensity and texture measurements.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleFlyImages.zip) (4 MB)

![Basic CellProfiler pipeline Fruit Fly Drosophilia Kc167 Cells example](http://d1zymp9ayga15t.cloudfront.net/images/FruitflyImg.jpg)

![Basic CellProfiler pipeline Fruit Fly Drosophilia Kc167 Cells example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/Fruitfly-coded.jpg)

#### Tumors

A simple pipeline that identifies and counts tumors in a mouse lung, and then measures their size.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleTumorImages.zip) (0.9 MB)

![Basic Cellprofiler pipeline mouse lung Tumor Cell Example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleTumorImg.png)

![Basic Cellprofiler pipeline mouse lung Tumor Cell Example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleTumorID.png)

#### Comet assay

This is a simple example of a DNA damage assay using single cell gel electrophoresis. Here, the measurement of interest is the length and intensity of the comet tail. Also, illumination correction is used to reduce background flourescence prior to measurement. Also shown is a silver-stained comet example in which the percentage of DNA contained in the tail is calculated.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleCometAssay.zip) (0.4 MB)

![Basic CellProfiler pipeline Comet tail DNA damage assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCometImg.png)

![Basic CellProfiler pipeline Comet tail DNA damage assay example - ID](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCometID.png)

### Specialized pipelines

In addition to cellular object and feature identification, these pipelines include some of the more specialized modules in CellProfiler for image pre-processing or measurement.

#### Cell/particle counting, and scoring the percentage of stained objects

CellProfiler is commonly used to count cells or other objects as well as percent-positives, by measuring the per-cell staining intensity. This pipeline shows how to do both of these tasks, and demonstrates how various modules may be used to accomplish the same result.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExamplePercentPositive.zip) (0.2 MB)

![Specialized CellProfiler pipeline Percent Positive count per-cell stain intensity example](http://d1zymp9ayga15t.cloudfront.net/images/ExamplePercentPosImg.png)

![Specialized CellProfiler pipeline Percent Positive count per-cell stain intensity example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/ExamplePercentPosID.png)

#### Yeast colony classification

This pipeline demonstrates how to classify and count objects on the basis of their measured features. The example identifies uniformly round objects, in this case, yeast colonies growing on a dish. The pipeline also shows how to load a template and align it to a cropped image, as well as how to use illumination correction to subtract for background illumination.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleYeastColonies_BT_Images.zip) (0.2 MB)

[[Tutorial]](http://d1zymp9ayga15t.cloudfront.net/papers/85-Bray_CurrentProtocols_2015.pdf)

![Specialized CellProfiler pipeline identify Yeast Colony Classification example](http://d1zymp9ayga15t.cloudfront.net/images/YeastCrop.jpg)

![Specialized CellProfiler pipeline identify Yeast Colony Classification example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/YeastCropID.jpg)

#### Yeast patch identification

This pipeline identifies patches of yeast growing in a 96 well plate, serving as an introduction to the grid defintion and identification modules.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleYeastPatchImages.zip) (0.4 MB)

![Specialized CellProfiler pipeline identify Yeast Patch example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleYeastPatch.png)

![Specialized CellProfiler pipeline identify Yeast Patch example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleYeastPatchID.png)

#### Tissue Neighbors

Tissue samples often have irregularly shaped cells with adjacent edges. This pipeline shows how to input a color tissue image, split it into its component channels, and then identify individual cells from a particular stain and record the number of neighbors that each cell has.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleNeighborsImages.zip) (0.1 MB)

![Specialized CellProfiler pipeline color Tissue image identify example](http://d1zymp9ayga15t.cloudfront.net/images/TissueNeighbors.jpg)

![Specialized CellProfiler pipeline color Tissue image identify example - ID](http://d1zymp9ayga15t.cloudfront.net/images/Clones1colorneighbors.jpg)

#### Wound Healing

In this example, cells are grown as a tissue monolayer. Rather than identifying individual cells, this pipeline quantifies the area occupied by the tissue sample.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleWoundHealingImages.zip) (1.1 MB)

![Specialized Cellprofiler pipeline quantify area Tissue Monolayer example](http://d1zymp9ayga15t.cloudfront.net/images/WOUND-IMG.gif)

![Specialized Cellprofiler pipeline quantify area Tissue Monolayer example](http://d1zymp9ayga15t.cloudfront.net/images/WOUND-ANALYSIS.gif)

#### Illumination Correction

Illumination correction is often important for both accurate segmentation and for intensity measurements. This example shows how the CorrectIlluminationCalculate and CorrectIlluminationApply modules are used to compensate for the non-uniformities in illumination often present in microscopy images.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleIlluminationCorrection.zip) (14.9 MB)

[[Tutorial]](http://d1zymp9ayga15t.cloudfront.net/content/ExampleIlluminationCorrection_Tutorial.pdf)

![Specialized Cellprofiler pipeline Illumination Correction example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleIlluminationCorrection_Orig.png)

![Specialized Cellprofiler pipeline Illumination Correction example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleIlluminationCorrection_Corr.png)

#### Colocalization

Measuring the colocalization between fluorescently labeled molecules is a widely used approach to measure the degree of spatial coincidence and potential interactions among subcellular species (e.g., proteins). This example shows how the object identifcation and RelateObjects modules are used to measure the degree of overlap between two fluorescent channels.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleColocalization.zip) (3.7 MB)

[[Tutorial]](http://d1zymp9ayga15t.cloudfront.net/content/ExampleColocalization_Tutorial.pdf)

![Specialized CellProfiler Colocalization Spation Coincidence Subcellular example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleColocalization_Orig.png)

![Specialized CellProfiler Colocalization Spation Coincidence Subcellular example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleColocalization_Masked.png)

#### Spot Detection, for beginners

In this practical you will learn how to set up an automated CellProfiler image analysis pipeline that will (1) identify individual cells in images, based on a nuclear stain, (2) identify dot-like signals, and (3) count the number of dots per cell and output this information to a spreadsheet. This quantification will enable you to compare the number of dots per cell in wild-type and mutant conditions as well as to measure how the number of dots per cell depends on primary antibody concentration.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleSpotDetection.zip) (1.5 MB)

[[Tutorial on Github]](https://github.com/tischi/cellprofiler-practical-NeuBIAS-Lisbon-2017/blob/master/practical-handout.md)

![Specialized CellProfiler Spot Detection pipeline example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleSpotDetection_Orig.png)

![Specialized CellProfiler Spot Detection pipeline example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleSpotDetection_Corr.png)

### Imaging Flow Cytometry

Imaging flow cytometry combines the high-throughput capabilities of conventional flow cytometry with single-cell imaging. CellProfiler can be used to analyze the resulting images from imaging flow cytometry, whether brightfield, darkfield, or fluorescence.

[[IFC website]](http://cellprofiler.org/imagingflowcytometry/index.html)

### Worm Toolbox

These pipelines have been developed for high-throughput screens on *C. elegans* and extract measurements on a per-worm basis.

The [Worm Toolbox](/wormtoolbox) page has further details on this workflow, as well as video tutorials, pipelines and image data in addition to those described below. (from C Wählby *et al.* Methods, 2014)

The [BBBC](http://www.broadinstitute.org/bbbc) also has *C. elegans* sample images and information, as well as assay "ground truth" of various kinds.

#### Untangle worms

In this pipeline, we identify individual worms and extract shape and intensity measurements. Worm untangling requires a worm model, which is provided together with the pipeline. If adjusting the pipeline to fit your own data, worm detection will likely improve by creating a new worm model based on your own image data.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExamplePipelineUntangle.zip) (1.3 MB)

![Worm Toolbox CellProfiler Shape Intensity Untangle Worms CellProfiler](http://d1zymp9ayga15t.cloudfront.net/images/ExampleUntangleInput.gif)

![Worm Toolbox CellProfiler Shape Intensity Untangle Worms CellProfiler](http://d1zymp9ayga15t.cloudfront.net/images/ExampleUntangleOutput.gif)

#### Straighten worms and extract intensity measurements using a low-resolution atlas

Once worms are untangled, this pipeline shows how they can be straightened and aligned with a low-resolution worm atlas to extract localized intensity measurements and compare patterns of reporter signals. Included are steps for identifying secondary objects (fluorescent marker signals) and relating these objects to individual worms, enabling count of signals on a per-worm basis.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExamplePipelineStraighten.zip) (968 KB)

![Worm Toolbox CellProfiler Straighten Worms example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleStraightenInput.gif)

![Worm Toolbox CellProfiler Straighten Worms example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleStraightenOutput.gif)

#### Create your own worm model

The UntangleWorms module has an "Untangle" mode and a "Train" mode. This pipeline describes how the "Train" mode is used to create a worm model. Training consists of providing a large number of images of worms that are representative of the worm variation within the population, and that do not touch or overlap. Note that this example download includes only two images and will not result in a good model, as it will not be representative of all possible variations of the worm shapes. We recommend using at least 60 worms to create a model.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExamplePipelineCreateModel.zip) (1.6 MB)

![Worm Toolbox Cellprofiler Create Untangle Train Model Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCreateModelInput.gif)

![Worm Toolbox Cellprofiler Create Untangle Train Model Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCreateModelOutput.gif)

#### Untangle worms and make measurements bright-field staining pattern phenotype

This pipeline detects individual worms by worm untangling and finds sub-objects (fatty regions stained with oil red O) within the worms. Using bright-field data only, it detects fatty regions by intensity thresholding in a single image channel and relates the fatty regions to individual worms. This enables detection of rare phenotypes in heterogeneous populations, phenotypes that would be missed if population averages were observed. More data can be found on the [BBBC](http://www.broadinstitute.org/bbbc).

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExamplePipelineOilRedO.zip) (852 KB)

![Worm Toolbox CellProfiler Untangle Sub-Object Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleOROinput.gif)

![Worm Toolbox CellProfiler Untangle Sub-Object Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleOROoutput.gif)

#### More Advanced Pipelines

These pipelines are more complex in terms in image processing, feature identification and the desired measurements.

Human cytoplasm-nucleus translocation assay (SBS Vitra) In this human cytoplasm-nucleus translocation assay, learn how to load a previously calculated illumination correction function for two separate channels, measure protein content in the nucleus and cytoplasm, and calculate the ratio as a measure of translocation. This is a clumpy cell type, so studying the settings in primary object identification may be helpful for users interested in the more advanced options that module offers. More about these images can be found at the [BBBC](http://www.broadinstitute.org/bbbc/BBBC014/).
 [[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleVitraImages.zip) (13 MB)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleVitraImg.png)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleVitraID.png)

#### Human cytoplasm-nucleus translocation assay (SBS Bioimage)

This example includes an advanced example of illumination correction - creating an illumination correction function from all images in a 96-well plate. This pipeline also demonstrates how to load dosage information via the LoadData module, how to use advanced methods for primary and seecondary object identifcation, and how to calculate the Z' factor, a measure of assay quality. More about these images can be found at the [BBBC](http://www.broadinstitute.org/bbbc/BBBC013/).

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleSBSImages.zip) (40 MB)

[[Tutorial]](http://d1zymp9ayga15t.cloudfront.net/content/papers/29-Carpenter_MethodsMolBio_2009.pdf)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay Illumination example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleSBSImg.png)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay Illumination example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleSBSID.png)

#### Speckle Counting

This pipeline shows how to identify smaller objects (foci) within larger objects (nuclei) and how to use the Relate module to establish a relationship between the two as well as perform per-object aggregate measurements (such as number of foci per nucleus).

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleSpecklesImages.zip) (3 MB)

![Advanced Pipeline CellProfiler Speckle Counting example](http://d1zymp9ayga15t.cloudfront.net/images/SpecklesAB.gif)

![Advanced Pipeline CellProfiler Speckle Counting example](http://d1zymp9ayga15t.cloudfront.net/images/SpecklesCD.gif)

#### Object Tracking and Metadata Management

This example shows an example of object tracking. This pipeline analyzes a time-lapse experiment to identify the cells and track them from frame to frame, which is challenging since the cells are also moving. In addition, this pipeline also extracts metadata from the filename and uses groups the images by metadata in order to independently process several sequences of images and output the measurements of each.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleTrackObjects.zip) (10 MB)

![Advanced Pipeline CellProfiler Object Tracking Metadata Management example](http://d1zymp9ayga15t.cloudfront.net/images/TrackingExampleImg.gif)

![Advanced Pipeline CellProfiler Object Tracking Metadata Management example](http://d1zymp9ayga15t.cloudfront.net/images/TrackingExampleID.gif)

#### Sequencing RNA molecules *in situ* combining CellProfiler with ImageJ plugins.

Some image analysis algorithms, such as more advanced image alignment, are not available in CellProfiler. However, functions available as ImageJ plugins can be called from CellProfiler. This pipeline shows how images from subsequent base-calling cycles can be aligned using ImageJ plugins from for RNA sequencing *in situ*.

Sequencing substrates are generated using gap-fill padlock probes and rolling circle amplification, followed by the sequencing-by-ligation chemistry (Ke *et al*, In situ sequencing for RNA analysis in preserved tissue and cells, Nature Methods, published online July 14, 2013, <https://doi.org/10.1038/nmeth.2563>). Note that additional ImageJ plugins are required and can be downloaded as described in the included README file. MATLAB scripts for sequence visualization are also included in the ZIP file.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleInSituSequencing.zip) (45 MB)

![Advanced Pipeline CellProfiler ImageJ In Situ example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleInSituSeqInput.jpg)

![Advanced Pipeline CellProfiler ImageJ In Situ example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleInSituSeqOutput.jpg)

### File Utilities

These pipelines show examples of file display and format manipulation.

#### Invert For Printing

Inverts RGB fluorescence microscopy images from a black background to a white background.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleInvertForPrinting.zip) (0.2 MB)

![File Utility CellProfiler Invert Print example](http://d1zymp9ayga15t.cloudfront.net/images/NotInverted.gif)

![File Utility CellProfiler Invert Print example](http://d1zymp9ayga15t.cloudfront.net/images/InvertedExamples.gif)

#### Color To Gray

Demonstrates how to separate a color image image into its component channels, and how to combine grayscale channel images into an RGB color image.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleColorToGray.zip) (0.8 MB)

![File Utility CellProfiler color to Gray example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleRGB.png)

![File Utility CellProfiler color to Gray example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleRGBSplit.gif)

#### Convert Image File Format

Loads image and saves them in a different file format.

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleDIBtoTIF.zip) (0.9 MB)

![File Utility File Format Conversion example](http://d1zymp9ayga15t.cloudfront.net/images/FileConvert.png)

### Published Pipelines

Pipelines which have appeared in published papers are provided [here](published_pipelines). Please keep in mind that the listed pipelines are specific to the published assay and that no images are provided.

CellProfiler Analyst Example Data and Properties File
-----------------------------------------------------

**Example database, configuration file, and images:** Single 96-well plate of human cellular images, for use with CellProfiler Analyst 2.0. More sample images and information on the image data can be found on the [Broad Bioimage Benchmark Collection (BBBC)](http://www.broadinstitute.org/bbbc/BBBC017/).

Moffat J et al., A lentiviral RNAi library for human and mouse genes applied to an arrayed viral high-content screen. Cell. 2006 Mar 24;124(6):1283-98

[[Download]](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/cpa_2.0_example.zip) (203MB zipped)

![CellProfiler Analyst logo](http://d1zymp9ayga15t.cloudfront.net/images/cpa_128.png)
