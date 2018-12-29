# Fake-Voice-Detection

Author: Kei Ishikawa, Xiaoran Chen, Ching Pui WAN, Allan Costa. 
The original code for [Cyclic GAN](https://github.com/leimao/Voice_Converter_CycleGAN) is by Lei Mao.<br>

Environment: ubuntu 18.04, Python 3.6

## Introduction


## Files

```
.
├──src
│   ├── convert.py
│   ├── download.py
│   ├── model.py
│   ├── module.py
│   ├── preprocess.py
│   ├── train.py
│   └── utils.py
│
├──data
│   ├──target_raw (Obama)
│   ├──target (Obama)
│   │   ├─ train_conversion
│   │   ├─ train_verification
│   │   └─ test
│   ├──source
│   │   └─ train_conversion
│   └──ubg
│   │   ├─ train_conversion
│   │   ├─ train_verification
│   │   └─ test
├── figures
├── README.md
```


## Requirments
Install all the requirements.

```bash
pip install --user -r requirements.txt
```
If librosa gives backend error, run following. (This is moduole load ffmpeg in HPC cluster in ETH.)
```bash
sudo apt-get ffmpeg
```

## Usage

### Before Running Code
```bash
$ cd path/Fake-Voice-Detection/
```

### Download Dataset
Download and unzip datasets and pretrained models.

```bash
$ python ./src/download.py
```

### Split the raw speech
```bash
$ python ./src/split_raw_speech.py
```