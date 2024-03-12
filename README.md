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
python siren_DT.py --experiment_name=$i --lr=$lr --sidelength=#512 --num_workers=16 --project=#project --max_steps=$max_steps --directory=#directory_for_images --batch_size=#18 --gpu_num=#0 --type=#origin
```