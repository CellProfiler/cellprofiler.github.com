---
layout: default
redirect_from:
- "/examples.html"
- "/examples.shtml"
---

### CellProfiler example images and pipelines

#### Basic Pipelines

-   [Human cells](#human-cells)
-   [Fruit fly cells](#fruit-fly-cells)
-   [Tumors](#tumors)
-   [Comet assay](#comet-assay)

#### Specialized Pipelines

-   [Cell/particle counting and scoring the percentage of stained objects](#cellparticle-counting-and-scoring-the-percentage-of-stained-objects)
-   [Yeast colony classification](#yeast-colony-classification)
-   [Yeast patch identification](#yeast-patch-identification)
-   [Tissue Neighbors](#tissue-neighbors)
-   [Wound Healing](#wound-healing)
-   [Illumination Correction](#illumination-correction)
-   [Colocalization](#colocalization)

#### WormToolbox Pipelines

-   [Untangle worms](#untangle-worms)
-   [Straighten worms and extract intensity measurements using a low-resolution atlas](#straighten-worms-and-extract-intensity-measurements-using-a-low-resolution-atlas)
-   [Untangle worms and make measurements bright-field staining pattern phenotype](#untangle-worms-and-make-measurements-bright-field-staining-pattern-phenotype)

#### More Advanced Pipelines

-   [Human cytoplasm-nucleus translocation assay (SBS Vitra)](#human-cytoplasm-nucleus-translocation-assay-sbs-vitra)
-   [Speckle Counting](#speckle-counting)
-   [Object Tracking and Metadata Management](#object-tracking-and-metadata-management)

#### Published Pipelines

-   [Published Pipelines](#published-pipelines)

Basic Pipelines
---------------

These pipelines are made for simple cellular and tissue image assays, and include some basic measurements.

#### Human cells

Human HT29 cells are fairly smooth and elliptical. This pipeline demonstrates how to accurately identify these cells and how to measurements cellular parameters such as morphology, count, intensity and texture.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleHuman.zip)] (0.4 MB)

![Basic CellProfiler pipeline Human HT29 Cell example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/HumanNuclei.jpg)

![Basic CellProfiler pipeline Human HT29 Cell example](http://d1zymp9ayga15t.cloudfront.net/images/HumanColorNucleism.jpg)

#### Fruit fly cells

In contrast to the HT29 cells, Drosophila Kc167 cells are a highly textured and clumpy cell type. This pipeline demonstrates how to identify these clumpy cells and obtain morphological, intensity and texture measurements.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleFly.zip)] (4 MB)

![Basic CellProfiler pipeline Fruit Fly Drosophilia Kc167 Cells example](http://d1zymp9ayga15t.cloudfront.net/images/FruitflyImg.jpg)

![Basic CellProfiler pipeline Fruit Fly Drosophilia Kc167 Cells example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/Fruitfly-coded.jpg)

#### Tumors

A simple pipeline that identifies and counts tumors in a mouse lung, and then measures their size.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleTumor.zip)] (0.9 MB)

![Basic Cellprofiler pipeline mouse lung Tumor Cell Example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleTumorImg.png)

![Basic Cellprofiler pipeline mouse lung Tumor Cell Example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleTumorID.png)

#### Comet assay

This is a simple example of a DNA damage assay using single cell gel electrophoresis. Here, the measurement of interest is the length and intensity of the comet tail. Also, illumination correction is used to reduce background flourescence prior to measurement. Also shown is a silver-stained comet example in which the percentage of DNA contained in the tail is calculated.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleCometAssay.zip)] (0.4 MB)

![Basic CellProfiler pipeline Comet tail DNA damage assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCometImg.png)

![Basic CellProfiler pipeline Comet tail DNA damage assay example - ID](http://d1zymp9ayga15t.cloudfront.net/images/ExampleCometID.png)

Specialized pipelines
---------------------

In addition to cellular object and feature identification, these pipelines include some of the more specialized modules in CellProfiler for image pre-processing or measurement.

#### Cell/particle counting and scoring the percentage of stained objects

CellProfiler is commonly used to count cells or other objects as well as percent-positives, by measuring the per-cell staining intensity. This pipeline shows how to do both of these tasks, and demonstrates how various modules may be used to accomplish the same result.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExamplePercentPositive.zip)] (0.2 MB)

![Specialized CellProfiler pipeline Percent Positive count per-cell stain intensity example](http://d1zymp9ayga15t.cloudfront.net/images/ExamplePercentPosImg.png)

![Specialized CellProfiler pipeline Percent Positive count per-cell stain intensity example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/ExamplePercentPosID.png)

#### Yeast colony classification

This pipeline demonstrates how to classify and count objects on the basis of their measured features. The example identifies uniformly round objects, in this case, yeast colonies growing on a dish. The pipeline also shows how to load a template and align it to a cropped image, as well as how to use illumination correction to subtract for background illumination.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleYeastColonies.zip)] (0.6 MB)

[[Tutorial](http://d1zymp9ayga15t.cloudfront.net/papers/85-Bray_CurrentProtocols_2015.pdf)]

![Specialized CellProfiler pipeline identify Yeast Colony Classification example](http://d1zymp9ayga15t.cloudfront.net/images/YeastCrop.jpg)

![Specialized CellProfiler pipeline identify Yeast Colony Classification example - segmented](http://d1zymp9ayga15t.cloudfront.net/images/YeastCropID.jpg)

#### Yeast patch identification

This pipeline identifies patches of yeast growing in a 96 well plate, serving as an introduction to the grid defintion and identification modules.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleYeastPatches.zip)] (0.5 MB)

![Specialized CellProfiler pipeline identify Yeast Patch example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleYeastPatch.png)

![Specialized CellProfiler pipeline identify Yeast Patch example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleYeastPatchID.png)

#### Tissue Neighbors

Tissue samples often have irregularly shaped cells with adjacent edges. This pipeline shows how to input a color tissue image, split it into its component channels, and then identify individual cells from a particular stain and record the number of neighbors that each cell has.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleNeighbors.zip)] (0.9 MB)

![Specialized CellProfiler pipeline color Tissue image identify example](http://d1zymp9ayga15t.cloudfront.net/images/TissueNeighbors.jpg)

![Specialized CellProfiler pipeline color Tissue image identify example - ID](http://d1zymp9ayga15t.cloudfront.net/images/Clones1colorneighbors.jpg)

#### Wound Healing

In this example, cells are grown as a tissue monolayer. Rather than identifying individual cells, this pipeline quantifies the area occupied by the tissue sample.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleWoundHealing.zip)] (1.2 MB)

![Specialized Cellprofiler pipeline quantify area Tissue Monolayer example](http://d1zymp9ayga15t.cloudfront.net/images/WOUND-IMG.gif)

![Specialized Cellprofiler pipeline quantify area Tissue Monolayer example](http://d1zymp9ayga15t.cloudfront.net/images/WOUND-ANALYSIS.gif)

#### Illumination Correction

Illumination correction is often important for both accurate segmentation and for intensity measurements. This example shows how the CorrectIlluminationCalculate and CorrectIlluminationApply modules are used to compensate for the non-uniformities in illumination often present in microscopy images.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleIlluminationCorrection.zip)] (17.6 MB)

[[Tutorial](http://d1zymp9ayga15t.cloudfront.net/content/ExampleIlluminationCorrection_Tutorial.pdf)]

![Specialized Cellprofiler pipeline Illumination Correction example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleIlluminationCorrection_Orig.png)

![Specialized Cellprofiler pipeline Illumination Correction example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleIlluminationCorrection_Corr.png)

#### Colocalization

Measuring the colocalization between fluorescently labeled molecules is a widely used approach to measure the degree of spatial coincidence and potential interactions among subcellular species (e.g., proteins). This example shows how the object identifcation and RelateObjects modules are used to measure the degree of overlap between two fluorescent channels.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleColocalization.zip)] (3.9 MB)

[[Tutorial](http://d1zymp9ayga15t.cloudfront.net/content/ExampleColocalization_Tutorial.pdf)]

![Specialized CellProfiler Colocalization Spation Coincidence Subcellular example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleColocalization_Orig.png)

![Specialized CellProfiler Colocalization Spation Coincidence Subcellular example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleColocalization_Masked.png)

### Imaging Flow Cytometry

Imaging flow cytometry combines the high-throughput capabilities of conventional flow cytometry with single-cell imaging. CellProfiler can be used to analyze the resulting images from imaging flow cytometry, whether brightfield, darkfield, or fluorescence.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleImagingFlowCytometryObjectsInGrid.zip)] (21.2 MB)

[[IFC website](http://cellprofiler.org/imagingflowcytometry/index.html)]

Worm Toolbox
------------

These pipelines have been developed for high-throughput screens on *C. elegans* and extract measurements on a per-worm basis.

The [Worm Toolbox](/wormtoolbox) page has further details on this workflow, as well as video tutorials, pipelines and image data in addition to those described below. (from C Wählby *et al.* Methods, 2014)

The [BBBC](http://www.broadinstitute.org/bbbc) also has *C. elegans* sample images and information, as well as assay "ground truth" of various kinds.

#### Untangle worms

In this pipeline, we identify individual worms and extract shape and intensity measurements. Worm untangling requires a worm model, which is provided together with the pipeline. If adjusting the pipeline to fit your own data, worm detection will likely improve by creating a new worm model based on your own image data.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleUntangleWorms.zip)] (1.4 MB)

![Worm Toolbox CellProfiler Shape Intensity Untangle Worms CellProfiler](http://d1zymp9ayga15t.cloudfront.net/images/ExampleUntangleInput.gif)

![Worm Toolbox CellProfiler Shape Intensity Untangle Worms CellProfiler](http://d1zymp9ayga15t.cloudfront.net/images/ExampleUntangleOutput.gif)

#### Straighten worms and extract intensity measurements using a low-resolution atlas

Once worms are untangled, this pipeline shows how they can be straightened and aligned with a low-resolution worm atlas to extract localized intensity measurements and compare patterns of reporter signals. Included are steps for identifying secondary objects (fluorescent marker signals) and relating these objects to individual worms, enabling count of signals on a per-worm basis.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleStraightenWorms.zip)] (1 MB)

![Worm Toolbox CellProfiler Straighten Worms example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleStraightenInput.gif)

![Worm Toolbox CellProfiler Straighten Worms example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleStraightenOutput.gif)

#### Untangle worms and make measurements bright-field staining pattern phenotype

This pipeline detects individual worms by worm untangling and finds sub-objects (fatty regions stained with oil red O) within the worms. Using bright-field data only, it detects fatty regions by intensity thresholding in a single image channel and relates the fatty regions to individual worms. This enables detection of rare phenotypes in heterogeneous populations, phenotypes that would be missed if population averages were observed. More data can be found on the [BBBC](http://www.broadinstitute.org/bbbc).

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleUntangleWormsBrightField.zip)] (1.7 MB)

![Worm Toolbox CellProfiler Untangle Sub-Object Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleOROinput.gif)

![Worm Toolbox CellProfiler Untangle Sub-Object Worm example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleOROoutput.gif)

More Advanced Pipelines
-----------------------

These pipelines are more complex in terms in image processing, feature identification and the desired measurements.

#### Human cytoplasm-nucleus translocation assay (SBS Vitra)

In this human cytoplasm-nucleus translocation assay, learn how to load a previously calculated illumination correction function for two separate channels, measure protein content in the nucleus and cytoplasm, and calculate the ratio as a measure of translocation. This is a clumpy cell type, so studying the settings in primary object identification may be helpful for users interested in the more advanced options that module offers. More about these images can be found at the [BBBC](http://www.broadinstitute.org/bbbc/BBBC014/).

[[Download](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleVitraImages.zip)] (4.4 MB)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleVitraImg.png)

![Advanced Pipeline CellProfiler Human Cytoplasm-Nucleus Translocation Assay example](http://d1zymp9ayga15t.cloudfront.net/images/ExampleVitraID.png)

#### Speckle Counting

This pipeline shows how to identify smaller objects (foci) within larger objects (nuclei) and how to use the Relate module to establish a relationship between the two as well as perform per-object aggregate measurements (such as number of foci per nucleus).

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleSpeckles.zip)] (2.7 MB)

![Advanced Pipeline CellProfiler Speckle Counting example](http://d1zymp9ayga15t.cloudfront.net/images/SpecklesAB.gif)

![Advanced Pipeline CellProfiler Speckle Counting example](http://d1zymp9ayga15t.cloudfront.net/images/SpecklesCD.gif)

#### Object Tracking and Metadata Management

This example shows an example of object tracking. This pipeline analyzes a time-lapse experiment to identify the cells and track them from frame to frame, which is challenging since the cells are also moving. In addition, this pipeline also extracts metadata from the filename and uses groups the images by metadata in order to independently process several sequences of images and output the measurements of each.

[[Download](http://cellprofiler-examples.s3.amazonaws.com/ExampleTrackObjects.zip)] (10 MB)

![Advanced Pipeline CellProfiler Object Tracking Metadata Management example](http://d1zymp9ayga15t.cloudfront.net/images/TrackingExampleImg.gif)

![Advanced Pipeline CellProfiler Object Tracking Metadata Management example](http://d1zymp9ayga15t.cloudfront.net/images/TrackingExampleID.gif)

Published Pipelines
-------------------

Pipelines which have appeared in published papers are provided [here](/examples/published_pipelines). Please keep in mind that the listed pipelines are specific to the published assay and that no images are provided.

CellProfiler Analyst Example Data and Properties File
-----------------------------------------------------

**Example database, configuration file, and images:** Single 96-well plate of human cellular images, for use with CellProfiler Analyst 2.0. More sample images and information on the image data can be found on the [Broad Bioimage Benchmark Collection (BBBC)](http://www.broadinstitute.org/bbbc/BBBC017/).

Moffat J et al., A lentiviral RNAi library for human and mouse genes applied to an arrayed viral high-content screen. Cell. 2006 Mar 24;124(6):1283-98

[[Download](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/cpa_2.0_example.zip)] (203MB zipped)

![CellProfiler Analyst logo](http://d1zymp9ayga15t.cloudfront.net/images/cpa_128.png)

#### Previous Examples

Previous examples (prior to 3.0) can be found on the [previous examples](/previous_examples) page, but we discourage their use because they are now outdated.
