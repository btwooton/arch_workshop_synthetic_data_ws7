# ARCH Workshop: Generating Synthetic EHR Data for Research [WS7]

### Links to Resources used During Workshop

- [Synthea Generic Module Builder](https://synthetichealth.github.io/module-builder/)
- [Synthea Github Page](https://github.com/synthetichealth/synthea)
- [Synthea Customizer](https://synthetichealth.github.io/spt/#/customizer)
- [Cross-sectional Pediatric Myopia Study](https://pmc.ncbi.nlm.nih.gov/articles/PMC6120514/)
- [Google Sheet w/ Probablity Calculations for Distributed Transitions in Myopia Module](https://docs.google.com/spreadsheets/d/1vfAni3XgbPsL_Ho7IHZ9py_RLtcB3uUOQdmRE3yoeA4/edit?usp=drive_link)
- [Synthea Overview](https://mitre.github.io/fhir-for-research/modules/synthea-overview)

## Options to Follow Along with the Hands On Module

### *Option 1.* Link to Notebook in Google Colab *(preferred)*:

1. [Synthetic Patient Generation with Synthea](https://colab.research.google.com/github/expmed/arch_workshop_synthetic_data_ws7/blob/main/Run_Synthea_Simulations_Colab.ipynb)


### *Option 2.* Minimal Local Environment Instructions *(for Workshop Attendees who Want to Run Locally)* 

These steps will help you install Python, set up a Conda environment, fetch the Synthea generator, and run the workshop notebooks locally.

📦 Step 1: Install Anaconda (Recommended)
Anaconda includes Python, Jupyter, and package management tools in one.

Download and install Anaconda for your operating system:

[Windows / macOS / Linux](https://www.anaconda.com/download)

After installing, open Anaconda Prompt (Windows) or a terminal (Mac/Linux).

📂 Step 2: Clone the Workshop Repository
If you're using Git:

```bash
git clone https://github.com/expmed/arch_workshop_synthetic_data_ws7.git
cd arch_workshop_synthetic_data_ws7
```
Or, download the ZIP from the provided link and extract it. Then navigate into the folder:

```bash
cd arch_workshop_synthetic_data_ws7
```
🧪 Step 3: Create and Activate the Conda Environment
This installs all required Python packages for the notebooks.

```bash
conda env create -f environment.yml
conda activate synthetic-data-generation  # replace with your env name if different
```
🔬 Step 4: Fetch the Synthea Executable
Download the Synthea JAR file to generate synthetic patient records.

Visit: [https://github.com/synthetichealth/synthea/releases](https://github.com/synthetichealth/synthea/releases)

Download the latest synthea-with-dependencies.jar

Move it to the workshop folder and optionally rename it:

```bash
mv ~/Downloads/synthea-with-dependencies.jar .
```
Now you can run it with:

```bash
java -jar synthea-with-dependencies.jar -c synthea.config -p 10
```
(If java is not installed, install OpenJDK or run brew install openjdk on macOS.)

📓 Step 5: Launch the Workshop Jupyter Notebook
From within your activated Conda environment and workshop directory:

```bash
jupyter notebook
```
Your browser will open automatically. Navigate to the .ipynb files for hands-on exercises. 