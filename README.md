# Balancing Cardiac Privacy with Quality in Video Recordings
[![DOI](https://zenodo.org/badge/1008067642.svg)](https://zenodo.org/doi/10.5281/zenodo.15734097)

## Summary
Facial videos can reveal hidden health information, such as heart rate, by analyzing subtle changes in skin color. While this can help with remote health monitoring, it also poses serious privacy risks, as health data can be extracted without permission. In this study, we propose a new method to protect such information. Our approach allows health signals to be removed from a video, encrypted, securely transmitted, and later restored by an authorized recipient. This reversible method keeps the video looking natural while ensuring that sensitive data cannot be misused. We test our framework on a set of real videos and show that it works reliably across different activities. This work could improve privacy in video calls, telehealth, and other everyday video applications.

### Repository structure
```
├── data/ # Place LGI-PPGI-DB dataset here (a small sample video is provided already).
├── pyRemoval/ # Reused and extended from https://github.com/saksham2001/rPPG-removal
│ └── filters/ # Implements sinusoidal modulation logic
├── pyVHR/ # Forked from https://github.com/phuselab/pyVHR (for rPPG signal extraction and all the analysis)
├── analysis.ipynb # Notebook to show how to use the filter
├── pyRemoval_Demo.ipynb # Additional from pyRemoval
├── requirements.txt # Python dependencies
├── LICENSE
├── README.md

```

## Setup
### Hardware Requirements
This code requires only a standard computer with enough RAM to support the in-memory operations. Although, the code can be run on a CPU, it is recommended to use a GPU for faster processing.

### Software Requirements
#### OS Requirements

This package can be installed on all major platforms (macOS, Linux and Windows). The package has been tested on the following systems:

* macOS: Ventura (13.6.1)
* Linux: Ubuntu 20.04.6 LTS

#### Python Dependencies
We recommend using python 3.8+ to run the scripts. Use the following commands to clone the repository and install all the required dependencies. Typically, the installation should take less than 10 minutes.
```Shell
git clone https://github.com/saksham2001/Balancing-Cardiac-Privacy
cd Balancing-Cardiac-Privacy
git clone https://github.com/saksham2001/rPPG-Removal
python3 -m pip install -r requirements.txt
```
**Note** Please ensure that you do not have the pyVHR python package installed. If you do, please uninstall it using `pip uninstall pyVHR` and use the modified version provided in this repository.

## Dataset
In the paper we use the LGI-PPGI dataset. The dataset can be downloaded from [https://github.com/partofthestars/LGI-PPGI-DB](https://github.com/partofthestars/LGI-PPGI-DB). 

A small video from the LGI-PPGI dataset is provided in [data/sample_video.avi](https://github.com/saksham2001/Balancing-Cardiac-Privacy/data/sample_video.avi) to demo the software.


<!-- ## Citation
If you use any of the data or resources provided on this page in any of your publications we ask you to cite the following work.
```add citation here``` -->

## Contact
If you have any questions, please feel free to contact us though email: Saksham Bhutani (sakshambhutani2001@gmail.com) or Mohamed Elgendi (moe.elgendi@hest.ethz.ch)

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/saksham2001/Balancing-Cardiac-Privacy/blob/main/LICENSE) file for details.

