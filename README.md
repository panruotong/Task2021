Fine-tune的命令
```
python -m fine_tune --train data/en_train.conll --dev data/en_dev.conll --out_dir . --model ./xlmr_ner/lightning_logs/version_1/checkpoints//xlmr_ner_timestamp_1637392205.260303_final.ckpt --model_name xlmr_ner --stage finetune --gpus 1 --epochs 2 --encoder_model xlm-roberta-base --batch_size 64 --lr 0.0001
```
拿dev set测试的命令

```
python -m evaluate --test data/en_dev.conll --out_dir . --gpus 1 --encoder_model xlm-roberta-base --model ./xlmr_ner/lightning_logs/version_2/checkpoints//xlmr_ner_timestamp_1637399827.1621466_final.ckpt --prefix xlmr_ner_results
```

English测试结果

DATALOADER:0 TEST RESULTS
{'ALLPRED': 1253.0,
 'ALLRECALLED': 1052.0,
 'ALLTRUE': 1230.0,
 'F1@CORP': 0.7967032967032465,
 'F1@CW': 0.5901639344261792,
 'F1@GRP': 0.7777777777777274,
 'F1@LOC': 0.848861283643842,
 'F1@PER': 0.9094017094016591,
 'F1@PROD': 0.7035830618892005,
 'MD@F1': 0.847362062021698,
 'MD@P': 0.839584996009577,
 'MD@R': 0.8552845528455284,
 'P@CORP': 0.8479532163742685,
 'P@CW': 0.5684210526315786,
 'P@GRP': 0.7819148936170208,
 'P@LOC': 0.8232931726907626,
 'P@PER': 0.901694915254237,
 'P@PROD': 0.6749999999999995,
 'R@CORP': 0.7512953367875643,
 'R@CW': 0.6136363636363632,
 'R@GRP': 0.7736842105263153,
 'R@LOC': 0.8760683760683756,
 'R@PER': 0.9172413793103444,
 'R@PROD': 0.7346938775510199,
 'loss': 4.675072363444737,
 'micro@F1': 0.788562223117147,
 'micro@P': 0.7813248204309656,
 'micro@R': 0.7959349593495935}

