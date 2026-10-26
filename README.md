# STAGE
STAGE: Spatio-Temporal Allelic Geostatistical Estimation

This repository contains the code and data for the STAGE pipeline. STAGE adapts continuous geostatistical methods to model the spatiotemporal spread of categorical pathogenic genetic variants.

## Repository Structure 
(1) **`STAGE_spatial.ipynb`**: The Part 1 Jupyter/Colab Notebook. This contains the primary tutorial for calculating the empirical spatial variogram and fitting the spherical model. 
(2) **`STAGE_spatiotemporal.ipynb`**: The Part 2 Jupyter/Colab Notebook. This contains the tutorial for expanding the framework across multiple years, calculating the empirical spatiotemporal variogram, and fitting the spherical model. 
(3) **`stage_spatiotemporal_sample_data.csv`**: A simulated *Avr-Pik* sample dataset with 100 sampling locations across a landscape and 3 years (2015-2017) . 
(4) **`avrpik_gt_distmatdf.csv`**: The empirical genetic distance matrix for the *Avr-Pik* variants used to structure the simulation. 


## How to Run the Code in Google Colab
The framework is optimized to run seamlessly in Google Colab. To evaluate the pipeline, please open the notebooks directly in your browser using the links below: 
1. **[Link to Part 1: STAGE Spatial Tutorial] (https://colab.research.google.com/drive/1TswRecRag1XzhrpmsdYF47N3Bb0HmGrD?usp=drive_link)** 
2. **[Link to Part 2: STAGE Spatiotemporal Tutorial] (https://colab.research.google.com/drive/1LWPfMSStSxyICKyfK7W_9YNszT0bSihz?usp=drive_link)** 

Once a notebook is open: 
1. In the top menu bar, select **Runtime > Run all**. 
2. The notebook will automatically configure the environment, download the required datasets  and generate the variogram plots. 
3. Model parameters will be output as a downloadable CSV (`fitted_variogram_model.csv`) within the Colab file explorer. 
## Alternative: Local Execution
If you prefer not to use a Google account to run the Colab environment, you can easily run this pipeline locally on your own machine. 

1. Download the notebooks (`STAGE_spatial.ipynb` and `STAGE_spatiotemporal.ipynb`), the `stage_spatiotemporal_sample_data.csv` and the `avrpik_gt_distmatdf.csv` file to the same local folder. 
(1). **[Link to stage_spatiotemporal_sample_data.csv] (https://drive.google.com/file/d/1bJFR6TXhEgeFPXj-dT_r8tZL_KIOi16K/view?usp=drive_link)** 
(2). **[Link to avrpik_gt_distmatdf.csv] (https://drive.google.com/file/d/1Vx8vU1Jb2vrLcPA0ahk9jEfhrqMA8837/view?usp=drive_link)**
2. Ensure you have a standard Python 3 environment installed with Jupyter Notebook. 
3. Install the required dependencies using pip: `pip install numpy pandas scipy scikit-learn scikit-gstat matplotlib seaborn` 
4. Open the notebooks in your local Jupyter environment and execute the cells. *Note: If running locally, you may ignore or delete the automated download cells at the top of the notebooks.*
