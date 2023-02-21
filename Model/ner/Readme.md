### Training BERT models

```
python run_ner.py --data_dir ./ \
 --labels ./labels.txt \
 --model_name_or_path bert-large-cased \
 --output_dir /scratch/kkpal/AISecKG/BLC \
 --max_seq_length  128 \
 --num_train_epochs 30 \
 --per_device_train_batch_size 32 \
 --save_steps 1000 \
 --seed 42 \
 --do_train \
 --do_eval \
 --do_predict \
 --overwrite_output_dir
```


### Results


BLU
==================
02/21/2023 00:45:05 - INFO - __main__ -   test_loss = 0.9023678302764893
02/21/2023 00:45:05 - INFO - __main__ -   test_accuracy_score = 0.8217352679893396
02/21/2023 00:45:05 - INFO - __main__ -   test_precision = 0.45490584737363726
02/21/2023 00:45:05 - INFO - __main__ -   test_recall = 0.5381008206330598
02/21/2023 00:45:05 - INFO - __main__ -   test_f1 = 0.49301825993555315
02/21/2023 00:45:05 - INFO - __main__ -   test_runtime = 2.2023
02/21/2023 00:45:05 - INFO - __main__ -   test_samples_per_second = 97.171
02/21/2023 00:45:05 - INFO - __main__ -   test_steps_per_second = 6.357

BBU
===
02/21/2023 00:52:22 - INFO - __main__ -   test_loss = 0.7777031660079956
02/21/2023 00:52:22 - INFO - __main__ -   test_accuracy_score = 0.8190701806336985
02/21/2023 00:52:22 - INFO - __main__ -   test_precision = 0.4569055036344756
02/21/2023 00:52:22 - INFO - __main__ -   test_recall = 0.5158264947245017
02/21/2023 00:52:22 - INFO - __main__ -   test_f1 = 0.48458149779735676
02/21/2023 00:52:22 - INFO - __main__ -   test_runtime = 1.1786
02/21/2023 00:52:22 - INFO - __main__ -   test_samples_per_second = 181.567
02/21/2023 00:52:22 - INFO - __main__ -   test_steps_per_second = 11.878

BLWWM
======
python run_ner.py --data_dir ./ --labels ./labels.txt --model_name_or_path bert-large-uncased-whole-word-masking --output_dir /scratch/kkpal/AISecKG/BLWWM --max_seq_length  128 --num_train_epochs 30 --per_device_train_batch_size 32 --save_steps 1000 --seed 42 --do_train --do_eval --do_predict --overwrite_output_dir
02/21/2023 00:56:17 - INFO - __main__ -   test_loss = 0.8153625130653381
02/21/2023 00:56:17 - INFO - __main__ -   test_accuracy_score = 0.832987859046491
02/21/2023 00:56:17 - INFO - __main__ -   test_precision = 0.498371335504886
02/21/2023 00:56:17 - INFO - __main__ -   test_recall = 0.5381008206330598
02/21/2023 00:56:17 - INFO - __main__ -   test_f1 = 0.5174746335963923
02/21/2023 00:56:17 - INFO - __main__ -   test_runtime = 2.2482
02/21/2023 00:56:17 - INFO - __main__ -   test_samples_per_second = 95.189
02/21/2023 00:56:17 - INFO - __main__ -   test_steps_per_second = 6.227

RB
===
python run_ner.py --data_dir ./ --labels ./labels.txt --model_name_or_path roberta-base --output_dir /scratch/kkpal/AISecKG/RB --max_seq_length  128 --num_train_epochs 30 --per_device_train_batch_size 32 --save_steps 1000 --seed 42 --do_train --do_eval --do_predict --overwrite_output_dir
02/21/2023 00:58:10 - INFO - __main__ -   test_loss = 0.851585865020752
02/21/2023 00:58:10 - INFO - __main__ -   test_accuracy_score = 0.8063369854900799
02/21/2023 00:58:10 - INFO - __main__ -   test_precision = 0.44195953141640043
02/21/2023 00:58:10 - INFO - __main__ -   test_recall = 0.48651817116060964
02/21/2023 00:58:10 - INFO - __main__ -   test_f1 = 0.46316964285714285
02/21/2023 00:58:10 - INFO - __main__ -   test_runtime = 1.5284
02/21/2023 00:58:10 - INFO - __main__ -   test_samples_per_second = 140.016
02/21/2023 00:58:10 - INFO - __main__ -   test_steps_per_second = 9.16

RL
====
python run_ner.py --data_dir ./ --labels ./labels.txt --model_name_or_path roberta-large --output_dir /scratch/kkpal/AISecKG/RL --max_seq_length  128 --num_train_epochs 30 --per_device_train_batch_size 32 --save_steps 1000 --seed 42 --do_train --do_eval --do_predict --overwrite_output_dir
02/21/2023 01:02:10 - INFO - __main__ -   test_loss = 0.9701179265975952
02/21/2023 01:02:10 - INFO - __main__ -   test_accuracy_score = 0.8270654427006219
02/21/2023 01:02:10 - INFO - __main__ -   test_precision = 0.4796926454445664
02/21/2023 01:02:10 - INFO - __main__ -   test_recall = 0.5123094958968347
02/21/2023 01:02:10 - INFO - __main__ -   test_f1 = 0.4954648526077098
02/21/2023 01:02:10 - INFO - __main__ -   test_runtime = 2.2422
02/21/2023 01:02:10 - INFO - __main__ -   test_samples_per_second = 95.443
02/21/2023 01:02:10 - INFO - __main__ -   test_steps_per_second = 6.244

BBC
====
python run_ner.py --data_dir ./ --labels ./labels.txt --model_name_or_path bert-base-cased --output_dir /scratch/kkpal/AISecKG/BBC --max_seq_length  128 --num_train_epochs 30 --per_device_train_batch_size 32 --save_steps 1000 --seed 42 --do_train --do_eval --do_predict --overwrite_output_dir
02/21/2023 01:05:33 - INFO - __main__ -   test_loss = 0.872787594795227
02/21/2023 01:05:33 - INFO - __main__ -   test_accuracy_score = 0.8143322475570033
02/21/2023 01:05:33 - INFO - __main__ -   test_precision = 0.47317596566523606
02/21/2023 01:05:33 - INFO - __main__ -   test_recall = 0.5169988276670574
02/21/2023 01:05:33 - INFO - __main__ -   test_f1 = 0.4941176470588235
02/21/2023 01:05:33 - INFO - __main__ -   test_runtime = 1.458
02/21/2023 01:05:33 - INFO - __main__ -   test_samples_per_second = 146.771
02/21/2023 01:05:33 - INFO - __main__ -   test_steps_per_second = 9.602

BLC
===
python run_ner.py --data_dir ./ --labels ./labels.txt --model_name_or_path bert-large-cased --output_dir /scratch/kkpal/AISecKG/BLC --max_seq_length  128 --num_train_epochs 30 --per_device_train_batch_size 32 --save_steps 1000 --seed 42 --do_train --do_eval --do_predict --overwrite_output_dir
02/21/2023 01:09:41 - INFO - __main__ -   test_loss = 0.8072407245635986
02/21/2023 01:09:41 - INFO - __main__ -   test_accuracy_score = 0.832987859046491
02/21/2023 01:09:41 - INFO - __main__ -   test_precision = 0.4872579001019368
02/21/2023 01:09:41 - INFO - __main__ -   test_recall = 0.5603751465416178
02/21/2023 01:09:41 - INFO - __main__ -   test_f1 = 0.5212649945474372
02/21/2023 01:09:41 - INFO - __main__ -   test_runtime = 2.1505
02/21/2023 01:09:41 - INFO - __main__ -   test_samples_per_second = 99.51
02/21/2023 01:09:41 - INFO - __main__ -   test_steps_per_second = 6.51

