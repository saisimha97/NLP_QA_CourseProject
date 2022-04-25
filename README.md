
NLP Project : Conditional Question Answering

TEAM:
Bhanu Sai Simha Vanam, Courtney Wilkerson , Keshav Bharadwaj Vaidyanathan, Morgan Levy




Make sure GPU is CUDA compatible and CUDNN is installed


conda create new -n QA_task python=3.7

conda activate QA_task

Navigate to workiung directory

pip install -r requirements.txt

********* For training *************


python train_script.py --learning_rate 3e-4 --num_train_epochs 5 --per_device_train_batch_size 8 \
    --model_name_or_path distilbert-base-uncased --dataset_name squad  --output_dir < enter output directory for model saving > \
     --do_train --do_eval 





********* For Inference / Testing ***********


Note: you can download the model which I trained using the link below. If you dont wish to train but to just test the model.

LINK: 
Model can be found in google drive :- https://drive.google.com/drive/folders/1cXHNbh_ZTOPJTheSmrM6WNAc1RMxbbqw?usp=sharing
edit model path in test_script.py
edit question and context variables in test_script.py
python test_script.py
------------------- OR ----------------

run through inference_QA jupyter notebook
