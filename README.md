# In Search of a Data Transformation That Accelerates Neural Field Training
### [Paper](https://arxiv.org/abs/2311.17094) | [Hugging Face](https://huggingface.co/papers/2311.17094)

Junwon Seo\*, Sangyoon Lee\*, Kwang In Kim, Jaeho Lee<br><br>
Pohang University of Science and Technology (POSTECH)

![pipeline](./assets/pipeline1.png)

<br>

This is the official Github page for the paper "In Search of a Data Transformation That Accelerates Neural Field Training"(CVPR 2023).

<br>

## SIREN experiments

Our experiments on SIREN are based on the official [SIREN](https://github.com/vsitzmann/siren) code.<br>

This repository does not contain any image dataset used in the manuscript.<br>
We used Kodak, DIV2K, CLIC for our main experiments. (Section 3.1. in our paper for details)
<br>

### Single Run

A single SIREN experiment can be implemented with

```
$ cd SIREN
$ python siren_DT.py --experiment_name= --lr= --sidelength= --num_workers=
--project= --max_steps= --directory= --batch_size= --gpu_num= --type=
```

Each commandline flag means<br>
* experiment_name
    * Indicates the number of the iamge you want to run the experiment on.
* lr
    * Learning rate with 2^lr.
    * Range `{2^{-8},...,2^{-16}}` in our manuscript/