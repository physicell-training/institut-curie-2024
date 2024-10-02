# PhysiCell Studio Setup Guide 
Last Updated Oct 2, 2024. 

This guide will help you set up PhysiCell Studio  with a pre-compiled  executable model (`project`) for your computer (currently Windows, Mac, and (hopefully) Linux). 

It will let you create rules-based simulation models without additional complex setup (e.g., C++ compilers). You need Python 3 installed on your computer (which will include the `pip3` command used below). Verify that you do and if not, install it. 

If you have difficulty with this setup, you can use the web-based version of PhysiCell Studio, at: 

[https://nanohub.org/tools/pcstudio](https://nanohub.org/tools/pcstudio) 

If you're a first time user, you'll need to register (free). I suggest using the Google login. 

## Step 1) Install Python (if you don't have it)
### On Windows:
Follow these steps or see the Anaconda option below.

* open a Command Line or Powershell terminal and type:

```python```

If it comes back with "Python 3.xx.xx" then you should be good. You can type `quit()` at the Python prompt (">>>") to exit the interpreter.
 
* Otherwise, if it says `command not found`, then download and install Python 3.11 from the [Microsoft Store](https://apps.microsoft.com/search?query=python&hl=en-us&gl=US).

### On a Mac:
Follow these steps or see the Anaconda option (next).

* open a Terminal shell and type

```python```

If it comes back with "Python 3.xx.xx" then you should be good. You can type `quit()` at the Python prompt (">>>") to exit the interpreter.

* Otherwise, if it says `command not found`, then download and install the latest "macOS 64-bit universal2 installer" from [www.python.org/downloads/macos/](https://www.python.org/downloads/macos/).

### Platform independent: install the Anaconda Python

* [https://www.anaconda.com/download](https://www.anaconda.com/download)

Note there's a "Skip registration" option) - this option will figure out what operating system you are running and download the appropriate Python package. Note that the full Anaconda installation is somewhat large, but the Miniconda alternative should work similarly. 

---
## Step 2) Download and Unzip PhysiCell Studio 
Visit the PhysiCell Studio repository and download the latest release. 

[https://github.com/PhysiCell-Tools/PhysiCell-Studio/releases](https://github.com/PhysiCell-Tools/PhysiCell-Studio/releases)

Download the source code (.zip or .tar.gz) to your home directory, and uncompress it. 

If you are in a shell or terminal, change to your home directory, and then use: 

```unzip PhysiCell-Studio-2.40.0.zip```

(Replace `PhysiCell-Studio-2.40.0.zip` with the name of the file you downloaded.) 

## Step 3) Move into a Terminal Window and Start Setup 
If you haven't done so already, open a terminal in your home directory. 

Then, change into the unzipped PhysiCell Studio directory (replace `PhysiCell-Studio-2.40.0` as appropriate): 

```cd PhysiCell-Studio-2.40.0```

Then, install required 3rd party Python modules for the Studio: 

```pip3 install -r requirements.txt```

Alternatively, you can use Anaconda for installing the required dependencies: 

```
conda env create -f environment.yml
conda activate studio
```

Then, run a script to download the executable `project` (the PhysiCell "template" sample project) for your operating system:

```python download_binary.py```

## Step 4) Open and Test PhysiCell Studio: 
If successful, you should be able to open the studio via; 

```python bin/studio.py```

If this opens, go to the `Run` tab and click the green `Run Simulation` button. You should see it run with a lot of details in the built-in window. Move to the `Plot` window and click the green `Play` button to start visualizing the test model.

If it starts moving through a simple simulation, you are good to go! 

## Step 5) View documentation
Visit: 

[https://github.com/PhysiCell-Tools/Studio-Guide/blob/main/README.md](https://github.com/PhysiCell-Tools/Studio-Guide/blob/main/README.md) 

## Step 6) Possible additional steps for Linux

If you are on Linux and the Studio does not display, you can try to run:

```sudo apt-get install libxcb-xinerama0```   # (assuming you have `sudo` privilege)

or use the Anaconda dependency installation mentioned in Step3. 


