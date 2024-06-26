# Battery Usage Analysis Tool for Linux

This is a simple utility tool for Linux that monitors battery level, CPU usage, screen brightness, etc with time and stores it in a txt file. 
One can then either use the data directly or use the python script to view it graphically. 

## Usage
1. Modify the file path variables (named as `ATTRIBUTE_file` ) according to your system in `battery.sh` (In case your system does not include keyboard backlight, you can leave the variable as is. Your dataset will store NaN values for this field.)
2. Run the bash file and input the time interval for the reading (in seconds)
3. The data is stored in `data_battery.txt`. (You can modify the `data_file` variable to set the name and the path of the data file) Remember that if the data file already exists, it will append to the dataset and not overwrite. 
4. You can run the `plot_battery.py` to plot the data. (You can always the run the script even when `battery.sh` is running)

## Dependencies
**For `battery.sh`** \
None! Just set the file paths accordingly. \
**For plot_battery.py**
- Numpy
- Matplotlib
- Pandas

### To be added in future releases
- GPU usage monitoring (Different GPUs require different utilities for the task. Nvidia GPUs require `nvidia-smi`, Intel GPU's require `intel-gpu-tools`, AMD either `fglrx` or `RadeonTop`.)
- Proper GUI tkinter program for it

### Copyright
Battery Usage Analysis Tool is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

Battery Usage Analysis Tool is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with Battery Usage Analysis Tool. If not, see <https://www.gnu.org/licenses/>.