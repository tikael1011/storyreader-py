Code for paper "predicting the quality of short narratives from social media" https://www.ijcai.org/proceedings/2017/0539.pdf

## Requirements:
install pytorch http://pytorch.org/

pip install --upgrade dill six tqdm

pip install --upgrade nltk

git clone https://github.com/pytorch/text.git

cd text

python setup.py install

pip install --upgrade pycrayon



## Quickstart

## Step 1: Prepare the data
All data must be in the data folder. 
```bash
python prepare.py
```

## Step 2: Preprocess
Fix story length to 360
```bash
python preprocess.py
```
Flexible length:
```bash
python preprocess.py --fix_length 0
```
Use pretrained word vectors
```bash
python preprocess.py --pre_word_vec WORD_VEC_PATH
```

## Step 3: Train
Flexible length:
```bash
python train.py --region_nums 0 --gpus 0
```

If preprocessed pre_word_vec:
```bash
python train.py --pre_word_vec --gpus 0
```

## Step 4: Test
```bash
python test.py --model MODEL_PATH
```
