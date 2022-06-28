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
git clone git@github.com:FiratSaritas/manhole-cover-retrainer.git
```

2. The images from the repository [manhole-cover-labelling](https://github.com/FiratSaritas/manhole-cover-labelling) from the folder ./data/images_transformed can be added to the folder ./data/images_transformed in this repository.

3. Take the labels.csv file that was created by repository [manhole-cover-labelling](https://github.com/FiratSaritas/manhole-cover-labelling) in the folder ./data/ and rename it to "new_label.csv" and add it to the folder ./data/ in that repository.

3. Install required packages

Preferably you create a new enviorment (conda environment is also possible).


```bash
pip install -r requirements.txt
```

Install Cuda:

```bash
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```


## Usage

1. run the code:
```bash
python retrainer.py
```

2. After that we can start the webbrowser and label our images:
```bash
python main.py
```

Output:
  - When you have trained the model, you get a .pth file `model.pth`

3. You can now replace this model with the old model in the repository [manhole-cover-model](https://github.com/FiratSaritas/manhole-cover-model)

## Guide -Tips


## Credits

This is a continuation of the repository [classification](https://github.com/FiratSaritas/manhole-cover-classification) and the actual work was created on the other repository.
