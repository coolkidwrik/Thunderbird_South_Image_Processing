# Thunderbird_South_Image_Processing
This repository contains data M8(Lagoon Nebula) from UBC's Thunderbird South Telescope and a jupyter lab file with code to process this data. Learn more about
UBC's Thunderbird South [here]([https://link-url-here.org](https://thunderbirdsouth.phas.ubc.ca/))

This repo also includes the complete solution code for the workshop, which includes code that is run to precalibrate the fits data from the telescope

---

## Workshop Overview

Astronomical images don’t start out beautiful — they’re full of noise, hot pixels, uneven lighting, and instrumental effects.  
To make sense of them, astronomers use a process called **CCD calibration** to clean and standardize the data before combining and visualizing it.

In this workshop, you’ll:
1. Understand the role of **dark**, **flat**, and **science** frames  
2. Use **Python and Astropy** to calibrate raw telescope data  
3. Create **master calibration frames** (master dark and master flat)  
4. Apply calibration to science exposures
6. Assemble a **color composite image (BVR)** of the Lagoon Nebula (M8)

---

## Intended Learning Outcomes of the Workshop

| Concept | Description |
|----------|--------------|
| **Dark Frames** | Measure thermal noise from the camera and remove it from science images. |
| **Flat Frames** | Correct for uneven illumination and dust on optics. |
| **Science Frames** | The real observations - what we actually want to study! |
| **Sigma Clipping** | Removes outlier pixels (e.g. cosmic rays, satellite trails). |
| **BVR Color Composition** | Combine separate Blue, Visual (Green), and Red filters to form a realistic color image. |

---
## Setup

### Cloning the Repo

There are big files on this repo. To clone this repo you need to import git large file storage(lfs).
Run the folowing code in your terminal
based on your operating system

<u> On MacOS </u>
```
brew install git-lfs
```

<u> On Windows:
Download from git-lfs.github.com or use: </u>
```
winget install git-lfs
```

<u>On Linux:</u>
```
sudo apt-get install git-lfs
```

### Getting Started (Google Colab Setup)

1. **Open the Colab Notebook**
   - Upload or open this folder to your Google Drive.

2. **Mount Google Drive**
   - The dataset should already be in your drive now.
   - Run the first code cell:
     ```python
     from google.colab import drive
     drive.mount('/content/drive')
     ```

3. **Update Your Path**
   - Modify the `path` variable to point to your data folder:
     ```python
     path = "/content/drive/MyDrive/Colab Notebooks/Thunderbird South Coding Workshop Data/M8_data"
     ```

4. **Run Each Section**
   - Follow the notebook in order.
   - Sections with `# TODO` are your exercises — try completing them before checking the hints.
   - Expand the collapsible **💡 Hints** under each TODO for help.

---


