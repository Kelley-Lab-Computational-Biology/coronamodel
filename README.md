# coronamodel
Kelley lab stochastic Coronavirus model

This GitHub folder is for the article Temporal Dynamics of Viral Load and False Negative Rate Influence the Levels of Testing Necessary to Combat COVID19 Spread. 
There are two folders and I will describe what is in and how to run each.

    1. FiguresScript
        This script is for producing Figure 6,7,8 seen in the paper. The raw data is stored in the mat files 
        'apparentfalsenegativerates.mat' and 'r0_all.mat'.
        
        In order to run. Download the folder and open in Matlab. 
        Run the file FiguresScript.mlx to produce the figures.
        
    2. Scenarios
            Scenarios runs the model itself. This can be done in two ways, separated by folders:
            
                  1. Scenarios_individually: 
                           Each version of the model can be run on its own with one input for Number of Tests and Frequency of Tests.
                           
                           To run, simply select a scenario:
                                    - Scenario1_PerfectTestsUniformSpread.mlx
                                    - Scenario2_SimpleUndetectabilityFastSpread.mlx
                                    - Scenario3_DynamicFalseNegSlowSpread.mlx
                                    - Scenario4_DynamicFalseNegFastSpread.mlx
                            Then specify your desired number of tests, frequency of test, iteration size (or don't).
                            
                            The output is a boxplot of the Rt showing the median and 95% Confidence Interval based on the number 
                            of iterations.
                            
                  2. Scenarios_makeHeatmapRt: Each version of the model can be run with a vector of Number of Tests and Frequency 
                            of Tests which enables the user to input multiple Number of Tests and/or Frequency of Tests. 
                            
                            To run, select 'Driver_makeHeatmapRt' in the scenarios folder. There you can input your vector or 
                            Number of Tests and Frequency of Tests as well as select which scenario conditions 
                            (same as listed above) on line 28 of the driver script.
                            
                            The output is a figure with 2 subplots. One subplot is a heatmap of the medians of every condition 
                            specified, and the second subplot is a heatmap of the 95th Percentile.
              
Enjoy!
-kfj
                          
