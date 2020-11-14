# Run Onebit Adam for SQuAD 1.1 Finetuning

Install GluonNLP master
```
nlp_data prepare_squad --version 1.1 --save_path data
cd ckpt
wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-large-uncased-whole-word-masking-pytorch_model.bin
cd ..
pip install cupy
bash run_squad_deepspeed_onebitadam.sh squad_onebitadam
```
