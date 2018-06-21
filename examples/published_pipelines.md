---
redirect_from:
    - "/published_pipelines.html"
    - "/published_pipelines.shtml"
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta content="width=device-width, initial-scale=1, maximum-scale=1" name="viewport">
    <meta content="IE=10; IE=9; IE=8; IE=7; IE=EDGE" http-equiv="X-UA-Compatible">
    <meta charset="UTF-8">
    <link href="/images/favicon.ico" rel="shortcut icon" type="image/x-icon">
    <title>CellProfiler | Free open-source software for measuring and analyzing cell images</title>
    <meta content="CellProfiler" property="og:title">
    <meta content="http://cellprofiler.org" property="og:url">
    <meta content="http://cellprofiler.org/images/gallery.png" property="og:image">
    <meta content="CellProfiler is a free open-source software for measuring and analyzing cell images" property="og:description">
    <link href="/css/app.css" rel="stylesheet"><!--Google Analytics-->

    <script>
                 (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
                 (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
                 m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
                 })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

                 ga('create', 'UA-83178912-1', 'auto');
                 ga('send', 'pageview');

    </script><!-- Piwik -->

    <script type="text/javascript">
               var _paq = _paq || [];
               _paq.push(['trackPageView']);
               _paq.push(['enableLinkTracking']);
               (function() {
                 var u="//cellprofiler.piwikpro.com/";
                 _paq.push(['setTrackerUrl', u+'piwik.php']);
                 _paq.push(['setSiteId', 1]);
                 var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
                 g.type='text/javascript'; g.async=true; g.defer=true; g.src=u+'piwik.js'; s.parentNode.insertBefore(g,s);
               })();
    </script> <noscript>
    <p><img alt="" src="//cellprofiler.piwikpro.com/piwik.php?idsite=1" style="border:0;"></p></noscript><!-- End Piwik Code -->
</head>
<body>
    <!--Google Analytics - PHP tracking-->
    <?php include_once("analyticstracking.php") ?><!--End of Google Analytics - PHP tracking-->
    <div class="top bar"></div>
    <div class="documentation-container">
        <div class="row">
            <div class="column-3 hidden-mobile overview-container">
                <script src="http://code.jquery.com/jquery-latest.min.js" type="text/javascript">
                </script>
                <section></section><a href="/"><img src="/images/cp_logo.png" style="margin-left:20px; margin-top:20px" width="175px"></a>
                <section class="top">
                    <a href="/releases/">Download</a>
                </section>
                <section class="top">
                    <a href="/help">Help</a>
                    <ul class="sub" style="list-style-type:none">
                        <li>
                            <a href="/getting_started/">Getting started</a>
                        </li>
                        <li>
                            <a href="/examples">Examples</a>
                        </li>
                        <li>
                            <a href="/tutorials">Tutorials</a>
                        </li>
                        <li>
                            <a href="http://forum.cellprofiler.org/">Forum</a>
                        </li>
                        <li>
                            <a href="http://blog.cellprofiler.org/">Blog</a>
                        </li>
                        <li>
                            <a href="/supportplan/">Custom support</a>
                        </li>
                        <li>
                            <a href="/outreach/">Educational modules</a>
                        </li>
                        <li>
                            <a href="/citations/">Cite us</a>
                        </li>
                    </ul>
                </section>
                <section>
                    <a href="/about/">About</a>
                </section>
                <section class="top">
                    <a href="/cp-analyst/">CellProfiler Analyst</a>
                </section>
                <section>
                    <a href="http://www.broadinstitute.org">
                        <img src="/images/broad_logo.png" style="vertical-align: middle;height:50px">
                        <h3 class="hidden-mobile"></h3>
                    </a>
                    <a href="http://www.facebook.com/cellprofiler">
                        <img src="/images/facebook.svg" style="margin-left:10px; margin-top:21px" width="35px">
                    </a>
                    <a href="http://twitter.com/CellProfiler">
                        <img src="/images/twitter.svg" style="margin-left:10px; margin-top:21px" width="35px">
                    </a>
                    <a href="https://blog.cellprofiler.org/">
                        <img src="/images/wordpress_logo.png" style="margin-left:10px; margin-top:21px" width="35px">
                    </a>
                    <h4 class="hidden-mobile"></h4>
                </section>
            </div>
            <div class="column-3 hidden-mobile empty-container"></div>
            <div class="column-7 mobile-column-3 details-container">
                <section>
                    <div class="row">
                        <div class="column-12">
                            <ul>
                                <li class="navsearch">
                                    <form action="http://google.com/search" method="get" onsubmit="location.href = this.action + '?&amp;q=%2Bsite:cellprofiler.org+' + this.query.value; return false;">
                                        <input maxlength="255" name="query" size="20" type="text" value=""> <input type="submit" value="search">
                                    </form>
                                </li>
                                <li style="list-style: none; display: inline">
                                    <h1><a id="PublishedPipelines" name="PublishedPipelines"></a>Published pipelines</h1>
                                    <p>CellProfiler enables reproducible research because a saved pipeline includes all the modules and settings. Here, we provide links to pipelines used in some published studies, as well as the version of CellProfiler used to create them. You can instead download the most <a href="../releases">current version</a> of CellProfiler; older pipelines should automatically update to the current version when loaded.</p>
                                    <p>If you used CellProfiler in a publication and would like to post your pipelines here, please <a href="mailto:imagingadmin@broadinstitute.org">contact us</a>; we would be happy to host them. Please remember to give CellProfiler the proper <a href="/citations">citation</a> in your paper.</p>
                                    <p>Please note that each download link contains a compressed ZIP file with the following:</p>
                                    <ul>
                                        <li>The CellProfiler pipelines.</li>
                                        <li>Supplemental notes describing the pipelines.</li>
                                    </ul>
                                    <p></p>
                                    <h2>List of publications</h2>
                                    <ul>
                                        <li class="li_ul">
                                            <a id="Jones_2008" name="Jones_2008"></a>Jones, TR, Carpenter AE, Lamprecht MR, Moffat J, Silver SJ, Grenier JK, Castoreno AB, Eggert US, Root DE, Golland P, Sabatini DM (2008). Scoring diverse cellular morphologies in image-based screens with iterative feedback and machine learning. <span style="font-style:italic">PNAS</span> 106(6):1826–1831 / <a href="https://doi.org/10.1073/pnas.0808843106">doi</a>. PMID: 19188593. PMCID: PMC2634799
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/Jones_PNAS_2009_training_sets.zip">[Download]</a>
                                        </li>
                                        <li class="li_ul">
                                            <a id="Logan_2010" name="Logan_2010"></a>Logan DJ, Carpenter AE (2010). Screening cellular feature measurements for image-based assay development. <span style="font-style:italic">J Biomol Screen</span> 15(7): 840–846 / <a href="https://doi.org/10.1177/1087057110370895">doi</a>. PMID: 20516293
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://www.broadinstitute.org/bbbc/BBBC013/">[Broad Bioimage Benchmark Collection entry]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Cataldo_2010" name="Cataldo_2010"></a>Cataldo, Anne M; McPhie, Donna L; Lange, Nicholas T; Punzell, Steven; Elmiligy, Sarah; Ye, Nancy Z; Froimowitz, Michael P; Hassinger, Linda C; Menesale, Emily B; Sargent, Laura W; Logan, David J; Carpenter, Anne E; Cohen, Bruce M (2010). Abnormalities in Mitochondrial Structure in Cells from Patients with Bipolar Disorder. <span style="font-style:italic">Am. J. Pathol.</span> 177(2): 575–585 / <a href="https://doi.org/10.2353/ajpath.2010.081068">doi</a>. PMID: 20566748 PMCID: PMC2913344
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/small_files/Cataldo_2010.cp.zip">[Download]</a> (CellProfiler version <a href="http://http://cellprofiler.org/previousReleases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Elkabets_2010" name="Elkabets_2010"></a>Elkabets M, Gifford AM, Scheel C, Nilsson B, Reinhardt F, Bray MA, Carpenter AE, Jirstr&ouml;m K, Magnuson K, Ebert BL, Ponten F, Weinberg RA, McAllister SS (2011). Human tumors instigate granulin-expressing hematopoietic cells that promote malignancy by activating stromal fibroblasts in mice. <span style="font-style:italic">J Clin Invest</span> 121(2):784-99 / <a href="https://doi.org/10.1172/JCI43757">doi</a>. PMID: 21266779 PMCID: PMC3026724
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Elkabets_2010.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v9978">2.0.9978</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Bray_2011" name="Bray_2011"></a>Bray MA, Fraser AN, Hasaka TP, Carpenter AE (2012). Workflow and metrics for image quality control in large-scale high-content screens. <span style="font-style:italic">J Biomol Screening</span> 17(2):135-143 / <a href="https://doi.org/10.1177/1087057111420292">doi</a>. PMID: 21956170
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Bray_2011_SupplementalMaterial.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Gonzalez_2012" name="Gonzalez_2012"></a>Gonz&aacute;lez JE, Barquinero JF, Lee M, Garc&iacute;a O, Casac&oacute; A (2012). Radiosensitization induced by the anti-epidermal growth factor receptor monoclonal antibodies cetuximab and nimotuzumab in A431 cells. <i>Cancer Biol Ther</i> 13(2):1-6 / <a href="https://doi.org/10.4161/cbt.13.2.18439">doi</a>. PMID: 22231391
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/CancerBiolTher_Gonzalez_2012.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Kitami_2012" name="Kitami_2012"></a>Kitami T, Logan DJ, Negri J, Hasaka T, Tolliday NJ, Carpenter AE, Spiegelman BM, Mootha VK (2012). A chemical screen probing the relationship between mitochondrial content and cell size. <span style="font-style:italic">PLoS ONE</span> 7(3):e33755 / <a href="https://doi.org/10.1371/journal.pone.0033755">doi</a>. PMID: 22479437
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/PIPE_main_batch_InformerBigRun_Threshold_CP10997.cp">[Download]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Gonzalez_2012b" name="Gonzalez_2012b"></a>González JE, Romero I, Barquinero JF, Garcia O. (2012). Automatic analysis of silver-stained comets by CellProfiler software. <span style="font-style:italic">Mutation Research</span> 748(1-2):60-4 / <a href="https://doi.org/10.1016/j.mrgentox.2012.06.007">doi</a>. PMID: 22771502
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/MutationResearch_Gonzalez_2012.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Hartwell_2012" name="Hartwell_2012"></a>Hartwell KA, Miller PG, Mukherjee S, Kahn AR, Stewart AL, Logan DJ, Negri JM, Duvet M, J&auml;r&aring;s M, Puram R, Dancik V, Al-Shahrour F, Kindler T, Tothova Z, Chattopadhyay S, Hasaka T, Narayan R, Dai M, Huang C, Shterental S, Chu LP, Haydu JE, Shieh JH, Steensma DP, Munoz B, Bittker JA, Shamji AF, Clemons PA, Tolliday NJ, Carpenter AE, Gilliland DG, Stern AM, Moore MA, Scadden DT, Schreiber SL, Ebert BL, Golub TR (2013). Niche-based screening identifies small-molecule inhibitors of leukemia stem cells. <span style="font-style:italic">Nat Chem Biol</span> 9(12):840-8 / <a href="https://doi.org/10.1038/nchembio.1367">doi</a>. PMID: 24161946
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Hartwell_2012.zip">[Download]</a> (Note:CellProfiler version 7807 for Windows7 64bit included in download) (CellProfiler Analyst version <a href="http://cellprofiler.org/releases/">11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Chudnovsky_2012" name="Chudnovsky_2012"></a>Chudnovsky Y, Kim D, Zheng S, Whyte WA, Bansal M, Bray MA, Gopal S, Theisen MA, Bilodeau S, Thiru P, Muffat J, Yilmaz OH, Mitalipova M, Woolard K, Lee J, Nishimura R, Sakata N, Fine HA, Carpenter AE, Silver SJ, Verhaak RGW, Califano A, Young RA, Ligon KL, Mellinghoff IK, Root DE, Sabatini DM, Hahn WC, Chheda MG (2014). ZFHX4 interacts with the NuRD core member CHD4 and regulates the glioblastoma tumor-initiating cell state. <span style="font-style:italic">Cell Reports</span> 6(2):313-24 / <a href="https://doi.org/10.1016/j.celrep.2013.12.032">doi</a>. PMID: 24440720
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/CellReports_Chudnovsky_2012.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Nieland_2014" name="Nieland_2014"></a>Nieland, TJF; Logan, DJ; Saulnier, J; Lam, D; Johnson, C; Root, DE; Carpenter, AE; Sabatini, BL (2014). High Content Image Analysis Identifies Novel Regulators of Synaptogenesis in a High-Throughput RNAi Screen of Primary Neurons <span style="font-style:italic">PLoS ONE</span> 9(3).e91744 / <a href="https://doi.org/10.1371/journal.pone.0091744">doi</a>. PMID: 24633176
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/PLoSOne_Nieland_2014.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Moldovan_2014" name="Moldovan_2014"></a>Moldovan L, Anghelina M, Kantor T, Jones D, Ramadan E, Xiang Y, Huang K, Kolipaka A, Malarkey W, Ghasemzadeh N, Mohler PJ, Quyyumi A, Moldovan NI (2014). A module of human peripheral blood mononuclear cell rranscriptional network containing primitive and differentiation markers is related to specific cardiovascular health variables. <span style="font-style:italic">PLoS ONE</span> 9(4):e95124 / <a href="https://doi.org/10.1371/journal.pone.0095124">doi</a>. PMID: 24759906
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/PLoSOne_Moldovan_2014.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="SheikKhalil_2014" name="SheikKhalil_2014"></a>Sheik-Khalil E, Bray MA, Ozkaya Şahin G, Scarlatti G, Jansson M, Carpenter AE, Feny&ouml; EM (2014). Automated image-based assay for evaluation of HIV neutralization and cell-to-cell fusion inhibition. <span style="font-style:italic">BMC Infect Dis</span> 14:472 / <a href="https://doi.org/10.1186/1471-2334-14-472">doi</a>. PMID: 25176034
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/SheikKhalil_2014.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Singh_2014" name="Singh_2014"></a>Singh S, Bray MA, Jones TR, Carpenter AE (2014). Pipeline for illumination correction of images for high-throughput microscopy. <span style="font-style:italic">Journal of Microscopy</span> 256(3):231-6 / <a href="https://doi.org/10.1111/jmi.12178">doi</a>. PMID: 25228240
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/JMicroscopy_Singh_2014.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#2.1.0">2.1.0</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Metelo_2013" name="Metelo_2013"></a>Metelo AM, Noonan HR, Li X, Jin Y, Baker R, Kamentsky L, Zhang Y, van Rooijen E, Shin J, Carpenter AE, Yeh JR, Peterson RT, Iliopoulos O (2015). Pharmacological HIF2&alpha; inhibition improves VHL disease-associated phenotypes in zebrafish model. <span style="font-style:italic">Journal of Clinical Investigation</span> 25(5): 1987-97 / <a href="https://doi.org/10.1172/JCI73665">doi</a>. PMID: 25866969
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Metelo_2013.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v11710">2.0.11710</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Du_2014" name="Du_2014"></a>Du Z, Abedalthagafi M, Aizer AA, McHenry AR, Sun HH, Bray MA, Viramontes O, Machaidze R, Brastianos PK, Reardon DA, Dunn IF, Freeman GJ, Ligon KL, Carpenter AE, Alexander BM, Agar NY, Rodig SJ, Bradshaw EM, Santagata S (2014). Increased expression of the immune modulatory molecule PD-L1 (CD274) in anaplastic meningioma. <span style="font-style:italic">Oncotarget</span> 10;6(7):4704-16 / <a href="https://doi.org/10.18632/oncotarget.3082">doi</a>. PMID: 25609200
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Du_2014.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#2.1.0">2.1.0</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Leavesley_2015" name="Leavesley_2015"></a>Leavesley SJ, Nakhmani A, Gao Y, Rich TC (2015). Automated Image Analysis of FRET Signals for Subcellular cAMP Quantification. <span style="font-style:italic">Methods in Molecular Biology</span> 1294:59-70 / <a href="https://doi.org/10.1007/978-1-4939-2537-7_5">doi</a>. PMID: 25783877
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Leavesley_2015.zip">[Download]</a> (CellProfiler version <a href="../previous_releases#2.1.1">2.1.1</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Logan_2015" name="Logan_2015"></a>Logan DJ, Shan J, Bhatia SN, Carpenter AE (2015). Quantifying co-cultured cell phenotypes in high-throughput using pixel-based classification. <span style="font-style:italic">Methods</span> 96:6-11 / <a href="https://doi.org/10.1016/j.ymeth.2015.12.002">doi</a>. PMID: 26687239. PMCID: PMC4766037.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://www.broadinstitute.org/bbbc/BBBC026/">[Broad Bioimage Benchmark Collection entry]</a>
                                        </li>
                                        <li class="li_ul">
                                            <a id="Jolly_2015" name="Jolly_2015"></a>Jolly AL, Luan CH, Dusel BE, Dunne SF, Winding MJ, Dixit VJ, Robins C, Saluk JL, Logan DJ, Carpenter AE, Cohen, AR, Gelfand VI (2015). A Genome-wide RNAi screen for microtubule network formation and lysosome motility regulation in Drosophila S2 cells. <span style="font-style:italic">Cell Reports</span> 14(3):611-20 / <a href="https://doi.org/10.1016/j.celrep.2015.12.051">doi</a>. PMID: 26774481.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Jolly_Lysomsome_Motility_2015.zip">[Download]</a> (CellProfiler version <a href="/previous_releases#v10997">2.0.10997</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Ricci_2015" name="Ricci_2015"></a>Ricci F, Subramanian A, Wade M (2015). Open access to high-content clonogenic analysis. <span style="font-style:italic">Journal of Biomolecular Screening</span> 20(3): 391-401 / <a href="http://www.dx.doi.org/10.1177/1087057114557775">doi</a>. PMID: 25381257.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Ricci_2015.zip">[Download]</a> (CellProfiler version <a href="http://d1zymp9ayga15t.cloudfront.net/releases/2.1.1/CellProfiler_2.1.1_win64_r20140723174500.exe">version 2.1.1 (revision 6c2d896; for Windows 64-bit).</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Grenfell_2016" name="Grenfell_2016"></a>Grenfell A, Strzelecka M, Crowder ME, Helmke KJ, Schlaitz AL, Heald R (2016). A versatile multivariate image analysis pipeline reveals features of Xenopus extract spindles. <span style="font-style:italic">Journal of Cell Biology</span> 213(1): 127-136 / <a href="http://www.dx.doi.org/10.1083/jcb.201509079">doi</a>. PMID: 27044897.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Grenfell_2016.zip">[Download]</a> (CellProfiler version <a href="../previous_releases#2.1.1">2.1.1</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Buys_2015" name="Buys_2015"></a>Dordea AC, Bray MA, Allen K, Fei F, Gregory M, Carpenter AE, Buys ES (2016). An open-source computational tool to automatically quantify immunolabeled retinal ganglion cells. <span style="font-style:italic">Experimental Eye Research</span> / <a href="https://doi.org/10.1016/j.exer.2016.04.012">doi</a>. PMID: 27119563. PMCID: PMC4903927.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Buys_2015.zip">[Download]</a> (CellProfiler version <a href="../previous_releases#2.1.1">2.1.1</a>)
                                        </li>
                                        <li class="li_ul">
                                            <a id="Shan_2016" name="Shan_2016"></a>Shan J, Logan DJ, Root DE, Carpenter AE, and Bhatia SN (2016). High-throughput platform for the identification of molecular factors involved in phenotypic stabilization of primary human hepatocytes in vitro. <span style="font-style:italic">Journal of Biomolecular Screening</span>. 21(9):897-911 / <a href="https://doi.org/10.1177/1087057116660277">doi</a> . PMID: 27650791. PMCID: in process.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Shan_et_al_2016.zip">[Download]</a>
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Melo_Filho_2016" name="Melo_Filho_2016"></a>Melo-Filho CC, Dantas RF, Braga RC, Neves BJ, Senger MR, Valente WCG, Rezende-Neto JM, Chaves WT, Muratov EN, Paveley RA, Furnham N, Kamentsky L, Carpenter AE, Silva-Junior FP, Andrade CH (2016). QSAR-Driven Discovery of Novel Chemical Scaffolds Active against <i>Schistosoma mansoni</i>. <span style="font-style:italic">Journal of Chemical Information and Modeling</span> / <a href="https://doi.org/10.1021/acs.jcim.6b00055">doi</a>.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Melo_Filho_2016.zip">[Download]</a>
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Zimmermann_Meisse_2017" name="Zimmermann_Meisse_2017"></a>Zimmermann-Meisse G, Prévost G, Jover E (2017). Above and beyond C5a Receptor Targeting by Staphylococcal Leucotoxins: Retrograde Transport of Panton-Valentine Leucocidin and γ-Hemolysin. <span style="font-style:italic">Toxins</span> / <a href="https://doi.org/10.3390/toxins9010041">doi</a>.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Zimmermann_Meisse_2016.zip">[Download]</a>
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Bray_2017" name="Bray_2017"></a>Bray MA, Gustafsdottir SM, Ljosa V, Singh S, Sokolnicki KL, Bittker JA, Bodycombe NE, Dancík V, Hasaka TP, Hon CS, Kemp MM, Li K, Walpita D, Wawer MJ, Golub TR, Schreiber SL, Clemons PA, Shamji AF, Carpenter AE (2017). A dataset of images and morphological profiles of 30,000 small-molecule treatments using the Cell Painting assay. <span style="font-style:italic">Gigascience</span> / <a href="https://doi.org/10.1093/gigascience/giw014">doi</a>.
                                        <li class="li_ul" style="list-style:none">
                                            <a href="https://github.com/gigascience/paper-bray2017">[Github repository]</a> (CellProfiler version <a href="http://cellprofiler.org/previous_releases#2.1.1">2.1.1</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Barczak_2017" name="Barczak_2017"></a>Barczak A, Avraham R, Singh S, Luo SS, Zhang WR, Bray MA, Hinman AE, Thompson M, Nietupski RM, Golas A, Montgomery P, Fitzgerald M, Smith RS, White DW, Tischler AD, Carpenter AE, and Hung DT (2017). Systematic, multiparametric analysis of Mycobacterium tuberculosis intracellular infection offers insight into coordinated virulence. <span style="font-style:italic">PLoS ONE</span> .
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Barczak_PLoSONE_2017.zip">[Download]</a>
                                        </li>
                                        <li class="li_ul">
                                            <a id="Sucic_2017" name="Sucic_2017"></a>Sucic L, Galati-Fournier V, Kym U, Pfeifle V, Gros S, Schäfer KH, Holland-Cunz S, Keck S (2017). Increased regulatory T cells in pediatric acute appendicitis. <span style="font-style:italic">Pediatr Allergy Immunol.</span> <a href="https://doi.org/10.1111/pai.12797">doi</a>. PMID: 28881058.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Sucic_2017.zip">[Download]</a> (CellProfiler version <a href="http://cellprofiler.org/previous_releases#2.2.0">2.2.0</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Erben_2017" name="Erben_2017"></a>Erben L, He M-X, Laeremans A, Park E, Buonanno A (2017). QA Novel Ultrasensitive In Situ Hybridization Approach to Detect Short Sequences and Splice Variants with Cellular Resolution. <span style="font-style:italic">Mol Neurobiol.</span> / <a href="https://doi.org/10.1007/s12035-017-0834-6">doi</a>. PMID: 29264769.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Erben_2017.zip">[Download]</a> (CellProfiler version <a href="http://cellprofiler.org/previous_releases#2.2.0">2.2.0</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Bray_2018" name="Bray_2018"></a>Bray MA, Carpenter AE (2018). Quality Control for High-Throughput Imaging Experiments Using Machine Learning in Cellprofiler. <span style="font-style:italic">Methods Mol. Biol.</span> / <a href="https://doi.org/10.1007/978-1-4939-7357-6_7">doi</a>. PMID: 29082489.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Bray_MIMB_2018.zip">[Download]</a> (CellProfiler version <a href="http://cellprofiler.org/previous_releases#2.2.0">2.2.0</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Zhang_2018" name="Zhang_2018"></a>Zhang H, Ericsson M, Virtanen M, Weström S, Wählby C, Vahlquist A, Törmä H (2018). Quantitative image analysis of protein expression and colocalisation in skin sections. <span style="font-style:italic">Exp Dermatol.</span> / <a href="https://doi.org/10.1111/exd.13457">doi</a>. PMID: 29094393.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Zhang_2018.zip">[Download]</a> (CellProfiler version <a href="http://cellprofiler.org/previous_releases#2.2.0">2.2.0</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Bouçanova_2018" name="Bouçanova_2018"></a>Bouçanova F, Maia AF, Cruz A, Millar V, Mendes Pinto I, Relvas JB, Domingues HS (2018). Collar occupancy: A new quantitative imaging tool for morphometric analysis of oligodendrocytes. <span style="font-style:italic">J Neurosci Methods</span> 294:122–135 / <a href="https://doi.org/10.1016/j.jneumeth.2017.11.014">doi</a>. PMID: 29174019.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="https://github.com/andrefilipemaia/Collar-occupancy">[Github repository]</a> (CellProfiler version <a href="">2.2.0 </a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Salzmann_2018" name="Salzmann_2018"></a>Salzmann M, Hoesel B, Haase M, Mussbacher M, Schrottmaier WC, Kral-Pointner JB, Finsterbusch M, Mazharian A, Assinger A, Schmid JA (2018). A novel method for automated assessment of megakaryocyte differentiation and proplatelet formation. <span style="font-style:italic">Platelets</span> :1–8 / <a href="https://doi.org/10.1080/09537104.2018.1430359">doi</a>. PMID: 29461915.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Salzmann_2018.zip">[Download]</a> (CellProfiler version <a href="/releases">3.0.0</a>)
                                        </li>
                                        <li class="li_ul&quot;">
                                            <a id="Niels_2018" name="Niels_2018"></a>Van Tol N, Rolloos M, van Loon P, van der Zaal B. J. (2018). MeioSeed: a CellProfiler-based program to count fluorescent seeds for crossover frequency analysis in Arabidopsis thaliana.  <span style="font-style:italic">Plant Methods</span>, 14: 32. / <a href="https://dx.doi.org/10.1186%2Fs13007-018-0298-3">doi</a>. PMCID: PMC5905130.
                                        </li>
                                        <li class="li_ul" style="list-style:none">
                                            <a href="http://d1zymp9ayga15t.cloudfront.net/PublishedPipelines/Niels_2018.zip">[Download]</a> (includes pipeline and classifier files) (CellProfiler version <a href="/releases">2.1.1</a>)
                                        </li>
                                    </ul>
                                    <!--Remove and add as needed, based on if there are pre-publication pipelines presently--
        <h2>
          Pre-publication pipelines
        </h2>

        <ul>

        </ul>
-->
                                </li>
                            </ul>
                        </div>
                    </div>
                </section>
            </div>
        </div>
    </div>
</body>
</html>
