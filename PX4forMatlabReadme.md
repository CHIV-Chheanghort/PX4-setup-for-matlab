
CHAPTER1: 	Windows PowerShell

1, Open Windows PowerShell, run as administrator.
2, Type “wsl --install -d Ubuntu-22.04” then press Enter.








	Reboot ur laptop if the processing is too slow. (optional)

3, After completed 100%, It will pop up “Enter your name:”. Enter your name then press ENTER!!
Then, fill your password, (E.g. 66574) “REMEMBER UR PASSWORD BCUS IT WLL NOT SHOWN UP”

Chapter2:                                          	 WSL
1, Step1: Run WSL as administrator type < sudo apt update>
2, Step2: Type < sudo apt upgrade >
3, Step3: Type < sudo apt install gedit >





Chapter3:   	 Downloading Support Package and Setup

1, Go to any browser to download px4 support package and then download it 
Link: https://www.mathworks.com/matlabcentral/fileexchange/70016-uav-toolbox-support-package-for-px4-autopilots
!!! Do not run it yet, wait until you finish the Clone step
2. Clone PX4 Firmware Path 
	This step required you to not properly to avoid getting error while processing installation!!!
Link: https://www.mathworks.com/help/releases/R2025b/uav/px4/ug/px4-firmware-path-wsl2.html
Follow the instruction the link

3. Go to your download location open this px4.mlpkginstall. (Wait a few minutes until this tap show up).














Click Next, then you will see this section shown up:












Click Validate, then next
4. Toolchain Setup















You can click on Link or copy and paste this link below:
https://www.mathworks.com/help/releases/R2025b/uav/px4/ug/setup-px4-toolchain-wsl.html
Follow this instruction in the link!
It should be show like below:
 

5. PX4 Autopilot and Build Target
	In this case we choose board: PX4 Pixhawk 4 
	Build target: px4_fmu-5v_multicopter
Then click Next
you will find the new tab showing this:












	Follow this pictures guide:
























Click on the Link to download QGroundControl if you haven’t gotten yet
NOTE: Make sure in stall in the local drive C: 












then next,













Build Firmware
!!!Before build firmware make sure you plug in PX4 Pixhawk 




Click upload Firmware:








Plug and unplug till the process is processing in the command window of MATLAB.

	Then Get Accelerometer data 














Click Next, Finish















	Note: If there is an error in building firmware


 

1.	Check the root cause by running this comment in WSL
cd /home/username/PX4-Autopilot 
make px4_fmu-v5_default  # (Replace with your specific hardware target)
2.	If this fails in the terminal, it will give you a specific line number or missing package name.
e.g.

 In this case, the error caused by an incompatibility between the PX4 source code and the version of the Python package in Ubuntu environment so the it means that package version is 4.0 or higher but we need the python package to be 3.3.4 version
	Solution
1.	Uninstall the current version using this command lines in WSL:
pip uninstall em
pip uninstall empy
2.	Install the correct version with this command below:
pip install empy==3.3.4
3.	Clean the previous build with this command:
cd ~/PX4-Autopilot
make clean
make distclean
4.	Finally verification 
Run this command:
python3 -c "import em; print(em.__version__)"
it should be showing 3.3.4 version 
Now finally the error has been solved and we can now build the firmware. 😊

CHAPTER1: 	Windows PowerShell

1, Open Windows PowerShell, run as administrator.
2, Type “wsl --install -d Ubuntu-22.04” then press Enter.








	Reboot ur laptop if the processing is too slow. (optional)

3, After completed 100%, It will pop up “Enter your name:”. Enter your name then press ENTER!!
Then, fill your password, (E.g. 66574) “REMEMBER UR PASSWORD BCUS IT WLL NOT SHOWN UP”

Chapter2:                                          	 WSL
1, Step1: Run WSL as administrator type < sudo apt update>
2, Step2: Type < sudo apt upgrade >
3, Step3: Type < sudo apt install gedit >





Chapter3:   	 Downloading Support Package and Setup

1, Go to any browser to download px4 support package and then download it 
Link: https://www.mathworks.com/matlabcentral/fileexchange/70016-uav-toolbox-support-package-for-px4-autopilots
!!! Do not run it yet, wait until you finish the Clone step
2. Clone PX4 Firmware Path 
	This step required you to not properly to avoid getting error while processing installation!!!
Link: https://www.mathworks.com/help/releases/R2025b/uav/px4/ug/px4-firmware-path-wsl2.html
Follow the instruction the link

3. Go to your download location open this px4.mlpkginstall. (Wait a few minutes until this tap show up).














Click Next, then you will see this section shown up:












Click Validate, then next
4. Toolchain Setup















You can click on Link or copy and paste this link below:
https://www.mathworks.com/help/releases/R2025b/uav/px4/ug/setup-px4-toolchain-wsl.html
Follow this instruction in the link!
It should be show like below:
 

5. PX4 Autopilot and Build Target
	In this case we choose board: PX4 Pixhawk 4 
	Build target: px4_fmu-5v_multicopter
Then click Next
you will find the new tab showing this:












	Follow this pictures guide:
























Click on the Link to download QGroundControl if you haven’t gotten yet
NOTE: Make sure in stall in the local drive C: 












then next,













Build Firmware
!!!Before build firmware make sure you plug in PX4 Pixhawk 




Click upload Firmware:








Plug and unplug till the process is processing in the command window of MATLAB.

	Then Get Accelerometer data 














Click Next, Finish















	Note: If there is an error in building firmware


 

1.	Check the root cause by running this comment in WSL
cd /home/username/PX4-Autopilot 
make px4_fmu-v5_default  # (Replace with your specific hardware target)
2.	If this fails in the terminal, it will give you a specific line number or missing package name.
e.g.

 In this case, the error caused by an incompatibility between the PX4 source code and the version of the Python package in Ubuntu environment so the it means that package version is 4.0 or higher but we need the python package to be 3.3.4 version
	Solution
1.	Uninstall the current version using this command lines in WSL:
pip uninstall em
pip uninstall empy
2.	Install the correct version with this command below:
pip install empy==3.3.4
3.	Clean the previous build with this command:
cd ~/PX4-Autopilot
make clean
make distclean
4.	Finally verification 
Run this command:
python3 -c "import em; print(em.__version__)"
it should be showing 3.3.4 version 
Now finally the error has been solved and we can now build the firmware. 😊

