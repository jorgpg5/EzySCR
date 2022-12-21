# EzyScore

A semi-automated system prototype that annotates skin conductance data.

![annotation_demo](https://user-images.githubusercontent.com/70129680/182296665-e576958a-582b-4192-b34b-8b282089e593.gif)

# Installation and setup

To install this software, we'll need Anaconda and Git. If you already have them, you can skip to the **User Guide** section.

Please download and install [Anaconda](https://www.anaconda.com/products/distribution). Please do not check or uncheck any installation options.

![image](https://user-images.githubusercontent.com/70129680/182262876-d91d2d50-b4dc-44db-a0aa-1f91cf8c1146.png)

Please download and install [Git](https://git-scm.com/downloads)
![image](https://user-images.githubusercontent.com/70129680/182263939-001858b8-8782-42c3-9122-fb90833f80f2.png)

# Setup

Go to the folder where you want save the interface software. Open a git bash (right click on the folder and select Git Bash here)
![image](https://user-images.githubusercontent.com/70129680/182267804-5e0ee31f-08a1-4f18-a833-ebb2b297d5fe.png)

We will clone this repo. Copy the location of this repo: \

![image](https://user-images.githubusercontent.com/70129680/182267909-9d469508-eb72-4768-8b1e-d04db9fa9b85.png)

Use the next command:

**git clone https://github.com/jorgpg5/EzyScore.git"

Then, we will open an anaconda prompt. Type "anaconda prompt" on the windows search bar.

![image](https://user-images.githubusercontent.com/70129680/182268122-659eb2b1-66e3-4946-919e-689ea0379720.png)

We will install the interface by using the yml file in the repo.

In the anaconda prompt, go to the folder where you cloned this repo with Git.

### For Windows

Run the next command for **windows**:

**conda env create -f environment.yml**

### For MacOS

Run the next command for **MacOS**:

**conda env create -f environment_mac.yml**


The virtual environment that hosts the annotation interface should be ready after a few minutes.

When the installation of the virtual environment has finished, run the next commands:

**conda activate ezyscore** \
**voila ezyscore.ipynb**

Voila! (pun intended :P) your interface is ready to use.

# User guide

**Note: Before you run the interface, you need to double-check a couple of things.**

**1.- Check that the folder structure is the same as the repo.** \
**2.- Check that you have the .m files in the dataset folder. If you have the .acq files, you'll need to use AcqKnowledge to convert the .acq files into .m files.**

To run the interface, go to the folder where you cloned this repo.

Enter the following commands:

**conda activate ezyscore** \
**voila ezyscore.ipynb**

The last command will open a browser where the interface is hosted.

- Enter the name of the file that you want to analyse (without the extension type, i.e. Acq_P301). If the file is not in the dataset folder, the interface will ask you to verify the filename.
- Wait a few seconds while the data is preprocessed. Then Click on the "Start Annotation" button.
- The interface will be loaded. To annotate, click and drag the markers on the chart. If you're not happy with the annotation or just want to start over, click on the  "Reset" button.
- To visualise a preview of the data that will be saved, click on "Visualise Annotation".
- Click on "Next" or "Prev" to change events. The data will be saved on the fly. When these buttons are pressed, the annotations will be saved in the "annotated_data" folder. To make sure that all the data has been annotated, please go through the all events in that file.

**Troubleshooting:**

**- If you want to see the code or change some stuff, type "jupyter notebook" in the terminal where you cloned the repo. Then, open the jupyter notebook to modify/see the code.** \
**- If something goes wrong, just refresh the page and the interface will start from the beginning.** \
**- If you open the annotated file located in the "annotated_data" folder, please close the csv file before making more annotations. By not doing so, the interface will have issues as it won't be able to write the data into the csv file.**
