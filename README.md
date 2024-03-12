# In Search of a Data Transformation That Accelerates Neural Field Training
### [Paper](https://arxiv.org/abs/2311.17094) | [Hugging Face](https://huggingface.co/papers/2311.17094)

Junwon Seo\*, Sangyoon Lee\*, Kwang In Kim, Jaeho Lee<br><br>
Pohang University of Science and Technology (POSTECH)

![pipeline](./assets/pipeline1.png)

<br>

This is the official Github page for the paper "In Search of a Data Transformation That Accelerates Neural Field Training"(CVPR 2023).

<br>

## SIREN experiments

Our experiments on SIREN are based on the official code for the paper ["Implicit Neural Representations with Periodic Activation Functions"](https://github.com/vsitzmann/siren).<br>

This repository does not contain any image dataset used in the manuscript.<br>
We used Kodak, DIV2K, CLIC for our main experiments. (Section 3.1. in our paper for details)
<br>

### Setup

A single SIREN experiment can be implemented with

```
$ cd SIREN
$ python siren_DT.py --experiment_name= --lr= --sidelength= --num_workers= --project= \
--max_steps= --directory= --batch_size= --gpu_num= --type=
```
<br>

Whole experiments for the Kodak dataset can be implemented with

```
$ cd SIREN
$ sh run_siren.sh
```
<br>

Description for the flags in the command line. <br><br>

* experiment_name `ex) 1`
    * Indicates the number of the iamge you want to run the experiment on.
* lr `ex) -10`
    * Learning rate with 2<sup>lr</sup>.
    * Range {2<sup>-8</sup>,...,2<sup>-16</sup>} used in our manuscript.
* sidelength `ex) 512`
    * Sidelength of the image.
    * All images used in the experiments were uniformly sized at 512*512.
* num_workers `ex) 16`
    * Use 16 in our experiments.
* project `ex) SIREN`
    * Name of your wandb project.
    * Learning curves can be easily found with wandb.
* max_steps `ex) 10000`
* directory `ex) kodak_ori`
    * Name of your directory for the image dataset.
    * Change our code according to the name of your path and files.
* batch_size `ex) 18`
    * Full batch for the 512*512 image.
* gpu_num `ex) 0`
* type `ex) origin`
    * Type of data transformation for the experiment.
    * You can use other data transformations in our python code.

<br>

### Loss Landscape

All loss landscapes in our paper can be shown in the [Demo](https://huggingface.co/spaces/lyunm1206/Interactive_Loss_Landscapes) with 3D interactive versions.<br>
<br>
![pipeline](./assets/demo.png)