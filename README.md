
# TriMod-Fusion-for-Multimodal-Named-Entity-Recognition-in-Social-Media
Due to its informal and ambiguous nature, social media content presents challenges for Named Entity Recognition (NER). Traditional models struggle with this, prompting research into multimodal approaches that integrate text and images. However, existing methods fail to effectively align visual and textual entities. In this paper, we propose TriMod, a novel Transformer-based model that fuses textual, visual, and hashtag features for improved NER. Experiments on a multimodal dataset show that TriMod outperforms state-of-the-art methods, achieving higher precision, recall, and F1 scores.

In this repo, we have the two Datasets and Codes for our CASCON'2024 paper: 

[TriMod Fusion for Multimodal Named Entity Recognition in Social Media.](https://arxiv.org/abs/2501.08267)

Author: Mosab Alfaqeeh

Email: 18mmoa@queensu.ca

Date: November 1, 2024


# Data
The preprocessed CoNLL format files are provided in this repo. For each tweet, the first line is its image id, and the following lines are its textual contents.

Step 1：Download each tweet's associated images via this link (https://drive.google.com/file/d/1PpvvncnQkgDNeBMKVgG2zFYuRhbL873g/view)

Step 2: Change the image path in line 552 and line 554 of the "run_Trimod_crf.py" file

Step 3: Download the pre-trained ResNet-152 via this link (https://download.pytorch.org/models/resnet152-b121ed2d.pth)

Setp 4: Put the pre-trained ResNet-152 model under the folder named "resnet"



# Set CUDA device (adjust based on your system)


## Usage/Examples

```javascript
export CUDA_VISIBLE_DEVICES=0

```



# Evaluate the Model (safer alternative: modify script directly)
If modification is absolutely necessary, use:

## Usage/Examples

```javascript
sed -i "s/float(report.split('\\n')[-3].split(' ')[-2].split(' ')[-1])/float(report.split('\\n')[-4].split(' ')[-2].split(' ')[-1])/" evaluation_script.py
```


# Additional Evaluation using Hugging Face Transformers
python -m pip install -q evaluate seqeval
python evaluation_script.py



# Citation

```javascript


@INPROCEEDINGS{10837944,
  author={Alfaqeeh, Mosab},
  booktitle={2024 34th International Conference on Collaborative Advances in Software and COmputiNg (CASCON)}, 
  title={TriMod Fusion for Multimodal Named Entity Recognition in Social Media}, 
  year={2024},
  volume={},
  number={},
  pages={1-9},
  keywords={Visualization;Social networking (online);Face recognition;User-generated content;Named entity recognition;Transformers;Feature extraction;Software;Data models;Context modeling},
  doi={10.1109/CASCON62161.2024.10837944}}

```

# Acknowledgements
-By using the provided datasets, you acknowledge and accept the copyrights set forth by Twitter and the dataset providers.

-Codebase adapted from Hugging Face Transformers: https://github.com/huggingface/transformers"
