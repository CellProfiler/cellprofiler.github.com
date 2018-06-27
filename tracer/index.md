---
layout: default
---

Tracer
======

*A component of CellProfiler Analyst cell image analysis software*

**CellProfiler Tracer** is a data visualization and exploration tool for time-lapse image-based assays. Tracer is available within CellProfiler Analyst and enables visualization and quality assessment of cellular trajectories obtained via time-lapse imaging.

In the world of cellular image analysis, time-lapse assays remain one of the more challenging domains in biology. Often, the dynamic behavior of organisms, cells, organelles, or molecular assemblies can only appreciated by observing them over time. While a wide range of tracking algorithms have been developed, open-source tools tailored towards the visualization of their results, in particular the assessment of the result quality, are uncommon. In particular, for high-content screening purposes, where the biologist is looking at a large number of per-cell measurements, it is vital to be able to visually assess the development of these measurements across time within the local context of the cell being examined.

The [Imaging Platform](http://www.broadinstitute.org/~anne/) at the [Broad Institute](http://www.broadinstitute.org/) specializes in producing the rich set of measurements characteristic of these screening efforts. In addition, we have included object tracking functionality in our CellProfiler open-source software. Lastly, we have developed CellProfiler Analyst for the purpose of data exploration. We have leveraged all of these capabilities into a new package, CellProfiler Tracer.

[![](http://d1zymp9ayga15t.cloudfront.net/images/download_button.png)](http://d1zymp9ayga15t.cloudfront.net/files/software/CellProfiler-Analyst.exe)
(Windows 64-bit)

 Source code available [below](#tech_notes).

- **Important installation notes:**

    -   Tracer is a modification of the CellProfiler Analyst package. If you already have CellProfiler Analyst installed on your system, it is recommended to install the Tracer version to a different folder.
    -   The Java Development Environment (JDK) is required for Tracer to run; download from [here](http://www.oracle.com/technetwork/java/javase/downloads/index.html). Make sure to install the 64-bit Windows version, and then add the JDK *bin* location to your PATH environment variable ([instructions](https://java.com/en/download/help/path.xml)).

**Questions?** Please direct them to our online [forum](http://forum.cellprofiler.org/c/cpa-dev) dedicated to CellProfiler Analyst.

#### Quick links

-   [Tutorial](#tutorial)
    -   [Data display](#data_display)
    -   [Control panel components](#control_panel)
    -   [Trajectory context menu](#context_menu)
    -   [Quality assessment metrics](#quality_assessment)
-   [Files needed for the tutorials](#files_needed)
-   [Technical and developer notes](#tech_notes)

![](http://d1zymp9ayga15t.cloudfront.net/images/xyt_screenshot.png)


* * * * *

Tutorial
--------

### Data display

To start a Tracer session, start the Tracer version of the CellProfiler Analyst application (available

[here](http://d1zymp9ayga15t.cloudfront.net/files/software/CellProfiler-Analyst.exe)), which will request a properties file. The *properties file* is a human-readable configuration file which provides the configuration details for the collected data. If CellProfiler is used to produce the data to be analyzed in Tracer, the [ExportToDatabase](http://d1zymp9ayga15t.cloudfront.net/CPmanual/ExportToDatabase.html) module can be used to automatically generate a properties file. Otherwise, one can be created manually; please refer to the [Examples](http://cellprofiler.org/examples.shtml#cpa_examples) page or the "Files needed" section below for an template properties file. Once this file is loaded, the main CellProfiler Analyst user interface is displayed and Tracer is selected from the row of icons presented

![](http://d1zymp9ayga15t.cloudfront.net/images/cpa_screenshot.png)

The data set used in this example consists of dividing cells in a Drosophila embryo ([download](#dataset2)), in which the genes were modified to make the DNA fluorescent. CellProfiler was used to analyze this movie using the [TrackObjects](http://d1zymp9ayga15t.cloudfront.net/CPmanual/TrackObjects.html) module to track the individual cells across time, and collect measurements such as intensity, morphology and texture; the pipeline is available here ([download](#dataset2)).

When starting Tracer, this tracking data is read in order to construct a network graph that is displayed in two complementary formats:

![](http://d1zymp9ayga15t.cloudfront.net/images/tracer.png)

- The panel on the left is an **XYT plot** which shows the evolution of the individual cells across time; the spatial axes are the horizontal plane with the vertical axes representing time.

- The panel on the right is a **lineage plot** which shows the same graph as on the left, but without the spatial information so that the ancestor/descendant relationships can be seen in more detail.

- Below both is a **control panel** with various operations that can be used to re-display or interrogate the data.

### Control panel components

- A number of functions are available from the control panel:

    -   *Data Source:* If multiple movies were analyzed in the course of a single pipeline, they can be selected by index here.
    -   *Data Tracks:* The original, unedited tracks are the default for this drop-down. Edits made to the trajectories may saved under a new identifier and are then also listed here.
    -   *Select Tracks to Visualize...:* This button will bring up a listbox allowing selection of any individual trajectory to better assess its behavior. Multiple trajectories can be selected.
    -   *Show LAP Diagnostic Graphs:* (This button only appears if the LAP method was used in the object tracking in CellProfiler) Pressing this button will bring up a new window displaying histograms of two linear-assignment problem (LAP)-related metrics (described in Jaqaman and Danuser, 2009):
        -   The frame-to-frame displacement histogram is useful for determining the appropriate search radius to find an object from one frame to the next. The histogram is typically unimodal and decays with higher linking distances. A decay towards zero indicates that the given maximum search radius is sufficiently large; if the distribution decay is truncated, then the specified maximum search radius is too small. The tool will report the abscissa at 95% of the maximum count as the recommended search radius.
        -   The gap length histogram can be used for finding the optimal time window for reconnecting trajectory gaps resulting from the temporary disappearance of an object. A distribution which plateaus towards longer gap lengths indicates that the chosen time window is too large, and gaps are probably being closed incorrectly. A distribution with no plateau indicates a proper time window length.
    -   *Data Measurements:* Any of the cellular measurements generated during the analysis run may be selected here. Selecting "Other derived metrics…" from the drop-down enables additional tools in the control panel, described below.
    -   *Colormap:* The color scheme to apply to both panels may be selected here.
    -   *Update Display:* Press this button whenever a change is made to the data source, measurement, tracks and colormap drop-downs.
    -   *? (question mark):* Click this button and then click on an interface element to bring up help for that element.
    -   *Derived Metrics:* This drop-down is activated when "Derived metrics" is selected from "Data Measurements". It lists the various quality control metrics that are generated from the graph topology of the tracked data. The metrics are listed below.

### Trajectory context menu items

-   Right-clicking on either panel brings up a number of options:

    -   *Select cell using object ID:* The image and object index can entered in order to select a cell in the panels. This can be used in place of finding and clicking on a individual cell.
    -   *Make all trajectories visible:* Restores the visibility of all trajectories in the panels.
    -   *Display measurement heatmap...:* Displays a heatmap of measurements averaged across all trajectroies for each timepoint. You can select which measurements to display. The display is shown using the current colormap.

-   If a cell is selected in the panels, the context menu shows the selected trajectory number plus the image number/object number index of the selected cell. Additional context menu options are also shown:

    -   *Show selected cell as...:* This gives additional options of showing the selected cell in the following ways:
        -   *Image tile:* Shows a square "window" displaying an individual cell. The size of the tile is set with the `image_tile_size` field in the properties file.
        -   *Full image:* Shows the full image, with the selected cell highlighted with a small square dot.
        -   *Data table from select trajectory:* Provides tabular data of measurement values along the trajectory containing the selected cell. A data table is displayed with each row representing the frame index and the column values corresponding that of the currently selected measurement in the control panel.
    -   *Define trajectory segment as...:* A contiguous sub-section of the trajectory (the trajectory segment) containing the selected object can be defined with this option. A trajectory segment can be defined in the following ways:
        -   *Endpoint #1:* Use the selected point to define the first endpoint of a segment.
        -   *Endpoint #2:* Use the selected point to define the second endpoint of a segment.
        -   *N frames before/after:* Enter the number of frames upstream and downstream of the selected cell in order to define the segment. If there are branchpoints upstream/downstream of the cell, the longer branch will be used.
    -   *Display trajectory segment as...:* The trajectory segment can be displayed in the following ways:
        -   *Synchrogram (Image montage):* Display an image montage (synchrogram) of the selected cell as a series of image tiles, with the selected cell centered in the middle of the tile.
        -   *Plot of currently selected measurement:* Display a graph of the currently selected measurement along the points specified by the trajectory segment.

### Quality assessment metrics

-   The trajectories in both panels can be color-coded according to network graph topological metrics; it is these metrics which allow for assessment of tracking quality.

    -   *Singletons:* Trajectories of very short length are highlighted. Problems in image foreground identification may produce objects that appear transiently and then disappear.
    -   *Crossings:* In biology, cells typically do not merge, so a merge event followed quickly by a split is more likely the result of two neighboring cells getting erroneously combined for a few frames. This would be indicated in a graph as an node with an in-degree \> 1 and an out-degree \> 1.
    -   *Loops:* Transient errors in segmentation in which a single cell is erroneously divided into multiple pieces tend to occur as a brief temporal split and merge of a single object. In graph terminology, this is characterized as a simple cycle, an element readily identifiable in a graph as a closed loop.
    -   *BetweennessCentrality:* Another more flexible approach to the above is to examine the betweenness centrality of the nodes downstream from a branchpoint. The betweenness centrality of a node is the sum of the number of paths that traverse that node. A downstream node located on a short branch would have a lower betweenness centrality than nodes on a longer branch.
    -   *NodesWithinDistanceCutoff:* An alternate version of the above is one where the new object terminates at t = 1 rather than being registered as a merge with the original object. In this case, the graph appears as a branchpoint in which one branch is much shorter than the other. Such terminal nodes can be detected as those (a) within a certain node distance from the branchpoint and (b) an out-degree of 0. This is most likely due to a mis-segmentation in which one piece was subsequently lost.

    For the "Singletons" and "Nodes within Distance Cutoff" metrics, the user can enter the number of nodes defining a singleton or a terminal branch, respectively. For the "Singletons" metric, a button is available which presents the user with a histogram of the track lengths along with some basic statistics, e.g., total number of tracks, number of singletons, etc.

    Upon selecting a metric, pressing the "Update Plot" button will re-draw the trajectories with the flagged nodes highlighted in red for ease of viewing. At this point, the user has several buttons for how to treat these nodes:

    -   *Preview Pruned Edges:* Toggling this button will re-draw the graphs with the linking edges of the flagged nodes removed.
    -   *Add Pruning To Edits:* Add the pruning selection to a list of graph edits. This allows the user build an edited version of the original graph based on the cumulative results of several metrics.
    -   *Save Edited Tracks...:* Create a new graph based on the final list of graph edits. This graph will be assigned a name provided by the user, and will then be added to the "Data Tracks" drop-down. The derived metrics will be re-calculated for this graph, so further edits can be made with updated information. Additionally, the new graph will be added to the adjacency table in the database so it can retrieved across Tracer sessions.

* * * * *

Files needed for the tutorials
------------------------------

We have two sample datasets available to use with Tracer. The image data is in the form of individual image frames; the movies shown below are for illustrative purposes.

Note that CellProfiler 2.1 or greater should be used to run the pipelines ([download](/releases)).

[Two image sequences of MCF-7 cells labeled with NLS-mCerulean fusion protein, plus analysis pipeline](http://d1zymp9ayga15t.cloudfront.net/tracer/files/dataset1.zip) (ZIP, 54MB). Contributed by Albert Yeh ([Ramaswamy lab](http://www.massgeneral.org/cancer/research/researchlab.aspx?id=1188)).

![](http://d1zymp9ayga15t.cloudfront.net/files/videos/1.gif) ![](http://d1zymp9ayga15t.cloudfront.net/files/videos/5.gif)

[An image sequence of a *Drosophila* blastoderm embryo with GFP-histone marking the nuclear DNA, plus analysis pipeline](http://d1zymp9ayga15t.cloudfront.net/files/dataset2.zip) (ZIP, 25MB). Contributed by Victoria Foe ([Foe lab](http://celldynamics.org/celldynamics/people/foe/)).

![](http://d1zymp9ayga15t.cloudfront.net/files/videos/cropped.gif)

Note that when using the properties files associated with these datasets, the *images* and *output* subfolders must stay in the same location relative to the properties files and the SQLite database (.db) file.

* * * * *

Technical and developer notes
-----------------------------

### Source code

The [source code](https://github.com/CellProfiler/CellProfiler-Analyst/tree/cellprofiler-tracer) is available as a branch from the main CellProfiler Analyst public repository on GitHub.

### Compilations

Currently, compiled versions are available for Windows 64-bit only. Producing a compilation for Mac OS would require a significant amount of additional work.

### Data schema

-   Tracer is designed to process and explore any MySQL- or SQLite-based database of image-based screening data structure according to the following simple scheme:

    -   An *image table* with the rows corresponding to channel data from single field of view at a single timepoint and the columns containing the image data (e.g., the name of the treatment condition, the path to and filename of the original image, etc.). A requirement for this table is an image index, a column of integers referencing each site acquired.
    -   At least *one object table* with rows corresponding to a given object (e.g., cells) from a single image table row and the columns containing the object data (e.g., area of the cell, intensity of DNA stain in the nucleus, location of the cell in the original image). Required for this table is an image index as described above, as well as an object index, a column of integers reference each object identified in an image.
    -   In addition, an *object relationship table* is also required. Each row corresponds to the image and object index for a given object and that of its “parent”, i.e, tracked predecessor.

For large image-based screens (\>10,000 images), the typical workflow is to store the data set remotely on an MySQL database due to the prohibitive storage requirements for the collected measurements. However, using SQLite for local storage provides the same functionality and is more suitable for small or intermediate-level screens.

The image and object data tables are automatically produced by the [ExportToDatabase](http://d1zymp9ayga15t.cloudfront.net/CPmanual/ExportToDatabase.html) module if the raw images are analyzed with CellProfiler 1.0 and above. The object relationship table is also produced by this module if using CellProfiler 2.1.0 and above. Ideally, the tracking data should be produced using the [TrackObjects](http://d1zymp9ayga15t.cloudfront.net/CPmanual/TrackObjects.html) module, but any tracking algorithm capable of producing the requisite relationship table will suffice.

### Dependencies

-   [wxPython](http://www.lfd.uci.edu/~gohlke/pythonlibs/#wxpython) 2.8+ (3.0+ is NOT supported)
-   [matplotlib](http://www.lfd.uci.edu/~gohlke/pythonlibs/#matplotlib) 1.3+ (note additional dependencies at link)
-   [MySQL-python](http://www.lfd.uci.edu/~gohlke/pythonlibs/#mysql-python) 1.2+
-   [Enthought Tool Suite](http://www.lfd.uci.edu/~gohlke/pythonlibs/#ets) (for Mayavi2)
-   [VTK](http://www.lfd.uci.edu/~gohlke/pythonlibs/#vtk) (5.10+)
-   [NetworkX](http://www.lfd.uci.edu/~gohlke/pythonlibs/#networkx) (1.7+)
-   [NumPy-MKL](http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy) (1.71+)
-   [configobj](https://pypi.python.org/pypi/configobj) (required by Enthought)
-   [decorator](https://pypi.python.org/pypi/decorator) (required by networkx)
-   [verlib (required by distutils)](https://pypi.python.org/pypi/verlib)
-   [python-bioformats](https://pypi.python.org/pypi/python-bioformats/)
-   [python-javabridge](https://pypi.python.org/pypi/javabridge/)
