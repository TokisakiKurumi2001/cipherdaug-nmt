The official code for the paper [CipherDAug: Ciphertext based Data Augmentation for Neural Machine Translation](https://arxiv.org/pdf/2204.00665.pdf) accepted to appear at ACL 2022 main conference.

### more scripts and instructions coming soon ..

## Generating ciphertexts from plaintext

The simplest way to generate ciphertexts based on the [python script](cipher/encipher.py) would be
```
python cipher/encipher.py -i  path/to/inoput-file --keys a-key-value \
    --char-dict-path path/to/store/char-dictionary/necessary > output/path/and/filename
```

For intended usage and ease of generting named data files, look at the bash script `encipher.sh`. This script is for IWSLT14 De-En but can easily be changed to other lang pairs.
```
bash encipher.sh -s de -t en -x src
```
the `-x` denotes the (src/tgt) side to encipher and we recommend using `-x src` only. Note that `-x tgt` hasn't been tested since the initial phases of the project.

## CipherDAug fork of FairSeq

[Our fork](https://github.com/protonish/fairseq-cipherdaug) of [FairSeq](https://github.com/pytorch/fairseq) is crucial for the working of this codebase. More details on the changes [here](https://github.com/protonish/fairseq-cipherdaug/blob/main/README.md).

## Cite
```
Bibtex : @inproceedings { kambhatla-etal-2022-cipherdaug,
   abbr="ACL",
   title = "CipherDAug: Ciphertext Based Data Augmentation for Neural Machine Translation",
   author = "Kambhatla, Nishant and
   Born, Logan and
   Sarkar, Anoop",
   booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics: Long Paper (To Appear)",
   month = may,
   year = "2022",
   address = "Online",
   publisher = "Association for Computational Linguistics",
   } 
```
