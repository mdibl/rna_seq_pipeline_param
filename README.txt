Time Stamped Projects and Descriptions

jcoffman_001.1559775549   Learning to Run Pipelines
jcoffman_001_1559678964   Learning to Run Pipelines
jcoffman_001.1560276857   Learning to Run Pipelines
jcoffman_001.1560344582   Learning to Run Pipelines
jcoffman_001.1561383557   Learning to Run Pipelines
jcoffman_001.1561661050   Copied unmodified CWL workflows (pe - unstranded - w/ sjdb) to new directory, test, failed
jcoffman_001.1561668222   Copied unmodified CWL workflows (pe - unstranded - w/ sjdb) to new directory, test, successful
jcoffman_001.1561730462   Umodified CWL workflow (pe - unstranded - w/ sjdb). sjdbOverhang set to 49 in JSON template. (My reason for       
                          doing this: online forums suggest optimal length is -1 readlength, and Sample 1 of Coffman data has read -
                          length 50. Previous sjdbOverhang setting was 100. FAILED: "EXITING because of fatal PARAMETERS error: present 
                          --sjdbOverhang=49 is not equal to the value at the genome generation step =100." Leaving this unexplored for now 
                          and moving to parameters that are potentially more interesting.
jcoffman_001.1561736697   Unmodified CWL workflow (pe - unstranded - w/ sjdb). Attempting to pass --outFilterMultimapNmax value of 1 when 
                          default is 10. I believe I will be able to accomplish this w/o modding cwl as it is present exactly as nthreads
                          is in both pipeline and individual step nested workflows. 
