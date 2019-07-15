Time Stamped Projects and Descriptions

jcoffman_001.1559775549:   Learning to Run Pipelines

jcoffman_001_1559678964:   Learning to Run Pipelines

jcoffman_001.1560276857:   Learning to Run Pipelines

jcoffman_001.1560344582:   Learning to Run Pipelines

jcoffman_001.1561383557:   Learning to Run Pipelines

jcoffman_001.1561661050:   Copied unmodified CWL workflows (pe - unstranded - w/ sjdb) to new directory, test, failed

jcoffman_001.1561668222:   Copied unmodified CWL workflows (pe - unstranded - w/ sjdb) to new directory, test, successful

jcoffman_001.1561730462:   Umodified CWL workflow (pe - unstranded - w/ sjdb). sjdbOverhang set to 49 in JSON template. (My reason for doing this: online forums suggest optimal length is -1 readlength, and Sample 1 of Coffman data has read - length 50. Previous sjdbOverhang setting was 100. FAILED: "EXITING because of fatal PARAMETERS error: present --sjdbOverhang=49 is not equal to the value at the genome generation step =100." Leaving this unexplored for now and moving to parameters that are potentially more interesting.

jcoffman_001.1561736697:    Unmodified CWL workflow (pe - unstranded - w/ sjdb). Attempting to pass --outFilterMultimapNmax value of 1 when default is 10. I believe I will be able to accomplish this w/o modding cwl as it is present exactly as nthreads is in both pipeline and individual step nested workflows. Everything except the QUANT step worked. Wasn't able to interpret console error response. I'm going to try to modify the sample-specific (sample 1) json file as to pass 10 for --outFilterMultimapNmax, which is the default value. This will allow me to determine whether or not failure is due to the value I passed through the JSON file, or the fact I am passing a parameter. THIS SUCCESSFULLY generated .___.____.rsem.genes.results. 

jcoffman_001.1561985819:   Uses JSON file from sample SL94881 with --outFilterMultimapNmax value set to 9 as template. Only run with SL94881. Failed to produce genes.results file. Attempting rerun on the cloud. This may be related to lack of specification of param at the level of the workflow. Cloud run was successful, but further analysis is needed to determine whether parameter made any difference.

jcoffman_001.1562004646:   It appears --outFilterMultimapNmax values are hardcoded at the level of the analysis step. There are two references to this paramemter in the default 03-map...., the first is a value of 1, and the second is a value of 20. In this run I've modified the cwl script so the first reference to outFilterMultimapnMax has value =2. Sample-single-pipeline-loca Run #385

jcoffman_001.1562012036:  Identical to original jcoffman_001.1561736697 with --outFilterMultimapNmax set = 1, except this one is run on cloud. Success of jcoffman_001.1562004646 indicates pipeline success may be related to an issue specific to the local server. Run-cwl-cloud #160.
                                      
jcoffman_001.1562073104:  In this run I've modified the cwl script so the first reference to outFilterMultimapnMax has value =10. Local 
                          single sample run #386. 

jcoffman_001.1562086760: alignIntronMax changed from 1000000 to 100000 in cwl of 03-map....., local build.

jcoffman_001.1562098405: outFilterMismatchNoverReadLmax changed from 0.04 to 0.1 in cwl of 03-map..., hard-coded. This made a difference in expected read counts. It seems though high reads counds might be disproportionately affected. 

jcoffman_001.1562160660: outFilterMismatchNoverReadLmax changed from 0.04 to 0.004 in cwl of 03-map..., hard-coded.

jcoffman_001.1562175149: outFilterMismatchNoverReadLmax changed from 0.04 to 0.4 in cwl of 03-map..., hard-coded.

jcoffman_001.1562270812: sjdbScore changed for 1 to 5 in cwl of 03-map..., hardcoded. General elevation in read counts. 

jcoffman_001.1562334134: sjdbScore set from 1 to 0.2 in 03-map ..., hardcoded. After multiple attempts and variations this run never worked. I'm aborting it. 

jcoffman_001.1562611492: sjdbScore set from 1 to 2 in 03-map ..., hardcoded. 

jcoffman_001.1562684990: outFilterMismatchNmax set from 999 to 100 in 03-map ..., hardcoded. 

jcoffman_001.1562695614:outFilterMismatchNoverReadLmax changed from 0.04 to 0.004, JSON PASS TEST

jcoffman_001.1562717283: outFilterMismatchNoverReadLmax changed from 0.04 to 0.004, Hard coded control JSON PASS TEST

jcoffman_001.1562768838: --alignSJoverhangMin changed from 8 to 20, Hard Coded 03-map...

jcoffman_001.1562791941: --outFilterMatchNmin added of 03-map .. cwl file, default 0 changed to 1. I couldn't get this run to work properly. Jenkins reports success but doesn't produces *.genes.results. Sometimes, I can delete the sample folder in scratch created by the run, and the run log in scratch, and retrigger the run - successfully producing a *.genes.results, but in this case, after 3 attempts I was unable to produce the file. 

jcoffman_001.1562869653 : --outFilterMismatchNoverReadLmax (Hard Coded) changed from 0.04 to 0.004 in )3-map . . . cwl, and analysis triggered for all Coffman cortisol data.

jcoffman_001.1563039743: --outFilterMismatchNoverReadLmax (Hard Coded) changed from 0.04 to 0.013 in )3-map . . . cwl, and analysis triggered for all Coffman cortisol data.

jcoffman_001.1563195792: --outFilterMismatchNoverReadLmax (Hard Coded) changed from 0.04 to 0.022 in )3-map . . . cwl, and analysis triggered for all Coffman cortisol data.
