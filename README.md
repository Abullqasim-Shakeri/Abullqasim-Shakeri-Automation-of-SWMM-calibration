# Abullqasim-Shakeri-Automation-of-SWMM-calibration
This code was written down by me, for a class project in order to calibrate SWMM model for all 48 given rain events. 

For the new modified code, the following steps will apply:  
1. for each rain event it will replace the Imperviousness, width and slope values for all catchments at once, and then it run the model for the given values.  
2. It will calculate the NSE and PFE values
3. At third step, I put some conditions:  
  * if NSE value be greater than 0.88 and PFE value is smaller than 0.15 it will add the imperviousness, width, slope and their respective NSE and PFE values to the “calibrated_sub.csv, after that, it will break out of this loop and continue with the next rain event calibration.  
  * But if the above-mentioned condition was not fulfilled it will go back to first step and loop again, but each time with new random values for each parameter until the condition is fulfilled. 
  * I realized for some rain events it will take a lot of time to be calibrated, in order to save time and also see if the code is working or not, I wrote a short condition. if the loops continue more than 150 times, and the above-mentioned condition was not fulfilled, it should break out of the loop and continue with next rain event. So the NSE and PFE values for the rain events which were not calibrated, are the NSE and PFE value of the last loop (150th).     There was possibility to not add the NSE and PFE values for those rain events, or add a text like “this rain event was not calibrated”. Or even add another condition to ease the calibration criteria for those rain event if they were not calibrated after 150 time, I mean instead of 0.88 for NSE and 0.15 for PFE, they could be calibrated with 0.85 of NSE and 0.20 of PFE. But for all these conditions it needed a bit of more time to write them down. Since I was a bit busy with submission of another report yesterday. So, I thought it would be fine if I just leave them that way. Therefor you can ignore the NSE and PFE for not calibrated rain events.

The csv file contain of observed data was deleted from the repository due to data sharing permision. 
