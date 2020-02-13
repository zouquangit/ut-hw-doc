This procedure acts under the assumption that the user is utilizing the
pre-built CCM QA setup.

1. Turn on both oscilloscopes connected to the LVR
2. Take a master slave CCM pair
    1. Validate that the pair are both either 1.2, 1.5, or 2.5 V

3. Install the CCM master-slave pair on channels 1 & 2 of the LVR.

    !!! note
        In the case of a master-slave pair, you CANNOT install 2 masters or
        2 slaves on the same 2-channel pair

4. Set the input voltage of the power supply to ~5.5 V
5. Note the wave pattern on the first oscilloscope displaying 4
   distinct channels.

    !!! note
        Note that channels 1 and 2 correspond to the master, where
        channels 3 and 4 correspond to the slave.

        ![](ccm_qa1.png)

        The waveform displayed should be a smooth curve as shown in the figure
        above.

6. Locate the variable resistor on the master CCM, and note the voltage
   reading on channel 1 of the second oscilloscope, denoted `Vtop`.

7. Adjust the variable resistor so the voltage reading of channel 1
   corresponds to the voltage of the CCM (i.e. a 1.5 V CCM should have
   a channel reading of ~1.5 V) as shown below for a 1.5 V CCM

    ![](ccm_qa2.png)

8. After adjusting the variable resistor, go back to the first
   oscilloscope readings
9. If the waveform displayed is still not smooth, note the following
    1. If the bottom two curves ONLY are not smooth, this indicates a
       problem with the slave

    2. If BOTH curves are not smooth, replace the master CCM with a
       validated master CCM with the same voltage identity.
        1. If after replacing the curve is smooth and normal, the
           previous master CCM has a problem
        2. If after replacing the bottom curve is not smooth, this
           indicates a problem with the previous master CCM and the
           current slave CCM