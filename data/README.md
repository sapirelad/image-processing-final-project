Dataset description and preprocessing notes.
Raw videos are not included due to size constraints.

# Dataset Description

## Data Source
The dataset was self-collected for this project using a mobile phone camera.

## Motion Classes
The dataset includes two motion classes:
- **walk** – walking motion
- **wave** – hand waving motion

## Dataset Structure
The raw data is organized as follows:

data_raw/
 ├── train/
 │   ├── walk/
 │   └── wave/
 └── test/
     ├── walk/
     └── wave/

Each directory contains short video clips (≈7 seconds each).

## Dataset Size
- Train set: 2 videos per class
- Test set: 2 videos per class

## Preprocessing
The following preprocessing steps are applied:
- Conversion to grayscale
- Spatial resizing to 64×64 pixels
- Frame subsampling (every_n parameter)
- Motion-based spatio-temporal block sampling

## Data Availability
The raw video files are **not included** in this repository due to file size constraints.
Paths to the dataset can be configured in the notebook using the `BASE` variable.

