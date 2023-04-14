# PET
Pattern Exploiting Training

## 1. 라이브러리 설치
```
-f https://download.pytorch.org/whl/torch_stable.html
numpy==1.19
jsonpickle==1.1
scikit-learn==0.23.1
torch===1.5.0
torchvision==0.6.0
transformers==3.0.2
tqdm==4.48.1

# 추가 설치
jsonpickle
jsonlines
sentencepiece
```

## 2. 데이터 준비
train.jsonl,  unlabeled.jsonl, val.jsonl

## 3. PVP 정의
custom PVP 클래스, DataProcessor 클래스

## 4. Unlabeled dataset Annotation
```
python cli.py --method ipet --pattern_ids 0 1 --data_dir DATASET_FOLDER --model_type korea_bert --model_name_or_path klue/bert-base --task_name CUSTOM_TASK --output_dir output --do_train --wrapper_type mlm --pet_repetitions 2 --ipet_generations 2
```
