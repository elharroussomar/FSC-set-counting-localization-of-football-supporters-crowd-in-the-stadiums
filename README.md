#FSC-set-counting-localization-of-football-supporters-crowd-in-the-stadiums

This repository contains the datasets of football supporters crowd in the stadium for the paper:

"FSC-set: counting, localization of football supporters crowd in the stadiums"

The crowd counting and localization data is intended to support research in dense crowd analysis. This dataset can be found : https://drive.google.com/drive/folders/1A_6ohodGYK7M_ZCyBugny1PP4FJv4u0Y?usp=sharing

<img src="https://github.com/elharroussomar/FSC-set-counting-localization-of-football-supporters-crowd-in-the-stadiums/blob/main/FSC-Set-Samples.png" alt="FSC-Set-Samples">
<div class="animate-fade-in-delay h-64 md:h-96">
   <img src="https://github.com/elharroussomar/FSC-set-counting-localization-of-football-supporters-crowd-in-the-stadiums/blob/main/FSC-Set-Samples.png" alt="FSC-Set-Samples">
</div>
📝 Dataset Overview

The FSC-Set (Football Supporters Crowd Dataset) is a large-scale collection of images designed for crowd counting and individual localization in highly dense stadium environments. The annotations provide precise ground truth data for developing and evaluating advanced computer vision models, particularly those involved in edge detection and high-resolution feature analysis. 

📊 Dataset Statistics

Feature

Value

Total Number of Images

6,000

Total Annotated Individuals

Over 1.5 Million

Annotation Method

Manual Point Annotation (Head Coordinates)

Image Diversity

Varying FOV, illumination, resolution, and scale

📁 File Structure

The dataset is organized to separate the visual data from the ground truth coordinates:

FSC-set-counting-localization/
├── images/
│   ├── scene_0001.jpg
│   └── ... (6000 total images)
└── annotations/
    ├── scene_0001.txt
    └── ... (6000 total annotation files)


Annotation Details

Format: Typically a .txt or equivalent file where each line represents one annotated person.

Content: The $(x, y)$ coordinates of the person's head or center point within the image.

🚀 Usage

Integration with CH-RNet/PIDiNet

This dataset is used to train and validate crowd localization techniques, which often rely on highly refined edge or density maps. The dense point annotations can be converted into density maps for model training, aligning with the methods utilized in networks like those referenced above.

❗ Note: Due to the large volume of images and annotations, the full data files may be hosted externally. Please [Specify how users can download the dataset, e.g., Visit the project website for download links] to obtain the complete data package.

📜 Citation

If this dataset is used in your academic work, please cite the corresponding paper:

@article{Elharrouss2022FSCSet,
  title={FSC-Set: Counting, Localization of Football Supporters Crowd in the Stadiums},
  author={Elharrouss, Omar and Almaadeed, Noora and Abualsaud, Khalid and Al-Maadeed, Somaya and Al-Ali, Aisha and Al-Maadeed, Alaa},
  journal={IEEE Access},
  volume={10},
  pages={10446--10457},
  year={2022},
  doi={10.1109/ACCESS.2022.3144607}
}


⚖️ License

This dataset is released under the [LICENSE NAME, e.g., Creative Commons Attribution 4.0 International License (CC BY 4.0)]. Please refer to the LICENSE file in the repository for specific usage terms.
