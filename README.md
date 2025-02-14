<img src="https://img.shields.io/badge/status-online-green" />

# manhole-cover-retrainer

This repository trains the resnet152 model to predict manhole covers in 13 different classes:

  - Rost/Strassenrost
  - Vollguss/Pickelloch belueftet
  - Gussbeton/Pickelloch geschlossen
  - Vollguss/Pickelloch geschlossen
  - Gussbeton/Pickelloch belueftet
  - Vollguss/Handgriff geschlossen
  - Gussbeton/Handgriff seitlich
  - Rost/Einlauf rund
  - Rost/Strassenrost gewoelbt
  - Vollguss/Aufklappbar
  - Gussbeton/Handgriff mitte
  - Vollguss/Handgriff geschlossen, verschraubt
  - Andere/-
  

## Installation

1. Clone project locally 

```bash
git clone git@github.com:tozzodatascience/manhole-cover-retrainer.git
```

2. Take the images from the repository [manhole-cover-labelling](https://github.com/tozzodatascience/manhole-cover-labelling) from the folder ./data/images_transformed and added it to the folder ./data/images_transformed in this repository.

3. Take the labels.csv file that was created by repository [manhole-cover-labelling](https://github.com/tozzodatascience/manhole-cover-labelling) in the folder ./data/ and rename it to "new_labels.csv" and add it to the folder ./data/ in that repository.

4. Download old Images

Download images as Folder (images_transformed) from Google Drive and add it to the folder ./images_transformed here: (https://drive.google.com/drive/folders/14zy988QQwlV-Gd1dwj1quepru-XlZOqp?usp=sharing)

5. Install required packages

create a new enviorment with conda.

```bash
conda create --name retrainer
```

```bash
activate retrainer
```

Install Cuda:

```bash
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

```bash
pip install -r requirements.txt
```


## Usage

1. run the code:
```bash
python retrainer.py
```

Output:
  - When you have trained the model, you get a .pth file `model.pth`

2. You can now replace this model with the old model in the repository [manhole-cover-model](https://github.com/tozzodatascience/manhole-cover-model)


## Credits

This is a continuation of the repository [manhole-cover-classification](https://github.com/FiratSaritas/manhole-cover-classification) and the actual work was created on the other repository.
