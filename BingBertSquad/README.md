# Run SQuAD 1.1 Finetuning

Install GluonNLP master
```
nlp_data prepare_squad --version 1.1 --save-path squad
cd ckpt
wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-large-uncased-whole-word-masking-pytorch_model.bin -O bert-large-uncased-whole-word-masking-pytorch_model.bin 
wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-large-uncased-whole-word-masking-config.json -O bert-large-uncased-whole-word-masking-config.json 
cd ..
bash run_squad_hf_deepspeed.sh 8 ckpt/bert-large-uncased-whole-word-masking-pytorch_model.bin squad squad_out ckpt/bert-large-uncased-whole-word-masking-config.json
```
