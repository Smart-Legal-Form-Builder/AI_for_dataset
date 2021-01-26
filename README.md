# script_generation_kr

### finetuning

```sh
python main.py --epoch=200 --data_file_path=./train.csv --save_path=./checkpoint/ --load_path=./checkpoint/KoGPT2_checkpoint_240000.tar --batch_size=1
```
----------
### generation
download trained model [here](https://drive.google.com/file/d/1UHC9fCE8pU15iacOpXkegjg9ONkzURKT/view?usp=sharing) or train your own model through finetuning
```sh
python generator.py --temperature=1.0 --text_size=100 --load_path=./checkpoint/KoGPT2_checkpoint_240000.tar --tmp_sent="우리는 지난"
```
or<br>
`generator_ngram_creativity.ipynb`(recommended option)

--------

### Korean Bert Score
```sh
git clone https://github.com/lovit/KoBERTScore
cd ko-BERTScore
python setup.py install
```

-------
### reference
- [for parameter description in finetuning, generation](https://github.com/gyunggyung/KoGPT2-FineTuning)  
- [for ko-bert score](https://github.com/lovit/KoBERTScore)
