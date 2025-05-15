# Versitile Tips & Tricks
- A helpful note for all procedures is to first go to the AcqMode page, find the Channel Mask section and ensure all channels that you are not using are disabled.
- Make sure you are using the correct plot and statstics type
- If you have any issues, the solution maybe be found within the CAEN & Janus Cheat Sheet

# Cosmics

## Single SiPMs
1. Ensure the connection to all the SiPMs is secure, tape the tiles to the fixture atop the SiPM, close the dark box and set the HV Bias to a suitable level for the SiPM. 
2. In AcqMode in Janus, set the Bunch Trigger Source to TLOGIC. Then find Trigger Logic within the same page and set that Maj64.
3. In the Discr page, find the T-Discr mask and disable every channel expect for the channels corresponding to the top and bottom SiPMs. 

## Stacked Boards
1. Switch the back of the CAEN unit from the original red plate (64 Channel FERS) to the green Oak Ridge LFHCAL-HQCD adapter 
2. Use the blue wide cabling to hook up the CAEN unit to the board stack.
3. Ensure all boards within the stack are properly connected. 
4. In AcqMode, set Bunch Trigger Source to TLOGIC. In Trigger Logic within the same page set it to OR32_AND2.
5. In Discr page, find the T-Discr mask and disable every channel expect for the channels corresponding to the top and bottom boards.

# SPS
1. Ensure the waveform generator is set up correctly 
2. Make sure the waveform generator is connected to the CAEN unit
3. Set the Bunch Trigger Source in AcqMode to the corresponding input channel on the CAEN unit 

# Testing for Grounding Issues
1. Set up whatever experiment you are going to run 
2. Go into AcqMode and set the Bunch Trigger Source to PTRG
3. Find Periodic Trigger Period on the same page and set it to 1 ms
3. In Spectroscopy set Pedestal Position to >100, in order to see the full pedestal. 
4. Let the program run for a minute or two, keep in mind a disconnected channel will have an RMS around 6
