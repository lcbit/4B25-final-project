# A Functionalized Sensor for Museum Monitoring 
###### Qian WANG, Emmanuel, qw251

## Project summary
The project aims to develop a hardware system for museum environmental monitoring based on integrated warp platform. It provides an entry-level prototype for highly integrated low-cost monitoring system suitable for large-scale deployment. 

Three main contributions, both research and commericalization are listed as follows; (a) Acquire data and knowledge for museum environmental factors; (b) Based on the abundant data collected, enable the potential for better museum structural design and improve the daily relic preservation strategies; (c) Lower system cost can potentially lead to higher deployment rates for not only research but also commercial use. 

This project would eventually beneﬁt those who are working for preservation in the areas like museums. It can also provide a low-cost monitoring system solution for researchers focusing on real-time environmental performance analyses.

## Repository layout
The system firmware is built based upon Warp-firmware, made available to public by Physical Computation Laboratory, Cambridge.

In order for the project to work, it is essential to do the following.

    cd ./Warp-firmware/build/ksdk1.1.0
and then type in

    ./build.sh
to build the project.

To run the system, use the following commands

    /Applications/SEGGER/JLink/JLinkExe -device MKL03Z32XXX4 -if SWD -speed 4000 -CommanderScript ../../tools/scripts/jlink.commands
In the other shell window, launch the JLink RTT client to interact with the Warp platform and obtain the raw data.

Full information on how to configure Warp-firmware is shown in https://github.com/physical-computation/Warp-firmware

Except for the repositories present in the link above. There are three repositories. The raw data for measurements are stored in the /Data folder. The /Reference folder contains datasheets as well as references. The /BME680 Driver folder in warp-firmware/src/boot contains the referenced Bosch code for data calibration and ADC value convertion.
